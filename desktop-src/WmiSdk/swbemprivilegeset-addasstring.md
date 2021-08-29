---
description: Puede usar el método AddAsString del objeto SWbemPrivilegeSet para agregar un privilegio a una colección SWbemPrivilegeSet mediante una cadena de privilegios.
ms.assetid: 729ed4e3-2c5c-4bb4-acc6-cf9ad0d5eaf1
ms.tgt_platform: multiple
title: Método SWbemPrivilegeSet.AddAsString (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.AddAsString
- ISWbemPrivilegeSet.AddAsString
- ISWbemPrivilegeSet.AddAsString
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f474f1650cae338a7790ac6d5cb66a248be6c6658d5f2577efcc56870000cc66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860065"
---
# <a name="swbemprivilegesetaddasstring-method"></a>Método SWbemPrivilegeSet.AddAsString

Puede usar el **método AddAsString** del objeto [**SWbemPrivilegeSet**](swbemprivilegeset.md) para agregar un privilegio a una **colección SWbemPrivilegeSet** mediante una cadena de privilegios. Use este método para agregar un privilegio o para habilitar un privilegio para [**objetos SWbemSecurity.**](swbemsecurity.md) Vea [Ejecutar operaciones con privilegios mediante VBScript.](executing-privileged-operations-using-vbscript.md)

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
objPrivilege = .AddAsString( _
  ByVal strPrivilege, _
  [ ByVal bIsEnabled ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*strPrivilege* 
</dt> <dd>

Obligatorio. Una de las cadenas de privilegios. Para obtener una lista completa de estas cadenas y las constantes WMI asociadas, vea [**Constantes de privilegios**](privilege-constants.md). Cada cadena de privilegios representa un privilegio específico. Por ejemplo, para agregar el privilegio que usa para apagar un sistema informático, use la **cadena SeShutdownPrivilege.**

</dd> <dt>

*bIsEnabled* \[ Opcional\]
</dt> <dd>

Valor booleano que habilita o deshabilita este privilegio. El valor predeterminado es **True**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, este método devuelve [**un objeto SWbemPrivilege**](swbemprivilege.md) que representa el nuevo privilegio. De lo contrario, se devuelve un objeto NULL.

## <a name="error-codes"></a>Códigos de error

Tras la finalización del **método AddAsString,** el **objeto Err** puede contener el código de error en la lista siguiente.

<dl> <dt>

**wbemErrFailed:** 2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> </dl>

## <a name="examples"></a>Ejemplos

En el ejemplo de código de VBScript siguiente se crea un nuevo puerto para un servidor de impresión mediante [**\_ Win32 TCPIPPrinterPort**](/windows/desktop/CIMWin32Prov/win32-tcpipprinterport). **SeLoadDriverPrivilege** es necesario para esta operación. Consulte [Ejecución de operaciones con privilegios.](executing-privileged-operations.md)


```VB
Set objWMIService = GetObject("Winmgmts:")
objWMIService.Security_.Privileges. _
    AddAsString "SeLoadDriverPrivilege", True
Set objNewPort = objWMIService.Get _
    ("Win32_TCPIPPrinterPort").SpawnInstance_
objNewPort.Name = "IP_111.222.111.11"
objNewPort.Protocol = 1
objNewPort.HostAddress = "111.222.111.11"
objNewPort.PortNumber = "9999"
objNewPort.SNMPEnabled = False
objNewPort.Put_
```



También se describe un ejemplo de código con este método en el [**tema SWbemPrivilegeSet.**](swbemprivilegeset.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemPrivilegeSet<br/>                                                     |
| IID<br/>                      | IID \_ ISWbemPrivilegeSet<br/>                                                      |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemPrivilegeSet**](swbemprivilegeset.md)
</dt> <dt>

[**SWbemPrivilegeSet.Add**](swbemprivilegeset-add.md)
</dt> <dt>

[**SWbemPrivilegeSet.Remove**](swbemprivilegeset-remove.md)
</dt> <dt>

[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[**Constantes de privilegios**](privilege-constants.md)
</dt> <dt>

[Ejecución de operaciones con privilegios](executing-privileged-operations.md)
</dt> <dt>

[Ejecución de operaciones con privilegios mediante VBScript](executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

