---
title: Clase SystemRestoreConfig
description: Proporciona propiedades para controlar la frecuencia de creación del punto de restauración programado y la cantidad de espacio en disco consumido en cada unidad.
ms.assetid: ed09e03f-8cc1-4923-8f39-bbe7d9a19b44
keywords:
- Clase SystemRestoreConfig Restaurar sistema
- Clase SystemRestoreConfig Restaurar sistema , descrito
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247922"
---
# <a name="systemrestoreconfig-class"></a>Clase SystemRestoreConfig

Proporciona propiedades para controlar la frecuencia de creación del punto de restauración programado y la cantidad de espacio en disco consumido en cada unidad.

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

## <a name="members"></a>Members

La **clase SystemRestoreConfig** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase SystemRestoreConfig** tiene estas propiedades.

<dl> <dt>

**DiskPercent**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cantidad máxima de espacio en disco en cada unidad que puede usar Restaurar sistema. Este valor se especifica como un porcentaje del espacio total de unidad. El valor predeterminado es 12 por ciento.

**Windows Vista:** Recibe un valor de la Servicio de instantáneas de volumen (VSS). Se trata de la cantidad máxima de espacio en disco en cada unidad que puede usar Restaurar sistema. El valor predeterminado es el 15 % del espacio total de unidad o el 30 % del espacio disponible, lo que sea menor.

</dd> <dt>

**RPGlobalInterval**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Intervalo de tiempo absoluto en el que se crean los puntos de control del sistema programados, en segundos. El valor predeterminado es 86 400 (24 horas).

**Windows Vista:** Recibe un valor del programador de tareas para Restaurar sistema. Cero si la tarea está deshabilitada.

</dd> <dt>

**RPLifeInterval**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Intervalo de tiempo durante el que se conservan los puntos de restauración, en segundos. Cuando un punto de restauración es anterior a este intervalo especificado, se elimina. El límite de antigüedad predeterminado es de 90 días.

**Windows Vista:** Recibe un valor de **UINTMAX.**

</dd> <dt>

**RPSessionInterval**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Intervalo de tiempo en el que se crean puntos de control programados del sistema durante la sesión, en segundos. El valor predeterminado es cero, lo que indica que la característica está desactivada.

**Windows Vista:** Recibe cero si Restaurar sistema está deshabilitado.

</dd> </dl>

## <a name="examples"></a>Ejemplos

No se admite el código de ejemplo siguiente. Use la herramienta de línea de Vssadmin.exe para cambiar el tamaño del espacio de unidad reservado.

**Windows XP:** Se admite este ejemplo.


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
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                         |
| Espacio de nombres<br/>                | Raíz \\ predeterminada<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Sr.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Puntos de restauración](restore-points.md)
</dt> <dt>

[Instrumental de administración de Windows](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

