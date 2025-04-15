## Hola a todos, soy Carlos Saiz



## Entrega Entornos de desarrollo

## PASOS PARA CREAR UN FORMULARIO EN POWERSHELL
### 1-Crea el Formulario centrado:
##### #Formulario
##### $Label=New-Object System.Windows.Forms.Label
##### $Form.Text="Formulario"
##### $Form.Size=New-Object System.Drawing.Size(500,500)
##### $Form.StartPosition="CenterScreen"

### 2-Crea una etiqueta:
##### #Etiqueta
##### $Label=New-Object System.Windows.Forms.Label
##### $Label.Text="Etiqueta de ejemplo"
##### $Label.AutoSize=$True
##### $Label.Location=New-Object System.Drawing.Size(160,160)

### 3-Crea una caja de texto:
##### #Caja de texto
##### $TextBox = New-Object System.Windows.Forms.TextBox
##### $TextBox.Location = New-Object System.Drawing.Size(100,180)
##### $TextBox.Size = New-Object System.Drawing.Size(260,20)

### 4-Crea un boton Enter y un boton Escape:
##### #Botón1
##### $Button1=New-Object System.Windows.Forms.Button
##### $Button1.Size=New-Object System.Drawing.Size(75,23)
#####$Button1.Text="Botón OK"
##### $Button1.Location=New-Object System.Drawing.Size(120,220)
#####
##### #Botón2
##### $Button2=New-Object System.Windows.Forms.Button
##### $Button2.Size=New-Object System.Drawing.Size(75,23)
##### $Button2.Text="Botón Cancelar"
##### $Button2.Location=New-Object System.Drawing.Size(220,220)

### 5-Añade la funcionalidad al formulario y los botones:
##### El boton Enter almacenara el contenido de la caja de texto en una variable.
##### El boton Escape saldra del formulario.
##### $Form.KeyPreview = $True
##### $Form.Add_KeyDown({if ($_.KeyCode -eq "Enter"){$Var=$TextBox.Text;Write-Host $Var;$Form.Close()}})
##### $Form.Add_KeyDown({if ($_.KeyCode -eq "Escape"){$Form.Close()}})
##### $Button1.Add_Click({$Var=$TextBox.Text;Write-Host $Var})
##### $Button2.Add_Click({$Form.Close()})

### 6-Añade todo al formulario:
##### #Añadir etiqueta
##### $Form.Controls.Add($Label)
 
##### #Añadir botones
##### $Form.Controls.Add($Button1)
##### $Form.Controls.Add($Button2)
 
##### #Añadir caja de texto
##### $Form.Controls.Add($TextBox)
 
##### $Form.ShowDialog()

## Contenido sacado de:
#### https://www.jesusninoc.com/01/30/crear-un-formulario-en-powershell/


![image](https://user-images.githubusercontent.com/114073080/226470011-cfd8901d-3171-4319-95ac-c8a703df9412.png)

<!--
**CarlosSaizLeal-CES/CarlosSaizLeal-CES** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
