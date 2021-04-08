---
title: Asegurarse de que los elementos de la interfaz de usuario se denominan correctamente
description: En este tema se describe la manera correcta de especificar los nombres de los elementos de la interfaz de usuario en las aplicaciones de Microsoft Win32 para que Microsoft Active Accessibility pueda exponer con precisión los nombres a las aplicaciones cliente a través del IAccessible \ 32; Propiedad nombre.
ms.assetid: 5b8f23cb-9906-4cc4-83d4-73fdf96ed681
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db3c4f1fc129aea9b793bac1935d678645b28fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995315"
---
# <a name="ensuring-that-ui-elements-are-correctly-named"></a><span data-ttu-id="c31d9-103">Asegurarse de que los elementos de la interfaz de usuario se denominan correctamente</span><span class="sxs-lookup"><span data-stu-id="c31d9-103">Ensuring that UI Elements are Correctly Named</span></span>

<span data-ttu-id="c31d9-104">En este tema se describe la manera correcta de especificar los nombres de los elementos de la interfaz de usuario en las aplicaciones de Microsoft Win32 para que Microsoft Active Accessibility pueda exponer con precisión los nombres a las aplicaciones cliente a través de la propiedad [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) [Name](name-property.md).</span><span class="sxs-lookup"><span data-stu-id="c31d9-104">This topic describes the correct way to specify the names of the UI elements in your Microsoft Win32 applications so that Microsoft Active Accessibility can accurately expose the names to client applications through the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) [Name property](name-property.md).</span></span>

<span data-ttu-id="c31d9-105">La información de esta sección se aplica solo a Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="c31d9-105">The information in this section applies to Microsoft Active Accessibility only.</span></span> <span data-ttu-id="c31d9-106">No se aplica a las aplicaciones que usan la automatización de la interfaz de usuario de Microsoft o las basadas en lenguajes de marcado, como HTML, HTML dinámico (DHTML) o XML.</span><span class="sxs-lookup"><span data-stu-id="c31d9-106">It does not apply to applications that use Microsoft UI Automation or those based on markup languages such as HTML, Dynamic HTML (DHTML), or XML.</span></span>

