---
title: Funciones del recopilador de eventos de Windows
description: En la siguiente lista se describen brevemente las funciones que se usan en el recopilador de eventos de Windows.
ms.assetid: 48155df6-ba9c-4abe-ba84-6190cee95878
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c20e3bbee6226d385681c7471bb7fd3f337dfa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356678"
---
# <a name="windows-event-collector-functions"></a><span data-ttu-id="54be4-103">Funciones del recopilador de eventos de Windows</span><span class="sxs-lookup"><span data-stu-id="54be4-103">Windows Event Collector Functions</span></span>

<span data-ttu-id="54be4-104">En la siguiente lista se describen brevemente las funciones que se usan en el recopilador de eventos de Windows.</span><span class="sxs-lookup"><span data-stu-id="54be4-104">The following list briefly describes the functions that are used in Windows Event Collector.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="54be4-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="54be4-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="54be4-106">**EcClose**</span><span class="sxs-lookup"><span data-stu-id="54be4-106">**EcClose**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecclose)
</dt> <dd>

<span data-ttu-id="54be4-107">Cierra un identificador recibido de otras funciones del recopilador de eventos.</span><span class="sxs-lookup"><span data-stu-id="54be4-107">Closes a handle received from other Event Collector functions.</span></span>

</dd> <dt>

[<span data-ttu-id="54be4-108">**EcDeleteSubscription**</span><span class="sxs-lookup"><span data-stu-id="54be4-108">**EcDeleteSubscription**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecdeletesubscription)
</dt> <dd>

<span data-ttu-id="54be4-109">Elimina una suscripción existente</span><span class="sxs-lookup"><span data-stu-id="54be4-109">Deletes an existing subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="54be4-110">**EcEnumNextSubscription**</span><span class="sxs-lookup"><span data-stu-id="54be4-110">**EcEnumNextSubscription**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecenumnextsubscription)
</dt> <dd>

<span data-ttu-id="54be4-111">Continúa la enumeración de las suscripciones registradas en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="54be4-111">Continues the enumeration of the subscriptions registered on the local machine.</span></span>

</dd> <dt>

[<span data-ttu-id="54be4-112">**EcGetObjectArrayProperty**</span><span class="sxs-lookup"><span data-stu-id="54be4-112">**EcGetObjectArrayProperty**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecgetobjectarrayproperty)
</dt> <dd>

<span data-ttu-id="54be4-113">Recupera los valores de propiedad de los orígenes de eventos de una suscripción.</span><span class="sxs-lookup"><span data-stu-id="54be4-113">Retrieves property values for the event sources of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="54be4-114">**EcGetObjectArraySize**</span><span class="sxs-lookup"><span data-stu-id="54be4-114">**EcGetObjectArraySize**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecgetobjectarraysize)
</dt> <dd>

<span data-ttu-id="54be4-115">Recupera el número de índices de la matriz de valores de propiedad para los orígenes de eventos de una suscripción.</span><span class="sxs-lookup"><span data-stu-id="54be4-115">Retrieves the number of indexes of the array of property values for the event sources of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="54be4-116">**EcGetSubscriptionProperty**</span><span class="sxs-lookup"><span data-stu-id="54be4-116">**EcGetSubscriptionProperty**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty)
</dt> <dd>

<span data-ttu-id="54be4-117">Recupera un valor de propiedad de un objeto de suscripción.</span><span class="sxs-lookup"><span data-stu-id="54be4-117">Retrieves a property value from a subscription object.</span></span>

</dd> <dt>

[<span data-ttu-id="54be4-118">**EcGetSubscriptionRunTimeStatus**</span><span class="sxs-lookup"><span data-stu-id="54be4-118">**EcGetSubscriptionRunTimeStatus**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionruntimestatus)
</dt> <dd>

<span data-ttu-id="54be4-119">Recupera la información de estado de tiempo de ejecución para un origen de eventos de una suscripción o la propia suscripción.</span><span class="sxs-lookup"><span data-stu-id="54be4-119">Retrieves the run time status information for an event source of a subscription or the subscription itself.</span></span>

