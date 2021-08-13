---
description: Excluye los discos de la operación autochk que se ejecutará en el siguiente reinicio.
ms.assetid: 5df2bc3b-e149-4853-aa02-af4cb8af6da0
ms.tgt_platform: multiple
title: Método ExcludeFromAutochk de la Win32_LogicalDisk clase
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
ms.openlocfilehash: a37171c594cb3a51b131220bb604234bcae108fa025ea6343da99fdc998a7dc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118676133"
---
# <a name="excludefromautochk-method-of-the-win32_logicaldisk-class"></a>Método ExcludeFromAutochk de la clase LogicalDisk de Win32 \_

El **método ExcludeFromAutochk** excluye los discos de la **operación autochk** que se ejecutará en el siguiente reinicio.

En este tema se Managed Object Format sintaxis MOF . Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 ExcludeFromAutochk(
  [in] string LogicalDisk[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Disco lógico* \[ En\]
</dt> <dd>

Lista de unidades que se deben excluir de **autochk** en el siguiente reinicio. La sintaxis de cadena consta de la letra de unidad seguida de dos puntos para el disco lógico.

Ejemplo: "C:"

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) cuando no se produce ningún error. Los valores se enumeran en la lista siguiente. Para obtener códigos de error adicionales, [**vea Constantes de error WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Correcto** (0)
</dt> <dt>

**Error: unidad remota** (1)
</dt> <dt>

**Error: unidad extraíble** (2)
</dt> <dt>

**Error: unidad no directorio raíz** (3)
</dt> <dt>

**Error: unidad desconocida** (4)
</dt> </dl>

## <a name="remarks"></a>Observaciones

Si no se excluye, **la función autochk** se realiza en el disco cuando se establece el bit desatensado para el disco. Tenga en cuenta que las llamadas para excluir discos no son acumulativas. Si se realiza una llamada para excluir algunos discos, la nueva lista no se agrega a la lista de discos que ya están marcados para la exclusión. La nueva lista de discos sobrescribe la lista anterior. Este método solo es aplicable a las instancias de disco lógico que representan un disco físico en la máquina. No es aplicable a las unidades lógicas asignadas.

## <a name="examples"></a>Ejemplos

El siguiente ejemplo de código VBScript garantiza que Autochk.exe se ejecute en la unidad C la próxima vez que se reinicie el equipo, incluso si el "bit sucio" se ha establecido en la unidad C.


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
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Disco lógico \_ win32**](win32-logicaldisk.md)
</dt> <dt>

[Clases de hardware del sistema de equipo](computer-system-hardware-classes.md)
</dt> </dl>

 