-   [<span data-ttu-id="c31d9-107">Información general</span><span class="sxs-lookup"><span data-stu-id="c31d9-107">Overview</span></span>](#overview)
-   [<span data-ttu-id="c31d9-108">Cómo la nomenclatura incorrecta causa problemas</span><span class="sxs-lookup"><span data-stu-id="c31d9-108">How Incorrect Naming Causes Problems</span></span>](#how-incorrect-naming-causes-problems)
-   [<span data-ttu-id="c31d9-109">Cómo obtiene MSAA la propiedad Name</span><span class="sxs-lookup"><span data-stu-id="c31d9-109">How MSAA Gets the Name Property</span></span>](#how-msaa-gets-the-name-property)
-   [<span data-ttu-id="c31d9-110">Cómo buscar y corregir problemas de nomenclatura</span><span class="sxs-lookup"><span data-stu-id="c31d9-110">How to Find and Correct Naming Problems</span></span>](#how-to-find-and-correct-naming-problems)
-   [<span data-ttu-id="c31d9-111">Cómo asignar un nombre correcto a un TrackBar</span><span class="sxs-lookup"><span data-stu-id="c31d9-111">How to Correctly Name a Trackbar</span></span>](#how-to-correctly-name-a-trackbar)
-   [<span data-ttu-id="c31d9-112">Cómo usar etiquetas invisibles para asignar nombres a los controles</span><span class="sxs-lookup"><span data-stu-id="c31d9-112">How to Use Invisible Labels to Name Controls</span></span>](#how-to-use-invisible-labels-to-name-controls)
-   [<span data-ttu-id="c31d9-113">Cómo usar la anotación directa para especificar la propiedad Name</span><span class="sxs-lookup"><span data-stu-id="c31d9-113">How to Use Direct Annotation to Specify the Name Property</span></span>](#how-to-use-direct-annotation-to-specify-the-name-property)
    -   [<span data-ttu-id="c31d9-114">Pasos para anotar la propiedad Name</span><span class="sxs-lookup"><span data-stu-id="c31d9-114">Steps for Annotating the Name Property</span></span>](#steps-for-annotating-the-name-property)
    -   [<span data-ttu-id="c31d9-115">Ejemplo de anotar la propiedad Name</span><span class="sxs-lookup"><span data-stu-id="c31d9-115">Example of Annotating the Name Property</span></span>](#example-of-annotating-the-name-property)
-   [<span data-ttu-id="c31d9-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c31d9-116">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="c31d9-117">Información general</span><span class="sxs-lookup"><span data-stu-id="c31d9-117">Overview</span></span>

<span data-ttu-id="c31d9-118">En Microsoft Active Accessibility, cada elemento de la interfaz de usuario de una aplicación se representa mediante un objeto que expone la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="c31d9-118">In Microsoft Active Accessibility, each UI element in an application is represented by an object that exposes the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="c31d9-119">Las aplicaciones cliente utilizan las propiedades y los métodos de la interfaz **IAccessible** para interactuar con el elemento de la interfaz de usuario y recuperar información sobre él.</span><span class="sxs-lookup"><span data-stu-id="c31d9-119">Client applications use the properties and methods of the **IAccessible** interface to interact with the UI element and to retrieve information about it.</span></span> <span data-ttu-id="c31d9-120">Una de las propiedades más importantes que expone la interfaz **IAccessible** es la [propiedad Name](name-property.md).</span><span class="sxs-lookup"><span data-stu-id="c31d9-120">One of the most important properties exposed by the **IAccessible** interface is the [Name property](name-property.md).</span></span> <span data-ttu-id="c31d9-121">Las aplicaciones cliente se basan en la propiedad Name para buscar, identificar o anunciar un elemento de la interfaz de usuario al usuario.</span><span class="sxs-lookup"><span data-stu-id="c31d9-121">Client applications rely on the Name property to find, identify, or announce a UI element to the user.</span></span> <span data-ttu-id="c31d9-122">Si Microsoft Active Accessibility no puede exponer correctamente la propiedad Name de un elemento de la interfaz de usuario determinado, las aplicaciones cliente no podrán presentar ese elemento de la interfaz de usuario al usuario, y el elemento de la interfaz de usuario no estará accesible para los usuarios con discapacidades.</span><span class="sxs-lookup"><span data-stu-id="c31d9-122">If Microsoft Active Accessibility cannot properly expose the Name property of a particular UI element, client applications will be unable to present that UI element to the user, and the UI element will be inaccessible to users with disabilities.</span></span>

## <a name="how-incorrect-naming-causes-problems"></a><span data-ttu-id="c31d9-123">Cómo la nomenclatura incorrecta causa problemas</span><span class="sxs-lookup"><span data-stu-id="c31d9-123">How Incorrect Naming Causes Problems</span></span>

<span data-ttu-id="c31d9-124">Para ilustrar los problemas causados por la nomenclatura incorrecta de los elementos de la interfaz de usuario, tenga en cuenta el formato de entrada de nombre que se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="c31d9-124">To illustrate the problems caused by incorrect naming of UI elements, consider the name entry form shown in the following illustration.</span></span>

![Ilustración de un formulario simple para escribir el nombre y el apellido](images/incorrect-form.png)

<span data-ttu-id="c31d9-126">Aunque los elementos de la interfaz de usuario del formulario son correctos, la implementación mediante programación es incorrecta.</span><span class="sxs-lookup"><span data-stu-id="c31d9-126">Although the UI elements in the form look okay, the programmatic implementation is incorrect.</span></span> <span data-ttu-id="c31d9-127">En un cliente de Microsoft Active Accessibility como un lector de pantalla, la [propiedad Name](name-property.md) del control de edición superior es "Last Name:" y la propiedad Name del control de edición inferior es una cadena vacía ("").</span><span class="sxs-lookup"><span data-stu-id="c31d9-127">To a Microsoft Active Accessibility client such as a screen reader, the [Name property](name-property.md) of the top edit control is "Last Name:", and the Name property of the bottom edit control is an empty string ("").</span></span> <span data-ttu-id="c31d9-128">El lector de pantalla leerá el control de edición superior como "Last Name", aunque se espera que el usuario escriba el nombre.</span><span class="sxs-lookup"><span data-stu-id="c31d9-128">The screen reader will read the top edit control as "Last Name", although the user is expected to type in the first name.</span></span> <span data-ttu-id="c31d9-129">El lector de pantalla leerá el segundo control de edición como "sin nombre", por lo que el usuario no tendrá ninguna idea de lo que debe escribir en el segundo control de edición.</span><span class="sxs-lookup"><span data-stu-id="c31d9-129">The screen reader will read the second edit control as "no name", so the user will have no idea what to type into the second edit control.</span></span> <span data-ttu-id="c31d9-130">El lector de pantalla no puede ayudar al usuario a escribir datos en este formato sencillo.</span><span class="sxs-lookup"><span data-stu-id="c31d9-130">The screen reader is unable to assist the user in entering data into this simple form.</span></span>

<span data-ttu-id="c31d9-131">Otro problema del formulario es que no se ha asignado ninguna tecla de método abreviado a ninguno de los controles de edición.</span><span class="sxs-lookup"><span data-stu-id="c31d9-131">Another problem with the form is that no shortcut keys are assigned to either of the edit controls.</span></span> <span data-ttu-id="c31d9-132">El usuario se ve obligado a cualquier pestaña a los controles o a usar el mouse.</span><span class="sxs-lookup"><span data-stu-id="c31d9-132">The user is forced to either tab to the controls or use the mouse.</span></span>

<span data-ttu-id="c31d9-133">En las secciones siguientes se explica el origen de estos problemas y se proporcionan directrices para corregirlos.</span><span class="sxs-lookup"><span data-stu-id="c31d9-133">The following sections explain the source of these problems and provide guidelines for correcting them.</span></span>

## <a name="how-msaa-gets-the-name-property"></a><span data-ttu-id="c31d9-134">Cómo obtiene MSAA la propiedad Name</span><span class="sxs-lookup"><span data-stu-id="c31d9-134">How MSAA Gets the Name Property</span></span>

<span data-ttu-id="c31d9-135">Microsoft Active Accessibility obtiene la cadena de la [propiedad Name](name-property.md) de diferentes ubicaciones en función del tipo del elemento de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="c31d9-135">Microsoft Active Accessibility gets the [Name property](name-property.md) string from different locations depending on the type of the UI element.</span></span> <span data-ttu-id="c31d9-136">Para la mayoría de los elementos de la interfaz de usuario que tienen el texto de ventana asociado, Microsoft Active Accessibility usa el texto de la ventana como la cadena de la propiedad Name.</span><span class="sxs-lookup"><span data-stu-id="c31d9-136">For most UI elements that have associated window text, Microsoft Active Accessibility uses the window text as the Name property string.</span></span> <span data-ttu-id="c31d9-137">Algunos ejemplos de este tipo de elemento de la interfaz de usuario son los controles como botones, elementos de menú e información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="c31d9-137">Examples of this type of UI element include controls such as buttons, menu items, and tooltips.</span></span>

<span data-ttu-id="c31d9-138">En el caso de los siguientes controles, Microsoft Active Accessibility omite el texto de la ventana y, en su lugar, busca una etiqueta de texto estático (o etiqueta de cuadro de grupo) inmediatamente antes del control en el orden de tabulación.</span><span class="sxs-lookup"><span data-stu-id="c31d9-138">For the following controls, Microsoft Active Accessibility ignores the window text and instead looks for a static text label (or group box label) immediately preceding the control in the tab order.</span></span>

-   <span data-ttu-id="c31d9-139">Cuadros combinados</span><span class="sxs-lookup"><span data-stu-id="c31d9-139">Combo Boxes</span></span>
-   <span data-ttu-id="c31d9-140">Selectores de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="c31d9-140">Date and Time Pickers</span></span>
-   <span data-ttu-id="c31d9-141">Editar y controles Rich Edit</span><span class="sxs-lookup"><span data-stu-id="c31d9-141">Edit and Rich Edit controls</span></span>
-   <span data-ttu-id="c31d9-142">Controles de direcciones IP</span><span class="sxs-lookup"><span data-stu-id="c31d9-142">IP Address controls</span></span>
-   <span data-ttu-id="c31d9-143">Cuadros de lista</span><span class="sxs-lookup"><span data-stu-id="c31d9-143">List Boxes</span></span>
-   <span data-ttu-id="c31d9-144">Vistas de lista</span><span class="sxs-lookup"><span data-stu-id="c31d9-144">List Views</span></span>
-   <span data-ttu-id="c31d9-145">Barras de progreso</span><span class="sxs-lookup"><span data-stu-id="c31d9-145">Progress Bars</span></span>
-   <span data-ttu-id="c31d9-146">Barras</span><span class="sxs-lookup"><span data-stu-id="c31d9-146">Scrollbars</span></span>
-   <span data-ttu-id="c31d9-147">Controles estáticos que tienen el \_ icono SS o el \_ estilo de mapa de bits SS</span><span class="sxs-lookup"><span data-stu-id="c31d9-147">Static controls that have the SS\_ICON or SS\_BITMAP style</span></span>
-   <span data-ttu-id="c31d9-148">Trackbars</span><span class="sxs-lookup"><span data-stu-id="c31d9-148">Trackbars</span></span>
-   <span data-ttu-id="c31d9-149">Vistas de árbol</span><span class="sxs-lookup"><span data-stu-id="c31d9-149">Tree Views</span></span>

<span data-ttu-id="c31d9-150">Si los controles anteriores no van acompañados de etiquetas de texto estático, o si las etiquetas no se implementan correctamente, Microsoft Active Accessibility no puede proporcionar la [propiedad de nombre](name-property.md) correcta a las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="c31d9-150">If the preceding controls are not accompanied by static text labels, or if the labels are not implemented correctly, Microsoft Active Accessibility cannot provide the correct [Name property](name-property.md) to client applications.</span></span>

<span data-ttu-id="c31d9-151">La mayoría de los controles anteriores realmente tienen el texto de la ventana asociado.</span><span class="sxs-lookup"><span data-stu-id="c31d9-151">Most of the preceding controls actually do have associated window text.</span></span> <span data-ttu-id="c31d9-152">El editor de recursos genera automáticamente el texto de la ventana, que consta de una cadena genérica, como "Edit1" o "listbox3".</span><span class="sxs-lookup"><span data-stu-id="c31d9-152">The resource editor automatically generates the window text, which consists of a generic string such as "edit1" or "listbox3".</span></span> <span data-ttu-id="c31d9-153">Aunque los desarrolladores pueden reemplazar el texto de la ventana generado por texto más significativo, la mayoría de las tareas nunca lo hacen.</span><span class="sxs-lookup"><span data-stu-id="c31d9-153">Although developers can replace the generated window text with more meaningful text, most never do.</span></span> <span data-ttu-id="c31d9-154">Dado que el texto de la ventana generada no tiene ningún significado para el usuario, Microsoft Active Accessibility lo omite y usa la etiqueta de texto estático correspondiente en su lugar.</span><span class="sxs-lookup"><span data-stu-id="c31d9-154">Because the generated window text has no meaning to the user, Microsoft Active Accessibility ignores it and uses the accompanying static text label instead.</span></span>

## <a name="how-to-find-and-correct-naming-problems"></a><span data-ttu-id="c31d9-155">Cómo buscar y corregir problemas de nomenclatura</span><span class="sxs-lookup"><span data-stu-id="c31d9-155">How to Find and Correct Naming Problems</span></span>

<span data-ttu-id="c31d9-156">En el formulario de entrada nombre que se muestra en el modo en que la nomenclatura incorrecta causa problemas, la causa de los problemas es que el orden de tabulación de los controles es incorrecto.</span><span class="sxs-lookup"><span data-stu-id="c31d9-156">In the name entry form shown in How Incorrect Naming Causes Problems, the cause of the problems is that the tab order of the controls is incorrect.</span></span> <span data-ttu-id="c31d9-157">Examinar la interfaz de usuario con una herramienta de prueba, como [inspeccionar](inspect-objects.md) , revelaría los problemas con la jerarquía de objetos.</span><span class="sxs-lookup"><span data-stu-id="c31d9-157">Examining the UI with a testing tool such as [Inspect](inspect-objects.md) would reveal the problems with the object hierarchy.</span></span> <span data-ttu-id="c31d9-158">En la captura de pantalla siguiente se muestra la jerarquía de objetos rotas del formulario de entrada nombre tal y como aparece en inspeccionar.</span><span class="sxs-lookup"><span data-stu-id="c31d9-158">The following screen shot shows the broken object hierarchy of the name entry form as it appears in Inspect.</span></span>

![captura de pantalla de la herramienta inspeccionar que muestra una jerarquía de objetos incorrecta del formulario de entrada nombre](images/incorrect-object-hierarchy.png)

<span data-ttu-id="c31d9-160">En la captura de pantalla anterior, observe que la jerarquía de objetos no coincide con la estructura de los controles tal y como aparecen en la interfaz de usuario del formulario de entrada de nombre.</span><span class="sxs-lookup"><span data-stu-id="c31d9-160">In the previous screen shot, notice that the object hierarchy does not match the structure of the controls as they appear in the user interface of the name entry form.</span></span> <span data-ttu-id="c31d9-161">Observe también que [inspeccionar](inspect-objects.md) ha asignado el nombre incorrecto al elemento siguiente al último (es el control de edición para escribir el nombre y debe ser un nombre "nombre:".</span><span class="sxs-lookup"><span data-stu-id="c31d9-161">Also notice that [Inspect](inspect-objects.md) has assigned the incorrect name to the next-to-last item (it is the edit control for entering the first name and should be a named "First Name:".</span></span> <span data-ttu-id="c31d9-162">Por último, observe que inspeccionar no pudo encontrar un nombre para el último elemento (es el control de edición para escribir el apellido y debe tener el nombre "Last Name:".</span><span class="sxs-lookup"><span data-stu-id="c31d9-162">Finally, notice that Inspect could not find a name for the last item (it is the edit control for entering the last name and should have a name of "Last Name:".</span></span>

<span data-ttu-id="c31d9-163">En el ejemplo siguiente se muestra el contenido del archivo de recursos para el formulario de entrada Name.</span><span class="sxs-lookup"><span data-stu-id="c31d9-163">The following example shows the contents of the resource file for the name entry form.</span></span> <span data-ttu-id="c31d9-164">Observe que el orden de tabulación no es coherente con la estructura lógica de los controles tal y como aparecen en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="c31d9-164">Notice that the tab order is not consistent with the logical structure of the controls as they appear in the user interface.</span></span> <span data-ttu-id="c31d9-165">Observe también que no se han especificado teclas de método abreviado para los dos controles de edición.</span><span class="sxs-lookup"><span data-stu-id="c31d9-165">Also notice that no shortcut keys are specified for the two edit controls.</span></span>

``` syntax
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
    LTEXT           "First Name:",IDC_STATIC,8,16,43,8
    LTEXT           "Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDIT1,53,15,120,12,ES_AUTOHSCROLL
    EDITTEXT        IDC_EDIT2,53,34,120,12,ES_AUTOHSCROLL
END
```

<span data-ttu-id="c31d9-166">Para corregir los problemas con el formulario de entrada de nombre, se debe editar el archivo de recursos (. RC) para especificar los métodos abreviados de teclado y los controles deben colocarse en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="c31d9-166">To correct the problems with the name entry form, the resource (.rc) file should be edited to specify keyboard shortcuts, and the controls should be placed in the following order:</span></span>

1.  <span data-ttu-id="c31d9-167">La etiqueta de texto estático "&First Name:".</span><span class="sxs-lookup"><span data-stu-id="c31d9-167">The "&First Name:" static text label.</span></span>
2.  <span data-ttu-id="c31d9-168">Control de edición para escribir el nombre (IDC \_ EDIT1).</span><span class="sxs-lookup"><span data-stu-id="c31d9-168">The edit control for entering the first name (IDC\_EDIT1).</span></span>
3.  <span data-ttu-id="c31d9-169">La etiqueta de texto estático "&Last Name:".</span><span class="sxs-lookup"><span data-stu-id="c31d9-169">The "&Last Name:" static text label.</span></span>
4.  <span data-ttu-id="c31d9-170">Control de edición para escribir el apellido (IDC \_ EDIT2).</span><span class="sxs-lookup"><span data-stu-id="c31d9-170">The edit control for entering the last name (IDC\_EDIT2).</span></span>
5.  <span data-ttu-id="c31d9-171">Botón de opción predeterminado "Aceptar".</span><span class="sxs-lookup"><span data-stu-id="c31d9-171">The "OK" default push button.</span></span>

<span data-ttu-id="c31d9-172">En el ejemplo siguiente se muestra el archivo de recursos corregido para el formulario de entrada Name:</span><span class="sxs-lookup"><span data-stu-id="c31d9-172">The following example shows the corrected resource file for the name entry form:</span></span>

``` syntax
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    LTEXT           "&First Name:",IDC_STATIC,8,16,43,8
    EDITTEXT        IDC_EDIT1,53,15,120,12,ES_AUTOHSCROLL
    LTEXT           "&Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDIT2,53,34,120,12,ES_AUTOHSCROLL
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
END
```

<span data-ttu-id="c31d9-173">Para realizar correcciones en un archivo de recursos, puede editar el archivo directamente, o bien puede usar la herramienta orden de tabulación en Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c31d9-173">To make corrections to a resource file, you can either edit the file directly, or you can use the Tab Order tool in Microsoft Visual Studio.</span></span> <span data-ttu-id="c31d9-174">Puede tener acceso a la herramienta orden de tabulación en Visual Studio presionando CTRL + D o seleccionando el **orden de tabulación** en el menú **formato** .</span><span class="sxs-lookup"><span data-stu-id="c31d9-174">You can access the Tab Order tool in Visual Studio either by pressing CTRL+D, or by selecting **Tab Order** from the **Format** menu.</span></span>

<span data-ttu-id="c31d9-175">Después de corregir y volver a compilar la aplicación, la interfaz de usuario del formulario de entrada names tendrá el mismo aspecto que antes.</span><span class="sxs-lookup"><span data-stu-id="c31d9-175">After correcting and rebuilding the application, the UI of the names entry form will look the same as it did before.</span></span> <span data-ttu-id="c31d9-176">Sin embargo, Microsoft Active Accessibility ahora proporcionará las propiedades de nombre correctas a las aplicaciones cliente y establecerá el foco correctamente cuando el usuario presione los métodos abreviados de teclado ALT + F o ALT + L.</span><span class="sxs-lookup"><span data-stu-id="c31d9-176">However, Microsoft Active Accessibility will now provide the correct Name properties to client applications, and will set the focus correctly when the user presses the ALT+F or ALT+L keyboard shortcuts.</span></span> <span data-ttu-id="c31d9-177">Además, [inspeccionar](inspect-objects.md) mostrará la jerarquía de objetos correcta, como se muestra en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="c31d9-177">Also, [Inspect](inspect-objects.md) will show the correct object hierarchy, as the following screen shot shows.</span></span>

![captura de pantalla de la herramienta explorador accesible que muestra una jerarquía de objetos correcta del formulario de entrada nombre](images/correct-object-hierarchy.png)

## <a name="how-to-correctly-name-a-trackbar"></a><span data-ttu-id="c31d9-179">Cómo asignar un nombre correcto a un TrackBar</span><span class="sxs-lookup"><span data-stu-id="c31d9-179">How to Correctly Name a Trackbar</span></span>

<span data-ttu-id="c31d9-180">Al definir una barra de desplazamiento (o control deslizante), asegúrese de que la etiqueta de texto estático principal de la barra de desplazamiento aparece delante de la barra de desplazamiento y de que las etiquetas de texto estático de los intervalos mínimo y máximo aparecen después de la barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="c31d9-180">When defining a trackbar (or slider), ensure that the main static text label for the trackbar appears before the trackbar, and that the static text labels for the minimum and maximum ranges appear after the trackbar.</span></span> <span data-ttu-id="c31d9-181">Recuerde que Microsoft Active Accessibility usa la etiqueta de texto estático que precede inmediatamente a un control como la [propiedad Name](name-property.md) del control.</span><span class="sxs-lookup"><span data-stu-id="c31d9-181">Remember that Microsoft Active Accessibility uses the static text label that immediately precedes a control as the [Name property](name-property.md) for the control.</span></span> <span data-ttu-id="c31d9-182">Colocar la etiqueta de texto estático principal inmediatamente antes de la barra de título y las demás etiquetas después, garantiza que Microsoft Active Accessibility proporciona la propiedad de nombre correcta a un cliente.</span><span class="sxs-lookup"><span data-stu-id="c31d9-182">Placing the main static text label immediately before the trackbar, and the other labels after it, ensures that Microsoft Active Accessibility provides the correct Name property to a client.</span></span>

<span data-ttu-id="c31d9-183">En la ilustración siguiente se muestra una barra de título típica con una etiqueta de texto estático principal denominada "Speed" y etiquetas de texto estático para los intervalos mínimo ("min") y máximo ("Max").</span><span class="sxs-lookup"><span data-stu-id="c31d9-183">The following illustration shows a typical trackbar with a main static text label called "Speed", and static text labels for the minimum ("min") and maximum ("max") ranges.</span></span>

![Ilustración de un control TrackBar que tiene una etiqueta principal y etiquetas para los intervalos mínimo y máximo](images/speed-trackbar.png)

<span data-ttu-id="c31d9-185">En el ejemplo siguiente se muestra la manera correcta de definir una barra de presentación y sus etiquetas de texto estático en el archivo de recursos:</span><span class="sxs-lookup"><span data-stu-id="c31d9-185">The following example shows the correct way to define a trackbar and its static text labels in the resource file:</span></span>

``` syntax
BEGIN
    ...

    LTEXT           "&Speed",IDC_STATIC,47,20,43,8
    CONTROL         "",IDC_SLIDER1,"msctls_trackbar32",
                    TBS_AUTOTICKS | TBS_BOTH | WS_TABSTOP,
                    32,32,62,23
    LTEXT           "min",IDC_STATIC,16,37,15,8
    LTEXT           "max",IDC_STATIC,94,38,43,8

    ...
END
```

## <a name="how-to-use-invisible-labels-to-name-controls"></a><span data-ttu-id="c31d9-186">Cómo usar etiquetas invisibles para asignar nombres a los controles</span><span class="sxs-lookup"><span data-stu-id="c31d9-186">How to Use Invisible Labels to Name Controls</span></span>

<span data-ttu-id="c31d9-187">No siempre es posible o deseable tener una etiqueta visible para cada control.</span><span class="sxs-lookup"><span data-stu-id="c31d9-187">It is not always possible or desirable to have a visible label for every control.</span></span> <span data-ttu-id="c31d9-188">Por ejemplo, a veces agregar etiquetas puede producir cambios no deseados en la apariencia de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="c31d9-188">For example, sometimes adding labels can cause undesirable changes in the appearance of the UI.</span></span> <span data-ttu-id="c31d9-189">En este caso, puede usar etiquetas invisibles.</span><span class="sxs-lookup"><span data-stu-id="c31d9-189">In this case, you can use invisible labels.</span></span> <span data-ttu-id="c31d9-190">Microsoft Active Accessibility seguirá recopilando el texto asociado a una etiqueta invisible, pero la etiqueta no aparecerá en la interfaz de usuario visual ni interferirá con ella.</span><span class="sxs-lookup"><span data-stu-id="c31d9-190">Microsoft Active Accessibility will still pick up the text associated with an invisible label, but the label will not appear in, or interfere with, the visual UI.</span></span>

<span data-ttu-id="c31d9-191">Al igual que con las etiquetas visibles, una etiqueta invisible debe preceder inmediatamente al control en el orden de tabulación.</span><span class="sxs-lookup"><span data-stu-id="c31d9-191">As with visible labels, an invisible label must immediately precede the control in the tab order.</span></span> <span data-ttu-id="c31d9-192">Para hacer que una etiqueta sea invisible en un archivo de recursos (. RC), agregue `NOT WS_VISIBLE` o `|~WS_VISIBLE` a la parte de estilo del control de texto estático.</span><span class="sxs-lookup"><span data-stu-id="c31d9-192">To make a label invisible in a resource file (.rc), add `NOT WS_VISIBLE` or `|~WS_VISIBLE` to the style part of the static text control.</span></span> <span data-ttu-id="c31d9-193">Si usa el editor de recursos en Visual Studio, puede establecer la propiedad visible en false.</span><span class="sxs-lookup"><span data-stu-id="c31d9-193">If you are using the Resource Editor in Visual Studio, you can set the Visible property to False.</span></span>

## <a name="how-to-use-direct-annotation-to-specify-the-name-property"></a><span data-ttu-id="c31d9-194">Cómo usar la anotación directa para especificar la propiedad Name</span><span class="sxs-lookup"><span data-stu-id="c31d9-194">How to Use Direct Annotation to Specify the Name Property</span></span>

<span data-ttu-id="c31d9-195">Los proxies predeterminados incluidos en el componente de tiempo de ejecución de Microsoft Active Accessibility, Oleacc.dll, proporcionan automáticamente un objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para todos los controles estándar de Windows.</span><span class="sxs-lookup"><span data-stu-id="c31d9-195">The default proxies included in the Microsoft Active Accessibility runtime component, Oleacc.dll, automatically provide an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object for all of the standard Windows controls.</span></span> <span data-ttu-id="c31d9-196">Si personaliza un control estándar de Windows, los proxies predeterminados hacen lo mejor para proporcionar con precisión todas las propiedades **IAccessible** para el control personalizado.</span><span class="sxs-lookup"><span data-stu-id="c31d9-196">If you customize a standard Windows control, the default proxies do their best to accurately provide all of the **IAccessible** properties for your customized control.</span></span> <span data-ttu-id="c31d9-197">Debe probar exhaustivamente un control personalizado para asegurarse de que los proxies predeterminados proporcionan valores de propiedad precisos y completos.</span><span class="sxs-lookup"><span data-stu-id="c31d9-197">You should thoroughly test a customized control to ensure that the default proxies are providing accurate and complete property values.</span></span> <span data-ttu-id="c31d9-198">Si las pruebas revela valores de propiedad inexactos o incompletos, es posible que pueda utilizar la técnica de anotación dinámica llamada anotación directa para proporcionar los valores de propiedad correctos y agregar los que faltan.</span><span class="sxs-lookup"><span data-stu-id="c31d9-198">If testing reveals inaccurate or incomplete property values, you may be able to use the Dynamic Annotation technique called direct annotation to provide correct property values and add those that are missing.</span></span>

<span data-ttu-id="c31d9-199">Tenga en cuenta que la anotación dinámica no es solo para los controles admitidos por los servidores proxy de Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="c31d9-199">Note that Dynamic Annotation is not just for controls supported by the Microsoft Active Accessibility proxies.</span></span> <span data-ttu-id="c31d9-200">También puede utilizarlo para modificar o proporcionar propiedades para cualquier control que proporcione su propia implementación de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="c31d9-200">You can also use it to modify or provide properties for any control that provides its own [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementation.</span></span>

<span data-ttu-id="c31d9-201">Esta sección se centra en el uso de la anotación directa para proporcionar un valor correcto para la [propiedad Name](name-property.md) del objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de un control.</span><span class="sxs-lookup"><span data-stu-id="c31d9-201">This section focuses on using direct annotation to provide a correct value for the [Name property](name-property.md) of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object for a control.</span></span> <span data-ttu-id="c31d9-202">También puede utilizar la anotación directa para proporcionar también otros valores de propiedades.</span><span class="sxs-lookup"><span data-stu-id="c31d9-202">You can use direct annotation to provide other properties values as well.</span></span> <span data-ttu-id="c31d9-203">Además, hay disponibles otras técnicas de anotación dinámica junto con la anotación directa, y las características y capacidades de la API de anotación dinámica se extienden mucho más allá de lo que se describe en esta sección.</span><span class="sxs-lookup"><span data-stu-id="c31d9-203">Also, other Dynamic Annotation techniques beside direct annotation are available, and the features and capabilities of the Dynamic Annotation API extend far beyond what is described in this section.</span></span> <span data-ttu-id="c31d9-204">Para obtener más información sobre la anotación dinámica, consulte [API de anotación dinámica](dynamic-annotation-api.md).</span><span class="sxs-lookup"><span data-stu-id="c31d9-204">For more information about Dynamic Annotation, see [Dynamic Annotation API](dynamic-annotation-api.md).</span></span>

### <a name="steps-for-annotating-the-name-property"></a><span data-ttu-id="c31d9-205">Pasos para anotar la propiedad Name</span><span class="sxs-lookup"><span data-stu-id="c31d9-205">Steps for Annotating the Name Property</span></span>

<span data-ttu-id="c31d9-206">El uso de la anotación directa para cambiar la [propiedad Name](name-property.md) de un control implica los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="c31d9-206">Using direct annotation to change the [Name Property](name-property.md) of a control involves the following steps.</span></span>

1.  <span data-ttu-id="c31d9-207">Incluya los archivos de encabezado siguientes:</span><span class="sxs-lookup"><span data-stu-id="c31d9-207">Include the following header files:</span></span>
    -   <span data-ttu-id="c31d9-208">Initguid. h</span><span class="sxs-lookup"><span data-stu-id="c31d9-208">Initguid.h</span></span>
    -   <span data-ttu-id="c31d9-209">Oleacc. h</span><span class="sxs-lookup"><span data-stu-id="c31d9-209">Oleacc.h</span></span>

    > [!Note]  
    > <span data-ttu-id="c31d9-210">Para definir los GUID, debe incluir Initguid. h antes de oleacc. h en el mismo archivo.</span><span class="sxs-lookup"><span data-stu-id="c31d9-210">To define GUIDs, you must include Initguid.h before Oleacc.h in the same file.</span></span>

     

2.  <span data-ttu-id="c31d9-211">Inicialice la biblioteca de modelo de objetos componentes (COM) mediante una llamada a la función [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) , normalmente durante el proceso de inicialización de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c31d9-211">Initialize the Component Object Model (COM) library by calling the [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) function, typically during the application initialization process.</span></span>
3.  <span data-ttu-id="c31d9-212">Poco después de crear el control de destino (normalmente durante el mensaje de [ \_ INITDIALOG de WM](../dlgbox/wm-initdialog.md) ), cree una instancia del administrador de anotaciones y obtenga un puntero a su puntero [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .</span><span class="sxs-lookup"><span data-stu-id="c31d9-212">Soon after the target control is created (typically during the [WM\_INITDIALOG](../dlgbox/wm-initdialog.md) message), create an instance of the annotation manager and obtain a pointer to its [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) pointer.</span></span>
4.  <span data-ttu-id="c31d9-213">Anote la [propiedad Name](name-property.md) del control de destino mediante el método [**IAccPropServices:: SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) .</span><span class="sxs-lookup"><span data-stu-id="c31d9-213">Annotate the [Name Property](name-property.md) of the target control by using the [**IAccPropServices::SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) method.</span></span>

5.  <span data-ttu-id="c31d9-214">Libere el puntero [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .</span><span class="sxs-lookup"><span data-stu-id="c31d9-214">Release the [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) pointer.</span></span>
6.  <span data-ttu-id="c31d9-215">Antes de que se destruya el control de destino (normalmente al controlar el mensaje de [ \_ destrucción de WM](../winmsg/wm-destroy.md) ), cree una instancia del administrador de anotaciones y obtenga un puntero a su interfaz [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .</span><span class="sxs-lookup"><span data-stu-id="c31d9-215">Before the target control is destroyed (typically when handling the [WM\_DESTROY](../winmsg/wm-destroy.md) message), create an instance of the annotation manager and obtain a pointer to its [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) interface.</span></span>
7.  <span data-ttu-id="c31d9-216">Use el método [**IAccPropServices:: ClearHwndProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) para borrar las anotaciones de [propiedades de nombre](name-property.md) del control de destino.</span><span class="sxs-lookup"><span data-stu-id="c31d9-216">Use the [**IAccPropServices::ClearHwndProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) method to clear the [Name property](name-property.md) annotations from the target control.</span></span>
8.  <span data-ttu-id="c31d9-217">Libere el puntero [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .</span><span class="sxs-lookup"><span data-stu-id="c31d9-217">Release the [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) pointer.</span></span>
9.  <span data-ttu-id="c31d9-218">Antes de salir de la aplicación (normalmente al procesar el mensaje de [ \_ destrucción de WM](../winmsg/wm-destroy.md) ), libere la biblioteca com llamando a la función [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) .</span><span class="sxs-lookup"><span data-stu-id="c31d9-218">Before your application exits (typically while processing the [WM\_DESTROY](../winmsg/wm-destroy.md) message), release the COM library by calling the [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) function.</span></span>

<span data-ttu-id="c31d9-219">La función [**IAccPropServices:: SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) toma cinco parámetros.</span><span class="sxs-lookup"><span data-stu-id="c31d9-219">The [**IAccPropServices::SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) function takes five parameters.</span></span> <span data-ttu-id="c31d9-220">Los tres primeros (*hWnd*, *idObject* y *idChild*) se combinan para identificar el control.</span><span class="sxs-lookup"><span data-stu-id="c31d9-220">The first three—*hwnd*, *idObject*, and *idChild*—combine to identify the control.</span></span> <span data-ttu-id="c31d9-221">El cuarto parámetro, *idProp*, especifica el identificador de la propiedad que se va a cambiar.</span><span class="sxs-lookup"><span data-stu-id="c31d9-221">The fourth parameter, *idProp*, specifies the identifier of the property to be changed.</span></span> <span data-ttu-id="c31d9-222">Para cambiar la [propiedad Name](name-property.md), establezca *idProp* en **\_ \_ el nombre** de la ACC.</span><span class="sxs-lookup"><span data-stu-id="c31d9-222">To change the [Name property](name-property.md), set *idProp* to **PROPID\_ACC\_NAME**.</span></span> <span data-ttu-id="c31d9-223">(Para obtener una lista de otras propiedades que se pueden establecer a través de la anotación directa, vea [usar la anotación directa](using-direct-annotation.md)). El último parámetro de **SetHwndPropStr**, *Str*, es la nueva cadena que se va a usar como la propiedad Name.</span><span class="sxs-lookup"><span data-stu-id="c31d9-223">(For a list of other properties that you can set through direct annotation, see [Using Direct Annotation](using-direct-annotation.md).) The last parameter of **SetHwndPropStr**, *str*, is the new string to use as the Name property.</span></span>

### <a name="example-of-annotating-the-name-property"></a><span data-ttu-id="c31d9-224">Ejemplo de anotar la propiedad Name</span><span class="sxs-lookup"><span data-stu-id="c31d9-224">Example of Annotating the Name Property</span></span>

<span data-ttu-id="c31d9-225">En el ejemplo de código siguiente se muestra cómo utilizar la anotación directa para cambiar la [propiedad Name](name-property.md) del objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de un control.</span><span class="sxs-lookup"><span data-stu-id="c31d9-225">The following example code shows how to use direct annotation to change the [Name property](name-property.md) of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object for a control.</span></span> <span data-ttu-id="c31d9-226">Para simplificar las cosas, en el ejemplo se usa una cadena codificada de forma rígida ("nombre del control nuevo") para establecer la propiedad nombre.</span><span class="sxs-lookup"><span data-stu-id="c31d9-226">To keep things simple, the example uses a hard-coded string ("New Control Name") to set the Name property.</span></span> <span data-ttu-id="c31d9-227">Las cadenas codificadas de forma rígida no deben usarse en la versión final de la aplicación porque no se pueden localizar.</span><span class="sxs-lookup"><span data-stu-id="c31d9-227">Hard-coded strings should not be used in the final version of your application because they cannot be localized.</span></span> <span data-ttu-id="c31d9-228">En su lugar, cargue siempre las cadenas del archivo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c31d9-228">Instead, always load strings from your resource file.</span></span> <span data-ttu-id="c31d9-229">Además, en el ejemplo no se muestran las llamadas a las funciones [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) y [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) .</span><span class="sxs-lookup"><span data-stu-id="c31d9-229">Also, the example does not show the calls to the [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) functions.</span></span>


```C++
#include <initguid.h>
#include <oleacc.h>

// AnnotateControlName - Uses direct annotation to change the Name property 
// of the IAccessible object for a control.
//
// hDlg - Handle of the dialog box that contains the control.
// hwndCtl - Handle of the control whose Name property is to be changed.
HRESULT AnnotateControlName(HWND hDlg, HWND hwndCtl)
{
    HRESULT hr;        

    IAccPropServices *pAccPropSvc = NULL;  

    // Create an instance of the annotation manager and retrieve the 
    // IAccPropServices pointer.
    hr = CoCreateInstance(CLSID_AccPropServices, NULL, CLSCTX_SERVER, 
        IID_IAccPropServices, (void **) &pAccPropSvc);

    if (hr != S_OK || pAccPropSvc == NULL)
        return hr;

    // Set the Name property for the control.
    // Note: A hard-coded string is used here to keep the example simple.
    // Always use localizable string resources in your applications. 
    hr = pAccPropSvc->SetHwndPropStr(hwndCtl, OBJID_CLIENT, CHILDID_SELF, 
        PROPID_ACC_NAME, L"New Control Name");

    pAccPropSvc->Release();
    
    return hr;
}

// RemoveAnnotatedNameFromControl - Removes the annotated name from the 
// Name property of the IAccessible object for a control.
//
// hDlg - Handle of the dialog box that contains the control.
// hwndCtl - Handle of the control whose annotated name is to be removed.
HRESULT RemoveAnnotatedNameFromControl(HWND hDlg, HWND hwndCtl)
{
    HRESULT hr;

    IAccPropServices *pAccPropSvc = NULL;

    // Create an instance of the annotation manager and retrieve the 
    // IAccPropServices pointer.
    hr = CoCreateInstance(CLSID_AccPropServices, NULL, CLSCTX_SERVER, 
        IID_IAccPropServices, (void **) &pAccPropSvc);

    if (hr != S_OK || pAccPropSvc == NULL)
        return hr;

    // Remove the annotated name from the Name property for the control.
    MSAAPROPID propid = PROPID_ACC_NAME;
    hr = pAccPropSvc->ClearHwndProps(hwndCtl, OBJID_CLIENT, CHILDID_SELF, 
        &propid, 1);

    // Release the annotation manager.
    pAccPropSvc->Release();

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="c31d9-230">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c31d9-230">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c31d9-231">**Vista**</span><span class="sxs-lookup"><span data-stu-id="c31d9-231">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c31d9-232">API de anotación dinámica</span><span class="sxs-lookup"><span data-stu-id="c31d9-232">Dynamic Annotation API</span></span>](dynamic-annotation-api.md)
</dt> <dt>

[<span data-ttu-id="c31d9-233">Proporcionar la propiedad Name</span><span class="sxs-lookup"><span data-stu-id="c31d9-233">Providing the Name Property</span></span>](providing-the-name-property.md)
</dt> <dt>

[<span data-ttu-id="c31d9-234">Herramientas de pruebas</span><span class="sxs-lookup"><span data-stu-id="c31d9-234">Testing Tools</span></span>](testing-tools.md)
</dt> </dl>

 

 