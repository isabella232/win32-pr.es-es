---
description: El proveedor de eventos entrega los eventos WMI a un consumidor temporal o permanente. El sistema de eventos WMI utiliza la comparación de descriptores de seguridad en los eventos y SID de la cuenta de usuario para controlar el acceso a los eventos.
ms.assetid: 86eaeb5c-c27e-4794-88e2-e0ffbb885290
ms.tgt_platform: multiple
title: Proteger eventos WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31280a4be25e358e28477bf6be060637f3f96bad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276133"
---
# <a name="securing-wmi-events"></a><span data-ttu-id="87e5f-104">Proteger eventos WMI</span><span class="sxs-lookup"><span data-stu-id="87e5f-104">Securing WMI Events</span></span>

<span data-ttu-id="87e5f-105">El [*proveedor de eventos*](gloss-e.md) entrega los eventos WMI a un consumidor [*temporal*](gloss-t.md) o [*permanente*](gloss-p.md) .</span><span class="sxs-lookup"><span data-stu-id="87e5f-105">WMI events are delivered by the [*event provider*](gloss-e.md) to a [*temporary*](gloss-t.md) or [*permanent*](gloss-p.md) consumer.</span></span> <span data-ttu-id="87e5f-106">El sistema de eventos WMI utiliza la comparación de [*descriptores de seguridad*](gloss-s.md) en los eventos y [*SID*](gloss-s.md) de la cuenta de usuario para controlar el acceso a los eventos.</span><span class="sxs-lookup"><span data-stu-id="87e5f-106">The WMI event system uses the comparison of [*security descriptors*](gloss-s.md) on events and user account [*SIDs*](gloss-s.md) to control event access.</span></span>

<span data-ttu-id="87e5f-107">Los eventos se entregan en forma de una instancia de una clase de eventos normalmente, pero no necesariamente, derivadas de [**\_ \_ Event**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="87e5f-107">Events are delivered in the form of an instance of an event class usually, but not necessarily, derived ultimately from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="87e5f-108">WMI proporciona varias clases de eventos generales en las [clases del sistema WMI](wmi-system-classes.md), como [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md).</span><span class="sxs-lookup"><span data-stu-id="87e5f-108">WMI supplies several general event classes in the [WMI System Classes](wmi-system-classes.md), such as [**\_\_InstanceModificationEvent**](--instancemodificationevent.md).</span></span> <span data-ttu-id="87e5f-109">Los proveedores también pueden proporcionar sus propias clases de eventos.</span><span class="sxs-lookup"><span data-stu-id="87e5f-109">Providers may also supply their own event classes.</span></span> <span data-ttu-id="87e5f-110">Por ejemplo, el [proveedor del registro del sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) tiene clases de eventos que informan del cambio de una clave o un valor del registro, como [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span><span class="sxs-lookup"><span data-stu-id="87e5f-110">For example, the [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider) has event classes that report the change of a registry key or value, such as [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span></span>

<span data-ttu-id="87e5f-111">En los temas siguientes se proporciona información acerca de la protección de la entrega de eventos para proveedores y la recepción segura de eventos para aplicaciones y scripts de cliente:</span><span class="sxs-lookup"><span data-stu-id="87e5f-111">The following topics supply information about securing delivery of events for providers and receiving events securely for client scripts and applications:</span></span>

-   [<span data-ttu-id="87e5f-112">Proporcionar eventos de forma segura</span><span class="sxs-lookup"><span data-stu-id="87e5f-112">Providing Events Securely</span></span>](providing-events-securely.md)
-   [<span data-ttu-id="87e5f-113">Recepción segura de eventos</span><span class="sxs-lookup"><span data-stu-id="87e5f-113">Receiving Events Securely</span></span>](receiving-events-securely.md)

## <a name="related-topics"></a><span data-ttu-id="87e5f-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="87e5f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87e5f-115">Mantenimiento de la seguridad de WMI</span><span class="sxs-lookup"><span data-stu-id="87e5f-115">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

 
