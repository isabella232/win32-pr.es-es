---
description: El ejemplo de notificaciones automáticas aborda un escenario hipotético para un asesor de seguros.
ms.assetid: bec4333a-62ca-4254-a39b-04bc2c556992
title: Ejemplo de formulario de notificaciones automáticas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c5ff78a3c38036ef9352660b4d7959e2ad87e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360977"
---
# <a name="auto-claims-form-sample"></a>Ejemplo de formulario de notificaciones automáticas

El ejemplo de notificaciones automáticas aborda un escenario hipotético para un asesor de seguros. El trabajo del Asesor requiere que lo visite con los clientes en su hogar o empresa y que escriba la información de su demanda en un formulario. Para aumentar la productividad del asesor, su Departamento de ti desarrolla una aplicación de Tablet PC que le permite escribir información de notificaciones de forma rápida y precisa a través de dos controles de entrada manuscrita: controles [InkEdit](/previous-versions/ms835842(v=msdn.10)) y [InkPicture](/previous-versions/ms583740(v=vs.100)) .

En este ejemplo, se utiliza un control [InkEdit](/previous-versions/ms835842(v=msdn.10)) para cada campo de entrada de texto. Un usuario escribe la información relevante sobre una póliza de seguros y un vehículo en estos campos con un lápiz. El control [InkPicture](/previous-versions/ms583740(v=vs.100)) se usa para agregar tinta sobre una imagen de automóvil para resaltar las áreas dañadas del automóvil. El ejemplo de notificaciones automáticas está disponible para C \# y Microsoft Visual Basic .net. En este tema se describe el Visual Basic .NET.

La clase autoclaims se define como una subclase de [System. Windows. Forms. Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) , y se define una clase anidada para crear y administrar capas de tinta para diferentes tipos de daños. Se definen cuatro controladores de eventos para realizar las siguientes tareas:

-   Inicializar las capas de formulario y de entrada de lápiz.
-   Volver a dibujar el control [InkPicture](/previous-versions/ms583740(v=vs.100)) .
-   Seleccionar una capa de tinta a través del cuadro de lista.
-   Cambiar la visibilidad de una capa de tinta.

> [!Note]  
> Las versiones de este ejemplo están disponibles en C \# y Visual Basic .net. La versión que se describe en esta sección es Visual Basic .NET. Los conceptos son los mismos entre las versiones.

 

## <a name="defining-the-form-and-ink-layers"></a>Definir las capas de formulario y de entrada de lápiz

Debe importar el espacio de nombres [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)) :


```VB
Imports Microsoft.Ink
```




```VB
// The Ink namespace, which contains the Tablet PC Platform API
using Microsoft.Ink;
```



Después, en la clase autoclaims, `InkLayer` se define una clase anidada y se declara una matriz de cuatro `InkLayer` objetos. (InkLayer contiene un objeto [Microsoft. Ink. Ink](/previous-versions/ms583670(v=vs.100)) para almacenar la tinta y valores [System. Drawing. color](/dotnet/api/system.drawing.color?view=netcore-3.1) y **booleanos** para almacenar el color y el estado oculto de la capa). Se declara un quinto objeto de entrada manuscrita para controlar la tinta del [InkPicture](/previous-versions/ms583740(v=vs.100)) cuando se ocultan todos los niveles de tinta.


```VB
' Declare the array of ink layers used the vehicle illustration.
Dim inkLayers(3) As InkLayer

' Declare an empty ink object (used when we don't want to draw
' any ink).
Dim emptyInk As Ink

' Declare a value to hold the index of selected ink
Dim selectedIndex As Integer

' Declare a value to hold whether the selected ink is hidden
Dim selectedHidden As Boolean 
```




```VB
// Declare the array of ink layers used the vehicle illustration.
InkLayer[] inkLayers;

// Declare an empty ink object (used when we don't want to draw
// any ink).
Ink emptyInk;

// Declare a value to hold the index of selected ink
int selectedIndex = -1;

// Declare a value to hold whether the selected ink is hidden
bool selectedHidden = false;
```



