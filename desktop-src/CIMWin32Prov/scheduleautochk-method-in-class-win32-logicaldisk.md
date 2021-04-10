---
description: Programa el Autochk para que se ejecute en la unidad de disco representada por el LogicalDisk de Win32 \_ en el siguiente reinicio si se ha establecido el bit de integridad.
ms.assetid: 34f4c26b-6bfb-45d9-9d6c-0a9b735355f3
ms.tgt_platform: multiple
title: Método ScheduleAutoChk de la clase Win32_LogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.ScheduleAutoChk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2707810d919c119aff35f2313e9aa5218f7948f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998191"
---
# <a name="scheduleautochk-method-of-the-win32_logicaldisk-class"></a>Método ScheduleAutoChk de la \_ clase Win32 LogicalDisk

El método de clase **ScheduleAutoChk** programa el Autochk para que se ejecute en la unidad de disco representada por el [**\_ LogicalDisk de Win32**](win32-logicaldisk.md) en el siguiente reinicio si se ha establecido el bit de integridad.

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 ScheduleAutoChk(
  [in] string LogicalDisk[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*LogicalDisk* \[ de\]
</dt> <dd>

Especifica la lista de unidades que se van a programar para Autochk en el siguiente reinicio. La sintaxis de la cadena se compone de la letra de unidad seguida de dos puntos para el disco lógico, por ejemplo: "C:"

> [!Note]  
> Compruebe siempre la validez de las letras de unidad de la matriz *LogicalDisk* cuando los datos proceden de un origen desconocido o de un origen que no es de confianza.

 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si es correcto y otro valor si se produce algún otro error. Los valores se muestran en la lista siguiente. Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Sin errores** (0)
</dt> <dt>

**Error: unidad remota** (1)
</dt> <dt>

**Error: unidad extraíble** (2)
</dt> <dt>

**Error: la unidad no es el directorio raíz** (3)
</dt> <dt>

**Error: unidad desconocida** (4)
</dt> </dl>

## <a name="remarks"></a>Observaciones

Este método solo es aplicable a las instancias de disco lógico que representan un disco físico en el equipo. Este método no es aplicable a las unidades lógicas asignadas.

## <a name="examples"></a>Ejemplos

Los siguientes ejemplos de VBScript y PowerShell programan Autochk.exe ejecutarse en la unidad C la próxima vez que se reinicie el equipo.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk") 
 
errReturn = objDisk.ScheduleAutoChk(Array("C:")) 
```


```PowerShell

Invoke-WmiMethod -path win32_logicaldisk -Name ScheduleAutoChk -ArgumentList @(&quot;C:&quot;)
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LogicalDisk de Win32 \_**](win32-logicaldisk.md)
</dt> </dl>

 

