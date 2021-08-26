---
description: Almacena y recupera información sobre las suscripciones de eventos. Esta interfaz amplía la interfaz IEventSubscription2.
ms.assetid: fd1c136e-6e4e-42ca-a951-4aa5fcdfaa49
title: Interfaz IEventSubscription3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3
api_type:
- COM
api_location: ''
ms.openlocfilehash: cbb6c5b19ed6116c59642e8dc5c0aa8eabf4800b066904f2132c7d182f2b7bbd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070635"
---
# <a name="ieventsubscription3-interface"></a>Interfaz IEventSubscription3

Almacena y recupera información sobre las suscripciones de eventos. Esta interfaz amplía la [**interfaz IEventSubscription2.**](ieventsubscription2.md)

## <a name="when-to-implement"></a>Cuándo implementar

No es necesario implementar la interfaz **IEventSubscription3.** Una clase de objeto de evento (CLSID CEventSubscription) proporcionada por el sistema \_ implementa **IEventSubscription3**.

## <a name="when-to-use"></a>Cuándo se usa

El [sistema de eventos COM+](com--events.md) usa esta interfaz para obtener información sobre suscripciones individuales.

## <a name="members"></a>Miembros

La **interfaz IEventSubscription3** hereda de **IEventSubscription2.** **IEventSubscription3** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz IEventSubscription3** tiene estas propiedades.



| Propiedad                                                                                  | Tipo de acceso           | Descripción                                                |
|:------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------|
| [**EventClassApplicationID**](ieventsubscription3-eventclassapplicationid.md)<br/> | Lectura/escritura<br/> | GUID de aplicación del objeto de clase de eventos.<br/> |
| [**EventClassPartitionID**](ieventsubscription3-eventclasspartitionid.md)<br/>     | Lectura/escritura<br/> | GUID de partición del objeto de clase de eventos.<br/>   |
| [**SubscriberApplicationID**](ieventsubscription3-subscriberapplicationid.md)<br/> | Lectura/escritura<br/> | GUID de aplicación del suscriptor.<br/>         |
| [**SubscriberPartitionID**](ieventsubscription3-subscriberpartitionid.md)<br/>     | Lectura/escritura<br/> | GUID de partición del suscriptor.<br/>           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IEventSubscription2**](ieventsubscription2.md)
</dt> </dl>

 

 