Cada capa tiene su propio objeto de [entrada de lápiz](/previous-versions/ms583670(v=vs.100)) . Hay cuatro áreas discretas de interés en el formulario de notificaciones (cuerpo, ventanas, neumáticos y faros), por lo que se usan cuatro objetos InkLayer. Un usuario puede ver cualquier combinación de capas a la vez.

## <a name="initializing-the-form-and-ink-layers"></a>Inicializar las capas de formulario y de entrada de lápiz

El `Load` controlador de eventos inicializa el objeto [Ink](/previous-versions/ms583670(v=vs.100)) y los cuatro `InkLayer` objetos.


```VB
' Initialize the empty ink
emptyInk = New Ink()

' Initialize the four different layers of ink on the vehicle diagram:  
' vehicle body, windows, tires, and headlights.
inkLayers(0) = New InkLayer(New Ink(), Color.Red, False)
inkLayers(1) = New InkLayer(New Ink(), Color.Violet, False)
inkLayers(2) = New InkLayer(New Ink(), Color.LightGreen, False)
inkLayers(3) = New InkLayer(New Ink(), Color.Aqua, False)
```




```VB
// Initialize the empty ink
emptyInk = new Ink();

// Initialize the four different layers of ink on the vehicle diagram:  
// vehicle body, windows, tires, and headlights.
inkLayers = new InkLayer[4];
inkLayers[0] = new InkLayer(new Ink(), Color.Red, false);
inkLayers[1] = new InkLayer(new Ink(), Color.Violet, false);
inkLayers[2] = new InkLayer(new Ink(), Color.LightGreen, false);
inkLayers[3] = new InkLayer(new Ink(), Color.Aqua, false);
```



A continuación, seleccione la primera entrada (cuerpo) en el cuadro de lista.


```VB
' By default, select the first ink layer
lstAnnotationLayer.SelectedIndex = 0
```




```VB
// By default, select the first ink layer
lstAnnotationLayer.SelectedIndex = 0;
```



Por último, establezca el color de la tinta del control [InkPicture](/previous-versions/ms583740(v=vs.100)) en la entrada del cuadro de lista seleccionada actualmente.


```VB
inkPictVehicle.DefaultDrawingAttributes.Color =
      inkLayers(lstAnnotationLayer.SelectedIndex).ActiveColor
```




```VB
inkPictVehicle.DefaultDrawingAttributes.Color = inkLayers[lstAnnotationLayer.SelectedIndex].ActiveColor;
```



## <a name="redrawing-the-inkpicture-control"></a>Volver a dibujar el control InkPicture

En el controlador de eventos [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) del control de [InkPicture](/previous-versions/ms583740(v=vs.100)) , se comprueban las capas de tinta para determinar cuáles están ocultas. Si no se oculta una capa, el procedimiento de evento la muestra mediante el método [Draw](/previous-versions/ms828488(v=msdn.10)) de la propiedad de [representador](/previous-versions/ms582196(v=vs.100)) . Si observa el Examinador de objetos, verá que la propiedad Microsoft. Ink. InkPicture. Renderer se define como un objeto [Microsoft. Ink. Renderer](/previous-versions/ms828481(v=msdn.10)) :


```VB
Private Sub inkPictVehicle_Paint(ByVal sender As System.Object, ByVal e As System.Windows.Forms.PaintEventArgs) Handles inkPictVehicle.Paint
    Dim layer As InkLayer

    ' Cycle through each ink layer.  If it is visible, paint it.
    ' Note that it is necessary to customize the paint
    ' behavior, since we want to hide/show different ink layers.
    For Each layer In inkLayers
        If (Not layer.Hidden) Then
            inkPictVehicle.Renderer.Draw(e.Graphics, layer.ActiveInk.Strokes)
        End If
    Next
End Sub
```




```VB
private void inkPictVehicle_Paint(object sender, System.Windows.Forms.PaintEventArgs e)
{
    // Cycle through each ink layer.  If it is visible, paint it.
    // Note that it is necessary to customize the paint
    // behavior, since we want to hide/show different ink layers.
    foreach (InkLayer layer in inkLayers)
    {
        if (!layer.Hidden)
        {
             inkPictVehicle.Renderer.Draw(e.Graphics,layer.ActiveInk.Strokes);
        }
    }          
}
```



