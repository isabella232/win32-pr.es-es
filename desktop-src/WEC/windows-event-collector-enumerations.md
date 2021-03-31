---
title: Enumeraciones del recopilador de eventos de Windows
description: En la tabla siguiente se enumeran las enumeraciones del SDK del recopilador de eventos de Windows.
ms.assetid: 3775aa7c-ef35-4534-b709-15624fd7a90d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32d2617c6eb0052ec1ac41d5f197d9216c253054
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418792"
---
# <a name="windows-event-collector-enumerations"></a><span data-ttu-id="e1d30-103">Enumeraciones del recopilador de eventos de Windows</span><span class="sxs-lookup"><span data-stu-id="e1d30-103">Windows Event Collector Enumerations</span></span>

<span data-ttu-id="e1d30-104">En la tabla siguiente se enumeran las enumeraciones del SDK del recopilador de eventos de Windows.</span><span class="sxs-lookup"><span data-stu-id="e1d30-104">The following table lists the enumerations of the Windows Event Collector SDK.</span></span>



| <span data-ttu-id="e1d30-105">Enumeración</span><span class="sxs-lookup"><span data-stu-id="e1d30-105">Enumeration</span></span>                                                                                               | <span data-ttu-id="e1d30-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1d30-106">Description</span></span>                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1d30-107">**\_modo de \_ configuración de suscripción de EC \_**</span><span class="sxs-lookup"><span data-stu-id="e1d30-107">**EC\_SUBSCRIPTION\_CONFIGURATION\_MODE**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_configuration_mode)                       | <span data-ttu-id="e1d30-108">Especifica modos de configuración diferentes que cambian la configuración predeterminada de una suscripción.</span><span class="sxs-lookup"><span data-stu-id="e1d30-108">Specifies different configuration modes that change the default settings for a subscription.</span></span>                                            |
| [<span data-ttu-id="e1d30-109">**\_formato de \_ contenido de suscripción de EC \_**</span><span class="sxs-lookup"><span data-stu-id="e1d30-109">**EC\_SUBSCRIPTION\_CONTENT\_FORMAT**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_content_format)                               | <span data-ttu-id="e1d30-110">Especifica cómo se representarán los eventos en el equipo que envía los eventos antes de que los eventos se envíen al equipo del recopilador de eventos.</span><span class="sxs-lookup"><span data-stu-id="e1d30-110">Specifies how events will be rendered on the computer that sends the events before the events are sent to the event collector computer.</span></span> |
| [<span data-ttu-id="e1d30-111">**\_tipo de \_ credenciales de suscripción de EC \_**</span><span class="sxs-lookup"><span data-stu-id="e1d30-111">**EC\_SUBSCRIPTION\_CREDENTIALS\_TYPE**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_credentials_type)                           | <span data-ttu-id="e1d30-112">Especifica el tipo de credenciales que se van a usar al comunicarse con orígenes de eventos.</span><span class="sxs-lookup"><span data-stu-id="e1d30-112">Specifies the type of credentials to use when communicating with event sources.</span></span>                                                         |
| [<span data-ttu-id="e1d30-113">**\_modo de \_ entrega de suscripción de EC \_**</span><span class="sxs-lookup"><span data-stu-id="e1d30-113">**EC\_SUBSCRIPTION\_DELIVERY\_MODE**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_delivery_mode)                                 | <span data-ttu-id="e1d30-114">Especifica cómo se entregan los eventos a través de una suscripción de eventos (mediante un modelo de inserción o de extracción).</span><span class="sxs-lookup"><span data-stu-id="e1d30-114">Specifies how events are delivered through an event subscription (using a push or pull model).</span></span>                                          |
| [<span data-ttu-id="e1d30-115">**identificador de la propiedad de suscripción de EC \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e1d30-115">**EC\_SUBSCRIPTION\_PROPERTY\_ID**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id)                                     | <span data-ttu-id="e1d30-116">Define valores para identificar las propiedades de suscripción de eventos usadas para la configuración de la suscripción.</span><span class="sxs-lookup"><span data-stu-id="e1d30-116">Defines values to identify event subscription properties used for subscription configuration.</span></span>                                           |
| [<span data-ttu-id="e1d30-117">**estado \_ activo de estado de tiempo de ejecución de suscripción de EC \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e1d30-117">**EC\_SUBSCRIPTION\_RUNTIME\_STATUS\_ACTIVE\_STATUS**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_runtime_status_active_status) | <span data-ttu-id="e1d30-118">Especifica el estado de una suscripción o un origen de eventos con respecto a una suscripción.</span><span class="sxs-lookup"><span data-stu-id="e1d30-118">Specifies the status of a subscription or an event source with respect to a subscription.</span></span>                                               |
| [<span data-ttu-id="e1d30-119">**\_identificador de \_ información de estado de tiempo de ejecución de suscripción de \_ \_ EC \_**</span><span class="sxs-lookup"><span data-stu-id="e1d30-119">**EC\_SUBSCRIPTION\_RUNTIME\_STATUS\_INFO\_ID**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_runtime_status_info_id)             | <span data-ttu-id="e1d30-120">Especifica un valor que identifica una propiedad del estado de tiempo de ejecución de un origen de eventos o una suscripción.</span><span class="sxs-lookup"><span data-stu-id="e1d30-120">Specifies a value that identifies a property of the runtime status of an event source or a subscription.</span></span>                                |
| [<span data-ttu-id="e1d30-121">**\_tipo de suscripción de EC \_**</span><span class="sxs-lookup"><span data-stu-id="e1d30-121">**EC\_SUBSCRIPTION\_TYPE**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_type)                                                    | <span data-ttu-id="e1d30-122">Especifica el tipo de suscripción que se va a usar (una suscripción iniciada o iniciada por el origen).</span><span class="sxs-lookup"><span data-stu-id="e1d30-122">Specifies the type of subscription to use (a source initiated or collector initiated subscription).</span></span>                                     |
| [<span data-ttu-id="e1d30-123">**\_tipo de variante EC \_**</span><span class="sxs-lookup"><span data-stu-id="e1d30-123">**EC\_VARIANT\_TYPE**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_variant_type)                                                              | <span data-ttu-id="e1d30-124">Define los valores que especifican los tipos de datos que se utilizan en las funciones del recopilador de eventos de Windows.</span><span class="sxs-lookup"><span data-stu-id="e1d30-124">Defines the values that specify the data types that are used in the Windows Event Collector functions.</span></span>                                  |



 

 

 




