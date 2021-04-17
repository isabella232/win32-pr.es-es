---
description: Excluye los discos de la operación de AUTOCHK que se ejecutarán en el siguiente reinicio.
ms.assetid: 5df2bc3b-e149-4853-aa02-af4cb8af6da0
ms.tgt_platform: multiple
title: Método ExcludeFromAutochk de la clase Win32_LogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.ExcludeFromAutochk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c41d93111742e975490d97169c7e9147ba5fb1ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659485"
---
# <a name="excludefromautochk-method-of-the-win32_logicaldisk-class"></a>Método ExcludeFromAutochk de la \_ clase Win32 LogicalDisk

El método **ExcludeFromAutochk** excluye los discos de la operación **Autochk** que se va a ejecutar en el siguiente reinicio.

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 ExcludeFromAutochk(
  [in] string LogicalDisk[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*LogicalDisk* \[ de\]
</dt> <dd>

Lista de unidades que deben excluirse de **Autochk** en el siguiente reinicio. La sintaxis de la cadena se compone de la letra de unidad seguida de dos puntos para el disco lógico.

Ejemplo: "C:"

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si no se produce ningún error. Los valores se muestran en la lista siguiente. Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Correcto** (0)
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

Si no se excluye, **Autochk** se realiza en el disco cuando se establece el bit de integridad del disco. Tenga en cuenta que las llamadas para excluir discos no son acumulativas. Si se realiza una llamada para excluir algunos discos, la nueva lista no se agrega a la lista de discos que ya están marcados para su exclusión. La nueva lista de discos sobrescribe la lista anterior. Este método solo es aplicable a las instancias de disco lógico que representan un disco físico en el equipo. No es aplicable a las unidades lógicas asignadas.

## <a name="examples"></a>Ejemplos

El siguiente ejemplo de código de VBScript garantiza que Autochk.exe no se ejecutarán en la unidad C la próxima vez que se reinicie el equipo, incluso si se ha establecido el "bit de integridad" en la unidad C.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk") 
 
errReturn = objDisk.ExcludeFromAutoChk(Array("C:")) 
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
</dt> <dt>

[Clases de hardware de sistema del equipo](computer-system-hardware-classes.md)
</dt> </dl>

 

