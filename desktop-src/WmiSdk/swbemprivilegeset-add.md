---
description: El método Add del objeto SWbemPrivilegeSet agrega un objeto SWbemPrivilege a la colección SWbemPrivilegeSet. Si ya existe un privilegio con el mismo nombre en la colección, se reemplaza.
ms.assetid: 7d44193f-60e1-4e83-8640-31d8df509d98
ms.tgt_platform: multiple
title: Método SWbemPrivilegeSet.Add (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Add
- ISWbemPrivilegeSet.Add
- ISWbemPrivilegeSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 54b45779f4954f1cee454b5cf171e374e215555902e3389c7c47f5a59bc989eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954884"
---
# <a name="swbemprivilegesetadd-method"></a>Método SWbemPrivilegeSet.Add

El **método Add** del objeto [**SWbemPrivilegeSet**](swbemprivilegeset.md) agrega un objeto [**SWbemPrivilege**](swbemprivilege.md) a la **colección SWbemPrivilegeSet.** Si ya existe un privilegio con el mismo nombre en la colección, se reemplaza.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
objPrivilege = .Add( _
  ByVal iPrivilege, _
  [ ByVal bIsEnabled ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*iPrivilege* 
</dt> <dd>

Obligatorio. Una de las constantes WMI del [**grupo WbemPrivilegeEnum.**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) Estas constantes son básicamente enteros que representan privilegios específicos. Por ejemplo, para agregar el privilegio que le permite apagar un sistema informático, use la **constante wbemPrivilegeShutdown.** En un script, debe usar el equivalente numérico de 23 (0x17). Para obtener una lista completa de estas constantes y las cadenas de privilegios asociadas, vea [**Constantes de privilegios**](privilege-constants.md).

</dd> <dt>

*bIsEnabled* \[ Opcional\]
</dt> <dd>

Valor booleano que habilita o deshabilita este privilegio. El valor predeterminado es **TRUE.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, el método devuelve [**un objeto SWbemPrivilege**](swbemprivilege.md) que representa el nuevo privilegio. De lo contrario, se devuelve un objeto NULL.

## <a name="error-codes"></a>Códigos de error

Tras la finalización del **método Add,** el **objeto Err** puede contener el código de error en la lista siguiente.

<dl> <dt>

**wbemErrFailed:** 2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> </dl>

## <a name="examples"></a>Ejemplos

En el tema [**SWbemPrivilegeSet**](swbemprivilegeset.md) se describe un ejemplo de código con este método.

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

[Ejecución de operaciones con privilegios](executing-privileged-operations.md)
</dt> <dt>

[Ejecución de operaciones con privilegios mediante VBScript](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[**SWbemPrivilegeSet.AddAsString**](swbemprivilegeset-addasstring.md)
</dt> <dt>

[**SWbemPrivilegeSet.Remove**](swbemprivilegeset-remove.md)
</dt> <dt>

[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[**Constantes de privilegios**](privilege-constants.md)
</dt> </dl>

 

 




