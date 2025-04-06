# Semiconductor_Packaging

# NASSCOM - Fundamentals of Electronic Packaging Design and Testing 
28.03.2025-06.04.2025

## Lab 1 (Module 3) - Thermal analysis of a Flip-Chip BGA package 
using Ansys Electronics Desktop Student


Making a Flip-chip BGA package: importing geometry, setting up AED

We will use Icepak Tool:
Create an Icepak design inside the project:
![image](https://github.com/user-attachments/assets/d9e6534d-123c-4d4a-85b6-bf95c9679c1c)

![image](https://github.com/user-attachments/assets/926c309d-4728-4968-a0ae-53265ee9d16d)


Flow:
1. make the 3D Model
2. Assign thermal boundary conditions on edges
3. Add monitors (specify edges, points, what we will monitor)
4. ask the sw to perform a Finite element Analysis (solving thermal equations on a mesh)
5. analyze the results.

The emphasys is not doing a 3D model, but to analyze a packages, what are the different settings of the package.
so we will import an existing Flipchip_BGA package:
![image](https://github.com/user-attachments/assets/cb88d7e2-89e4-4297-af23-154f7d8f6cc4)
![image](https://github.com/user-attachments/assets/ca7b5313-ae19-45b4-affa-a02b77c3724c)
We will take the default dimensions (15x15mm, 1.6mm package thickness)
![image](https://github.com/user-attachments/assets/cbfaab41-6f50-4ca3-8ee4-827c7748ed58)
For the die, we keep the defaults size, power = 1W, material (Si), 10um bump size, no heat sink
![image](https://github.com/user-attachments/assets/5692acf6-1097-4f4e-8621-be68175cc64d)
For the substrate, we keep the defaults (number of layers, thickness, coverage, trace material – Cu, vias settings; 
![image](https://github.com/user-attachments/assets/e32bb51c-08cf-430f-952c-4b0025d588bb)

On the Solder tab, we keep the defaults
We will create the model using the default settings:
![image](https://github.com/user-attachments/assets/afe547d8-72ec-4012-a0aa-fd162187cd9f)

Top model:
![image](https://github.com/user-attachments/assets/21e5df50-c437-450b-b1bf-6b64b12b3cc7)

Die source:
![image](https://github.com/user-attachments/assets/e0eb1499-edbf-416d-b8c7-23cd78f7c5b5)

Ball group (16x16=256 balls):
![image](https://github.com/user-attachments/assets/a7d59489-4a97-4b99-93e1-a3cbcfdcc46d)
Substrate:

![image](https://github.com/user-attachments/assets/7078be93-4f28-45ad-830d-854dd984343e)
Underfill:
![image](https://github.com/user-attachments/assets/e0d1553a-3f6d-4c1c-9d7b-2778674c71e0)

Vias:
![image](https://github.com/user-attachments/assets/6722f264-ecb0-47a9-9436-2f0642a995e1)



Die:

![image](https://github.com/user-attachments/assets/8aef8038-c382-4754-a15d-dc660db1badb)

Model (Design list):
![image](https://github.com/user-attachments/assets/3f33530c-fc4d-42ef-bb65-d06b79a0a11e)


For the Thermal analysis:
![image](https://github.com/user-attachments/assets/66691135-579f-41bc-b022-9831cb45be91)

Thermal boundary condition for the die: 1W coming from the “die source” = power generated in the die at its surface
![image](https://github.com/user-attachments/assets/4bf2fd88-416f-4e28-b4d6-6ad49cd63875)

![image](https://github.com/user-attachments/assets/b847b89f-7a03-415d-8284-2d3e83590639)

Create boundary condition on the substrate: 
![image](https://github.com/user-attachments/assets/2b10bd21-3af8-4bcc-a94e-20b7e865e5c1)

Substate sees the ambient temperature:
![image](https://github.com/user-attachments/assets/93e2d736-8ce6-4d47-a573-5755e5a50d0f)

Remove multiple boundary condition:
![image](https://github.com/user-attachments/assets/0035a478-703b-481d-899a-1fc1427fd5b4)
Adding monitors for the temperature in a few points:
![image](https://github.com/user-attachments/assets/562565df-f757-444b-8991-a7145f22d626)

Temperature of the substrate:
![image](https://github.com/user-attachments/assets/320da675-6d90-429a-842c-3c7cdc6939c7)

Monitor die temperature:
![image](https://github.com/user-attachments/assets/3bd3ab2d-990a-4139-bc80-8e41c7dd70dc)

![image](https://github.com/user-attachments/assets/0607bf43-60a7-4ce5-bd0c-ccdf994a6273)
Monitor underfill temperature:

![image](https://github.com/user-attachments/assets/13621c0b-887d-4c18-84a2-ddddb0dd3b95)

![image](https://github.com/user-attachments/assets/6b0a2d9c-4204-4640-bd08-dae91405b0ae)

So, 3 layers monitored:

![image](https://github.com/user-attachments/assets/583a03df-6b62-4bdf-a90d-6bfdfd1ec70e)

No need to define “Solar Loading”
 
![image](https://github.com/user-attachments/assets/4300074c-7f8d-4ce5-8842-b1e109052648)

Generate Mesh:

![image](https://github.com/user-attachments/assets/06f8fd08-1288-467b-845f-b0d3fe421668)

We are asked to save the project:
![image](https://github.com/user-attachments/assets/f97efb65-1230-407f-bc1f-6c32b4078e67)
![image](https://github.com/user-attachments/assets/de6773f5-27e0-47e3-a5bc-9db26b253498)
Mesh generated:
![image](https://github.com/user-attachments/assets/f662ec2e-fa1f-468a-a607-eb5e3429ba73)



Inspect the quality of the mesh:

![image](https://github.com/user-attachments/assets/9d49e8b9-c561-48d1-b72b-58ad6633afb4)



Keep all mesh settings to default

Mesh Operation is done:
![image](https://github.com/user-attachments/assets/9bda404f-3d77-4f45-b276-8dab27281185)

![image](https://github.com/user-attachments/assets/3f371c2d-ec03-4725-84d9-bc8a96a17ca6)

What is left is the Analysis:
Add a Solution Setup:
![image](https://github.com/user-attachments/assets/b612315e-972e-410d-9096-f6109fd63d47)

![image](https://github.com/user-attachments/assets/984fcd06-3aa7-46a8-affb-b65871751b1a)
Keep defaults (No radiation, laminar flow)
Keep defaults for Convergence settings:
![image](https://github.com/user-attachments/assets/6877a59f-156a-4ee0-b9b6-1ba995d1a2bc)

Click “ok” to add the Soluton Setuo “Setup1”
![image](https://github.com/user-attachments/assets/67a82ae5-abd5-485a-95f5-0bd4210d1345)
“Validate”:
![image](https://github.com/user-attachments/assets/20afdb91-a157-4258-acb7-f81815f17315)
![image](https://github.com/user-attachments/assets/b7638bbd-2d03-4746-b990-075d83827b06)

Warning:
![image](https://github.com/user-attachments/assets/5e5b5713-cc45-4d0e-a141-847efa3665c4)
Need to assign mesh to underfill:
![image](https://github.com/user-attachments/assets/924c101b-a58c-4314-9f82-ad9384ae0450)
![image](https://github.com/user-attachments/assets/38b1b88c-33b4-4b0d-be70-a6bc8ab67af4)
![image](https://github.com/user-attachments/assets/c6b42e7f-f8c8-44c9-9929-843fa9edcce2)

MeshRegion1 created:
![image](https://github.com/user-attachments/assets/1b12f08d-6906-4a15-a0fc-4794f5c4252f)

Generate Mesh again:
![image](https://github.com/user-attachments/assets/f0a86680-95f9-424b-a459-2adde5bf9355)

Mesh Generation never completes for MeshRegion1

![image](https://github.com/user-attachments/assets/ba590986-5c9e-4536-ad62-3ba61d3c387f)

=> Will delete it

![image](https://github.com/user-attachments/assets/099a1b99-b22b-4b0a-a1fe-a67d4cb2ae87)

And Start Analyzing (which will also recreate the mesh):

![image](https://github.com/user-attachments/assets/3c221e85-31b9-45a6-bf07-05a7e2f8e04d)

Complaints:

![image](https://github.com/user-attachments/assets/09503d6d-864c-4b96-98d6-82d6acc35476)

![image](https://github.com/user-attachments/assets/9998757a-d83f-4147-9592-18423b8059d2)

… because there is no radiation or convection defined, 
We are just set the 2 thermal boundary conditions, we only look at the thermal map

Analysis done:
![image](https://github.com/user-attachments/assets/29d81c0d-570d-4251-b31c-5cab3a88c3fd)

Select the whole package:
![image](https://github.com/user-attachments/assets/ee6e2645-82cc-4ca7-a7e0-bea2b7e86b21)

![image](https://github.com/user-attachments/assets/01a4dd76-3ee0-4b05-b8be-a135436c4c98)

Plot temperature:

![image](https://github.com/user-attachments/assets/448b819c-47fc-4139-84cb-05ce0f1ef057)
![image](https://github.com/user-attachments/assets/1e3e8d32-b5f8-459e-b034-b462901caa73)
![image](https://github.com/user-attachments/assets/0ba36620-5a26-496d-adc3-a8718e6b1ed9)

Result: temperature map:
![image](https://github.com/user-attachments/assets/bfa46f3e-f843-412c-b7d9-4c6a7205fb98)

Report temperature of the 3 monitored points:

![image](https://github.com/user-attachments/assets/a3785623-d10a-4b34-a0f1-079fe8cffb9f)
![image](https://github.com/user-attachments/assets/86d75d02-3cc7-47fa-bc4c-1bebe9035ea1)
![image](https://github.com/user-attachments/assets/855a461c-fa3c-43bc-bddb-99554f78d799)
![image](https://github.com/user-attachments/assets/b7ddca4f-b49c-4225-aa6c-9eb73cb8e84b)
![image](https://github.com/user-attachments/assets/60f6a82e-cb1c-412c-8202-a8a6f6e8452d)

![image](https://github.com/user-attachments/assets/b731cf47-f1d2-4c54-a78e-e774b0c349c9)
![image](https://github.com/user-attachments/assets/83de1653-c5a6-4517-bd05-d7896a588f67)
![image](https://github.com/user-attachments/assets/8c8a39d8-26a3-41a4-b546-28050d1ebff1)


Or, in a single Monitor Table:
![image](https://github.com/user-attachments/assets/2303085a-545c-485f-80ef-6ba6980f7269)





## Lab 2 (Module 5) Design a wire bond package (die, die attach, wire bonding, molding)

The model will be built in Q3D 
![image](https://github.com/user-attachments/assets/a410152a-0c3c-43d5-a6bf-f40e39225094)


![image](https://github.com/user-attachments/assets/c43094d7-31e0-4d86-8053-33402b8190f8)

Adding the die based on the specifications:
3mmx3mm, thickness 0.2mm
A corner of the die in (0,0,0)

“Draw” tab:

![image](https://github.com/user-attachments/assets/7fc1b8ba-d2bc-4a36-99da-4e5f84476642)

Select a rectangle:

![image](https://github.com/user-attachments/assets/8e070e95-49a7-47d8-9581-da8126605655)
Draw it:
![image](https://github.com/user-attachments/assets/119d79d9-7e84-4158-94b5-ba64b0ab97ff)
Modify properties:

![image](https://github.com/user-attachments/assets/49623f1a-f4b3-471f-828a-043aa4dd9e0f)

![image](https://github.com/user-attachments/assets/5d02aae4-d6cc-4c4d-9b0a-c88091939e46)

![image](https://github.com/user-attachments/assets/fd9e30d7-2f2a-4a5f-9d05-1d72fe5f0289)

Add the thickness:
Select the rectangle, then
Modeler > Surface > Thicken Sheet
![image](https://github.com/user-attachments/assets/69404a9a-6cd4-4a3c-901c-53c931f3f192)

![image](https://github.com/user-attachments/assets/542cfa55-ba50-4111-95e1-7b84345fa860)

![image](https://github.com/user-attachments/assets/ba21b5a0-bb11-4849-92f7-b81875cfe10c)
Rename “Rectangle” to “Die”:
Click on Rectangle, modify name
Also, set material to Si

![image](https://github.com/user-attachments/assets/97a6a2ba-3fa3-4457-84c1-5e3d71efddc6)
![image](https://github.com/user-attachments/assets/c23f5ce9-b933-4ff1-ac39-5232b3d8573c)


Add substrate:
Select “Rectangle”, draw it:


![image](https://github.com/user-attachments/assets/983e1f87-0b75-4e67-a099-05326a09faad)
![image](https://github.com/user-attachments/assets/f3518ae2-3583-4595-9814-9f25fe04552d)

Click on Rectangle1/CreateRectangle, adjust the size based on the spec (5mm x 5mm), adjust the position such as the die is on the center:

![image](https://github.com/user-attachments/assets/f5686aec-69af-4943-a675-70a659c9defb)

![image](https://github.com/user-attachments/assets/cdf34ad5-67b1-4d9a-ad20-3884e8a6ba8d)


Thickness of the substrate: 500u:
Select Substrate rectangle / Modeler>Surface>Thicken Sheet:

![image](https://github.com/user-attachments/assets/aceea74e-24c2-4c9e-ad5b-60e4cc140a34)

![image](https://github.com/user-attachments/assets/97cceb4a-5467-4304-8490-93878c783224)

=> thickness must be –5mm
Click on 3Thicken Sheet”:
![image](https://github.com/user-attachments/assets/24f8abb9-47a9-4577-923d-b155dd3f67da)

Adjust thickness to -5mm:
![image](https://github.com/user-attachments/assets/b702fe8e-2202-4c07-b304-574c5892f8a2)
![image](https://github.com/user-attachments/assets/2c75dfbb-3173-4f7a-a2e7-aa64997b1500)

Let’s adjust the substrate properties: Name, material
Click on Rectangle1:

![image](https://github.com/user-attachments/assets/95d010a4-4474-4cef-b335-6b3747fdfcd0)

![image](https://github.com/user-attachments/assets/fa62aec0-5313-4b44-b7b2-79d5d445f943)


But the die is not directly sitting on the substrate, there is also the die attach material, we need to adjust the Z position:

Click on Substrate/CreateRectangle:
![image](https://github.com/user-attachments/assets/194cc3b0-12e1-4354-8bdb-27692731e4d2)
![image](https://github.com/user-attachments/assets/dc7da8f5-5514-40d4-a014-fcf40f749bc1)
![image](https://github.com/user-attachments/assets/68af986c-3cc7-4889-9e29-e11cb7ca469e)

Adding the die attach material:
Create a rectangle with the same size as the die:






