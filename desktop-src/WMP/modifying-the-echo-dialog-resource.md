---
title: Modificar el recurso de cuadro de diálogo echo
description: Modificar el recurso de cuadro de diálogo echo
ms.assetid: 2a371004-82a5-42fb-b19c-ea1928a122a1
keywords:
- Complementos de Windows Media Player, páginas de propiedades de ejemplo echo
- complementos, páginas de propiedades de ejemplo echo
- Complementos de procesamiento de señal digital, páginas de propiedades de ejemplo de eco
- Complementos DSP, páginas de propiedades de ejemplo echo
- Ejemplo de complemento de DSP de eco, páginas de propiedades
- Ejemplo de complemento de DSP de eco, recurso de cuadro de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09caa800376a7962a11912bc582a091f0de52c16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357405"
---
# <a name="modifying-the-echo-dialog-resource"></a><span data-ttu-id="6a389-109">Modificar el recurso de cuadro de diálogo echo</span><span class="sxs-lookup"><span data-stu-id="6a389-109">Modifying the Echo Dialog Resource</span></span>

<span data-ttu-id="6a389-110">Debe cambiar el recurso de cuadro de diálogo que es la interfaz de usuario del objeto de página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="6a389-110">You need to change the dialog resource that is the user interface for the property page object.</span></span> <span data-ttu-id="6a389-111">En primer lugar, puede cambiar la etiqueta y el cuadro de edición existente para que sea útil para la propiedad tiempo de retraso y, a continuación, agregar un segundo cuadro de edición y una etiqueta para la propiedad mezcla húmeda.</span><span class="sxs-lookup"><span data-stu-id="6a389-111">You can first change the existing edit box and label to be useful for the delay time property and then add a second edit box and label for the wet mix property.</span></span>

<span data-ttu-id="6a389-112">Para editar el recurso de cuadro de diálogo en Visual C++:</span><span class="sxs-lookup"><span data-stu-id="6a389-112">To edit the dialog resource in Visual C++:</span></span>

1.  <span data-ttu-id="6a389-113">Haga clic en la pestaña **ResourceView** en el área de trabajo del proyecto.</span><span class="sxs-lookup"><span data-stu-id="6a389-113">Click the **ResourceView** tab in the Project Workspace.</span></span>
2.  <span data-ttu-id="6a389-114">Expanda el árbol recursos abriendo la carpeta de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="6a389-114">Expand the resources tree by opening the top level folder.</span></span>
3.  <span data-ttu-id="6a389-115">Abra la carpeta del **cuadro de diálogo** .</span><span class="sxs-lookup"><span data-stu-id="6a389-115">Open the **Dialog** folder.</span></span>
4.  <span data-ttu-id="6a389-116">Haga doble clic en el nombre del recurso de cuadro de diálogo, IDD \_ ECHOPROPPAGE.</span><span class="sxs-lookup"><span data-stu-id="6a389-116">Double-click the dialog resource name, IDD\_ECHOPROPPAGE.</span></span> <span data-ttu-id="6a389-117">El editor de recursos aparece en el panel derecho.</span><span class="sxs-lookup"><span data-stu-id="6a389-117">The resource editor appears in the right pane.</span></span>

## <a name="changing-the-existing-resources"></a><span data-ttu-id="6a389-118">Cambiar los recursos existentes</span><span class="sxs-lookup"><span data-stu-id="6a389-118">Changing the Existing Resources</span></span>

<span data-ttu-id="6a389-119">Para cambiar los recursos de la página de propiedades existente para la propiedad tiempo de retraso:</span><span class="sxs-lookup"><span data-stu-id="6a389-119">To change the existing property page resources for the delay time property:</span></span>

1.  <span data-ttu-id="6a389-120">En primer lugar, cambie el texto del control de texto estático existente.</span><span class="sxs-lookup"><span data-stu-id="6a389-120">First, change the text in the existing static text control.</span></span> <span data-ttu-id="6a389-121">Haga clic con el botón secundario en el control y seleccione **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="6a389-121">Right-click the control and then choose **Properties**.</span></span> <span data-ttu-id="6a389-122">En el campo **título** , escriba el nuevo título:</span><span class="sxs-lookup"><span data-stu-id="6a389-122">In the **Caption** field, type the new caption:</span></span>
    ```C++
    Delay time (0 to 2000):
    
    ```

    

2.  <span data-ttu-id="6a389-123">Cierre el cuadro de diálogo Propiedades del texto.</span><span class="sxs-lookup"><span data-stu-id="6a389-123">Close the Text Properties dialog box.</span></span>
3.  <span data-ttu-id="6a389-124">Ahora, cambie el nombre del control del cuadro de edición.</span><span class="sxs-lookup"><span data-stu-id="6a389-124">Now, change the name of the edit box control.</span></span> <span data-ttu-id="6a389-125">Para ello, haga clic con el botón secundario en el control y, a continuación, elija **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="6a389-125">To do this, right-click the control and then choose **Properties**.</span></span> <span data-ttu-id="6a389-126">En el campo **ID** , escriba un nuevo nombre para el control:</span><span class="sxs-lookup"><span data-stu-id="6a389-126">In the **ID** field, type a new name for the control:</span></span>
    ```C++
    IDC_DELAYTIME
    
    ```

    

4.  <span data-ttu-id="6a389-127">Cierre el cuadro de diálogo Editar propiedades.</span><span class="sxs-lookup"><span data-stu-id="6a389-127">Close the Edit Properties dialog box.</span></span>
5.  <span data-ttu-id="6a389-128">Guarde el recurso.</span><span class="sxs-lookup"><span data-stu-id="6a389-128">Save the resource.</span></span>
6.  <span data-ttu-id="6a389-129">Responda **sí** si se le pide que vuelva a cargar el archivo resource. h.</span><span class="sxs-lookup"><span data-stu-id="6a389-129">Answer **Yes** if prompted to reload the file resource.h.</span></span>
7.  <span data-ttu-id="6a389-130">Haga clic en la pestaña **FileView** en el área de trabajo del proyecto.</span><span class="sxs-lookup"><span data-stu-id="6a389-130">Click the **FileView** tab in the Project Workspace.</span></span> <span data-ttu-id="6a389-131">Abra Resource. h</span><span class="sxs-lookup"><span data-stu-id="6a389-131">Open resource.h</span></span>
8.  <span data-ttu-id="6a389-132">Busque el \# recurso de cuadro de edición definir para el factor de escala (IDC \_ SCALEFACTOR) y elimínelo.</span><span class="sxs-lookup"><span data-stu-id="6a389-132">Locate the \#define for the scale factor edit box resource (IDC\_SCALEFACTOR) and delete it.</span></span> <span data-ttu-id="6a389-133">Debe tener el mismo número de identificador que IDC \_ DELAYTIME.</span><span class="sxs-lookup"><span data-stu-id="6a389-133">It should have the same id number as IDC\_DELAYTIME.</span></span>

## <a name="adding-the-new-resources"></a><span data-ttu-id="6a389-134">Agregar los nuevos recursos</span><span class="sxs-lookup"><span data-stu-id="6a389-134">Adding the New Resources</span></span>

<span data-ttu-id="6a389-135">Para agregar los recursos de la nueva página de propiedades para la propiedad Mix húmeda:</span><span class="sxs-lookup"><span data-stu-id="6a389-135">To add the new property page resources for the wet mix property:</span></span>

1.  <span data-ttu-id="6a389-136">Haga clic en la pestaña **ResourceView** en el área de trabajo del proyecto para seleccionarla.</span><span class="sxs-lookup"><span data-stu-id="6a389-136">Click the **ResourceView** tab in the Project Workspace to select it.</span></span>
2.  <span data-ttu-id="6a389-137">Haga doble clic en el nombre del cuadro de diálogo Página de propiedades, ECHOPROPPAGE de IDD \_ .</span><span class="sxs-lookup"><span data-stu-id="6a389-137">Double-click the name of the property page dialog box, IDD\_ECHOPROPPAGE.</span></span> <span data-ttu-id="6a389-138">El editor de recursos aparece en el panel derecho.</span><span class="sxs-lookup"><span data-stu-id="6a389-138">The resource editor appears in the right pane.</span></span>
3.  <span data-ttu-id="6a389-139">Utilice el cuadro de herramientas para agregar un control de texto estático y un cuadro de edición a la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="6a389-139">Use the toolbox to add a static text control and an edit box to the property page.</span></span>
4.  <span data-ttu-id="6a389-140">Haga clic con el botón secundario en el control texto estático y elija **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="6a389-140">Right-click the static text control and choose **Properties**.</span></span>
5.  <span data-ttu-id="6a389-141">Escriba un nuevo nombre para el control de texto estático en el campo **ID** :</span><span class="sxs-lookup"><span data-stu-id="6a389-141">Type a new name for the static text control in the **ID** field:</span></span>
    ```C++
    IDC_MIXLABEL
    
    ```

    

6.  <span data-ttu-id="6a389-142">Escriba un título para la etiqueta:</span><span class="sxs-lookup"><span data-stu-id="6a389-142">Type a caption for the label:</span></span>
    ```C++
    Effect level (%):
    
    ```

    

7.  <span data-ttu-id="6a389-143">Cierre el cuadro de diálogo Propiedades del texto.</span><span class="sxs-lookup"><span data-stu-id="6a389-143">Close the Text Properties dialog box.</span></span>
8.  <span data-ttu-id="6a389-144">Haga clic con el botón secundario en el cuadro de edición y elija **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="6a389-144">Right-click the edit box and choose **Properties**.</span></span>
9.  <span data-ttu-id="6a389-145">Escriba un nuevo nombre para el cuadro de edición en el campo **ID** :</span><span class="sxs-lookup"><span data-stu-id="6a389-145">Type a new name for the edit box in the **ID** field:</span></span>
    ```C++
    IDC_WETMIX
    
    ```

    

10. <span data-ttu-id="6a389-146">Cierre el cuadro de diálogo Editar propiedades.</span><span class="sxs-lookup"><span data-stu-id="6a389-146">Close the Edit Properties dialog box.</span></span>

<span data-ttu-id="6a389-147">Al guardar el proyecto, es posible que se le pida que vuelva a cargar Resource. h.</span><span class="sxs-lookup"><span data-stu-id="6a389-147">When you save the project, you may be prompted to reload resource.h.</span></span> <span data-ttu-id="6a389-148">Si esto ocurre, haga clic en **sí** .</span><span class="sxs-lookup"><span data-stu-id="6a389-148">Click **Yes** if this happens.</span></span> <span data-ttu-id="6a389-149">El editor de recursos del cuadro de diálogo debe agregar los nombres de recursos y los números de identificador a Resource. h para los elementos que agregó.</span><span class="sxs-lookup"><span data-stu-id="6a389-149">The dialog box resource editor should add the resource names and id numbers to resource.h for the items you added.</span></span> <span data-ttu-id="6a389-150">Si por alguna razón esto no sucede, debe abrir Resource. h y escribir nuevas entradas para el control etiqueta y editar cuadro y asignar cada número de identificador único.</span><span class="sxs-lookup"><span data-stu-id="6a389-150">If for some reason this doesn't happen, you must open resource.h and type new entries for the label and edit box control, and assign each a unique id number.</span></span>

## <a name="modifying-and-adding-the-string-resources"></a><span data-ttu-id="6a389-151">Modificar y agregar los recursos de cadena</span><span class="sxs-lookup"><span data-stu-id="6a389-151">Modifying and Adding the String Resources</span></span>

<span data-ttu-id="6a389-152">El código de ejemplo del Asistente para complementos especifica un recurso de cadena denominado IDS \_ SCALERANGEERROR que contiene un mensaje que se muestra cuando la entrada del usuario está fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="6a389-152">The plug-in wizard sample code specifies a string resource named IDS\_SCALERANGEERROR that contains a message to display when the user input is out of range.</span></span> <span data-ttu-id="6a389-153">Puede modificar este recurso para que se adapte a sus necesidades del valor de tiempo de retraso siguiendo estos pasos en Visual C++:</span><span class="sxs-lookup"><span data-stu-id="6a389-153">You can modify this resource to suit your needs for the delay time value by following these steps in Visual C++:</span></span>

1.  <span data-ttu-id="6a389-154">Haga clic en la pestaña **ResourceView** .</span><span class="sxs-lookup"><span data-stu-id="6a389-154">Click the **ResourceView** tab.</span></span>
2.  <span data-ttu-id="6a389-155">Abra la carpeta de la **tabla de cadenas** .</span><span class="sxs-lookup"><span data-stu-id="6a389-155">Open the **String Table** folder.</span></span>
3.  <span data-ttu-id="6a389-156">Haga doble clic en el icono de la **tabla de cadenas** para abrir el editor de recursos.</span><span class="sxs-lookup"><span data-stu-id="6a389-156">Double-click the **String Table** icon to open the resource editor.</span></span>
4.  <span data-ttu-id="6a389-157">Haga doble clic en el nombre del recurso que desea editar, en este caso, IDS \_ SCALERANGEERROR.</span><span class="sxs-lookup"><span data-stu-id="6a389-157">Double-click the name of the resource you want to edit, in this case, IDS\_SCALERANGEERROR.</span></span> <span data-ttu-id="6a389-158">Aparecerá el cuadro de diálogo Propiedades de la cadena.</span><span class="sxs-lookup"><span data-stu-id="6a389-158">The String Properties dialog box appears.</span></span>
5.  <span data-ttu-id="6a389-159">Cambie el nombre del campo **ID** a ID \_ DELAYRANGEERROR.</span><span class="sxs-lookup"><span data-stu-id="6a389-159">Change the name in the **ID** field to IDS\_DELAYRANGEERROR.</span></span>
6.  <span data-ttu-id="6a389-160">Cambie el texto en el campo de **título** :</span><span class="sxs-lookup"><span data-stu-id="6a389-160">Change the text in the **Caption** field:</span></span>
    ```C++
    You must enter a delay time between 0 and 2000 milliseconds.
    
    ```

    

7.  <span data-ttu-id="6a389-161">Cierre el cuadro de diálogo Propiedades de la cadena.</span><span class="sxs-lookup"><span data-stu-id="6a389-161">Close the String Properties dialog box.</span></span>

<span data-ttu-id="6a389-162">Después, agregue un nuevo recurso de cadena para el mensaje de error de la propiedad Mix húmeda.</span><span class="sxs-lookup"><span data-stu-id="6a389-162">Next, add a new string resource for the wet mix property error message.</span></span>

1.  <span data-ttu-id="6a389-163">Haga doble clic en la línea vacía en la parte inferior del editor de recursos.</span><span class="sxs-lookup"><span data-stu-id="6a389-163">Double-click the empty line at the bottom of the resource editor.</span></span>
2.  <span data-ttu-id="6a389-164">Cambie el nombre del campo **ID** a ID \_ MIXRANGEERROR.</span><span class="sxs-lookup"><span data-stu-id="6a389-164">Change the name in the **ID** field to IDS\_MIXRANGEERROR.</span></span>
3.  <span data-ttu-id="6a389-165">Agregue el texto siguiente al campo de **título** :</span><span class="sxs-lookup"><span data-stu-id="6a389-165">Add the following text to the **Caption** field:</span></span>
    ```C++
    You must enter an effect level between 0 and 100 percent.
    
    ```

    

4.  <span data-ttu-id="6a389-166">Cierre el cuadro de diálogo Propiedades de la cadena.</span><span class="sxs-lookup"><span data-stu-id="6a389-166">Close the String Properties dialog box.</span></span>

<span data-ttu-id="6a389-167">Hay otros dos valores que desea cambiar en la tabla de cadenas.</span><span class="sxs-lookup"><span data-stu-id="6a389-167">There are two other values you will want to change in the String Table.</span></span> <span data-ttu-id="6a389-168">ID \_ . FRIENDLYNAME es el nombre que aparece en la interfaz de usuario de Media Player de Windows para identificar el complemento.</span><span class="sxs-lookup"><span data-stu-id="6a389-168">IDS\_FRIENDLYNAME is the name that appears in the Windows Media Player user interface to identify the plug-in.</span></span> <span data-ttu-id="6a389-169">\_La descripción de IDS le permite indicar al usuario sobre el complemento.</span><span class="sxs-lookup"><span data-stu-id="6a389-169">IDS\_DESCRIPTION lets you tell the user about your plug-in.</span></span> <span data-ttu-id="6a389-170">Ambas cadenas se pasan como parámetros a la función **IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin** , a la que se llama en el método DllRegisterServer en Echodll. cpp.</span><span class="sxs-lookup"><span data-stu-id="6a389-170">Both of these strings are passed as parameters to the **IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin** function, which is called in the DllRegisterServer method in Echodll.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a389-171">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6a389-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a389-172">**Modificar la página de propiedades de ejemplo echo**</span><span class="sxs-lookup"><span data-stu-id="6a389-172">**Modifying the Echo Sample Property Page**</span></span>](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




