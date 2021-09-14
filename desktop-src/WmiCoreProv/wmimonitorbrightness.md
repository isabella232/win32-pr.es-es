---
description: Representa los parámetros de brillo de un monitor de equipo.
ms.assetid: 01fa3efc-2a1d-4405-989f-2c180842c6b9
title: Clase WmiMonitorBrightness
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightness
- WmiMonitorBrightness.Active
- WmiMonitorBrightness.CurrentBrightness
- WmiMonitorBrightness.InstanceName
- WmiMonitorBrightness.Level
- WmiMonitorBrightness.Levels
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: b8d16c8dc20291a03fb205441c8826c85125970c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073090"
---
# <a name="wmimonitorbrightness-class"></a>Clase WmiMonitorBrightness

La **clase WMI WmiMonitorBrightness** representa los parámetros de brillo de un monitor de equipo.

## <a name="syntax"></a>Sintaxis

``` syntax
class WmiMonitorBrightness : MSMonitorClass
{
  boolean Active;
  uint8   CurrentBrightness;
          InstanceName;
  uint8   Level[];
  uint32  Levels;
};
```

## <a name="members"></a>Members

La **clase WmiMonitorBrightness** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase WmiMonitorBrightness** tiene estas propiedades.

<dl> <dt>

**Activo**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el monitor de destino está activo.

</dd> <dt>

**CurrentBrightness**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Brillo actual. Este valor debe ser un valor tomado de *Levels*.

Ejemplo: 100

</dd> <dt>

InstanceName
</dt> <dd> <dl> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: clave
</dt> </dl>

Nombre de la instancia de monitor específica.

</dd> <dt>

**Level**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz que contiene los posibles niveles de brillo.

Ejemplo: \[ 0, 1, 2, ..., 100 \] .

</dd> <dt>

**Niveles**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número total de niveles de brillo que admite el monitor, como se describe en *Nivel*.

Ejemplo: 101

</dd> </dl>

## <a name="examples"></a>Ejemplos

Para obtener más información y ejemplos de código sobre el uso de esta clase en PowerShell, vea [Usar PowerShell para](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx)informar y establecer el brillo del monitor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Espacio de nombres<br/>                | Wmi \\ raíz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




