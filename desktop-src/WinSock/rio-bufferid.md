---
description: Especifica un descriptor de búfer registrado que se usa con las extensiones de E/S registradas de Winsock.
ms.assetid: 87D0A3F6-A44C-4D7F-B276-7FD5DC2DE7A3
title: RIO_BUFFERID (Mswsockdef.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bde67e14a1cb591922ddc180ab8f308b8429c2b36c5998d313876200cd3a26c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097555"
---
# <a name="rio_bufferid"></a>BUFFERID \_ de RIO

La **\_ definición de tipo BUFFERID** de RIO especifica un descriptor de búfer registrado que se usa con las extensiones de E/S registradas de Winsock.


```C++
typedef struct RIO_BUFFERID_t* RIO_BUFFERID, **PRIO_BUFFERID;
```



<dl> <dt>

**BUFFERID \_ de RIO**
</dt> <dd>

Tipo de datos que especifica un descriptor de búfer registrado que se usa con las solicitudes de envío y recepción.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Las extensiones de E/S registradas de Winsock funcionan principalmente en búferes registrados mediante **objetos \_ BUFFERID de RIO.** Una aplicación obtiene un **\_ BUFFERID de RIO para** un búfer existente mediante la función [**RIORegisterBuffer.**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) Una aplicación puede liberar un registro mediante [**la función RIODeregisterBuffer.**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer)

Cuando un búfer existente se registra como un objeto **\_ BUFFERID de RIO** mediante la función [**RIORegisterBuffer,**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) determinados recursos internos se asignan desde la memoria física y el búfer de aplicación existente se bloqueará en la memoria física. Se llama a la función [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) para anular el registro del búfer, liberar estos recursos internos y permitir que el búfer se desbloquee y se libera de la memoria física.

El registro y la anulación de registro repetidos de los búferes de aplicación mediante las extensiones de E/S registradas de Winsock pueden provocar una degradación significativa del rendimiento. Los siguientes enfoques de administración de búfer deben tenerse en cuenta al diseñar una aplicación mediante las extensiones de E/S registradas de Winsock para minimizar el registro repetido y la anulación del registro de búferes de aplicación:

-   • Maximizar la reutilización de búferes.
-   • Mantenga un grupo limitado de búferes registrados sin usar para su uso por parte de la aplicación.
-   • Mantenga un grupo limitado de búferes registrados y realice copias de búfer entre estos búferes registrados y otros búferes no registrados.

La **\_ definición de tipo BUFFERID** de RIO se define en el archivo de encabezado *Mswsockdef.h* que se incluye automáticamente en el archivo de encabezado *Mswsock.h.* El *archivo de encabezado Mswsockdef.h* nunca debe usarse directamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                                  |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                        |
| Header<br/>                   | <dl> <dt>Mswsockdef.h (incluye Mswsock.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**RIO \_ BUF**](/windows/desktop/api/Mswsockdef/ns-mswsockdef-rio_buf)
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

 

 
