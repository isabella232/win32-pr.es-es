---
description: El historial reciente de cambios en los datos de reenvío para un equipo de destino.
ms.assetid: 621e2734-fc75-4e7a-9fae-de3d1b0272ae
ms.tgt_platform: multiple
title: Clase TargetForwardingHistory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TargetForwardingHistory
- TargetForwardingHistory.TargetEndpoint
- TargetForwardingHistory.TargetMac
- TargetForwardingHistory.TargetGuid
- TargetForwardingHistory.CollectorEndpoint
- TargetForwardingHistory.Computer
- TargetForwardingHistory.ForwarderType
- TargetForwardingHistory.Destination
- TargetForwardingHistory.DestinationPattern
- TargetForwardingHistory.Error
- TargetForwardingHistory.ConnectedSince
- TargetForwardingHistory.DisconnectedSince
- TargetForwardingHistory.WmiDateTime
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: 7fb713f98709f65de5fa32424f8a3484edaac758
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153573"
---
# <a name="targetforwardinghistory-class"></a>Clase TargetForwardingHistory

El historial reciente de cambios en los datos de reenvío para un equipo de destino.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Provider("BootEventCollectorWmiProvider"), Dynamic, AMENDMENT]
class TargetForwardingHistory
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

La clase **TargetForwardingHistory** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **TargetForwardingHistory** tiene estas propiedades.

<dl> <dt>

**CollectorEndpoint**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

La información del punto de conexión del servidor del recopilador. Esta propiedad tiene el formato de cadena *host*:*Puerto* .

</dd> <dt>

**Equipo**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

El nombre de equipo del equipo de destino.

</dd> <dt>

**ConnectedSince**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Marca de tiempo que indica cuándo se estableció la conexión para los datos de reenvío.

</dd> <dt>

**Destino**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

El destino de los datos de reenvío, como un nombre de archivo.

</dd> <dt>

**DestinationPattern**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Formato utilizado para generar el destino de los datos de reenvío.

</dd> <dt>

**DisconnectedSince**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Marca de tiempo que indica cuándo se desconectó la conexión.

</dd> <dt>

**Error**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Un mensaje de error que describe un error encontrado. Esta propiedad está vacía si no se encuentra ningún error.

</dd> <dt>

**ForwarderType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

El tipo de archivo que contiene los datos de reenvío, como ETL.

</dd> <dt>

**TargetEndpoint**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**fijo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

La información del punto de conexión del equipo de destino, en formato legible. Esta propiedad tiene el formato de cadena *host*:*Puerto* . Por ejemplo, "127.0.0.1:50000".

</dd> <dt>

**TargetGuid**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**fijo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

**GUID** de SMBIOS del equipo de destino.

</dd> <dt>

**TargetMac**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**fijo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Dirección MAC del equipo de destino.

</dd> <dt>

**WmiDateTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **fijos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Marca de tiempo de Cuándo se registró este cambio de estado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                       |
| Espacio de nombres<br/>                | Raíz de \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Proveedor WMI del recopilador de eventos de arranque](boot-event-collector-wmi-provider-portal.md)
</dt> </dl>

 

