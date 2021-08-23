---
description: La clase CAMEvent es un contenedor para eventos de restablecimiento manual y restablecimiento automático.
ms.assetid: 228b4e51-afc5-4cb6-b225-309013713983
title: Clase CAMEvent (Wxutil.h)
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
ms.openlocfilehash: ea87239628f001feaa82f84ca8c50941b56d3eb99f486934b551e832d1f588c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955534"
---
# <a name="camevent-class"></a>CLASE CAMEvent

![jerarquía de clases came class](images/util06.png)

La **clase CAMEvent** es un contenedor para eventos de restablecimiento manual y restablecimiento automático.

Esta clase proporciona una manera cómoda de administrar eventos, en lugar de llamar a funciones como [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)y [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent).



| Variables miembro protegidas                          | Descripción                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------|
| [**m \_ hEvent**](camevent-m-hevent.md)              | Identificador de eventos.                                                   |
| Métodos públicos                                      | Descripción                                                     |
| [**EVENTO CAM**](camevent-camevent.md)               | Método constructor.                                             |
| [**~CAMEvent**](camevent--camevent.md)             | Método destructor.                                              |
| [**de Azure Functions**](camevent-check.md)                     | Comprueba si el evento está establecido, sin bloquear.              |
| [**Restablecer**](camevent-reset.md)                     | Establece el estado del evento en nonsignaled.                     |
| [**Establecer**](camevent-set.md)                         | Señala el evento.                                              |
| [**Esperar**](camevent-wait.md)                       | Se bloquea hasta que se señala el evento o hasta que se produce un tiempo de espera. |
| Operadores                                           | Descripción                                                     |
| [**operador HANDLE**](camevent-operator-handle.md) | Recupera el identificador de evento.                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

