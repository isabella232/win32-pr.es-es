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
# <a name="windows-event-collector-functions"></a>Funciones del recopilador de eventos de Windows

En la siguiente lista se describen brevemente las funciones que se usan en el recopilador de eventos de Windows.

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

Recupera la información de estado de tiempo de ejecución para un origen de eventos de una suscripción o la propia suscripción.

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

Abre una suscripción existente o crea una nueva suscripción.

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

Reintenta la conexión con el origen de eventos de una suscripción que no está conectada.

</dd> </dl>

 

 