## <a name="selecting-an-ink-layer-through-the-list-box"></a>Seleccionar una capa de tinta a través del cuadro de lista

Cuando el usuario selecciona un elemento en el cuadro de lista, el controlador de eventos [SelectedIndexChanged](/dotnet/api/system.windows.forms.listbox.selectedindexchanged?view=netcore-3.1) comprueba primero que la selección ha cambiado y que el control [InkPicture](/previous-versions/ms583740(v=vs.100)) no está recopilando actualmente la entrada de lápiz. A continuación, establece el color de la tinta del control InkPicture en el color adecuado para la capa de tinta seleccionada. Además, actualiza la casilla ocultar capa para reflejar el estado oculto de la capa de tinta seleccionada. Por último, el método de [actualización](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) heredado del control InkPicture se usa para mostrar solo las capas deseadas en el control.


```VB
Private Sub chHideLayer_CheckedChanged(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles chHideLayer.CheckedChanged

    ' Provided that the new checked hidden value is different than
    ' the previous value...
    If (Not (chHideLayer.Checked = selectedHidden)) Then
        If (Not (inkPictVehicle.CollectingInk)) Then

            ' Update the array indicating the visibility of each ink layer
            inkLayers(lstAnnotationLayer.SelectedIndex).Hidden = chHideLayer.Checked

            ' Set the active ink object to the selected ink
            ' Note that if the current layer is not visible, empty
            ' ink is used to prevent flicker.
            inkPictVehicle.InkEnabled = False
            If (chHideLayer.Checked) Then
                inkPictVehicle.Ink = emptyInk
            Else
                inkPictVehicle.Ink = inkLayers(lstAnnotationLayer.SelectedIndex).ActiveInk
            End If

            ' Update the previous checkbox value to the current
            selectedHidden = chHideLayer.Checked

            ' If the layer is marked hidden, disable ink collection
            inkPictVehicle.InkEnabled = Not chHideLayer.Checked

            Me.Refresh()
       Else
            ' If ink collection is enabled, the active ink cannot be changed
            ' and it is necessary to restore the checkbox to its previous value.
            chHideLayer.Checked = selectedHidden
            MessageBox.Show("Cannot change visiblity while collecting ink.")
       End If
   End If
End Sub
```




```VB
private void lstAnnotationLayer_SelectedIndexChanged(object sender, System.EventArgs e)
{
    // Provided that the new selected index value is different than
    // the previous value...
    if (lstAnnotationLayer.SelectedIndex != selectedIndex) 
    {
        if (!inkPictVehicle.CollectingInk)
        {
            // Set the ink and visiblity of the current ink layer
            inkPictVehicle.DefaultDrawingAttributes.Color = inkLayers[lstAnnotationLayer.SelectedIndex].ActiveColor;
            chHideLayer.Checked = inkLayers[lstAnnotationLayer.SelectedIndex].Hidden;

            // Set the active ink object to the selected ink
            // Note that if the current layer is not visible, empty
            // ink is used to prevent flicker.
            inkPictVehicle.InkEnabled = false;
            inkPictVehicle.Ink = chHideLayer.Checked?emptyInk:inkLayers[lstAnnotationLayer.SelectedIndex].ActiveInk;
            inkPictVehicle.InkEnabled = !chHideLayer.Checked;
    
            selectedIndex = lstAnnotationLayer.SelectedIndex;

            this.Refresh();
        }
        else 
        {
            // If ink collection is enabled, the active ink cannot be changed
            // and it is necessary to restore the selection to its previous value.
            lstAnnotationLayer.SelectedIndex = selectedIndex;
            MessageBox.Show("Cannot change active ink while collecting ink.");
        }
    }
}
```



## <a name="changing-the-visibility-of-an-ink-layer"></a>Cambiar la visibilidad de una capa de tinta

El `CheckedChanged` controlador de eventos comprueba primero que la selección ha cambiado y que el control [InkPicture](/previous-versions/ms583740(v=vs.100)) no está recopilando actualmente la entrada de lápiz. A continuación, actualiza el estado oculto de la capa de tinta seleccionada, establece el valor de InkEnabled del control InkPicture en **false**,.

