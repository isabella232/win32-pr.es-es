---
title: Prácticas recomendadas para usar matrices seguras
description: Muchos métodos de interfaz de la automatización de la interfaz de usuario de Microsoft \ 32; La API toma argumentos denominados matrices seguras, del tipo de datos SAFEARRAY. En este tema se describen los procedimientos recomendados para usar matrices seguras en las aplicaciones de automatización de la interfaz de usuario.
ms.assetid: 07e87cfd-d565-41b5-a68d-b99dd191fa95
keywords:
- Automatización de la interfaz de usuario, matrices seguras
- Automatización de la interfaz de usuario, proveedores
- Automatización de la interfaz de usuario, clientes
- Automatización de la interfaz de usuario, convertir entre tipos de datos
- clientes, matrices seguras
- proveedores, automatización de la interfaz de usuario
- matrices seguras
- tipos de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12ade30398f8fbeb43336707f66a0709dfab83d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105704993"
---
# <a name="best-practices-for-using-safe-arrays"></a><span data-ttu-id="ff87c-112">Prácticas recomendadas para usar matrices seguras</span><span class="sxs-lookup"><span data-stu-id="ff87c-112">Best Practices for Using Safe Arrays</span></span>

<span data-ttu-id="ff87c-113">Muchos métodos de interfaz de la API de automatización de la interfaz de usuario de Microsoft toman argumentos denominados matrices seguras, del tipo de datos [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) .</span><span class="sxs-lookup"><span data-stu-id="ff87c-113">Many interface methods of the Microsoft UI Automation API take arguments called safe arrays, of the [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) data type.</span></span> <span data-ttu-id="ff87c-114">En este tema se describen los procedimientos recomendados para usar matrices seguras en las aplicaciones de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="ff87c-114">This topic describes the best practices for using safe arrays in a UI Automation applications.</span></span>

## <a name="clients"></a><span data-ttu-id="ff87c-115">Clientes</span><span class="sxs-lookup"><span data-stu-id="ff87c-115">Clients</span></span>

<span data-ttu-id="ff87c-116">Todas las matrices seguras que se usan con los métodos de la API de cliente de automatización de la interfaz de usuario son matrices unidimensionales de base cero.</span><span class="sxs-lookup"><span data-stu-id="ff87c-116">All safe arrays that are used with the UI Automation client API methods are zero-based, one-dimensional arrays.</span></span> <span data-ttu-id="ff87c-117">Para crear una matriz segura para un método de cliente de automatización de la interfaz de usuario, use la función [**SafeArrayCreateVector**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraycreatevector) y para leer y escribir en una matriz segura, use las funciones [**SafeArrayGetElement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraygetelement) y [**SafeArrayPutElement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayputelement) .</span><span class="sxs-lookup"><span data-stu-id="ff87c-117">To create a safe array for a UI Automation client method, use the [**SafeArrayCreateVector**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraycreatevector) function, and to read from and write to a safe array, use the [**SafeArrayGetElement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraygetelement) and [**SafeArrayPutElement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayputelement) functions.</span></span> <span data-ttu-id="ff87c-118">Cuando termine de usar una matriz segura, destruya siempre mediante la función [**SafeArrayDestroy**](/windows/desktop/api/oleauto/nf-oleauto-safearraydestroy) , tanto si creó la matriz segura como si la recibió desde un método de cliente de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="ff87c-118">When you finish using a safe array, always destroy it by using the [**SafeArrayDestroy**](/windows/desktop/api/oleauto/nf-oleauto-safearraydestroy) function, whether you created the safe array or received it from a UI Automation client method.</span></span>

