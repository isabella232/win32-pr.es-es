---
description: Programa Autochk para que se ejecute en la unidad de disco representada por el disco lógico win32 en el siguiente reinicio si se establece \_ el bit desa prueba.
ms.assetid: 34f4c26b-6bfb-45d9-9d6c-0a9b735355f3
ms.tgt_platform: multiple
title: Método ScheduleAutoChk de la Win32_LogicalDisk clase
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
ms.openlocfilehash: 7e4920bdded79a7f63cbe7beaf28a70837ad7a47c2b28a1e37d83208b4f4e6f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588195"
---
# <a name="scheduleautochk-method-of-the-win32_logicaldisk-class"></a>Método ScheduleAutoChk de la clase LogicalDisk de Win32 \_

El método de clase **ScheduleAutoChk** programa la ejecución de Autochk en la unidad de disco representada por el disco lógico [**win32 \_**](win32-logicaldisk.md) en el siguiente reinicio si se establece el bit desa prueba.

En este tema se usa Managed Object Format sintaxis MOF (MOF). Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 ScheduleAutoChk(
  [in] string LogicalDisk[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Disco lógico* \[ En\]
</dt> <dd>

Especifica la lista de unidades que se programan para Autochk en el siguiente reinicio. La sintaxis de cadena consta de la letra de unidad seguida de dos puntos para el disco lógico, por ejemplo: "C:"

> [!Note]  
> Compruebe siempre la validez de las letras de unidad de la matriz *LogicalDisk* cuando los datos proceden de un origen desconocido o de un origen en el que no confíe.

 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si se realiza correctamente y otro valor si se produce cualquier otro error. Los valores se muestran en la lista siguiente. Para obtener códigos de error adicionales, [**vea Wmi Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Sin error** (0)
</dt> <dt>

**Error: unidad remota** (1)
</dt> <dt>

**Error: unidad extraíble** (2)
</dt> <dt>

**Error: unidad no directorio raíz** (3)
</dt> <dt>

**Error: unidad desconocida** (4)
</dt> </dl>

## <a name="remarks"></a>Comentarios

Este método solo es aplicable a las instancias de disco lógico que representan un disco físico en la máquina. Este método no es aplicable a las unidades lógicas asignadas.

## <a name="examples"></a>Ejemplos

La siguiente programación de ejemplos de VBScript y PowerShell Autochk.exe ejecutar en la unidad C la próxima vez que se reinicie el equipo.


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
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Disco lógico \_ win32**](win32-logicaldisk.md)
</dt> </dl>

 