</dd> <dt>

[<span data-ttu-id="54be4-120">**EcInsertObjectArrayElement**</span><span class="sxs-lookup"><span data-stu-id="54be4-120">**EcInsertObjectArrayElement**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecinsertobjectarrayelement)
</dt> <dd>

<span data-ttu-id="54be4-121">Inserta un objeto vacío en una matriz de valores de propiedad para los orígenes de eventos de una suscripción.</span><span class="sxs-lookup"><span data-stu-id="54be4-121">Inserts an empty object into an array of property values for the event sources of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="54be4-122">**EcOpenSubscriptionEnum**</span><span class="sxs-lookup"><span data-stu-id="54be4-122">**EcOpenSubscriptionEnum**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscriptionenum)
</dt> <dd>

<span data-ttu-id="54be4-123">Crea un enumerador de suscripciones para enumerar todas las suscripciones registradas en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="54be4-123">Creates a subscription enumerator to enumerate all registered subscriptions on the local machine.</span></span>

</dd> <dt>

[<span data-ttu-id="54be4-124">**EcOpenSubscription**</span><span class="sxs-lookup"><span data-stu-id="54be4-124">**EcOpenSubscription**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription)
</dt> <dd>

<span data-ttu-id="54be4-125">Abre una suscripción existente o crea una nueva suscripción.</span><span class="sxs-lookup"><span data-stu-id="54be4-125">Opens an existing subscription or creates a new subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="54be4-126">**EcSaveSubscription**</span><span class="sxs-lookup"><span data-stu-id="54be4-126">**EcSaveSubscription**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription)
</dt> <dd>

<span data-ttu-id="54be4-127">Guarda la información de configuración de la suscripción.</span><span class="sxs-lookup"><span data-stu-id="54be4-127">Saves subscription configuration information.</span></span>

</dd> <dt>

[<span data-ttu-id="54be4-128">**EcSetObjectArrayProperty**</span><span class="sxs-lookup"><span data-stu-id="54be4-128">**EcSetObjectArrayProperty**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecsetobjectarrayproperty)
</dt> <dd>

<span data-ttu-id="54be4-129">Establece un valor de propiedad en una matriz de valores de propiedad para los orígenes de eventos de una suscripción.</span><span class="sxs-lookup"><span data-stu-id="54be4-129">Sets a property value in an array of property values for the event sources of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="54be4-130">**EcSetSubscriptionProperty**</span><span class="sxs-lookup"><span data-stu-id="54be4-130">**EcSetSubscriptionProperty**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecsetsubscriptionproperty)
</dt> <dd>

<span data-ttu-id="54be4-131">Establece nuevos valores o actualiza los valores existentes de una suscripción.</span><span class="sxs-lookup"><span data-stu-id="54be4-131">Sets new values or updates existing values of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="54be4-132">**EcRemoveObjectArrayElement**</span><span class="sxs-lookup"><span data-stu-id="54be4-132">**EcRemoveObjectArrayElement**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecremoveobjectarrayelement)
</dt> <dd>

<span data-ttu-id="54be4-133">Quita un elemento de una matriz de objetos que contienen valores de propiedad para los orígenes de eventos de una suscripción.</span><span class="sxs-lookup"><span data-stu-id="54be4-133">Removes an element from an array of objects that contain property values for the event sources of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="54be4-134">**EcRetrySubscription**</span><span class="sxs-lookup"><span data-stu-id="54be4-134">**EcRetrySubscription**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecretrysubscription)
</dt> <dd>

<span data-ttu-id="54be4-135">Reintenta la conexión con el origen de eventos de una suscripción que no está conectada.</span><span class="sxs-lookup"><span data-stu-id="54be4-135">Retries connecting to the event source of a subscription that is not connected.</span></span>

</dd> </dl>

 

 




