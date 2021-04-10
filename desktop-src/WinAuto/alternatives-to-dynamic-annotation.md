---
title: Alternativas a la anotación dinámica
description: Alternativas a la anotación dinámica
ms.assetid: d8019c65-620b-4aa2-a631-cc32f34e5510
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0027cf9a9913efdff379d2f0c01e7bf22bc94f44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149395"
---
# <a name="alternatives-to-dynamic-annotation"></a><span data-ttu-id="dc1e3-103">Alternativas a la anotación dinámica</span><span class="sxs-lookup"><span data-stu-id="dc1e3-103">Alternatives to Dynamic Annotation</span></span>

<span data-ttu-id="dc1e3-104">Hay otras maneras de proporcionar compatibilidad de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) personalizada para los elementos de la interfaz de usuario y, en algunos casos, son la solución correcta.</span><span class="sxs-lookup"><span data-stu-id="dc1e3-104">There are other ways to provide customized [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) support for UI elements, and in some cases, they are the correct solution.</span></span> <span data-ttu-id="dc1e3-105">Antes de la anotación dinámica, estas técnicas alternativas eran las únicas opciones disponibles para los desarrolladores.</span><span class="sxs-lookup"><span data-stu-id="dc1e3-105">Prior to Dynamic Annotation, these alternative techniques were the only options available to developers.</span></span> <span data-ttu-id="dc1e3-106">Incluyen la implementación de toda la interfaz **IAccessible** y las técnicas de programación.</span><span class="sxs-lookup"><span data-stu-id="dc1e3-106">They include implementing all of the **IAccessible** interface and programmatic techniques.</span></span>

## <a name="implementing-all-of-the-iaccessible-interface"></a><span data-ttu-id="dc1e3-107">Implementar toda la interfaz IAccessible</span><span class="sxs-lookup"><span data-stu-id="dc1e3-107">Implementing All of the IAccessible Interface</span></span>

<span data-ttu-id="dc1e3-108">Una técnica alternativa consiste en implementar toda la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="dc1e3-108">One alternative technique is to implement all of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="dc1e3-109">Este enfoque suele ser necesario para los controles personalizados o los elementos de interfaz de usuario radicalmente diferentes; sin embargo, los costos de desarrollo y pruebas son lo suficientemente significativos como para evitarlo a menos que sea realmente necesario.</span><span class="sxs-lookup"><span data-stu-id="dc1e3-109">This approach is often necessary for custom controls or radically different UI elements; however, the development and test costs are significant enough that it should be avoided unless truly necessary.</span></span> <span data-ttu-id="dc1e3-110">Si el objetivo es modificar una sola propiedad, el costo es difícil de justificar.</span><span class="sxs-lookup"><span data-stu-id="dc1e3-110">If the goal is to modify a single property, the cost is difficult to justify.</span></span>

## <a name="programmatic-techniques"></a><span data-ttu-id="dc1e3-111">Técnicas de programación</span><span class="sxs-lookup"><span data-stu-id="dc1e3-111">Programmatic Techniques</span></span>

<span data-ttu-id="dc1e3-112">Otra opción consiste en usar técnicas de subclase y ajuste para modificar la información que se expone para una propiedad concreta.</span><span class="sxs-lookup"><span data-stu-id="dc1e3-112">Another option is to use subclassing and wrapping techniques to modify the information being exposed for a specific property.</span></span> <span data-ttu-id="dc1e3-113">Esta es la técnica que la anotación dinámica va a reemplazar.</span><span class="sxs-lookup"><span data-stu-id="dc1e3-113">This is the technique that Dynamic Annotation is intended to replace.</span></span> <span data-ttu-id="dc1e3-114">Para reemplazar una propiedad única mediante el uso de subclases y el ajuste, el desarrollador debe realizar los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="dc1e3-114">To override a single property by using subclassing and wrapping, the developer must perform the following steps:</span></span>

