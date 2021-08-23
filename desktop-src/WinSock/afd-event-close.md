---
description: Evento de seguimiento de red Winsock para la operación de cierre del socket.
ms.assetid: C59B2B51-288A-46C9-B390-26A18DB0C2FB
title: AFD_EVENT_CLOSE evento
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AFD_EVENT_CLOSE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9068809c052638e33d45a5affadc23a289fa65ae04e6b1a71af1e40e4b508b15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993755"
---
# <a name="afd_event_close-event"></a>Evento AFD \_ EVENT \_ CLOSE

El **evento AFD \_ EVENT \_ CLOSE** es un evento de seguimiento de red winsock para la operación de cierre del socket.


```C++
const EVENT_DESCRIPTOR AFD_EVENT_CLOSE = {0x3e9, 0x0, 0x10, 0x4, 0xf, 0x3e9, 0x8000000000000004};
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*EnterExit* 
</dt> <dd>

Información sobre este evento.

En la tabla siguiente se enumeran los valores posibles para *el parámetro EnterExit:*



| Valor                                                                        | Significado                                                                                              |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Inicio de una solicitud winsock.<br/>                                                           |
| <dl> <dt>1</dt> </dl> | Se completó la solicitud winsock.<br/>                                                            |
| <dl> <dt>2</dt> </dl> | El controlador afd winsock realizó una acción interna (anulando una conexión, por ejemplo).<br/>      |
| <dl> <dt>3</dt> </dl> | El controlador TCP/IP provocó que se produjese este evento. Esto suele indicar una notificación de datos.<br/> |
| <dl> <dt>4</dt> </dl> | El controlador AFD winsock provocó que se produjese este evento (por ejemplo, al establecer una opción de socket).<br/> |



 

</dd> <dt>

*Ubicación* 
</dt> <dd>

Campo privado que se usa internamente.

</dd> <dt>

*Process* 
</dt> <dd>

Dirección [EPROCESS](/windows-hardware/drivers/kernel/eprocess) del proceso que posee el socket relacionado. Se trata de una estructura opaca que actúa como objeto de proceso para un proceso. Para más información, consulte la documentación Windows Driver Kit para la [estructura EPROCESS.](/windows-hardware/drivers/kernel/eprocess)

</dd> <dt>

*Punto de conexión* 
</dt> <dd>

Dirección DEL PUNTO DE CONEXIÓN DE AFD \_ del socket.

</dd> <dt>

*Estado* 
</dt> <dd>

Código NTSTATUS de la operación.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Se hace un seguimiento del evento **\_ AFD EVENT \_ CLOSE** para que una operación de red Winsock cierre un socket. El canal para este evento es Winsock-AFD. El nivel de este evento es informativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Control del seguimiento de Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[**\_DESCRIPTOR DE EVENTOS**](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
</dt> <dt>

[Seguimiento de Winsock](winsock-tracing.md)
</dt> <dt>

[Niveles de seguimiento de Winsock](winsock-tracing-levels.md)
</dt> <dt>

[Detalles del seguimiento de cambios del catálogo de Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

