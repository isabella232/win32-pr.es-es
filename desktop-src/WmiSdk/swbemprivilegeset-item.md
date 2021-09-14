---
description: El método Item del objeto SWbemPrivilegeSet devuelve un objeto SWbemPrivilege de la colección. El método Item es el método predeterminado de un objeto SWbemPrivilegeSet.
ms.assetid: 93a35e65-99ee-40da-9415-4151ac635091
ms.tgt_platform: multiple
title: Método SWbemPrivilegeSet.Item (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Item
- ISWbemPrivilegeSet.Item
- ISWbemPrivilegeSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 7ea37ae758ec599198fc35a1fd2a4b89ff25a087
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070434"
---
# <a name="swbemprivilegesetitem-method"></a>Método SWbemPrivilegeSet.Item

El **método Item** del objeto [**SWbemPrivilegeSet**](swbemprivilegeset.md) devuelve un objeto [**SWbemPrivilege**](swbemprivilege.md) de la colección. El **método Item** es el método predeterminado de un objeto **SWbemPrivilegeSet.**

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
objPrivilege = .Item( _
  ByVal iPrivilege _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*iPrivilege* 
</dt> <dd>

Necesario. Una de las constantes WMI del [**grupo WbemPrivilegeEnum.**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) Estas constantes son básicamente enteros que representan privilegios específicos. Por ejemplo, para obtener el privilegio que le permite apagar un sistema Windows, use la constante **wbemPrivilegeShutdown** o el equivalente numérico de 23 (0x17).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, se devuelve el objeto [**SWbemPrivilege**](swbemprivilege.md) solicitado.

## <a name="error-codes"></a>Códigos de error

Tras la finalización del **método Item,** el **objeto Err** puede contener uno de los códigos de error de la lista siguiente.

<dl> <dt>

**wbemErrFailed:** 2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrNotFound:** 2147749890 (0x80041002)
</dt> <dd>

El privilegio especificado no existe.

</dd> </dl>

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de código de VBScript se usa **el método Item**


```VB
strComputer ="."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2")
Set colServices = objWMIService.ExecQuery( _
    "Select * from Win32_Service")
For Each objService In colServices
    WScript.Echo objService.Properties_.Item("Caption")
Next
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemPrivilegeSet<br/>                                                     |
| IID<br/>                      | IID \_ ISWbemPrivilegeSet<br/>                                                      |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemPrivilegeSet**](swbemprivilegeset.md)
</dt> <dt>

[Ejecución de operaciones con privilegios](executing-privileged-operations.md)
</dt> <dt>

[**SWbemPrivilege**](swbemprivilege.md)
</dt> </dl>

 

 




