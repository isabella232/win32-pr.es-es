---
description: La clase CAMEvent es un contenedor para los eventos de restablecimiento manual y de restablecimiento automático.
ms.assetid: 228b4e51-afc5-4cb6-b225-309013713983
title: Clase CAMEvent (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bde2db8adf2bb713df665e06eb2cc5f8d2a9a00f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670692"
---
# <a name="camevent-class"></a>Clase CAMEvent

![jerarquía de clases camevent](images/util06.png)

La clase **CAMEvent** es un contenedor para los eventos de restablecimiento manual y de restablecimiento automático.

Esta clase proporciona una manera cómoda de administrar eventos, en lugar de llamar a funciones como [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)y [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent).



| Variables de miembro protegidas                          | Descripción                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------|
| [**m \_ hEvent**](camevent-m-hevent.md)              | Identificador del evento.                                                   |
| Métodos públicos                                      | Descripción                                                     |
| [**CAMEvent**](camevent-camevent.md)               | Método de constructor.                                             |
| [**~ CAMEvent**](camevent--camevent.md)             | Método de destructor.                                              |
| [**de Azure Functions**](camevent-check.md)                     | Comprueba si el evento está establecido, sin bloqueos.              |
| [**Reset**](camevent-reset.md)                     | Establece el estado del evento en no señalado.                     |
| [**Conjunto**](camevent-set.md)                         | Señala el evento.                                              |
| [**Esperar**](camevent-wait.md)                       | Se bloquea hasta que se señale el evento o hasta que se agote el tiempo de espera. |
| Operadores                                           | Descripción                                                     |
| [**IDENTIFICADOR de operador**](camevent-operator-handle.md) | Recupera el identificador del evento.                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

