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
# <a name="auto-claims-form-sample"></a><span data-ttu-id="a3e30-103">Ejemplo de formulario de notificaciones automáticas</span><span class="sxs-lookup"><span data-stu-id="a3e30-103">Auto Claims Form Sample</span></span>

<span data-ttu-id="a3e30-104">El ejemplo de notificaciones automáticas aborda un escenario hipotético para un asesor de seguros.</span><span class="sxs-lookup"><span data-stu-id="a3e30-104">The Auto Claims sample addresses a hypothetical scenario for an insurance assessor.</span></span> <span data-ttu-id="a3e30-105">El trabajo del Asesor requiere que lo visite con los clientes en su hogar o empresa y que escriba la información de su demanda en un formulario.</span><span class="sxs-lookup"><span data-stu-id="a3e30-105">The assessor's work requires him or her to visit with clients at their home or business and to enter their claim information into a form.</span></span> <span data-ttu-id="a3e30-106">Para aumentar la productividad del asesor, su Departamento de ti desarrolla una aplicación de Tablet PC que le permite escribir información de notificaciones de forma rápida y precisa a través de dos controles de entrada manuscrita: controles [InkEdit](/previous-versions/ms835842(v=msdn.10)) y [InkPicture](/previous-versions/ms583740(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="a3e30-106">To increase the assessor's productivity, his IT department develops a tablet application that enables him or her to quickly and accurately enter claim information through two ink controls: [InkEdit](/previous-versions/ms835842(v=msdn.10)) and [InkPicture](/previous-versions/ms583740(v=vs.100)) controls.</span></span>

<span data-ttu-id="a3e30-107">En este ejemplo, se utiliza un control [InkEdit](/previous-versions/ms835842(v=msdn.10)) para cada campo de entrada de texto.</span><span class="sxs-lookup"><span data-stu-id="a3e30-107">In this sample, a [InkEdit](/previous-versions/ms835842(v=msdn.10)) control is used for each text input field.</span></span> <span data-ttu-id="a3e30-108">Un usuario escribe la información relevante sobre una póliza de seguros y un vehículo en estos campos con un lápiz.</span><span class="sxs-lookup"><span data-stu-id="a3e30-108">A user enters the relevant information about an insurance policy and vehicle into these fields with a pen.</span></span> <span data-ttu-id="a3e30-109">El control [InkPicture](/previous-versions/ms583740(v=vs.100)) se usa para agregar tinta sobre una imagen de automóvil para resaltar las áreas dañadas del automóvil.</span><span class="sxs-lookup"><span data-stu-id="a3e30-109">The [InkPicture](/previous-versions/ms583740(v=vs.100)) control is used to add ink over an automobile image to highlight damaged areas of the automobile.</span></span> <span data-ttu-id="a3e30-110">El ejemplo de notificaciones automáticas está disponible para C \# y Microsoft Visual Basic .net.</span><span class="sxs-lookup"><span data-stu-id="a3e30-110">The Auto Claims sample is available for C\# and Microsoft Visual Basic .NET.</span></span> <span data-ttu-id="a3e30-111">En este tema se describe el Visual Basic .NET.</span><span class="sxs-lookup"><span data-stu-id="a3e30-111">This topic describes the Visual Basic .NET.</span></span>

<span data-ttu-id="a3e30-112">La clase autoclaims se define como una subclase de [System. Windows. Forms. Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) , y se define una clase anidada para crear y administrar capas de tinta para diferentes tipos de daños.</span><span class="sxs-lookup"><span data-stu-id="a3e30-112">The AutoClaims Class is defined as a subclass of [System.Windows.Forms.Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) , and a nested class is defined for creating and managing layers of ink for different types of damage.</span></span> <span data-ttu-id="a3e30-113">Se definen cuatro controladores de eventos para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="a3e30-113">Four event handlers are defined to perform the following tasks:</span></span>

