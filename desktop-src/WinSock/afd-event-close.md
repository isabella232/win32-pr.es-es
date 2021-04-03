---
description: Evento de seguimiento de red Winsock para la operación de cierre del socket.
ms.assetid: C59B2B51-288A-46C9-B390-26A18DB0C2FB
title: Evento AFD_EVENT_CLOSE
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
ms.openlocfilehash: fbc6c63a3084db6a9be0a4b4ea7672d84881a29a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809764"
---
# <a name="afd_event_close-event"></a>Evento de cierre de \_ evento de AFD \_

El evento de **\_ \_ cierre de evento de AFD** es un evento de seguimiento de la red Winsock para la operación de cierre del socket.


```C++
const EVENT_DESCRIPTOR AFD_EVENT_CLOSE = {0x3e9, 0x0, 0x10, 0x4, 0xf, 0x3e9, 0x8000000000000004};
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*EnterExit* 
</dt> <dd>

Información sobre este evento.

En la tabla siguiente se enumeran los posibles valores para el parámetro *EnterExit* :



| Value                                                                        | Significado                                                                                              |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Inicio de una solicitud Winsock.<br/>                                                           |
| <dl> <dt>1</dt> </dl> | Se completó la solicitud Winsock.<br/>                                                            |
| <dl> <dt>2</dt> </dl> | El controlador Winsock AFD llevó a cabo una acción interna (anulando una conexión, por ejemplo).<br/>      |
| <dl> <dt>3</dt> </dl> | El controlador TCP/IP hizo que se produjera este evento. Normalmente, esto indica una notificación de datos.<br/> |
| <dl> <dt>4</dt> </dl> | El controlador Winsock AFD hizo que se produjera este evento (por ejemplo, si se establece una opción de socket).<br/> |



 

</dd> <dt>

*Ubicación* 
</dt> <dd>

Campo privado que se usa internamente.

</dd> <dt>

*Proceso* 
</dt> <dd>

La dirección [EPROCESS](/windows-hardware/drivers/kernel/eprocess) del proceso que posee el socket relacionado. Se trata de una estructura opaca que actúa como el objeto de proceso de un proceso. Para obtener más información, consulte la documentación del kit de controladores de Windows para la estructura [EPROCESS](/windows-hardware/drivers/kernel/eprocess) .

</dd> <dt>

*Punto de conexión* 
</dt> <dd>

Dirección del \_ punto de conexión de AFD del socket.

</dd> <dt>

*Estado* 
</dt> <dd>

Código NTSTATUS de la operación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Se realiza un seguimiento del evento de **\_ \_ cierre de evento de AFD** para que una operación de red Winsock cierre un socket. El canal de este evento es Winsock-AFD. El nivel de este evento es informativo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Control de seguimiento de Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[**descriptor de eventos \_**](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
</dt> <dt>

[Seguimiento de Winsock](winsock-tracing.md)
</dt> <dt>

[Niveles de seguimiento de Winsock](winsock-tracing-levels.md)
</dt> <dt>

[Detalles de seguimiento de cambios de catálogo Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

