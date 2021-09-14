---
title: RAS_PORT_STATISTICS estructura (Rassapi.h)
description: La estructura \_ RAS PORT STATISTICS informa de las estadísticas que recopila un servidor \_ RAS para un puerto conectado.
ms.assetid: c42c7059-ff92-4f49-a86e-2f47a083aa8e
keywords:
- RAS_PORT_STATISTICS ras de estructura
- PRAS_PORT_STATISTICS de estructura ras
topic_type:
- apiref
api_name:
- RAS_PORT_STATISTICS
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85e60fb001da3f8401e47c366eecc86aced22b77
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073872"
---
# <a name="ras_port_statistics-structure"></a>Estructura \_ RAS PORT \_ STATISTICS

\[La **estructura RAS PORT \_ \_ STATISTICS** no se admite a Windows Vista.\]

La **estructura RAS PORT \_ \_ STATISTICS** informa de las estadísticas que recopila un servidor RAS para un puerto conectado. El servidor RAS restablece los distintos contadores estadísticos cada vez que se conecta el puerto. Llame a [**la función RasAdminPortClearStatistics**](rasadminportclearstatistics.md) para forzar al servidor RAS a restablecer los contadores estadísticos.

Para un puerto que forma parte de una conexión de varios vínculos, esta estructura proporciona dos conjuntos de estadísticas. El primer conjunto contiene las estadísticas acumulativas de todos los puertos de la conexión. Estas estadísticas son las mismas para todos los puertos de la conexión. El segundo conjunto contiene las estadísticas de solo este puerto. Si el puerto no forma parte de una conexión de varios vínculos, ambos conjuntos de estadísticas tienen la misma información. Para determinar si un puerto forma parte de una conexión de varios vínculos, compruebe el bit PORT MULTILINKED en el miembro Flags de la estructura \_ [**RAS PORT \_ \_ 0 del**](ras-port-0-str.md) puerto. 

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _RAS_PORT_STATISTICS {
  DWORD dwBytesXmited;
  DWORD dwBytesRcved;
  DWORD dwFramesXmited;
  DWORD dwFramesRcved;
  DWORD dwCrcErr;
  DWORD dwTimeoutErr;
  DWORD dwAlignmentErr;
  DWORD dwHardwareOverrunErr;
  DWORD dwFramingErr;
  DWORD dwBufferOverrunErr;
  DWORD dwBytesXmitedUncompressed;
  DWORD dwBytesRcvedUncompressed;
  DWORD dwBytesXmitedCompressed;
  DWORD dwBytesRcvedCompressed;
  DWORD dwPortBytesXmited;
  DWORD dwPortBytesRcved;
  DWORD dwPortFramesXmited;
  DWORD dwPortFramesRcved;
  DWORD dwPortCrcErr;
  DWORD dwPortTimeoutErr;
  DWORD dwPortAlignmentErr;
  DWORD dwPortHardwareOverrunErr;
  DWORD dwPortFramingErr;
  DWORD dwPortBufferOverrunErr;
  DWORD dwPortBytesXmitedUncompressed;
  DWORD dwPortBytesRcvedUncompressed;
  DWORD dwPortBytesXmitedCompressed;
  DWORD dwPortBytesRcvedCompressed;
} RAS_PORT_STATISTICS, *PRAS_PORT_STATISTICS;
```



## <a name="members"></a>Members

<dl> <dt>

**dwBytesXmited**
</dt> <dd>

Especifica el número total de bytes transmitidos por la conexión.

</dd> <dt>

**dwBytesRcved**
</dt> <dd>

Especifica el número total de bytes recibidos por la conexión.

</dd> <dt>

**dwFramesXmited**
</dt> <dd>

Especifica el número total de fotogramas transmitidos por la conexión.

</dd> <dt>

**dwFramesRcved**
</dt> <dd>

Especifica el número total de fotogramas recibidos por la conexión.

</dd> <dt>

**dwCrcErr**
</dt> <dd>

Especifica el número total de errores de CRC en la conexión. Los errores de CRC se producen por el error de una comprobación de redundancia cíclica. Un error de CRC indica que uno o varios caracteres del paquete de datos recibido se encontraron desasolados al llegar.

</dd> <dt>

**dwTimeoutErr**
</dt> <dd>

Especifica el número total de errores de tiempo de espera en la conexión. Los errores de tiempo de espera se producen cuando no se recibe a tiempo un carácter esperado. Cuando esto sucede, el software asume que los datos se han perdido y solicita que se reenviarán.

</dd> <dt>

**dwAlignmentErr**
</dt> <dd>

Especifica el número total de errores de alineación en la conexión. Los errores de alineación se producen cuando un carácter recibido no es el esperado. Esto suele ocurrir cuando se pierde un carácter o cuando se produce un error de tiempo de espera.

</dd> <dt>

**dwHardwareOverrunErr**
</dt> <dd>

Especifica el número total de errores de saturación de hardware en la conexión. Estos errores indican el número de veces que el equipo de envío ha transmitido caracteres más rápido que el hardware del equipo receptor puede procesarlos. Si este problema persiste, reduzca la velocidad de conexión de BPS en el cliente.

</dd> <dt>

**dwFramingErr**
</dt> <dd>

Especifica el número total de errores de trama en la conexión. Se produce un error de trama cuando se recibe un carácter asincrónico con un bit inicial o de detenerse no válido.

</dd> <dt>

**dwBufferOverrunErr**
</dt> <dd>

Especifica el número total de errores de saturación del búfer en la conexión. Se produce un error de saturación del búfer cuando el equipo de envío transmite caracteres más rápido de lo que el equipo receptor puede alojarlos. Si este problema persiste, reduzca la velocidad de conexión de BPS en el cliente.

</dd> <dt>

**dwBytesXmitedUncompressed**
</dt> <dd>

Especifica el número total de bytes transmitidos sin comprimir por la conexión.

</dd> <dt>

**dwBytesRcvedUncompressed**
</dt> <dd>

Especifica el número total de bytes recibidos sin comprimir por la conexión.

</dd> <dt>

**dwBytesXmitedCompressed**
</dt> <dd>

Especifica el número total de bytes transmitidos comprimidos por la conexión.

</dd> <dt>

**dwBytesRcvedCompressed**
</dt> <dd>

Especifica el número total de bytes recibidos comprimidos por la conexión.

</dd> <dt>

**dwPortBytesXmited**
</dt> <dd>

Especifica el número total de bytes transmitidos por el puerto.

</dd> <dt>

**dwPortBytesRcved**
</dt> <dd>

Especifica el número total de bytes recibidos por el puerto.

</dd> <dt>

**dwPortFramesXmited**
</dt> <dd>

Especifica el número total de fotogramas transmitidos por el puerto.

</dd> <dt>

**dwPortFramesRcved**
</dt> <dd>

Especifica el número total de fotogramas recibidos por el puerto.

</dd> <dt>

**dwPortCrcErr**
</dt> <dd>

Especifica el número total de errores de CRC en el puerto. Los errores de CRC se producen por el error de una comprobación de redundancia cíclica. Un error de CRC indica que uno o varios caracteres del paquete de datos recibido se encontraron desasolados al llegar.

</dd> <dt>

**dwPortTimeoutErr**
</dt> <dd>

Especifica el número total de errores de tiempo de espera en el puerto. Los errores de tiempo de espera se producen cuando no se recibe a tiempo un carácter esperado. Cuando esto sucede, el software asume que los datos se han perdido y solicita que se reenviarán.

</dd> <dt>

**dwPortAlignmentErr**
</dt> <dd>

Especifica el número total de errores de alineación en el puerto. Los errores de alineación se producen cuando un carácter recibido no es el esperado. Esto suele ocurrir cuando se pierde un carácter o cuando se produce un error de tiempo de espera.

</dd> <dt>

**dwPortHardwareOverrunErr**
</dt> <dd>

Especifica el número total de errores de saturación de hardware en el puerto. Estos errores indican el número de veces que el equipo de envío ha transmitido caracteres más rápido que el hardware del equipo receptor puede procesarlos. Si este problema persiste, reduzca la velocidad de conexión de BPS en el cliente.

</dd> <dt>

**dwPortFramingErr**
</dt> <dd>

Especifica el número total de errores de trama en el puerto. Se produce un error de trama cuando se recibe un carácter asincrónico con un bit inicial o de detenerse no válido.

</dd> <dt>

**dwPortBufferOverrunErr**
</dt> <dd>

Especifica el número total de errores de saturación del búfer en el puerto. Se produce un error de saturación del búfer cuando el equipo de envío transmite caracteres más rápido de lo que el equipo receptor puede alojarlos. Si este problema persiste, reduzca la velocidad de conexión de BPS en el cliente.

</dd> <dt>

**dwPortBytesXmitedUncompressed**
</dt> <dd>

Especifica el número total de bytes transmitidos sin comprimir por el puerto. Si el puerto forma parte de una conexión de varios vínculos, este miembro no es válido. En su lugar, use las estadísticas de compresión para la conexión.

</dd> <dt>

**dwPortBytesRcvedUncompressed**
</dt> <dd>

Especifica el número total de bytes recibidos sin comprimir por el puerto. Si el puerto forma parte de una conexión de varios vínculos, este miembro no es válido. En su lugar, use las estadísticas de compresión para la conexión.

</dd> <dt>

**dwPortBytesXmitedCompressed**
</dt> <dd>

Especifica el número total de bytes transmitidos comprimidos por el puerto. Si el puerto forma parte de una conexión de varios vínculos, este miembro no es válido. En su lugar, use las estadísticas de compresión para la conexión.

</dd> <dt>

**dwPortBytesRcvedCompressed**
</dt> <dd>

Especifica el número total de bytes recibidos comprimidos por el puerto. Si el puerto forma parte de una conexión de varios vínculos, este miembro no es válido. En su lugar, use las estadísticas de compresión para la conexión.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Rassapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Introducción al Servicio de acceso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Estructuras de administración del servidor RAS](ras-server-administration-structures.md)
</dt> <dt>

[**PUERTO \_ \_ RAS 0**](ras-port-0-str.md)
</dt> <dt>

[**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md)
</dt> <dt>

[**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md)
</dt> <dt>

[**RasAdminPortClearStatistics**](rasadminportclearstatistics.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





