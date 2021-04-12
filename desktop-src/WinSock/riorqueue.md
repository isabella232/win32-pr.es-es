---
description: Especifica un descriptor de socket utilizado por las solicitudes de envío y recepción con las extensiones de e/s registradas de Winsock.
ms.assetid: 50E9516C-6078-4466-A593-3F29E4783740
title: RIO_RQ (Mswsockdef. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c25abebbe40842532f3cca180868b5b3786e756d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360547"
---
# <a name="rio_rq"></a>Río \_ PET

La definición de tipo de **Rio \_ PET** especifica un descriptor de socket utilizado por las solicitudes de envío y recepción con las extensiones de e/s registradas de Winsock.


```C++
typedef struct RIO_RQ_t* RIO_RQ, **PRIO_RQ;
```



<dl> <dt>

**Río \_ PET**
</dt> <dd>

Un tipo de datos que especifica un descriptor de socket utilizado por las solicitudes de envío y recepción.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las extensiones de e/s registradas de Winsock funcionan principalmente en un objeto **Rio \_ PET** en lugar de un socket. Una aplicación obtiene un **río \_ PET** para un socket existente mediante la función [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) . Se debe haber creado el socket de entrada mediante una llamada a la función [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) con la marca de **Rio de \_ marca \_ WSA** establecida en el parámetro *dwFlags* .

Después de obtener un objeto **Rio \_ PET** , el descriptor de socket subyacente sigue siendo válido. Una aplicación puede seguir utilizando el socket subyacente para establecer y consultar las opciones de socket, emitir ioctl y, en última instancia, cerrar el socket.

> [!Note]  
> Por motivos de eficacia, el acceso a las colas de finalización (estructuras [**\_ CQ de Rio**](riocqueue.md) ) y a las colas de solicitudes (Structs **\_ PET** ) no están protegidos por primitivas de sincronización. Si necesita tener acceso a una cola de finalización o solicitud desde varios subprocesos, el acceso debe coordinarse mediante una sección crítica, un bloqueo de escritura de lector fino o un mecanismo similar. Este bloqueo no es necesario para el acceso a un único subproceso. Distintos subprocesos pueden tener acceso a solicitudes o colas de finalización independientes sin bloqueos. La necesidad de sincronización solo se produce cuando varios subprocesos intentan obtener acceso a la misma cola. La sincronización también es necesaria si varios subprocesos emiten y reciben en el mismo socket porque las operaciones de envío y recepción utilizan la cola de solicitudes del socket.

 

La definición de tipo de [**Rio \_ PET**](riocqueue.md) se define en el archivo de encabezado *Mswsockdef. h* que se incluye automáticamente en el archivo de encabezado *mswsock. h* . El archivo de encabezado *Mswsockdef. h* nunca debe usarse directamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                                  |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                        |
| Encabezado<br/>                   | <dl> <dt>Mswsockdef. h (incluye mswsock. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue)
</dt> <dt>

[**RIOReceive**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive)
</dt> <dt>

[**RIOReceiveEx**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex)
</dt> <dt>

[**RIOResizeRequestQueue**](/previous-versions/windows/desktop/legacy/hh437204(v=vs.85))
</dt> <dt>

[**RIOSend**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend)
</dt> <dt>

[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))
</dt> <dt>

[**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)
</dt> </dl>

 

 
