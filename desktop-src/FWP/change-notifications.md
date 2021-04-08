---
title: Notificaciones de cambios
description: Las notificaciones de cambio del motor de filtrado de base (BFE) siguen el patrón de publicación/suscripción.
ms.assetid: 443f1767-5694-4584-ba0f-229275900774
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c7a3a2069525cc44823ed975fade3b5f100efd8
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "103994967"
---
# <a name="change-notifications"></a><span data-ttu-id="f71ed-103">Notificaciones de cambios</span><span class="sxs-lookup"><span data-stu-id="f71ed-103">Change Notifications</span></span>

<span data-ttu-id="f71ed-104">Las notificaciones de cambio del motor de filtrado de base (BFE) siguen el patrón de publicación/suscripción: para recibir una de las notificaciones de cambios publicadas, una aplicación tiene que suscribirse a ella.</span><span class="sxs-lookup"><span data-stu-id="f71ed-104">The Base Filtering Engine (BFE) change notifications follow the publish/subscribe pattern: in order to receive one of the published change notifications, an application has to subscribe to it.</span></span>

<span data-ttu-id="f71ed-105">Las notificaciones de cambios de BFE publicadas son agregar y quitar para [**llamadas**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_subscription0), [**filtros**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_subscription0), [**proveedores**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_subscription0), [**contextos de proveedor**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_subscription0)y [**subcapas**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_subscription0).</span><span class="sxs-lookup"><span data-stu-id="f71ed-105">The published BFE change notifications are Add and Remove for [**callouts**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_subscription0), [**filters**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_subscription0), [**providers**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_subscription0), [**provider contexts**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_subscription0), and [**sub-layers**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_subscription0).</span></span>

<span data-ttu-id="f71ed-106">Para suscribirse a una de las notificaciones anteriores, una aplicación llama a la función de administración de [**\* SubscribeChanges0 de Fwpm**](fwp-mgmt-functions.md) correspondiente (por ejemplo, [**FwpmCalloutSubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscribechanges0)).</span><span class="sxs-lookup"><span data-stu-id="f71ed-106">To subscribe to one of the above notifications, an application calls the corresponding [**Fwpm\*SubscribeChanges0**](fwp-mgmt-functions.md) management function (for example, [**FwpmCalloutSubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscribechanges0)).</span></span> <span data-ttu-id="f71ed-107">BFE llama a la función de devolución de llamada que se pasa como argumento a **Fwpm \* SubscribeChanges0** cuando se produce el cambio al que se ha suscrito.</span><span class="sxs-lookup"><span data-stu-id="f71ed-107">The callback function passed as an argument to **Fwpm\*SubscribeChanges0** is invoked by BFE when the change to which it subscribed occurs.</span></span>

<span data-ttu-id="f71ed-108">Para cancelar la suscripción a una de las notificaciones anteriores, una aplicación llama a la función de administración de **\* UnsubscribeChanges0 de Fwpm** correspondiente (por ejemplo, [**FwpmCalloutUnsubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutunsubscribechanges0)).</span><span class="sxs-lookup"><span data-stu-id="f71ed-108">To unsubscribe to one of the above notifications, an application calls the corresponding **Fwpm\*UnsubscribeChanges0** management function (for example, [**FwpmCalloutUnsubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutunsubscribechanges0)).</span></span>

<span data-ttu-id="f71ed-109">Para ver las suscripciones actuales de una de las notificaciones anteriores, una aplicación llama a la función de administración de [**\* SubscriptionsGet0 de Fwpm**](fwp-mgmt-functions.md) correspondiente (por ejemplo, [**FwpmCalloutSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscriptionsget0)).</span><span class="sxs-lookup"><span data-stu-id="f71ed-109">To see the current subscriptions for one of the above notifications, an application calls the corresponding [**Fwpm\*SubscriptionsGet0**](fwp-mgmt-functions.md) management function (for example [**FwpmCalloutSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutsubscriptionsget0)).</span></span>

<span data-ttu-id="f71ed-110">Las notificaciones de cambio ofrecidas por BFE son:</span><span class="sxs-lookup"><span data-stu-id="f71ed-110">The change notifications offered by the BFE are:</span></span>

-   <span data-ttu-id="f71ed-111">Asincrónico: la llamada de función que desencadenó una notificación puede volver antes de que la notificación se envíe a todos los suscriptores.</span><span class="sxs-lookup"><span data-stu-id="f71ed-111">Asynchronous — The function call that triggered a notification may return before the notification has been dispatched to all subscribers.</span></span>
-   <span data-ttu-id="f71ed-112">No confiable: no se garantiza que las notificaciones se entreguen correctamente.</span><span class="sxs-lookup"><span data-stu-id="f71ed-112">Unreliable — No guarantee is made that notifications will be successfully delivered.</span></span>

<span data-ttu-id="f71ed-113">Los suscriptores no reciben notificaciones de los cambios realizados con el identificador de sesión que usaron para suscribirse.</span><span class="sxs-lookup"><span data-stu-id="f71ed-113">Subscribers do not receive notifications for changes made with the session handle they used to subscribe.</span></span> <span data-ttu-id="f71ed-114">Por lo general, solo es necesario informar a los suscriptores de los cambios realizados por otros usuarios. ya saben qué cambios se realizaron por sí mismos.</span><span class="sxs-lookup"><span data-stu-id="f71ed-114">Generally, subscribers only need to be informed of the changes made by others; they already know which changes were made by themselves.</span></span>

 

 




