---
description: Usado por Microsoft Internet Explorer System Event Notification Service (SENS) para acceder al almacén de datos de eventos. Esta interfaz extiende la interfaz IEventSystem.
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
ms.openlocfilehash: 6ecee3137750da9f86b61696799a3a7c6e7177beb2b92fb386712a6c90f69d07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070605"
---
# <a name="ieventsystem2-interface"></a>Interfaz IEventSystem2

Usado por Microsoft Internet Explorer System Event Notification Service (SENS) para acceder al almacén de datos de eventos. Esta interfaz extiende la [**interfaz IEventSystem.**](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem)

## <a name="when-to-implement"></a>Cuándo implementar

No es necesario implementar la interfaz **IEventSystem2.** Un objeto de sistema de eventos proporcionado por el sistema (CLSID \_ CEventSystem) implementa **IEventSystem2**.

## <a name="when-to-use"></a>Cuándo se usa

Si usa SENS, puede llamar a los métodos de **IEventSystem2** para agregar y quitar objetos a y desde el almacén de eventos y para obtener objetos del almacén de eventos.

Dado [**que IEventPublisher**](/windows/desktop/api/eventsys/nn-eventsys-ieventpublisher) y el objeto publisher ya no se admiten, no se llama a [**IEventObjectChange**](/windows/desktop/api/Eventsys/nn-eventsys-ieventobjectchange) en el [**método ChangedPublisher.**](/windows/desktop/api/Eventsys/nf-eventsys-ieventobjectchange-changedpublisher)

## <a name="members"></a>Miembros

La **interfaz IEventSystem2** hereda de **IEventSystem**. **IEventSystem2** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IEventSystem2** tiene estos métodos.



| Método                                                                         | Descripción                                                                       |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [**GetVersion**](ieventsystem2-getversion.md)                                 | Recupera el número de versión del sistema de eventos.<br/>                      |
| [**VerifyTransientSubscribers**](ieventsystem2-verifytransientsubscribers.md) | Comprueba la existencia de todos los suscriptores transitorios en el almacén de datos.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/> |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IEventSystem**](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem)
</dt> </dl>

 

