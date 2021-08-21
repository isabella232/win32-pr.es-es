---
title: Windows Funciones del recopilador de eventos
description: En la lista siguiente se describen brevemente las funciones que se usan en Windows recopilador de eventos.
ms.assetid: 48155df6-ba9c-4abe-ba84-6190cee95878
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17dd89cb98e3803f171633df0f902250f1147a25bce9d43c83947c2d1e83b6ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117937227"
---
# <a name="windows-event-collector-functions"></a>Windows Funciones del recopilador de eventos

En la lista siguiente se describen brevemente las funciones que se usan en Windows recopilador de eventos.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose)
</dt> <dd>

Cierra un identificador recibido de otras funciones del recopilador de eventos.

</dd> <dt>

[**EcDeleteSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecdeletesubscription)
</dt> <dd>

Elimina una suscripción existente

</dd> <dt>

[**EcEnumNextSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecenumnextsubscription)
</dt> <dd>

Continúa la enumeración de las suscripciones registradas en el equipo local.

</dd> <dt>

[**EcGetObjectArrayProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetobjectarrayproperty)
</dt> <dd>

Recupera los valores de propiedad de los orígenes de eventos de una suscripción.

</dd> <dt>

[**EcGetObjectArraySize**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetobjectarraysize)
</dt> <dd>

Recupera el número de índices de la matriz de valores de propiedad para los orígenes de eventos de una suscripción.

</dd> <dt>

[**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty)
</dt> <dd>

Recupera un valor de propiedad de un objeto de suscripción.

</dd> <dt>

[**EcGetSubscriptionRunTimeStatus**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionruntimestatus)
</dt> <dd>

Recupera la información de estado de tiempo de ejecución de un origen de eventos de una suscripción o de la propia suscripción.

</dd> <dt>

[**EcInsertObjectArrayElement**](/windows/desktop/api/Evcoll/nf-evcoll-ecinsertobjectarrayelement)
</dt> <dd>

Inserta un objeto vacío en una matriz de valores de propiedad para los orígenes de eventos de una suscripción.

</dd> <dt>

[**EcOpenSubscriptionEnum**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscriptionenum)
</dt> <dd>

Crea un enumerador de suscripciones para enumerar todas las suscripciones registradas en el equipo local.

</dd> <dt>

[**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription)
</dt> <dd>

Abre una suscripción existente o crea una nueva.

</dd> <dt>

[**EcSaveSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription)
</dt> <dd>

Guarda la información de configuración de la suscripción.

</dd> <dt>

[**EcSetObjectArrayProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecsetobjectarrayproperty)
</dt> <dd>

Establece un valor de propiedad en una matriz de valores de propiedad para los orígenes de eventos de una suscripción.

</dd> <dt>

[**EcSetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecsetsubscriptionproperty)
</dt> <dd>

Establece nuevos valores o actualiza los valores existentes de una suscripción.

</dd> <dt>

[**EcRemoveObjectArrayElement**](/windows/desktop/api/Evcoll/nf-evcoll-ecremoveobjectarrayelement)
</dt> <dd>

Quita un elemento de una matriz de objetos que contienen valores de propiedad para los orígenes de eventos de una suscripción.

</dd> <dt>

[**EcRetrySubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecretrysubscription)
</dt> <dd>

Reintentos de conexión al origen de eventos de una suscripción que no está conectada.

</dd> </dl>

 

 




