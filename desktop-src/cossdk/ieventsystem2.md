---
description: Lo utiliza el servicio de notificación de eventos del sistema (SENS) de Microsoft Internet Explorer para tener acceso al almacén de datos de eventos. Esta interfaz extiende la interfaz IEventSystem.
ms.assetid: ad3c38a6-fa2d-4fcd-8782-1fac7595e829
title: Interfaz IEventSystem2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3a174c9457dc347257677e8111772ad14f0dc9fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496451"
---
# <a name="ieventsystem2-interface"></a>Interfaz IEventSystem2

Lo utiliza el servicio de notificación de eventos del sistema (SENS) de Microsoft Internet Explorer para tener acceso al almacén de datos de eventos. Esta interfaz extiende la interfaz [**IEventSystem**](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem) .

## <a name="when-to-implement"></a>Cuándo implementar

No es necesario implementar la interfaz **IEventSystem2** . Un objeto de sistema de eventos proporcionado por el sistema (CLSID \_ CEventSystem) implementa **IEventSystem2**.

## <a name="when-to-use"></a>Cuándo se usa

Si usa SENS, puede llamar a los métodos de **IEventSystem2** para agregar y quitar objetos en el almacén de eventos y para obtener objetos del almacén de eventos.

Dado que ya no se admiten [**IEventPublisher**](/windows/desktop/api/eventsys/nn-eventsys-ieventpublisher) y el objeto Publisher, no se llama a [**IEventObjectChange**](/windows/desktop/api/Eventsys/nn-eventsys-ieventobjectchange) en el método [**ChangedPublisher**](/windows/desktop/api/Eventsys/nf-eventsys-ieventobjectchange-changedpublisher) .

## <a name="members"></a>Miembros

La interfaz **IEventSystem2** hereda de **IEventSystem**. **IEventSystem2** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IEventSystem2** tiene estos métodos.



| Método                                                                         | Descripción                                                                       |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [**GetVersion**](ieventsystem2-getversion.md)                                 | Recupera el número de versión del sistema de eventos.<br/>                      |
| [**VerifyTransientSubscribers**](ieventsystem2-verifytransientsubscribers.md) | Comprueba la existencia de todos los suscriptores transitorios en el almacén de datos.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IEventSystem**](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem)
</dt> </dl>

 

