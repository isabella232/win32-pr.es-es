---
description: Representa un contenedor para las características de un intervalo de frecuencia admitido.
ms.assetid: eb07c10b-8d92-40bb-8a93-ebc5db46cfd3
title: FrequencyRangeDescriptor (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FrequencyRangeDescriptor
- FrequencyRangeDescriptor.Origin
- FrequencyRangeDescriptor.MinVSyncNumerator
- FrequencyRangeDescriptor.MinVSyncDenominator
- FrequencyRangeDescriptor.MaxVSyncNumerator
- FrequencyRangeDescriptor.MaxVSyncDenominator
- FrequencyRangeDescriptor.MinHSyncNumerator
- FrequencyRangeDescriptor.MinHSyncDenominator
- FrequencyRangeDescriptor.MaxHSyncNumerator
- FrequencyRangeDescriptor.MaxHSyncDenominator
- FrequencyRangeDescriptor.ConstraintType
- FrequencyRangeDescriptor.ActiveWidth
- FrequencyRangeDescriptor.ActiveHeight
- FrequencyRangeDescriptor.MaxPixelRate
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 287da7980da8e2837d44852b4cd2ecf2f098604a6478ab6c534104f82fb1fddf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097455"
---
# <a name="frequencyrangedescriptor-class"></a>FrequencyRangeDescriptor (clase)

La clase WMI **FrequencyRangeDescriptor** representa un contenedor para las características de un intervalo de frecuencia admitido. Las instancias de esta clase son elementos de la **matriz MonitorFreqRanges** [**en WmiMonitorListedFrequencyRanges.**](wmimonitorlistedfrequencyranges.md)

## <a name="syntax"></a>Sintaxis

``` syntax
class FrequencyRangeDescriptor
{
  uint8  Origin;
  uint32 MinVSyncNumerator;
  uint32 MinVSyncDenominator;
  uint32 MaxVSyncNumerator;
  uint32 MaxVSyncDenominator;
  uint32 MinHSyncNumerator;
  uint32 MinHSyncDenominator;
  uint32 MaxHSyncNumerator;
  uint32 MaxHSyncDenominator;
  uint32 ConstraintType;
  uint32 ActiveWidth;
  uint32 ActiveHeight;
  uint32 MaxPixelRate;
};
```

## <a name="members"></a>Miembros

La **clase FrequencyRangeDescriptor** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase FrequencyRangeDescriptor** tiene estas propiedades.

<dl> <dt>

**ActiveHeight**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Alto, en píxeles, de la imagen activa.

</dd> <dt>

**ActiveWidth**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ancho, en píxeles, de la imagen activa.

</dd> <dt>

**ConstraintType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de restricción para el intervalo de frecuencia.

</dd> <dt>

**MaxHSyncDenominator**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Denominador de sincronización horizontal máximo.

</dd> <dt>

**MaxHSyncNumerator**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Numerador de sincronización horizontal máximo en kilohercios (KHz).

</dd> <dt>

**MaxPixelRate**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Velocidad máxima de píxeles en Hertz (Hz).

</dd> <dt>

**MaxVSyncDenominator**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Denominador de sincronización vertical máximo.

</dd> <dt>

**MaxVSyncNumerator**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Numerador de sincronización vertical máximo, en Hertz (Hz).

</dd> <dt>

**MinHSyncDenominator**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Denominador de sincronización horizontal mínimo.

</dd> <dt>

**MinHSyncNumerator**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Numerador de sincronización horizontal mínimo en kilohercios (KHz).

</dd> <dt>

**MinVSyncDenominator**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Denominador de sincronización vertical mínimo.

</dd> <dt>

**MinVSyncNumerator**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Numerador de sincronización vertical mínimo, en Hertz (Hz).

</dd> <dt>

**Origen**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Origen.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 