-   <span data-ttu-id="a3e30-114">Inicializar las capas de formulario y de entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="a3e30-114">Initializing the form and ink layers.</span></span>
-   <span data-ttu-id="a3e30-115">Volver a dibujar el control [InkPicture](/previous-versions/ms583740(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="a3e30-115">Redrawing the [InkPicture](/previous-versions/ms583740(v=vs.100)) control.</span></span>
-   <span data-ttu-id="a3e30-116">Seleccionar una capa de tinta a través del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="a3e30-116">Selecting an ink layer through the list box.</span></span>
-   <span data-ttu-id="a3e30-117">Cambiar la visibilidad de una capa de tinta.</span><span class="sxs-lookup"><span data-stu-id="a3e30-117">Changing the visibility of an ink layer.</span></span>

> [!Note]  
> <span data-ttu-id="a3e30-118">Las versiones de este ejemplo están disponibles en C \# y Visual Basic .net.</span><span class="sxs-lookup"><span data-stu-id="a3e30-118">Versions of this sample are available in C\# and Visual Basic .NET.</span></span> <span data-ttu-id="a3e30-119">La versión que se describe en esta sección es Visual Basic .NET.</span><span class="sxs-lookup"><span data-stu-id="a3e30-119">The version discussed in this section is Visual Basic .NET.</span></span> <span data-ttu-id="a3e30-120">Los conceptos son los mismos entre las versiones.</span><span class="sxs-lookup"><span data-stu-id="a3e30-120">The concepts are the same between versions.</span></span>

 

## <a name="defining-the-form-and-ink-layers"></a><span data-ttu-id="a3e30-121">Definir las capas de formulario y de entrada de lápiz</span><span class="sxs-lookup"><span data-stu-id="a3e30-121">Defining the Form and Ink Layers</span></span>

<span data-ttu-id="a3e30-122">Debe importar el espacio de nombres [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)) :</span><span class="sxs-lookup"><span data-stu-id="a3e30-122">You need to import the [Microsoft.Ink](/previous-versions/ms826516(v=msdn.10)) namespace:</span></span>


```VB
Imports Microsoft.Ink
```




```VB
// The Ink namespace, which contains the Tablet PC Platform API
using Microsoft.Ink;
```



<span data-ttu-id="a3e30-123">Después, en la clase autoclaims, `InkLayer` se define una clase anidada y se declara una matriz de cuatro `InkLayer` objetos.</span><span class="sxs-lookup"><span data-stu-id="a3e30-123">Next, in the AutoClaims Class, a nested `InkLayer` class is defined and an array of four `InkLayer` objects is declared.</span></span> <span data-ttu-id="a3e30-124">(InkLayer contiene un objeto [Microsoft. Ink. Ink](/previous-versions/ms583670(v=vs.100)) para almacenar la tinta y valores [System. Drawing. color](/dotnet/api/system.drawing.color?view=netcore-3.1) y **booleanos** para almacenar el color y el estado oculto de la capa). Se declara un quinto objeto de entrada manuscrita para controlar la tinta del [InkPicture](/previous-versions/ms583740(v=vs.100)) cuando se ocultan todos los niveles de tinta.</span><span class="sxs-lookup"><span data-stu-id="a3e30-124">(InkLayer contains an [Microsoft.Ink.Ink](/previous-versions/ms583670(v=vs.100)) object for storing ink, and [System.Drawing.Color](/dotnet/api/system.drawing.color?view=netcore-3.1) and **Boolean** values for storing the color and hidden state of the layer.) A fifth Ink object is declared to handle ink for the [InkPicture](/previous-versions/ms583740(v=vs.100)) when all of the ink layers are hidden.</span></span>


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



<span data-ttu-id="a3e30-125">Cada capa tiene su propio objeto de [entrada de lápiz](/previous-versions/ms583670(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="a3e30-125">Each layer has its own [Ink](/previous-versions/ms583670(v=vs.100)) object.</span></span> <span data-ttu-id="a3e30-126">Hay cuatro áreas discretas de interés en el formulario de notificaciones (cuerpo, ventanas, neumáticos y faros), por lo que se usan cuatro objetos InkLayer.</span><span class="sxs-lookup"><span data-stu-id="a3e30-126">There are four discrete areas of interest in the claim form (body, windows, tires, and headlights), so four InkLayer objects are used.</span></span> <span data-ttu-id="a3e30-127">Un usuario puede ver cualquier combinación de capas a la vez.</span><span class="sxs-lookup"><span data-stu-id="a3e30-127">A user can view any combination of layers at once.</span></span>

## <a name="initializing-the-form-and-ink-layers"></a><span data-ttu-id="a3e30-128">Inicializar las capas de formulario y de entrada de lápiz</span><span class="sxs-lookup"><span data-stu-id="a3e30-128">Initializing the Form and Ink Layers</span></span>

<span data-ttu-id="a3e30-129">El `Load` controlador de eventos inicializa el objeto [Ink](/previous-versions/ms583670(v=vs.100)) y los cuatro `InkLayer` objetos.</span><span class="sxs-lookup"><span data-stu-id="a3e30-129">The `Load` event handler initializes the [Ink](/previous-versions/ms583670(v=vs.100)) object and the four `InkLayer` objects.</span></span>


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



<span data-ttu-id="a3e30-130">A continuación, seleccione la primera entrada (cuerpo) en el cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="a3e30-130">Then, select the first entry (Body) in the list box.</span></span>


```VB
' By default, select the first ink layer
lstAnnotationLayer.SelectedIndex = 0
```




```VB
// By default, select the first ink layer
lstAnnotationLayer.SelectedIndex = 0;
```



<span data-ttu-id="a3e30-131">Por último, establezca el color de la tinta del control [InkPicture](/previous-versions/ms583740(v=vs.100)) en la entrada del cuadro de lista seleccionada actualmente.</span><span class="sxs-lookup"><span data-stu-id="a3e30-131">Finally, set the ink color for the [InkPicture](/previous-versions/ms583740(v=vs.100)) control to the currently selected list box entry.</span></span>


```VB
inkPictVehicle.DefaultDrawingAttributes.Color =
      inkLayers(lstAnnotationLayer.SelectedIndex).ActiveColor
```




```VB
inkPictVehicle.DefaultDrawingAttributes.Color = inkLayers[lstAnnotationLayer.SelectedIndex].ActiveColor;
```



## <a name="redrawing-the-inkpicture-control"></a><span data-ttu-id="a3e30-132">Volver a dibujar el control InkPicture</span><span class="sxs-lookup"><span data-stu-id="a3e30-132">Redrawing the InkPicture Control</span></span>

<span data-ttu-id="a3e30-133">En el controlador de eventos [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) del control de [InkPicture](/previous-versions/ms583740(v=vs.100)) , se comprueban las capas de tinta para determinar cuáles están ocultas.</span><span class="sxs-lookup"><span data-stu-id="a3e30-133">In the [InkPicture](/previous-versions/ms583740(v=vs.100)) Control's inherited [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) event handler, the ink layers are checked to determine which are hidden.</span></span> <span data-ttu-id="a3e30-134">Si no se oculta una capa, el procedimiento de evento la muestra mediante el método [Draw](/previous-versions/ms828488(v=msdn.10)) de la propiedad de [representador](/previous-versions/ms582196(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="a3e30-134">If a layer is not hidden, the event procedure displays it by using the [Renderer](/previous-versions/ms582196(v=vs.100)) property's [Draw](/previous-versions/ms828488(v=msdn.10)) method.</span></span> <span data-ttu-id="a3e30-135">Si observa el Examinador de objetos, verá que la propiedad Microsoft. Ink. InkPicture. Renderer se define como un objeto [Microsoft. Ink. Renderer](/previous-versions/ms828481(v=msdn.10)) :</span><span class="sxs-lookup"><span data-stu-id="a3e30-135">If you look in the Object Browser, you'll see that the Microsoft.Ink.InkPicture.Renderer property is defined as a [Microsoft.Ink.Renderer](/previous-versions/ms828481(v=msdn.10)) object:</span></span>


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



## <a name="selecting-an-ink-layer-through-the-list-box"></a><span data-ttu-id="a3e30-136">Seleccionar una capa de tinta a través del cuadro de lista</span><span class="sxs-lookup"><span data-stu-id="a3e30-136">Selecting an Ink Layer through the List Box</span></span>

<span data-ttu-id="a3e30-137">Cuando el usuario selecciona un elemento en el cuadro de lista, el controlador de eventos [SelectedIndexChanged](/dotnet/api/system.windows.forms.listbox.selectedindexchanged?view=netcore-3.1) comprueba primero que la selección ha cambiado y que el control [InkPicture](/previous-versions/ms583740(v=vs.100)) no está recopilando actualmente la entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="a3e30-137">When the user selects an item in the list box, the [SelectedIndexChanged](/dotnet/api/system.windows.forms.listbox.selectedindexchanged?view=netcore-3.1) event handler first checks that the selection has changed and that the [InkPicture](/previous-versions/ms583740(v=vs.100)) control is not currently collecting ink.</span></span> <span data-ttu-id="a3e30-138">A continuación, establece el color de la tinta del control InkPicture en el color adecuado para la capa de tinta seleccionada.</span><span class="sxs-lookup"><span data-stu-id="a3e30-138">It then sets the ink color of the InkPicture control to the appropriate color for the selected ink layer.</span></span> <span data-ttu-id="a3e30-139">Además, actualiza la casilla ocultar capa para reflejar el estado oculto de la capa de tinta seleccionada.</span><span class="sxs-lookup"><span data-stu-id="a3e30-139">Also, it updates the Hide Layer check box to reflect the selected ink layer's hidden status.</span></span> <span data-ttu-id="a3e30-140">Por último, el método de [actualización](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) heredado del control InkPicture se usa para mostrar solo las capas deseadas en el control.</span><span class="sxs-lookup"><span data-stu-id="a3e30-140">Finally, the InkPicture control's inherited [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) method is used to display only the desired layers within the control.</span></span>


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



## <a name="changing-the-visibility-of-an-ink-layer"></a><span data-ttu-id="a3e30-141">Cambiar la visibilidad de una capa de tinta</span><span class="sxs-lookup"><span data-stu-id="a3e30-141">Changing the Visibility of an Ink Layer</span></span>

<span data-ttu-id="a3e30-142">El `CheckedChanged` controlador de eventos comprueba primero que la selección ha cambiado y que el control [InkPicture](/previous-versions/ms583740(v=vs.100)) no está recopilando actualmente la entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="a3e30-142">The `CheckedChanged` event handler first checks that the selection has changed and that the [InkPicture](/previous-versions/ms583740(v=vs.100)) control is not currently collecting ink.</span></span> <span data-ttu-id="a3e30-143">A continuación, actualiza el estado oculto de la capa de tinta seleccionada, establece el valor de InkEnabled del control InkPicture en **false**,.</span><span class="sxs-lookup"><span data-stu-id="a3e30-143">It then updates the selected ink layer's hidden status, sets the InkPicture control's InkEnabled to **FALSE**, .</span></span>

<span data-ttu-id="a3e30-144">A continuación, la propiedad InkEnabled del control InkPicture está establecida en **false** antes de actualizar su propiedad Ink.</span><span class="sxs-lookup"><span data-stu-id="a3e30-144">Next, the InkPicture control's InkEnabled property is set to **FALSE** before updating its Ink property.</span></span>

<span data-ttu-id="a3e30-145">Por último, el control [InkPicture](/previous-versions/ms583740(v=vs.100)) está habilitado o deshabilitado para la parte del vehículo en cuestión en función de si la casilla ocultar capa está activada y el método [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) del control InkPicture se usa para mostrar solo las capas deseadas en el control.</span><span class="sxs-lookup"><span data-stu-id="a3e30-145">Finally, the [InkPicture](/previous-versions/ms583740(v=vs.100)) control is either enabled or disabled for the particular vehicle part based on whether the Hide Layer check box is selected, and the InkPicture control's [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) method is used to display only the desired layers within the control.</span></span>


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



## <a name="closing-the-form"></a><span data-ttu-id="a3e30-146">Cierre del formulario</span><span class="sxs-lookup"><span data-stu-id="a3e30-146">Closing the Form</span></span>

<span data-ttu-id="a3e30-147">En el código generado por el diseñador de Windows Forms, los controles [InkEdit](/previous-versions/ms835842(v=msdn.10)) y [InkPicture](/previous-versions/ms583740(v=vs.100)) se agregan a la lista de componentes del formulario cuando se inicializa el formulario.</span><span class="sxs-lookup"><span data-stu-id="a3e30-147">In the Windows Form Designer generated code, the [InkEdit](/previous-versions/ms835842(v=msdn.10)) and [InkPicture](/previous-versions/ms583740(v=vs.100)) controls are added to the form's component list when the form is initialized.</span></span> <span data-ttu-id="a3e30-148">Cuando se cierra el formulario, los controles InkEdit y InkPicture se eliminan, así como los demás componentes del formulario, mediante el método [Dispose](/previous-versions/dotnet/netframework-3.5/ms571303(v=vs.90)) del formulario.</span><span class="sxs-lookup"><span data-stu-id="a3e30-148">When the form closes, the InkEdit and InkPicture controls are disposed, as well as the other components of the form, by the form's [Dispose](/previous-versions/dotnet/netframework-3.5/ms571303(v=vs.90)) method.</span></span> <span data-ttu-id="a3e30-149">El método Dispose del formulario también desecha los objetos de [entrada de lápiz](/previous-versions/ms583670(v=vs.100)) creados para el formulario.</span><span class="sxs-lookup"><span data-stu-id="a3e30-149">The form's Dispose method also disposes the [Ink](/previous-versions/ms583670(v=vs.100)) objects that are created for the form.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3e30-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a3e30-150">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a3e30-151">[Microsoft. Ink. Ink](/previous-versions/ms583670(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="a3e30-151">[Microsoft.Ink.Ink](/previous-versions/ms583670(v=vs.100))</span></span>
</dt> <dt>

[<span data-ttu-id="a3e30-152">InkPicture (control)</span><span class="sxs-lookup"><span data-stu-id="a3e30-152">InkPicture Control</span></span>](inkpicture-control.md)
</dt> <dt>

[<span data-ttu-id="a3e30-153">Control InkEdit</span><span class="sxs-lookup"><span data-stu-id="a3e30-153">InkEdit Control</span></span>](inkedit-control.md)
</dt> </dl>

 

 
