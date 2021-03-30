---
description: Especifica un descriptor de búfer registrado usado con las extensiones de e/s registradas de Winsock.
ms.assetid: 87D0A3F6-A44C-4D7F-B276-7FD5DC2DE7A3
title: RIO_BUFFERID (Mswsockdef. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75bb439a567c361a056b750728d986891a1da468
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082401"
---
# <a name="rio_bufferid"></a>Río \_ BUFFERID

La definición de tipo de **Rio \_ BUFFERID** especifica un descriptor de búfer registrado que se usa con las extensiones de e/s registradas de Winsock.


```C++
typedef struct RIO_BUFFERID_t* RIO_BUFFERID, **PRIO_BUFFERID;
```



<dl> <dt>

**Río \_ BUFFERID**
</dt> <dd>

Un tipo de datos que especifica un descriptor de búfer registrado utilizado con solicitudes de envío y recepción.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las extensiones de e/s registradas de Winsock funcionan principalmente en búferes registrados mediante objetos **río \_ BUFFERID** . Una aplicación obtiene un **río \_ BUFFERID** para un búfer existente mediante la función [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) . Una aplicación puede liberar un registro mediante la función [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) .

Cuando un búfer existente se registra como un objeto **río \_ BUFFERID** mediante la función [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) , se asignan determinados recursos internos de la memoria física y el búfer de aplicación existente se bloqueará en la memoria física. Se llama a la función [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) para anular el registro del búfer, liberar estos recursos internos y permitir que el búfer se desbloquee y se libere de la memoria física.

El registro y la cancelación de registro repetidos de los búferes de la aplicación mediante las extensiones de e/s registradas de Winsock pueden provocar una degradación significativa del rendimiento. Se deben tener en cuenta los siguientes enfoques de administración de búfer al diseñar una aplicación mediante las extensiones de e/s registradas de Winsock para minimizar el registro y la cancelación de registro repetidos de los búferes de la aplicación:

-   • Maximice la reutilización de búferes.
-   • Mantener un grupo limitado de búferes registrados no utilizados para que la aplicación los use.
-   • Mantener un grupo limitado de búferes registrados y realizar copias de búfer entre estos búferes registrados y otros búferes no registrados.

La definición de tipo de **Rio \_ BUFFERID** se define en el archivo de encabezado *Mswsockdef. h* que se incluye automáticamente en el archivo de encabezado *mswsock. h* . El archivo de encabezado *Mswsockdef. h* nunca debe usarse directamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                                  |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                        |
| Encabezado<br/>                   | <dl> <dt>Mswsockdef. h (incluye mswsock. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Río \_ BUF**](/windows/desktop/api/Mswsockdef/ns-mswsockdef-rio_buf)
</dt> <dt>

[**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer)
</dt> <dt>

[**RIOReceive**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive)
</dt> <dt>

[**RIOReceiveEx**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex)
</dt> <dt>

[**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85))
</dt> <dt>

[**RIOSend**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend)
</dt> <dt>

[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))
</dt> </dl>

 

 
