---
title: Interfaz IReferenceClock
description: La interfaz IReferenceClock proporciona acceso a un reloj externo. Esta interfaz se proporciona para permitir que todas las rutinas de representación se sincronicen con el mismo reloj. Esta interfaz se puede obtener de un objeto de lector.
ms.assetid: 1424fd74-d56c-4338-801f-319ef975169f
keywords:
- Interfaz IReferenceClock formato de Windows Media
- Interfaz IReferenceClock formato de Windows Media, descrito
topic_type:
- apiref
api_name:
- IReferenceClock
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72d17ef362aa5436fe98443d86dff5ae31212650
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105704965"
---
# <a name="ireferenceclock-interface"></a>Interfaz IReferenceClock

La interfaz **IReferenceClock** proporciona acceso a un reloj externo. Esta interfaz se proporciona para permitir que todas las rutinas de representación se sincronicen con el mismo reloj.

Esta interfaz se puede obtener de un objeto de lector.

## <a name="members"></a>Miembros

La interfaz **IReferenceClock** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IReferenceClock** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IReferenceClock** tiene estos métodos.



| Método                                                   | Descripción                                                               |
|:---------------------------------------------------------|:--------------------------------------------------------------------------|
| [**AdvisePeriodic**](ireferenceclock-adviseperiodic.md) | No implementado por este SDK.<br/>                                   |
| [**AdviseTime**](ireferenceclock-advisetime.md)         | Solicita una notificación asincrónica de que ha transcurrido una hora.<br/> |
| [**GetTime**](ireferenceclock-gettime.md)               | Recupera el tiempo de referencia actual.<br/>                          |
| [**No notificar**](ireferenceclock-unadvise.md)             | Cancela una solicitud de notificación.<br/>                                |



 

## <a name="remarks"></a>Observaciones

Para obtener información sobre otras interfaces que se pueden obtener con el método QueryInterface de esta interfaz, vea objeto Reader.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces**](interfaces.md)
</dt> </dl>

 