<span data-ttu-id="ff87c-119">Varios métodos de automatización de la interfaz de usuario, incluidos los métodos de recuperación de propiedades como [**GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue), recuperan [**variantes**](/windows/win32/api/oaidl/ns-oaidl-variant)s que pueden contener estructuras [**Point**](/previous-versions//dd162805(v=vs.85)) o [**UiaRect**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect) .</span><span class="sxs-lookup"><span data-stu-id="ff87c-119">Several UI Automation methods, including property-retrieval methods such as [**GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue), retrieve [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant)s that can contain [**POINT**](/previous-versions//dd162805(v=vs.85)) or [**UiaRect**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect) structures.</span></span> <span data-ttu-id="ff87c-120">Un **punto** se empaqueta en una **variante** como una matriz segura de dobles (VT \_ R8) con el miembro **x** en el índice 0 y el miembro **y** en el índice 1.</span><span class="sxs-lookup"><span data-stu-id="ff87c-120">A **POINT** is packed into a **VARIANT** as a safe array of doubles (VT\_R8) with the **x** member at index 0, and the **y** member at index 1.</span></span> <span data-ttu-id="ff87c-121">De forma similar, un **UiaRect** se empaqueta en una **variante** como una matriz segura de valores double con los miembros **izquierdo**, **superior**, **ancho** y **alto** en los índices 0 a 3, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="ff87c-121">Similarly, a **UiaRect** is packed into a **VARIANT** as a safe array of doubles with the **left**, **top**, **width**, and **height** members at indexes 0 through 3, respectively.</span></span> <span data-ttu-id="ff87c-122">En el caso de una matriz de estructuras **UiaRect** , la matriz segura contiene una matriz secuencial de cuatro valores Double para cada **UiaRect**.</span><span class="sxs-lookup"><span data-stu-id="ff87c-122">For an array of **UiaRect** structures, the safe array contains a sequential array of four doubles for each **UiaRect**.</span></span> <span data-ttu-id="ff87c-123">Los miembros **izquierdo**, **superior**, **ancho** y **alto** del primer **UiaRect** ocupan el índice 0 a 3, los miembros del segundo rectángulo ocupan el índice 4 a 7, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="ff87c-123">The **left**, **top**, **width**, and **height** members of the first **UiaRect** occupy index 0 through 3, the members of the second rectangle occupy index 4 through 7, and so on.</span></span>

<span data-ttu-id="ff87c-124">La interfaz [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) incluye los siguientes métodos para la conversión entre [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) y otros tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="ff87c-124">The [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) interface includes the following methods for converting between [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) and various other data types.</span></span>



| <span data-ttu-id="ff87c-125">Método</span><span class="sxs-lookup"><span data-stu-id="ff87c-125">Method</span></span>                                                                                               | <span data-ttu-id="ff87c-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff87c-126">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ff87c-127">**IUIAutomation::IntNativeArrayToSafeArray**</span><span class="sxs-lookup"><span data-stu-id="ff87c-127">**IUIAutomation::IntNativeArrayToSafeArray**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-intnativearraytosafearray)   | <span data-ttu-id="ff87c-128">Convierte una matriz de enteros en [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray).</span><span class="sxs-lookup"><span data-stu-id="ff87c-128">Converts an array of integers to a [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray).</span></span>                                          |
| [<span data-ttu-id="ff87c-129">**IUIAutomation::IntSafeArrayToNativeArray**</span><span class="sxs-lookup"><span data-stu-id="ff87c-129">**IUIAutomation::IntSafeArrayToNativeArray**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-intsafearraytonativearray)   | <span data-ttu-id="ff87c-130">Convierte un valor [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) de enteros en una matriz.</span><span class="sxs-lookup"><span data-stu-id="ff87c-130">Converts a [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) of integers to an array.</span></span>                                          |
| [<span data-ttu-id="ff87c-131">**IUIAutomation::SafeArrayToRectNativeArray**</span><span class="sxs-lookup"><span data-stu-id="ff87c-131">**IUIAutomation::SafeArrayToRectNativeArray**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-safearraytorectnativearray) | <span data-ttu-id="ff87c-132">Convierte un [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) que contiene coordenadas de rectángulo en una matriz de tipo **Rect**.</span><span class="sxs-lookup"><span data-stu-id="ff87c-132">Converts a [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) that contains rectangle coordinates to an array of type **RECT**.</span></span> |



 

## <a name="providers"></a><span data-ttu-id="ff87c-133">Proveedores</span><span class="sxs-lookup"><span data-stu-id="ff87c-133">Providers</span></span>

<span data-ttu-id="ff87c-134">Un proveedor debe implementar una serie de métodos de interfaz que la automatización de la interfaz de usuario llama para recuperar información del proveedor.</span><span class="sxs-lookup"><span data-stu-id="ff87c-134">A provider must implement a number of interface methods that UI Automation calls to retrieve information from the provider.</span></span> <span data-ttu-id="ff87c-135">Muchas veces, esta información se compone de una matriz de valores.</span><span class="sxs-lookup"><span data-stu-id="ff87c-135">Many times, this information consists of an array of values.</span></span> <span data-ttu-id="ff87c-136">Para devolver una matriz a la automatización de la interfaz de usuario, el proveedor debe empaquetar la matriz en una estructura [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) .</span><span class="sxs-lookup"><span data-stu-id="ff87c-136">To return an array to UI Automation, the provider must pack the array into a [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) structure.</span></span> <span data-ttu-id="ff87c-137">Los elementos de la matriz deben tener el tipo de datos esperado y deben aparecer en el orden esperado.</span><span class="sxs-lookup"><span data-stu-id="ff87c-137">The array elements must be of the expected data type, and must appear in the expected order.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff87c-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ff87c-138">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ff87c-139">**Vista**</span><span class="sxs-lookup"><span data-stu-id="ff87c-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ff87c-140">Información general acerca de las propiedades de UI Automation</span><span class="sxs-lookup"><span data-stu-id="ff87c-140">UI Automation Properties Overview</span></span>](uiauto-propertiesoverview.md)
</dt> <dt>

[<span data-ttu-id="ff87c-141">Fundamentos de UI Automation</span><span class="sxs-lookup"><span data-stu-id="ff87c-141">UI Automation Fundamentals</span></span>](entry-uiautocore-overview.md)
</dt> </dl>

 

 