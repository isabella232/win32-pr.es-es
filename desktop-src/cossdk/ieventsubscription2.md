---
description: Almacena y recupera información sobre las suscripciones de eventos. Esta interfaz amplía la interfaz IEventSubscription.
ms.assetid: f153afb7-c897-40f8-81ed-50308844cac5
title: Interfaz IEventSubscription2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription2
api_type:
- COM
api_location: ''
ms.openlocfilehash: bc7e3e41efc4b44c00c23f0910b8b696940fc1df
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888964"
---
# <a name="ieventsubscription2-interface"></a>Interfaz IEventSubscription2

Almacena y recupera información sobre las suscripciones de eventos. Esta interfaz amplía la [**interfaz IEventSubscription.**](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription)

## <a name="when-to-implement"></a>Cuándo implementar

No es necesario implementar la interfaz **IEventSubscription2.** Una clase de objeto de evento proporcionada por el sistema (CLSID \_ CEventSubscription) implementa **IEventSubscription2**.

## <a name="when-to-use"></a>Cuándo se usa

El [sistema de eventos COM+](com--events.md) usa esta interfaz para obtener información sobre suscripciones individuales.

## <a name="members"></a>Members

La **interfaz IEventSubscription2** hereda de **IEventSubscription.** **IEventSubscription2** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz IEventSubscription2** tiene estas propiedades.



| Propiedad                                                                      | Tipo de acceso           | Descripción                                                |
|:------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------|
| [**FilterCriteria**](ieventsubscription2-filtercriteria.md)<br/>       | Lectura y escritura<br/> | Criterios de filtro que rigen la suscripción.<br/> |
| [**SubscriberMoniker**](ieventsubscription2-subscribermoniker.md)<br/> | Lectura y escritura<br/> | Moniker del suscriptor.<br/>                       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IEventSubscription**](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription)
</dt> </dl>

 

 




