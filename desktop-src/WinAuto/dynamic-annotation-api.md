---
title: API de anotación dinámica
description: Dynamic Annotation API es una extensión de Microsoft Active Accessibility que permite a los desarrolladores personalizar la compatibilidad de IAccessible existente sin tener que usar técnicas de subclase o ajuste propensas a errores.
ms.assetid: 2daf0e76-b300-47e7-994b-d1d00d0dca4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7f73c1da79784fdd86652128b572fd81904023c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994602"
---
# <a name="dynamic-annotation-api"></a><span data-ttu-id="5eb98-103">API de anotación dinámica</span><span class="sxs-lookup"><span data-stu-id="5eb98-103">Dynamic Annotation API</span></span>

<span data-ttu-id="5eb98-104">Dynamic Annotation API es una extensión de Microsoft Active Accessibility que permite a los desarrolladores personalizar la compatibilidad de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) existente sin tener que usar técnicas de subclase o ajuste propensas a errores.</span><span class="sxs-lookup"><span data-stu-id="5eb98-104">The Dynamic Annotation API is an extension to Microsoft Active Accessibility that allows developers to customize existing [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) support without having to use error-prone subclassing or wrapping techniques.</span></span> <span data-ttu-id="5eb98-105">Este mecanismo también permite a los desarrolladores pasar sugerencias u otra información útil a los servidores proxy de Oleacc.dll.</span><span class="sxs-lookup"><span data-stu-id="5eb98-105">This mechanism also allows developers to pass hints or other useful information to the Oleacc.dll proxies.</span></span>

<span data-ttu-id="5eb98-106">La anotación dinámica se usa normalmente para corregir o modificar una instancia inexacta de un objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) expuesto por un proxy de Oleacc.dll existente.</span><span class="sxs-lookup"><span data-stu-id="5eb98-106">Dynamic Annotation is typically used to correct or amend an inaccurate instance of an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object exposed by an existing Oleacc.dll proxy.</span></span> <span data-ttu-id="5eb98-107">Por ejemplo, puede utilizarlo para invalidar las propiedades de [**nombre**](name-property.md) y [**función**](role-property.md) proporcionadas por el proxy predeterminado, y para proporcionar las propiedades de [**Descripción**](description-property.md) y [**ayuda**](help-property.md) (que es posible que el proxy predeterminado no proporcione).</span><span class="sxs-lookup"><span data-stu-id="5eb98-107">For example, you can use it to override the [**Name**](name-property.md) and [**Role**](role-property.md) properties provided by the default proxy, and to supply [**Description**](description-property.md) and [**Help**](help-property.md) properties (which may not be provided by the default proxy).</span></span>

<span data-ttu-id="5eb98-108">Con Windows 7, los desarrolladores pueden usar la API de anotación dinámica para anotar las propiedades de automatización de la interfaz de usuario de Microsoft, así como las propiedades de Microsoft Active Accessibility de los objetos de proxy que crea Oleacc.dll para los controles estándar de Windows.</span><span class="sxs-lookup"><span data-stu-id="5eb98-108">With Windows 7, developers can use the Dynamic Annotation API to annotate Microsoft UI Automation properties as well as Microsoft Active Accessibility properties of the proxy objects that Oleacc.dll creates for standard Windows controls.</span></span> <span data-ttu-id="5eb98-109">Los objetos de proxy de Oleacc.dll atienden a los clientes de Microsoft Active Accessibility y de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="5eb98-109">The Oleacc.dll proxy objects serve both Microsoft Active Accessibility and UI Automation clients.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5eb98-110">En esta sección</span><span class="sxs-lookup"><span data-stu-id="5eb98-110">In this section</span></span>

-   [<span data-ttu-id="5eb98-111">Información general</span><span class="sxs-lookup"><span data-stu-id="5eb98-111">Background Information</span></span>](background-information.md)
-   [<span data-ttu-id="5eb98-112">Alternativas a la anotación dinámica</span><span class="sxs-lookup"><span data-stu-id="5eb98-112">Alternatives to Dynamic Annotation</span></span>](alternatives-to-dynamic-annotation.md)
-   [<span data-ttu-id="5eb98-113">Tipos de anotación dinámica</span><span class="sxs-lookup"><span data-stu-id="5eb98-113">Types of Dynamic Annotation</span></span>](types-of-dynamic-annotation.md)
-   [<span data-ttu-id="5eb98-114">Anotación directa</span><span class="sxs-lookup"><span data-stu-id="5eb98-114">Direct Annotation</span></span>](direct-annotation.md)
-   [<span data-ttu-id="5eb98-115">Anotación de asignación de valores</span><span class="sxs-lookup"><span data-stu-id="5eb98-115">Value Map Annotation</span></span>](value-map-annotation.md)
-   [<span data-ttu-id="5eb98-116">Anotación de servidor</span><span class="sxs-lookup"><span data-stu-id="5eb98-116">Server Annotation</span></span>](server-annotation.md)
-   [<span data-ttu-id="5eb98-117">Problemas y limitaciones</span><span class="sxs-lookup"><span data-stu-id="5eb98-117">Issues and Limitations</span></span>](issues-and-limitations.md)

 

 