1.  <span data-ttu-id="dc1e3-115">Subclase del HWND del objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="dc1e3-115">Subclass the HWND of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object.</span></span>
2.  <span data-ttu-id="dc1e3-116">Interceptar el mensaje de [**WM \_ GETOBJECT**](wm-getobject.md) para el valor de IParam/OBJID correcto.</span><span class="sxs-lookup"><span data-stu-id="dc1e3-116">Intercept the [**WM\_GETOBJECT**](wm-getobject.md) message for the correct IParam/OBJID value.</span></span>
3.  <span data-ttu-id="dc1e3-117">Reenvíe el mensaje de [**WM \_ GETOBJECT**](wm-getobject.md) a la clase base mediante la función [*CallWndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="dc1e3-117">Forward the [**WM\_GETOBJECT**](wm-getobject.md) message to the base class using the [*CallWndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) function.</span></span> <span data-ttu-id="dc1e3-118">Si se devuelve cero, llame a [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject); de lo contrario, llame a [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) en el valor devuelto para obtener el puntero de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nativo del control.</span><span class="sxs-lookup"><span data-stu-id="dc1e3-118">If zero is returned, call [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject); otherwise, call [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) on the returned value to obtain the control's native [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span>
4.  <span data-ttu-id="dc1e3-119">Cree una clase contenedora, que implementa [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) y ajusta el puntero de la interfaz **IAccessible** devuelto en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="dc1e3-119">Create a wrapper class, which implements [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) and wraps the **IAccessible** interface pointer returned from the previous step.</span></span> <span data-ttu-id="dc1e3-120">Esta clase contenedora envía todos los métodos y propiedades al puntero de la interfaz **IAccessible** original, excepto los que se van a reemplazar.</span><span class="sxs-lookup"><span data-stu-id="dc1e3-120">This wrapper class sends all methods and properties to the original **IAccessible** interface pointer, except those that are to be overridden.</span></span> <span data-ttu-id="dc1e3-121">Esto implica la escritura de código de reenvío para todos los métodos y propiedades de la interfaz **IAccessible** , independientemente de cuántos se hayan invalidado realmente.</span><span class="sxs-lookup"><span data-stu-id="dc1e3-121">This involves writing forwarding code for all of the **IAccessible** interface's 21 properties and methods, regardless of how many are actually overridden.</span></span>

<span data-ttu-id="dc1e3-122">Además, los desarrolladores deben comprobar las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="dc1e3-122">Also, developers must verify the following conditions:</span></span>

-   <span data-ttu-id="dc1e3-123">El método o propiedad invalidados solo debe controlar los identificadores secundarios necesarios y reenviar todos los demás al puntero de la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) original.</span><span class="sxs-lookup"><span data-stu-id="dc1e3-123">The overridden method or property must only handle the required child IDs, and forward all others to the original [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span>
-   <span data-ttu-id="dc1e3-124">El ajuste también debe reenviar las interfaces [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) y [**IOleWindow**](/windows/desktop/api/oleidl/nn-oleidl-iolewindow) solo si el objeto original las admite.</span><span class="sxs-lookup"><span data-stu-id="dc1e3-124">Wrapping must also forward [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) and [**IOleWindow**](/windows/desktop/api/oleidl/nn-oleidl-iolewindow) interfaces only if the original object supports them.</span></span>
-   <span data-ttu-id="dc1e3-125">El recuento de referencias se debe administrar correctamente, especialmente si se admiten otras interfaces.</span><span class="sxs-lookup"><span data-stu-id="dc1e3-125">Reference counting must be handled correctly, especially if other interfaces are supported.</span></span>
-   <span data-ttu-id="dc1e3-126">Los valores devueltos de [**IDispatch**](idispatch-interface.md) se deben controlar correctamente, especialmente con el método [**ITypeInfo:: Invoke**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-invoke) , al que se debe llamar con un puntero de interfaz a la interfaz contenedora, no un puntero a la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) original.</span><span class="sxs-lookup"><span data-stu-id="dc1e3-126">[**IDispatch**](idispatch-interface.md) return values must be handled correctly, especially with the [**ITypeInfo::Invoke**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-invoke) method, which must be called with an interface pointer to the wrapper interface, not a pointer to the original [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span>

<span data-ttu-id="dc1e3-127">Estas técnicas requieren una cantidad considerable de trabajo, incluso si solo es necesario invalidar una o dos propiedades.</span><span class="sxs-lookup"><span data-stu-id="dc1e3-127">These techniques require a considerable amount of work, even if only one or two properties need to be overridden.</span></span> <span data-ttu-id="dc1e3-128">La mayoría del código resultante está relacionada con la subclase y el ajuste, y solo una pequeña fracción proporciona realmente la información invalidada.</span><span class="sxs-lookup"><span data-stu-id="dc1e3-128">The majority of the resulting code is concerned with subclassing and wrapping, and only a small fraction is actually providing the overridden information.</span></span>

<span data-ttu-id="dc1e3-129">Sin embargo, hay escenarios en los que se necesitan estas técnicas.</span><span class="sxs-lookup"><span data-stu-id="dc1e3-129">However, there are scenarios in which these techniques are needed.</span></span> <span data-ttu-id="dc1e3-130">Por ejemplo, si está realizando cambios estructurales para crear un elemento de interfaz de usuario de marcador de posición, debe usar estas técnicas en lugar de la anotación dinámica.</span><span class="sxs-lookup"><span data-stu-id="dc1e3-130">For example, if you are making structural changes to create a placeholder UI element, then you should use these techniques rather than Dynamic Annotation.</span></span>

## <a name="fixing-names-derived-from-labels"></a><span data-ttu-id="dc1e3-131">Corregir nombres derivados de etiquetas</span><span class="sxs-lookup"><span data-stu-id="dc1e3-131">Fixing Names Derived from Labels</span></span>

<span data-ttu-id="dc1e3-132">Algunos controles comunes de Microsoft Win32, como el control de cuadro de edición, casi siempre se usan con una etiqueta (una entrada LTEXT en el archivo de recursos) o un cuadro de grupo (GROUPBOX en el archivo de recursos).</span><span class="sxs-lookup"><span data-stu-id="dc1e3-132">Some Microsoft Win32 common controls, such as the edit box control, are nearly always used with a label (an LTEXT entry in the resource file) or a group box (GROUPBOX in the resource file).</span></span> <span data-ttu-id="dc1e3-133">Microsoft Active Accessibility deriva automáticamente la propiedad Name del control de su etiqueta.</span><span class="sxs-lookup"><span data-stu-id="dc1e3-133">Microsoft Active Accessibility automatically derives the name property of the control from its label.</span></span> <span data-ttu-id="dc1e3-134">Para estos controles, se omite el texto de la ventana (que se muestra en Microsoft Visual Studio como la propiedad Name o ID), porque normalmente se genera automáticamente y raramente es muy descriptivo. por ejemplo, "IDC \_ EDIT1".</span><span class="sxs-lookup"><span data-stu-id="dc1e3-134">For such controls, the window text (shown in Microsoft Visual Studio as the Name or ID property) is ignored, because it is usually autogenerated and seldom very descriptive; for example, "IDC\_EDIT1".</span></span>

<span data-ttu-id="dc1e3-135">Si la interfaz de usuario de la aplicación no está diseñada correctamente, es posible que Microsoft Active Accessibility no pueda establecer el nombre correctamente.</span><span class="sxs-lookup"><span data-stu-id="dc1e3-135">If the user interface of the application is not designed correctly, Microsoft Active Accessibility might not be able to set the name correctly.</span></span> <span data-ttu-id="dc1e3-136">Para asociar a un control, la etiqueta o el cuadro de grupo debe colocarse inmediatamente antes del control dinámico en el orden de tabulación.</span><span class="sxs-lookup"><span data-stu-id="dc1e3-136">To be associated with a control, the label or group box must be placed immediately before the dynamic control in the tab order.</span></span>

<span data-ttu-id="dc1e3-137">El orden de tabulación se puede cambiar mediante la herramienta en Visual Studio (en el menú **formato** cuando el editor de recursos está abierto) o editando directamente el archivo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dc1e3-137">Tab order can be changed by using the tool in Visual Studio (on the **Format** menu when the resource editor is open) or by directly editing the resource file.</span></span>

<span data-ttu-id="dc1e3-138">En el ejemplo siguiente se muestra la descripción de un archivo de recursos de un cuadro de diálogo que contiene dos cuadros de edición con etiqueta.</span><span class="sxs-lookup"><span data-stu-id="dc1e3-138">The following example shows a resource file's description of a dialog box that contains two labeled edit boxes.</span></span>


```C++
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
    LTEXT           "First Name:",IDC_STATIC,8,16,43,8
    LTEXT           "Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDITFIRSTNAME,53,15,120,12,ES_AUTOHSCROLL
    EDITTEXT        IDC_EDITLASTNAME,53,34,120,12,ES_AUTOHSCROLL
END
```



<span data-ttu-id="dc1e3-139">En este ejemplo, las etiquetas y los controles no aparecen en el orden de tabulación correcto.</span><span class="sxs-lookup"><span data-stu-id="dc1e3-139">In this example, the labels and controls are not listed in the correct tab order.</span></span> <span data-ttu-id="dc1e3-140">Como resultado, Microsoft Active Accessibility asigna el nombre "Last Name" al cuadro de edición First-Name y ningún nombre al cuadro de edición Last-Name.</span><span class="sxs-lookup"><span data-stu-id="dc1e3-140">As a result, Microsoft Active Accessibility assigns the name "Last Name" to the first-name edit box, and no name at all to the last-name edit box.</span></span>

<span data-ttu-id="dc1e3-141">En el ejemplo siguiente se muestra la lista de recursos correcta.</span><span class="sxs-lookup"><span data-stu-id="dc1e3-141">The following example shows the correct resource listing.</span></span> <span data-ttu-id="dc1e3-142">Tenga en cuenta también que las teclas de método abreviado se han designado en las etiquetas.</span><span class="sxs-lookup"><span data-stu-id="dc1e3-142">Note also that shortcut keys have been designated in the labels.</span></span>


```C++
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    LTEXT           "&First Name:",IDC_STATIC,8,16,43,8
    EDITTEXT        IDC_EDITFIRSTNAME,53,15,120,12,ES_AUTOHSCROLL
    LTEXT           "&Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDITLASTNAME,53,34,120,12,ES_AUTOHSCROLL
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
END
```



<span data-ttu-id="dc1e3-143">Cuando los controles tienen etiquetas adicionales, como los valores máximo y mínimo de una barra de control, estas etiquetas deben colocarse después del control en el orden de tabulación.</span><span class="sxs-lookup"><span data-stu-id="dc1e3-143">When controls have supplementary labels, such as for minimum and maximum values on a trackbar, these labels should be placed after the control in the tab order.</span></span> <span data-ttu-id="dc1e3-144">La etiqueta principal del control debe aparecer inmediatamente antes del propio control.</span><span class="sxs-lookup"><span data-stu-id="dc1e3-144">The main label of the control must appear immediately before the control itself.</span></span>

## <a name="naming-controls-without-labels"></a><span data-ttu-id="dc1e3-145">Asignar nombres a controles sin etiquetas</span><span class="sxs-lookup"><span data-stu-id="dc1e3-145">Naming Controls Without Labels</span></span>

<span data-ttu-id="dc1e3-146">No siempre es posible o deseable tener una etiqueta visible para cada control.</span><span class="sxs-lookup"><span data-stu-id="dc1e3-146">It is not always possible or desirable to have a visible label for every control.</span></span> <span data-ttu-id="dc1e3-147">Sin embargo, puede proporcionar un nombre para el control agregando una etiqueta invisible.</span><span class="sxs-lookup"><span data-stu-id="dc1e3-147">However, you can still provide a name for the control by adding an invisible label.</span></span> <span data-ttu-id="dc1e3-148">Como siempre, la etiqueta invisible debe preceder inmediatamente al control en el orden de tabulación.</span><span class="sxs-lookup"><span data-stu-id="dc1e3-148">As always, the invisible label must immediately precede the control in the tab order.</span></span>

<span data-ttu-id="dc1e3-149">Si usa el editor de recursos en Microsoft Visual Studio .NET, puede establecer la propiedad visible en false.</span><span class="sxs-lookup"><span data-stu-id="dc1e3-149">If you are using the Resource Editor in Microsoft Visual Studio .NET, you can set the Visible property to False.</span></span> <span data-ttu-id="dc1e3-150">Para hacer que la etiqueta sea invisible al editar el archivo de recursos (. RC), agregue no WS \_ visible o a la parte de estilo del control de etiqueta, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="dc1e3-150">To make the label invisible when editing the resource file (.rc), add NOT WS\_VISIBLE or to the style part of the label control, as shown in the following example.</span></span>


```C++
    LTEXT           "&FullName:",IDC_STATIC,111,23,44,8,NOT WS_VISIBLE
```



<span data-ttu-id="dc1e3-151">Tenga en cuenta que cualquier tecla de método abreviado designada funciona aunque la etiqueta sea invisible.</span><span class="sxs-lookup"><span data-stu-id="dc1e3-151">Note that any designated shortcut key works even though the label is invisible.</span></span>

 

 