A continuación, la propiedad InkEnabled del control InkPicture está establecida en **false** antes de actualizar su propiedad Ink.

Por último, el control [InkPicture](/previous-versions/ms583740(v=vs.100)) está habilitado o deshabilitado para la parte del vehículo en cuestión en función de si la casilla ocultar capa está activada y el método [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) del control InkPicture se usa para mostrar solo las capas deseadas en el control.


```VB
Private Sub chHideLayer_CheckedChanged(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles chHideLayer.CheckedChanged

    ' Provided that the new checked hidden value is different than
    ' the previous value...
    If (Not (chHideLayer.Checked = selectedHidden)) Then
        If (Not (inkPictVehicle.CollectingInk)) Then

            ' Update the array indicating the visibility of each ink layer
            inkLayers(lstAnnotationLayer.SelectedIndex).Hidden = chHideLayer.Checked

            ' Set the active ink object to the selected ink
            ' Note that if the current layer is not visible, empty
            ' ink is used to prevent flicker.
            inkPictVehicle.InkEnabled = False
            If (chHideLayer.Checked) Then
                inkPictVehicle.Ink = emptyInk
            Else
                inkPictVehicle.Ink = inkLayers(lstAnnotationLayer.SelectedIndex).ActiveInk
            End If

            ' Update the previous checkbox value to the current
            selectedHidden = chHideLayer.Checked

            ' If the layer is marked hidden, disable ink collection
            inkPictVehicle.InkEnabled = Not chHideLayer.Checked

            Me.Refresh()
        Else
            ' If ink collection is enabled, the active ink cannot be changed
            ' and it is necessary to restore the checkbox to its previous value.
            chHideLayer.Checked = selectedHidden
            MessageBox.Show("Cannot change visiblity while collecting ink.")
        End If
    End If
End Sub
```




```VB
private void chHideLayer_CheckedChanged(object sender, System.EventArgs e)
{
    // Provided that the new checked hidden value is different than
    // the previous value...
    if (chHideLayer.Checked != selectedHidden) 
    {
        if (!inkPictVehicle.CollectingInk)
        {
            // Update the array indicating the visibility of each ink layer
            inkLayers[lstAnnotationLayer.SelectedIndex].Hidden = chHideLayer.Checked;

            // Set the active ink object to the selected ink
            // Note that if the current layer is not visible, empty
            // ink is used to prevent flicker.
            inkPictVehicle.InkEnabled = false;
            inkPictVehicle.Ink = chHideLayer.Checked?emptyInk:inkLayers[lstAnnotationLayer.SelectedIndex].ActiveInk;
 
            // If the layer is marked hidden, disable ink collections
            inkPictVehicle.InkEnabled = !chHideLayer.Checked;

            // Update the previous checkbox value to reflect the current
            selectedHidden = chHideLayer.Checked;

            this.Refresh();
        }
        else 
        {
            // If ink collection is enabled, the active ink cannot be changed
            // and it is necessary to restore the checkbox to its previous value.
            chHideLayer.Checked = selectedHidden;
            MessageBox.Show("Cannot change visiblity while collecting ink.");
        }
    }
}
```



## <a name="closing-the-form"></a>Cierre del formulario

En el código generado por el diseñador de Windows Forms, los controles [InkEdit](/previous-versions/ms835842(v=msdn.10)) y [InkPicture](/previous-versions/ms583740(v=vs.100)) se agregan a la lista de componentes del formulario cuando se inicializa el formulario. Cuando se cierra el formulario, los controles InkEdit y InkPicture se eliminan, así como los demás componentes del formulario, mediante el método [Dispose](/previous-versions/dotnet/netframework-3.5/ms571303(v=vs.90)) del formulario. El método Dispose del formulario también desecha los objetos de [entrada de lápiz](/previous-versions/ms583670(v=vs.100)) creados para el formulario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Microsoft. Ink. Ink](/previous-versions/ms583670(v=vs.100))
</dt> <dt>

[InkPicture (control)](inkpicture-control.md)
</dt> <dt>

[Control InkEdit](inkedit-control.md)
</dt> </dl>

 

 
