---
description: Especifica un descriptor de socket utilizado por las solicitudes de envío y recepción con las extensiones de E/S registradas de Winsock.
ms.assetid: 50E9516C-6078-4466-A593-3F29E4783740
title: RIO_RQ (Mswsockdef.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 162b87d1ae320bfa0e74f08e5a0ef7493c053f39573249246e8b2884e74f599c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993585"
---
# <a name="rio_rq"></a>RIO \_ RQ

La **\_ definición de tipo RQ** de RIO especifica un descriptor de socket utilizado por las solicitudes de envío y recepción con las extensiones de E/S registradas de Winsock.


```C++
typedef struct RIO_RQ_t* RIO_RQ, **PRIO_RQ;
```



<dl> <dt>

**RIO \_ RQ**
</dt> <dd>

Tipo de datos que especifica un descriptor de socket utilizado por las solicitudes de envío y recepción.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Las extensiones de E/S registradas en Winsock funcionan principalmente en un objeto **\_ RQ de RIO** en lugar de en un socket. Una aplicación obtiene un **\_ RQ de RIO** para un socket existente mediante la función [**RIOCreateRequestQueue.**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) El socket de entrada se debe haber creado llamando a la función [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) con la marca **WSA \_ FLAG \_ RIO** establecida en el *parámetro dwFlags.*

Después de obtener un **objeto \_ RQ de RIO,** el descriptor de socket subyacente sigue siendo válido. Una aplicación puede seguir usando el socket subyacente para establecer y consultar las opciones de socket, emitir E/SCL y, en última instancia, cerrar el socket.

> [!Note]  
> Por motivos de eficiencia, el acceso a las colas de finalización (estructuras [**\_ CQ**](riocqueue.md) de RIO) y las colas de solicitudes (estructuras **\_ RQ** de RIO) no están protegidas por primitivos de sincronización. Si necesita acceder a una cola de finalización o solicitud desde varios subprocesos, el acceso debe coordinarse mediante una sección crítica, un bloqueo de escritura de lector remoto o un mecanismo similar. Este bloqueo no es necesario para el acceso de un único subproceso. Los distintos subprocesos pueden acceder a solicitudes o colas de finalización independientes sin bloqueos. La necesidad de sincronización solo se produce cuando varios subprocesos intentan acceder a la misma cola. También se requiere sincronización si varios subprocesos emiten envíos y recepción en el mismo socket porque las operaciones de envío y recepción usan la cola de solicitudes del socket.

 

La [**\_ definición de**](riocqueue.md) tipo RQ de RIO se define en el archivo de encabezado *Mswsockdef.h* que se incluye automáticamente en el archivo de encabezado *Mswsock.h.* El *archivo de encabezado Mswsockdef.h* nunca debe usarse directamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                                  |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                        |
| Header<br/>                   | <dl> <dt>Mswsockdef.h (incluye Mswsock.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

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

 

 
