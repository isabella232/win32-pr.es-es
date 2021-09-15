---
title: Interfaz IReferenceClock
description: La interfaz IReferenceClock proporciona acceso a un reloj externo. Esta interfaz se proporciona para permitir que todas las rutinas de representación se sincronicen con el mismo reloj. Esta interfaz se puede obtener de un objeto de lector.
ms.assetid: 1424fd74-d56c-4338-801f-319ef975169f
keywords:
- IReferenceClock interface windows Media Format
- IReferenceClock interface windows Media Format , descrito
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466702"
---
# <a name="ireferenceclock-interface"></a>Interfaz IReferenceClock

La **interfaz IReferenceClock** proporciona acceso a un reloj externo. Esta interfaz se proporciona para permitir que todas las rutinas de representación se sincronicen con el mismo reloj.

Esta interfaz se puede obtener de un objeto de lector.

## <a name="members"></a>Members

La **interfaz IReferenceClock** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IReferenceClock** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IReferenceClock** tiene estos métodos.



| Método                                                   | Descripción                                                               |
|:---------------------------------------------------------|:--------------------------------------------------------------------------|
| [**AdvisePeriodic**](ireferenceclock-adviseperiodic.md) | No implementado por este SDK.<br/>                                   |
| [**AdviseTime**](ireferenceclock-advisetime.md)         | Solicita una notificación asincrónica de que ha transcurrido un tiempo.<br/> |
| [**ConocerHora**](ireferenceclock-gettime.md)               | Recupera la hora de referencia actual.<br/>                          |
| [**Unadvise**](ireferenceclock-unadvise.md)             | Cancela una solicitud de notificación.<br/>                                |



 

## <a name="remarks"></a>Observaciones

Para obtener información sobre otras interfaces que se pueden obtener mediante el método QueryInterface de esta interfaz, vea Objeto Reader.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaces**](interfaces.md)
</dt> </dl>

 

