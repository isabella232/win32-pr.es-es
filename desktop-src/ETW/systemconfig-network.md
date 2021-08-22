---
description: Esta clase es la clase de tipo de evento para los eventos de red. La sintaxis siguiente se simplifica a partir del código MOF.
ms.assetid: afa994ef-dd1c-4909-a6cd-7021be4fff40
title: SystemConfig_Network clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Network
- SystemConfig_Network.TcbTablePartitions
- SystemConfig_Network.MaxHashTableSize
- SystemConfig_Network.MaxUserPort
- SystemConfig_Network.TcpTimedWaitDelay
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6b196e8c1ad5a997642cc48491e9d1a4b5e73bc26db71d5ea5258f7cf162a00a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069695"
---
# <a name="systemconfig_network-class"></a>Clase SystemConfig \_ Network

Esta clase es la clase de tipo de evento para los eventos de red.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[EventType(17), EventTypeName("Network")]
class SystemConfig_Network : SystemConfig
{
  uint32 TcbTablePartitions;
  uint32 MaxHashTableSize;
  uint32 MaxUserPort;
  uint32 TcpTimedWaitDelay;
};
```

## <a name="members"></a>Miembros

La **clase SystemConfig \_ Network** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase SystemConfig \_ Network** tiene estas propiedades.

<dl> <dt>

**MaxHashTableSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(2)
</dt> </dl>

Tamaño de la tabla hash en la que se almacenan los bloques de control TCP (TCB). TCP almacena bloques de control en una tabla hash para que pueda encontrarlos muy rápidamente.

</dd> <dt>

**MaxUserPort**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(3)
</dt> </dl>

Número de puerto más alto que TCP puede asignar cuando una aplicación solicita un puerto de usuario disponible del sistema. Normalmente, los puertos efímeros (los que se usan brevemente) se asignan a los números de puerto del 1024 al 5000.

El valor del número de puerto de usuario más alto que TCP puede asignar se controla mediante una configuración del Registro. Para obtener más información, [vea MaxUserPort](/previous-versions/windows/it-pro/windows-2000-server/cc938196(v=technet.10)).

</dd> <dt>

**TcbTablePartitions**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(1)
</dt> </dl>

Número de particiones de la tabla Bloque de control de transporte. La creación de particiones en la tabla Bloque de control de transporte minimiza la contención para el acceso a la tabla. Esto es especialmente útil en sistemas de varios procesadores.

</dd> <dt>

**TcpTimedWaitDelay**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId(4)
</dt> </dl>

El tiempo que debe transcurrir para que TCP pueda liberar una conexión cerrada y reutilizar sus recursos. Este intervalo entre el cierre y la versión se conoce como estado \_ TIME WAIT o 2MSL. Durante este tiempo, la conexión se puede volver a abrir con un costo mucho menor para el cliente y el servidor que establecer una nueva conexión.

RFC 793 publicado por el IETF requiere que TCP mantenga una conexión cerrada durante un intervalo al menos igual al doble de la duración máxima del segmento (2MSL) de la red. Cuando se libera una conexión, su par de sockets y el bloque de control TCP (TCB) se pueden usar para admitir otra conexión. De forma predeterminada, la MSL se define como 120 segundos y el valor de esta entrada es igual a dos MSL, o 4 minutos. Para obtener más información, [vea RFC 793](https://tools.ietf.org/html/rfc973).

La reducción del valor de esta entrada mediante una configuración del Registro permite que TCP libere conexiones cerradas más rápido, lo que proporciona más recursos para las nuevas conexiones. Sin embargo, si el valor es demasiado bajo, TCP podría liberar recursos de conexión antes de que se complete la conexión, lo que requiere que el servidor use recursos adicionales para restablecer la conexión.

Normalmente, TCP no libera las conexiones cerradas hasta que expira el valor de esta entrada. Sin embargo, TCP puede liberar conexiones antes de que expire este valor si se está quedando sin bloques de control TCP (TCB). El número de TCB que crea el sistema se controla mediante una configuración del Registro. Para obtener más información, [vea MaxFreeTCBs](/previous-versions/windows/it-pro/windows-2000-server/cc938178(v=technet.10)).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 
