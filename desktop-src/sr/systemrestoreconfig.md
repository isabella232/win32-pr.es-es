---
title: Clase SystemRestoreConfig
description: Proporciona propiedades para controlar la frecuencia de creación de puntos de restauración programados y la cantidad de espacio en disco consumido en cada unidad.
ms.assetid: ed09e03f-8cc1-4923-8f39-bbe7d9a19b44
keywords:
- Restauración del sistema de la clase SystemRestoreConfig
- SystemRestoreConfig (clase) restauración del sistema, descrito
topic_type:
- apiref
api_name:
- SystemRestoreConfig
- SystemRestoreConfig.RPSessionInterval
- SystemRestoreConfig.RPGlobalInterval
- SystemRestoreConfig.RPLifeInterval
- SystemRestoreConfig.DiskPercent
api_location:
- Root\Default
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58ded8a17cc4800e1aa2917ba7750c6c69434916
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422406"
---
# <a name="systemrestoreconfig-class"></a>Clase SystemRestoreConfig

Proporciona propiedades para controlar la frecuencia de creación de puntos de restauración programados y la cantidad de espacio en disco consumido en cada unidad.

## <a name="syntax"></a>Sintaxis

``` syntax
class SystemRestoreConfig
{
  uint32 RPSessionInterval;
  uint32 RPGlobalInterval;
  uint32 RPLifeInterval;
  uint32 DiskPercent;
};
```

## <a name="members"></a>Miembros

La clase **SystemRestoreConfig** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **SystemRestoreConfig** tiene estas propiedades.

<dl> <dt>

**DiskPercent**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La cantidad máxima de espacio en disco en cada unidad que puede usar Restaurar sistema. Este valor se especifica como un porcentaje del espacio total de la unidad. El valor predeterminado es 12 por ciento.

**Windows Vista:** Recibe un valor de la Servicio de instantáneas de volumen (VSS). Esta es la cantidad máxima de espacio en disco en cada unidad que puede usar Restaurar sistema. El valor predeterminado es el 15 por ciento del espacio total de la unidad o el 30 por ciento del espacio libre disponible, lo que sea menor.

</dd> <dt>

**RPGlobalInterval**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El intervalo de tiempo absoluto en el que se crean los puntos de control del sistema programados, en segundos. El valor predeterminado es 86.400 (24 horas).

**Windows Vista:** Recibe un valor del programador de tareas para restaurar el sistema. Cero si la tarea está deshabilitada.

</dd> <dt>

**RPLifeInterval**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Intervalo de tiempo para el que se conservan los puntos de restauración, en segundos. Cuando un punto de restauración es más antiguo que este intervalo especificado, se elimina. El límite de antigüedad predeterminado es de 90 días.

**Windows Vista:** Recibe un valor de **UINTMAX**.

</dd> <dt>

**RPSessionInterval**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El intervalo de tiempo en que se crean los puntos de control del sistema programados durante la sesión, en segundos. El valor predeterminado es cero, lo que indica que la característica está desactivada.

**Windows Vista:** Recibe cero si está deshabilitada la restauración del sistema.

</dd> </dl>

## <a name="examples"></a>Ejemplos

No se admite el siguiente código de ejemplo. Use la herramienta de línea de comandos Vssadmin.exe para cambiar el tamaño del espacio de la unidad reservada.

**Windows XP:** Este ejemplo es compatible.


```VB
'The SystemRestoreConfig class provides properties for controlling the frequency of 
'scheduled restore point creation and the amount of disk space consumed on each drive.

Set Args = wscript.Arguments
Set regSR = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestoreConfig='SR'")

If Args.Count() = 0 Then
    Wscript.Echo "Usage: RegSR [RP{Session|Global|Life}Interval[=value]] [DiskPercent[=value]]"
Else    
For i = 0 To Args.Count() - 1
    Myarg = Args.Item(i)
    Pos = InStr(Myarg, "=")
    If Pos <> 0 Then
        Myarray = Split(Myarg, "=", -1, 1)
        myoption = Myarray(0)
        value = Myarray(1)
    Else 
        myoption = Myarg
    End If    
    If myoption = "RPSessionInterval" Then
        If Pos = 0 Then
            Wscript.Echo "RPSessionInterval = " & regSR.RPSessionInterval
        Else    
            regSR.RPSessionInterval = value
            regSR.Put_
        End If
    ElseIf myoption = "RPGlobalInterval" Then
        If Pos = 0 Then
            Wscript.Echo "RPGlobalInterval = " & regSR.RPGlobalInterval
        Else    
            regSR.RPGlobalInterval = value
            regSR.Put_
        End If
    ElseIf myoption = "RPLifeInterval" Then
        If Pos = 0 Then
            Wscript.Echo "RPLifeInterval = " & regSR.RPLifeInterval
        Else    
            regSR.RPLifeInterval = value
            regSR.Put_
        End If
    ElseIf myoption = "DiskPercent" Then
        If Pos = 0 Then
            Wscript.Echo "DiskPercent = " & regSR.DiskPercent
        Else    
            regSR.DiskPercent = value
            regSR.Put_
        End If
    End If
Next
End If
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                         |
| Espacio de nombres<br/>                | Raíz \\ predeterminada<br/>                                                          |
| MOF<br/>                      | <dl> <dt>MOF</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Puntos de restauración](restore-points.md)
</dt> <dt>

[Instrumental de administración de Windows](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

