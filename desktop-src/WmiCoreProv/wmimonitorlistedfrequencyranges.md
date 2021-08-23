---
description: Enumera los intervalos de frecuencia admitidos por el monitor.
ms.assetid: e4713650-5f8c-4808-8b4f-1d29c54ab4e3
title: Clase WmiMonitorListedFrequencyRanges
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorListedFrequencyRanges
- WmiMonitorListedFrequencyRanges.Active
- WmiMonitorListedFrequencyRanges.InstanceName
- WmiMonitorListedFrequencyRanges.NumOfMonitorFreqRanges
- WmiMonitorListedFrequencyRanges.MonitorFreqRanges
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 41b49c293d5661d523138b01c093fce627e5bedf3d1e783dccb8248edf88546c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051143"
---
# <a name="wmimonitorlistedfrequencyranges-class"></a>Clase WmiMonitorListedFrequencyRanges

La clase WMI **WmiMonitorListedFrequencyRanges** enumera los intervalos de frecuencia admitidos por el monitor. Estos intervalos se encuentran en el bloque Definición de entrada de vídeo de Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) o en el archivo INF de Windows que contiene los datos del controlador de dispositivo.

## <a name="syntax"></a>Sintaxis

``` syntax
class WmiMonitorListedFrequencyRanges : MSMonitorClass
{
  boolean                  Active;
  string                   InstanceName;
  uint16                   NumOfMonitorFreqRanges;
  FrequencyRangeDescriptor MonitorFreqRanges[];
};
```

## <a name="members"></a>Miembros

La **clase WmiMonitorListedFrequencyRanges** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase WmiMonitorListedFrequencyRanges** tiene estas propiedades.

<dl> <dt>

**Activo**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el monitor activo.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Clave**
</dt> </dl>

Nombre de la instancia de monitor específica.

</dd> <dt>

**MonitorFreqRanges**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz FrequencyRangeDescriptor**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Lista de intervalos de frecuencia de supervisión representados por instancias de la [**clase FrequencyRangeDescriptor.**](frequencyrangedescriptor.md)

</dd> <dt>

**NumOfMonitorFreqRanges**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de intervalos de frecuencia de supervisión admitidos enumerados.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Espacio de nombres<br/>                | Wmi \\ raíz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




