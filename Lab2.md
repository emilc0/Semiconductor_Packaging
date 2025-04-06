
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

![image](Picture1.png)
![image](Picture2.png)
And add the thickness as -0.1mm:
![image](Picture3.png)
![image](Picture4.png)
Adjust properties: name, material:

![image](Picture5.png)
![image](Picture6.png)

Wire Bonding:

Draw bond pads, on the die and the on the substrate:
Create a rectangle, edit properties:

![image](Picture7.png)

Add thickness of 5um:

![image](Picture8.png)
![image](Picture9.png)


Create bond pad on the substrate:
Draw rectangle, adjust properties:

![image](Picture10.png)

And rename bond pads:
![image](Picture11.png)
Connect the Bond pads with Bond Wire:

![image](Picture12.png)
![image](Picture13.png)
![image](Picture14.png)
![image](Picture15.png)
We’ll choose the defaults parameters.
![image](Picture16.png)
Create a second die bonding pad:
![image](Picture17.png)
![image](Picture18.png)
![image](Picture19.png)
![image](Picture20.png)

And rename to diebondpad2:
![image](Picture21.png)

Create a second substrate bond pad, add thickness:
![image](Picture22.png)
![image](Picture23.png)
![image](Picture24.png)
![image](Picture25.png)
![image](Picture26.png)
![image](Picture27.png)
![image](Picture28.png)
![image](Picture29.png)

Select “Gold” for the bond wires material:
![image](Picture30.png)
![image](Picture31.png)

The mold compound will come over all the substrate, thickness > die attach (0.1mm) + die (0.2mm) + wire bond height (about 0.4mm)
To create mold, first create a rectangle over the substrate:

![image](Picture32.png)

Add thickness:
![image](Picture33.png)
![image](Picture34.png)

, name and material:
![image](Picture35.png)
![image](Picture36.png)

Enough mold compound height for laser marking, so wire bonds will not be affected
![image](Picture37.png)


