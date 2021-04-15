---
title: RAS_PORT_STATISTICS estructura (rassapi. h)
description: La \_ estructura de estadísticas del puerto ras informa de \_ las estadísticas que un servidor RAS recopila para un puerto conectado.
ms.assetid: c42c7059-ff92-4f49-a86e-2f47a083aa8e
keywords:
- RAS_PORT_STATISTICS de la estructura RAS
- PRAS_PORT_STATISTICS de puntero de estructura RAS
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676773"
---
# <a name="ras_port_statistics-structure"></a>Estructura de estadísticas del \_ Puerto ras \_

\[La estructura de **\_ \_ estadísticas del puerto ras** no es compatible con Windows Vista.\]

La estructura de **\_ \_ estadísticas del puerto ras** informa de las estadísticas que un servidor RAS recopila para un puerto conectado. El servidor RAS restablece los diversos contadores de estadísticas cada vez que se conecta el puerto. Llame a la función [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md) para obligar al servidor RAS a restablecer los contadores estadísticos.

En el caso de un puerto que forme parte de una conexión multivínculo, esta estructura proporciona dos conjuntos de estadísticas. El primer conjunto contiene las Estadísticas acumulativas para todos los puertos de la conexión. Estas estadísticas son las mismas para todos los puertos de la conexión. El segundo conjunto contiene las estadísticas de solo este puerto. Si el puerto no forma parte de una conexión de multivínculo, ambos conjuntos de estadísticas tienen la misma información. Para determinar si un puerto forma parte de una conexión de multivínculo, compruebe el \_ bit MULTIlinked del puerto en el miembro **Flags** de la estructura del puerto ras del puerto. [**\_ \_**](ras-port-0-str.md)

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



## <a name="members"></a>Miembros

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

Especifica el número total de errores de CRC en la conexión. Los errores de CRC se deben a un error en una comprobación de redundancia cíclica. Un error de CRC indica que uno o varios caracteres del paquete de datos recibido se detectaron inalterados al llegar.

</dd> <dt>

**dwTimeoutErr**
</dt> <dd>

Especifica el número total de errores de tiempo de espera en la conexión. Los errores de tiempo de espera se producen cuando no se recibe un carácter esperado en el tiempo. Cuando esto ocurre, el software presupone que los datos se han perdido y solicita que se reenvíen.

</dd> <dt>

**dwAlignmentErr**
</dt> <dd>

Especifica el número total de errores de alineación en la conexión. Los errores de alineación se producen cuando un carácter recibido no es el esperado. Esto suele suceder cuando se pierde un carácter o cuando se produce un error de tiempo de espera.

</dd> <dt>

**dwHardwareOverrunErr**
</dt> <dd>

Especifica el número total de errores de saturación de hardware en la conexión. Estos errores indican el número de veces que el equipo emisor ha transmitido caracteres más rápido que el equipo receptor puede procesarlos. Si el problema persiste, reduzca la velocidad de conexión de BPS en el cliente.

</dd> <dt>

**dwFramingErr**
</dt> <dd>

Especifica el número total de errores de tramas de la conexión. Se produce un error de tramas cuando se recibe un carácter asincrónico con un bit de inicio o detención no válido.

</dd> <dt>

**dwBufferOverrunErr**
</dt> <dd>

Especifica el número total de errores de saturación del búfer en la conexión. Se produce un error de saturación del búfer cuando el equipo emisor está transmitiendo caracteres más rápido que el equipo receptor. Si el problema persiste, reduzca la velocidad de conexión de BPS en el cliente.

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

Especifica el número total de bytes transmitidos por la conexión.

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

Especifica el número total de errores de CRC en el puerto. Los errores de CRC se deben a un error en una comprobación de redundancia cíclica. Un error de CRC indica que uno o varios caracteres del paquete de datos recibido se detectaron inalterados al llegar.

</dd> <dt>

**dwPortTimeoutErr**
</dt> <dd>

Especifica el número total de errores de tiempo de espera en el puerto. Los errores de tiempo de espera se producen cuando no se recibe un carácter esperado en el tiempo. Cuando esto ocurre, el software presupone que los datos se han perdido y solicita que se reenvíen.

</dd> <dt>

**dwPortAlignmentErr**
</dt> <dd>

Especifica el número total de errores de alineación en el puerto. Los errores de alineación se producen cuando un carácter recibido no es el esperado. Esto suele suceder cuando se pierde un carácter o cuando se produce un error de tiempo de espera.

</dd> <dt>

**dwPortHardwareOverrunErr**
</dt> <dd>

Especifica el número total de errores de saturación de hardware en el puerto. Estos errores indican el número de veces que el equipo emisor ha transmitido caracteres más rápido que el equipo receptor puede procesarlos. Si el problema persiste, reduzca la velocidad de conexión de BPS en el cliente.

</dd> <dt>

**dwPortFramingErr**
</dt> <dd>

Especifica el número total de errores de tramas en el puerto. Se produce un error de tramas cuando se recibe un carácter asincrónico con un bit de inicio o detención no válido.

</dd> <dt>

**dwPortBufferOverrunErr**
</dt> <dd>

Especifica el número total de errores de saturación del búfer en el puerto. Se produce un error de saturación del búfer cuando el equipo emisor está transmitiendo caracteres más rápido que el equipo receptor. Si el problema persiste, reduzca la velocidad de conexión de BPS en el cliente.

</dd> <dt>

**dwPortBytesXmitedUncompressed**
</dt> <dd>

Especifica el número total de bytes transmitidos sin comprimir por el puerto. Si el puerto forma parte de una conexión de multivínculo, este miembro no es válido. En su lugar, use las estadísticas de compresión de la conexión.

</dd> <dt>

**dwPortBytesRcvedUncompressed**
</dt> <dd>

Especifica el número total de bytes recibidos sin comprimir por el puerto. Si el puerto forma parte de una conexión de multivínculo, este miembro no es válido. En su lugar, use las estadísticas de compresión de la conexión.

</dd> <dt>

**dwPortBytesXmitedCompressed**
</dt> <dd>

Especifica el número total de bytes transmitidos por el puerto. Si el puerto forma parte de una conexión de multivínculo, este miembro no es válido. En su lugar, use las estadísticas de compresión de la conexión.

</dd> <dt>

**dwPortBytesRcvedCompressed**
</dt> <dd>

Especifica el número total de bytes recibidos comprimidos por el puerto. Si el puerto forma parte de una conexión de multivínculo, este miembro no es válido. En su lugar, use las estadísticas de compresión de la conexión.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Rassapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Introducción al servicio de acceso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Estructuras de administración del servidor RAS](ras-server-administration-structures.md)
</dt> <dt>

[**\_Puerto ras \_ 0**](ras-port-0-str.md)
</dt> <dt>

[**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md)
</dt> <dt>

[**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md)
</dt> <dt>

[**RasAdminPortClearStatistics**](rasadminportclearstatistics.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





