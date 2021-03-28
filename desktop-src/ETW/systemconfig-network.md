---
description: Esta clase es la clase de tipo de evento para eventos de red. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: afa994ef-dd1c-4909-a6cd-7021be4fff40
title: SystemConfig_Network (clase)
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
ms.openlocfilehash: 23b469c31645c6a5b04319f91b758ee19beb935c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984451"
---
# <a name="systemconfig_network-class"></a>\_Clase de red SystemConfig

Esta clase es la clase de tipo de evento para eventos de red.

La siguiente sintaxis se simplifica desde el código MOF.

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

La clase de **\_ red SystemConfig** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase de **\_ red SystemConfig** tiene estas propiedades.

<dl> <dt>

**MaxHashTableSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (2)
</dt> </dl>

Tamaño de la tabla hash en la que se almacenan los bloques de control TCP (TCBs). TCP almacena los bloques de control en una tabla hash para que pueda encontrarlos muy rápidamente.

</dd> <dt>

**MaxUserPort**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (3)
</dt> </dl>

El número de Puerto máximo TCP puede asignar cuando una aplicación solicita un puerto de usuario disponible del sistema. Normalmente, los puertos efímeros (los usados brevemente) se asignan a los números de puerto de 1024 a 5000.

El valor del número de puerto de usuario más alto que TCP puede asignar se controla mediante una configuración del registro. Para obtener más información, consulte [MaxUserPort](/previous-versions/windows/it-pro/windows-2000-server/cc938196(v=technet.10)).

</dd> <dt>

**TcbTablePartitions**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (1)
</dt> </dl>

El número de particiones en la tabla de bloque de control de transporte. La creación de particiones en la tabla de bloques de control de transporte minimiza la contención del acceso a las tablas. Esto es especialmente útil en sistemas multiprocesador.

</dd> <dt>

**TcpTimedWaitDelay**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: WmiDataId (4)
</dt> </dl>

El tiempo que debe transcurrir antes de que TCP pueda liberar una conexión cerrada y volver a usar sus recursos. Este intervalo entre el cierre y la versión se conoce como \_ Estado de espera de tiempo o estado de 2MSL. Durante este tiempo, la conexión se puede volver a abrir mucho menos en el cliente y el servidor que en el establecimiento de una nueva conexión.

RFC 793 publicado por IETF requiere que TCP mantenga una conexión cerrada para un intervalo de al menos igual al doble de la duración máxima del segmento (2MSL) de la red. Cuando se libera una conexión, su par de sockets y el bloque de control TCP (TCB) se pueden usar para admitir otra conexión. De forma predeterminada, el MSL se define como 120 segundos y el valor de esta entrada es igual a dos MSLs, o 4 minutos. Para obtener más información, consulte [RFC 793](https://tools.ietf.org/html/rfc973).

Reducir el valor de esta entrada mediante una configuración de registro permite a TCP liberar conexiones cerradas más rápido, lo que proporciona más recursos para las nuevas conexiones. Sin embargo, si el valor es demasiado bajo, es posible que TCP libere recursos de conexión antes de que se complete la conexión, lo que requiere que el servidor use recursos adicionales para restablecer la conexión.

Normalmente, TCP no libera las conexiones cerradas hasta que expire el valor de esta entrada. Sin embargo, TCP puede liberar conexiones antes de que este valor expire si se está quedando sin bloques de control TCP (TCBs). El número de TCBs que crea el sistema se controla mediante una configuración del registro. Para obtener más información, vea [MaxFreeTCBs](/previous-versions/windows/it-pro/windows-2000-server/cc938178(v=technet.10)).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 
