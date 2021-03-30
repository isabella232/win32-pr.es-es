---
title: Introducción técnica
description: Microsoft Active Accessibility mejora la forma en que las ayudas de accesibilidad (programas especializados que ayudan a las personas con discapacidades a usar los equipos de forma más eficaz) a trabajar con aplicaciones que se ejecutan en Microsoft Windows.
ms.assetid: d71ef40e-4c58-4ee6-8909-04ff4f8d20d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f3931c6a69e9b8caed849942424039178a7884
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778481"
---
# <a name="technical-overview"></a><span data-ttu-id="cff0b-103">Introducción técnica</span><span class="sxs-lookup"><span data-stu-id="cff0b-103">Technical Overview</span></span>

<span data-ttu-id="cff0b-104">Microsoft Active Accessibility mejora la forma en que las ayudas de accesibilidad (programas especializados que ayudan a las personas con discapacidades a usar los equipos de forma más eficaz) a trabajar con aplicaciones que se ejecutan en Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="cff0b-104">Microsoft Active Accessibility improves the way accessibility aids (specialized programs that help people with disabilities use computers more effectively) work with applications running on Microsoft Windows.</span></span>

<span data-ttu-id="cff0b-105">Microsoft Active Accessibility se basa en el modelo de objetos componentes (COM), desarrollado por Microsoft y es un estándar del sector que define una forma común para que las aplicaciones y los sistemas operativos se comuniquen.</span><span class="sxs-lookup"><span data-stu-id="cff0b-105">Microsoft Active Accessibility is based on the Component Object Model (COM), which was developed by Microsoft and is an industry standard that defines a common way for applications and operating systems to communicate.</span></span> <span data-ttu-id="cff0b-106">Microsoft Active Accessibility consta de los siguientes componentes:</span><span class="sxs-lookup"><span data-stu-id="cff0b-106">Microsoft Active Accessibility consists of the following components:</span></span>

-   <span data-ttu-id="cff0b-107">La interfaz COM [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), que expone información sobre los elementos de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="cff0b-107">The COM interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), which exposes information about UI elements.</span></span> <span data-ttu-id="cff0b-108">**IAccessible** también tiene propiedades y métodos para obtener información sobre el elemento de interfaz de usuario y manipularlo.</span><span class="sxs-lookup"><span data-stu-id="cff0b-108">**IAccessible** also has properties and methods for obtaining information about and manipulating that UI element.</span></span>
-   <span data-ttu-id="cff0b-109">WinEvents, un sistema de eventos que permite a los servidores notificar a los clientes el momento en que cambia un objeto accesible.</span><span class="sxs-lookup"><span data-stu-id="cff0b-109">WinEvents, an event system that allows servers to notify clients when an accessible object changes.</span></span>
-   <span data-ttu-id="cff0b-110">Oleacc.dll, un archivo DLL de soporte o de tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="cff0b-110">Oleacc.dll, a support or run-time DLL.</span></span>

<span data-ttu-id="cff0b-111">El archivo DLL de Microsoft Active Accessibility, Oleacc.dll, consta de los siguientes componentes:</span><span class="sxs-lookup"><span data-stu-id="cff0b-111">The Microsoft Active Accessibility DLL, Oleacc.dll, consists of the following components:</span></span>

-   <span data-ttu-id="cff0b-112">Funciones que permiten a los clientes solicitar un puntero de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) (por ejemplo, [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)).</span><span class="sxs-lookup"><span data-stu-id="cff0b-112">Functions that allow clients to request an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer (for example, [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)).</span></span>
-   <span data-ttu-id="cff0b-113">Funciones que permiten a los servidores devolver un puntero de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) a un cliente (por ejemplo, [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)).</span><span class="sxs-lookup"><span data-stu-id="cff0b-113">Functions that allow servers to return an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer to a client (for example, [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)).</span></span>
-   <span data-ttu-id="cff0b-114">Funciones para obtener texto localizado para los códigos de rol y estado (por ejemplo, [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) y [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta)).</span><span class="sxs-lookup"><span data-stu-id="cff0b-114">Functions for getting localized text for the role and state codes (for example, [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) and [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta)).</span></span>
-   <span data-ttu-id="cff0b-115">Algunas funciones auxiliares ([**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)).</span><span class="sxs-lookup"><span data-stu-id="cff0b-115">Some helper functions ([**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)).</span></span>
-   <span data-ttu-id="cff0b-116">Código que proporciona la implementación predeterminada de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para los controles de usuario y COMCTL estándar.</span><span class="sxs-lookup"><span data-stu-id="cff0b-116">Code that provides the default implementation of [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) for standard USER and COMCTL controls.</span></span> <span data-ttu-id="cff0b-117">Dado que estos implementan **IAccessible** en nombre de los controles del sistema, se conocen como *servidores proxy*.</span><span class="sxs-lookup"><span data-stu-id="cff0b-117">Because these implement **IAccessible** on behalf of the system controls, they are known as *proxies*.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cff0b-118">En esta sección</span><span class="sxs-lookup"><span data-stu-id="cff0b-118">In this section</span></span>

-   [<span data-ttu-id="cff0b-119">Cómo funciona Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="cff0b-119">How Active Accessibility Works</span></span>](how-active-accessibility-works.md)
-   [<span data-ttu-id="cff0b-120">Aspectos básicos de Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="cff0b-120">Active Accessibility Basics</span></span>](active-accessibility-basics.md)
-   [<span data-ttu-id="cff0b-121">Instrucciones de servidor</span><span class="sxs-lookup"><span data-stu-id="cff0b-121">Server Guidelines</span></span>](server-guidelines.md)
-   [<span data-ttu-id="cff0b-122">Directrices de cliente</span><span class="sxs-lookup"><span data-stu-id="cff0b-122">Client Guidelines</span></span>](client-guidelines.md)
-   [<span data-ttu-id="cff0b-123">Instrucciones COM y Unicode</span><span class="sxs-lookup"><span data-stu-id="cff0b-123">COM and Unicode Guidelines</span></span>](com-and-unicode-guidelines.md)

 

 




