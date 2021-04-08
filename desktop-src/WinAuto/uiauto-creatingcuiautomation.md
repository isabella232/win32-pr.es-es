---
title: Crear el objeto CUIAutomation
description: En esta sección se describe cómo empezar a escribir una aplicación cliente de automatización de la interfaz de usuario de Microsoft mediante la creación de instancias de un objeto que implementa IUIAutomation.
ms.assetid: 9b90da60-0204-48c1-bb16-ff4a843bac67
keywords:
- clientes, crear objeto CUIAutomation
- clients, CUIAutomation, objeto
- Automatización de la interfaz de usuario, objeto CUIAutomation
- Automatización de la interfaz de usuario, crear objeto CUIAutomation
- creación de un objeto CUIAutomation
- Objeto CUIAutomation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8162dac5276bbb22d00413276482cca34334fda5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995313"
---
# <a name="creating-the-cuiautomation-object"></a><span data-ttu-id="90e23-109">Crear el objeto CUIAutomation</span><span class="sxs-lookup"><span data-stu-id="90e23-109">Creating the CUIAutomation Object</span></span>

<span data-ttu-id="90e23-110">En esta sección se describe cómo empezar a escribir una aplicación cliente de automatización de la interfaz de usuario de Microsoft mediante la creación de instancias de un objeto que implementa [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).</span><span class="sxs-lookup"><span data-stu-id="90e23-110">This section describes how to get started writing a Microsoft UI Automation client application by instantiating an object that implements [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).</span></span>

<span data-ttu-id="90e23-111">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="90e23-111">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="90e23-112">El objeto CUIAutomation</span><span class="sxs-lookup"><span data-stu-id="90e23-112">The CUIAutomation Object</span></span>](#the-cuiautomation-object)
-   [<span data-ttu-id="90e23-113">Crear el objeto</span><span class="sxs-lookup"><span data-stu-id="90e23-113">Creating the Object</span></span>](#creating-the-object)
-   [<span data-ttu-id="90e23-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="90e23-114">Related topics</span></span>](#related-topics)

## <a name="the-cuiautomation-object"></a><span data-ttu-id="90e23-115">El objeto CUIAutomation</span><span class="sxs-lookup"><span data-stu-id="90e23-115">The CUIAutomation Object</span></span>

<span data-ttu-id="90e23-116">El primer paso en el uso de la automatización de la interfaz de usuario es crear un objeto de la clase [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="90e23-116">The first step in using UI Automation is to create an object of the [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) class.</span></span> <span data-ttu-id="90e23-117">Este objeto expone la interfaz [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) , que es la puerta de enlace a todos los demás objetos e interfaces que usan las aplicaciones cliente.</span><span class="sxs-lookup"><span data-stu-id="90e23-117">This object exposes the [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) interface, which is the gateway to all the other objects and interfaces that are used by client applications.</span></span> <span data-ttu-id="90e23-118">Entre otras cosas, **IUIAutomation** se usa para las tareas siguientes:</span><span class="sxs-lookup"><span data-stu-id="90e23-118">Among other things, **IUIAutomation** is used for the following tasks:</span></span>

-   <span data-ttu-id="90e23-119">Suscribirse a eventos.</span><span class="sxs-lookup"><span data-stu-id="90e23-119">Subscribing to events.</span></span>
-   <span data-ttu-id="90e23-120">Crear condiciones.</span><span class="sxs-lookup"><span data-stu-id="90e23-120">Creating conditions.</span></span> <span data-ttu-id="90e23-121">Las condiciones son objetos que se utilizan para restringir el ámbito de las búsquedas de los elementos de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="90e23-121">Conditions are objects used to narrow the scope of searches for UI Automation elements.</span></span>
-   <span data-ttu-id="90e23-122">Obtener elementos de UI Automation directamente desde el escritorio (el elemento raíz) o desde las coordenadas de pantalla o los identificadores de ventana.</span><span class="sxs-lookup"><span data-stu-id="90e23-122">Obtaining UI Automation elements directly from the desktop (the root element), or from screen coordinates or window handles.</span></span>
-   <span data-ttu-id="90e23-123">Crear objetos de rastreador de árbol que se pueden usar para navegar por la jerarquía de elementos de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="90e23-123">Creating tree walker objects that can be used to navigate the hierarchy of UI Automation elements.</span></span>
-   <span data-ttu-id="90e23-124">Convertir tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="90e23-124">Converting data types.</span></span>

## <a name="creating-the-object"></a><span data-ttu-id="90e23-125">Crear el objeto</span><span class="sxs-lookup"><span data-stu-id="90e23-125">Creating the Object</span></span>

<span data-ttu-id="90e23-126">Para empezar a usar la automatización de la interfaz de usuario en su aplicación, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="90e23-126">To get started using UI Automation in your application, take the following steps:</span></span>

-   <span data-ttu-id="90e23-127">Incluya UIAutomation. h en los encabezados del proyecto.</span><span class="sxs-lookup"><span data-stu-id="90e23-127">Include UIAutomation.h in your project headers.</span></span> <span data-ttu-id="90e23-128">UIAutomation. h coloca en los otros encabezados que definen la API.</span><span class="sxs-lookup"><span data-stu-id="90e23-128">UIAutomation.h brings in the other headers that define the API.</span></span>
-   <span data-ttu-id="90e23-129">Declare un puntero a [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).</span><span class="sxs-lookup"><span data-stu-id="90e23-129">Declare a pointer to [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).</span></span>
-   <span data-ttu-id="90e23-130">Inicialice el modelo de objetos componentes (COM).</span><span class="sxs-lookup"><span data-stu-id="90e23-130">Initialize the Component Object Model (COM).</span></span>
-   <span data-ttu-id="90e23-131">Cree una instancia de [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) y recupere la interfaz [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) en el puntero.</span><span class="sxs-lookup"><span data-stu-id="90e23-131">Create an instance of [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) and retrieve the [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) interface in your pointer.</span></span>

<span data-ttu-id="90e23-132">La función de ejemplo siguiente inicializa COM y, a continuación, crea el objeto [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) y recupera la interfaz [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) en el puntero *ppAutomation* .</span><span class="sxs-lookup"><span data-stu-id="90e23-132">The following example function initializes COM, and then creates the [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) object, retrieving the [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) interface in the *ppAutomation* pointer.</span></span>


```C++
#include <uiautomation.h>

// CoInitialize must be called before calling this function, and the  
// caller must release the returned pointer when finished with it.
// 
HRESULT InitializeUIAutomation(IUIAutomation **ppAutomation)
{
    return CoCreateInstance(CLSID_CUIAutomation, NULL,
        CLSCTX_INPROC_SERVER, IID_IUIAutomation, 
        reinterpret_cast<void**>(ppAutomation));
}
```



## <a name="related-topics"></a><span data-ttu-id="90e23-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="90e23-133">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="90e23-134">**Vista**</span><span class="sxs-lookup"><span data-stu-id="90e23-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="90e23-135">Información general sobre eventos de UI Automation</span><span class="sxs-lookup"><span data-stu-id="90e23-135">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> <dt>

[<span data-ttu-id="90e23-136">Obtener elementos de UI Automation</span><span class="sxs-lookup"><span data-stu-id="90e23-136">Obtaining UI Automation Elements</span></span>](uiauto-obtainingelements.md)
</dt> </dl>

 

 