---
description: Destinos conocidos que contienen los datos recopilados. Solo está disponible si el recopilador se está ejecutando con el registro de estado habilitado.
ms.assetid: ab0d2949-9808-49c3-8a0c-f2ce9c300a2a
ms.tgt_platform: multiple
title: Clase TargetForwardingDestination
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TargetForwardingDestination
- TargetForwardingDestination.TargetEndpoint
- TargetForwardingDestination.TargetMac
- TargetForwardingDestination.TargetGuid
- TargetForwardingDestination.CollectorEndpoint
- TargetForwardingDestination.Computer
- TargetForwardingDestination.ForwarderType
- TargetForwardingDestination.Destination
- TargetForwardingDestination.DestinationPattern
- TargetForwardingDestination.Error
- TargetForwardingDestination.ConnectedSince
- TargetForwardingDestination.DisconnectedSince
- TargetForwardingDestination.WmiDateTime
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: 58492b8b334085a6dd03c397558c4f10bc1fa4aff441f5b7bbfc7ba7cf37b0bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589005"
---
# <a name="targetforwardingdestination-class"></a>Clase TargetForwardingDestination

Destinos conocidos que contienen los datos recopilados. Solo está disponible si el recopilador se está ejecutando con el registro de estado habilitado.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Provider("BootEventCollectorWmiProvider"), Dynamic, AMENDMENT]
class TargetForwardingDestination
{
  string   TargetEndpoint;
  string   TargetMac;
  string   TargetGuid;
  string   CollectorEndpoint;
  string   Computer;
  string   ForwarderType;
  string   Destination;
  string   DestinationPattern;
  string   Error;
  DATETIME ConnectedSince;
  DATETIME DisconnectedSince;
  DATETIME WmiDateTime;
};
```

## <a name="members"></a>Miembros

La **clase TargetForwardingDestination** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase TargetForwardingDestination** tiene estas propiedades.

<dl> <dt>

**CollectorEndpoint**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Corregido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Información de host:puerto del punto de conexión en el lado del recopilador.

</dd> <dt>

**Equipo**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Corregido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nombre del equipo de destino, determinado por el recopilador según su configuración.

</dd> <dt>

**ConnectedSince**
</dt> <dd> <dl> <dt>

Tipo de datos: **DATETIME**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Corregido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Marca de tiempo de cuando se estableció la conexión.

</dd> <dt>

**Destino**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Destino de los datos. El significado depende del tipo de reenviador. Puede ser un nombre de archivo o alguna otra identificación.

</dd> <dt>

**DestinationPattern**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Corregido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Patrón utilizado para generar el destino de los datos. El significado depende del tipo y la configuración del reenviador. Para un destino fijo, sería el mismo que el propio destino. Para el destino con rotación de los archivos contendrá los caracteres de patrón que se reemplazarán por el índice real en el destino.

</dd> <dt>

**DisconnectedSince**
</dt> <dd> <dl> <dt>

Tipo de datos: **DATETIME**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Corregido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Marca de tiempo de cuando se ha eliminado la conexión.

</dd> <dt>

**Error**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Corregido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Mensaje de error si se ha encontrado un error. De lo contrario, estará vacío.

</dd> <dt>

**ForwarderType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Tipo del reenviador (por ejemplo, "etl").

</dd> <dt>

**TargetEndpoint**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Corregido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Información del punto de conexión del equipo de destino, en formato legible para el usuario. Esta propiedad tiene formato de *host:* cadena *de* puerto. Por ejemplo, "127.0.0.1:50000".

</dd> <dt>

**TargetGuid**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Corregido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

GUID de SMBIOS del equipo de destino (si se conoce).

</dd> <dt>

**TargetMac**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Corregido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Dirección MAC del equipo de destino (si se conoce).

</dd> <dt>

**WmiDateTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DATETIME**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Corregido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Marca de tiempo de cuando se registró este cambio de estado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                       |
| Espacio de nombres<br/>                | Raíz \\ de Microsoft Windows \\ \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



 

