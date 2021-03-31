---
title: Infraestructura de WinEvents
description: El sistema operativo Microsoft Windows incluye una característica, denominada WinEvents, que permite a los procesos y aplicaciones que se ejecutan en el escritorio de Windows intercambiar determinados tipos de información.
ms.assetid: ba97b00b-4a4c-4889-ae9c-8e92eb742849
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8846582a6d18f304cc08e3cb13ddb444cb278d7
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/29/2020
ms.locfileid: "103785554"
---
# <a name="winevents"></a><span data-ttu-id="6952d-103">WinEvents</span><span class="sxs-lookup"><span data-stu-id="6952d-103">WinEvents</span></span>

<span data-ttu-id="6952d-104">El sistema operativo Microsoft Windows incluye una característica, denominada *WinEvents*, que permite a los procesos y aplicaciones que se ejecutan en el escritorio de Windows intercambiar determinados tipos de información.</span><span class="sxs-lookup"><span data-stu-id="6952d-104">The Microsoft Windows operating system includes a feature, called *WinEvents*, that enables processes and applications running on the Windows desktop to exchange certain types of information.</span></span> <span data-ttu-id="6952d-105">Las herramientas de accesibilidad que usan la automatización de la interfaz de usuario de Microsoft y Microsoft Active Accessibility se encuentran entre los usuarios principales de WinEvents.</span><span class="sxs-lookup"><span data-stu-id="6952d-105">Accessibility tools that use Microsoft UI Automation and Microsoft Active Accessibility are among the primary users of the WinEvents.</span></span>

<span data-ttu-id="6952d-106">En el contexto de accesibilidad, los proveedores de automatización de la interfaz de usuario y los servidores de Microsoft Active Accessibility utilizan WinEvents para notificar a los clientes de los cambios en una interfaz de usuario de la aplicación, como cuando se ha creado o destruido un elemento de la interfaz de usuario, o cuando ha cambiado el nombre, el estado o el valor de un elemento.</span><span class="sxs-lookup"><span data-stu-id="6952d-106">In the context of accessibility, UI Automation providers and Microsoft Active Accessibility servers use WinEvents to notify clients of changes in an application UI, such as when a UI element has been created or destroyed, or when an element name, state, or value has changed.</span></span>

<span data-ttu-id="6952d-107">En esta sección se proporcionan sugerencias, instrucciones y ejemplos para ayudar a los clientes a controlar WinEvents y ayudar a los servidores a determinar cuándo se debe desencadenar el WinEvent adecuado.</span><span class="sxs-lookup"><span data-stu-id="6952d-107">This section provides suggestions, guidelines, and examples to help clients handle WinEvents and to help servers determine when to trigger the appropriate WinEvent.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6952d-108">En esta sección</span><span class="sxs-lookup"><span data-stu-id="6952d-108">In this section</span></span>

-   [<span data-ttu-id="6952d-109">¿Qué son los WinEvents?</span><span class="sxs-lookup"><span data-stu-id="6952d-109">What Are WinEvents?</span></span>](what-are-winevents.md)
-   [<span data-ttu-id="6952d-110">Registro de una función de enlace</span><span class="sxs-lookup"><span data-stu-id="6952d-110">Registering a Hook Function</span></span>](registering-a-hook-function.md)
-   [<span data-ttu-id="6952d-111">Eventos de Object-Level y de nivel de sistema</span><span class="sxs-lookup"><span data-stu-id="6952d-111">System-Level and Object-Level Events</span></span>](system-level-and-object-level-events.md)
-   [<span data-ttu-id="6952d-112">Funciones de enlace en contexto y fuera de contexto</span><span class="sxs-lookup"><span data-stu-id="6952d-112">In-Context and Out-of-Context Hook Functions</span></span>](in-context-and-out-of-context-hook-functions.md)
-   [<span data-ttu-id="6952d-113">Protección contra reentrada en funciones de enlace</span><span class="sxs-lookup"><span data-stu-id="6952d-113">Guarding Against Reentrancy in Hook Functions</span></span>](guarding-against-reentrancy-in-hook-functions.md)
-   [<span data-ttu-id="6952d-114">Asignación de identificadores de WinEvent</span><span class="sxs-lookup"><span data-stu-id="6952d-114">Allocation of WinEvent IDs</span></span>](allocation-of-winevent-ids.md)

<span data-ttu-id="6952d-115">Para obtener información general sobre el proceso de notificación de eventos en Microsoft Active Accessibility, consulte [WinEvents](winevents-overview.md) en [Technical Overview (introducción técnica](technical-overview.md)).</span><span class="sxs-lookup"><span data-stu-id="6952d-115">For an overview of the event notification process in Microsoft Active Accessibility, see [WinEvents](winevents-overview.md) in the [Technical Overview](technical-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6952d-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6952d-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6952d-117">Infraestructura común</span><span class="sxs-lookup"><span data-stu-id="6952d-117">Common Infrastructure</span></span>](common-infrastructure.md)
</dt> </dl>

 

 




