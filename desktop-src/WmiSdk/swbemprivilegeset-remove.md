---
description: El método Remove del objeto SWbemPrivilegeSet elimina un privilegio de la colección.
ms.assetid: 4c0b6d49-262c-4840-955b-35b16b68f29f
ms.tgt_platform: multiple
title: Método SWbemPrivilegeSet.Remove (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Remove
- ISWbemPrivilegeSet.Remove
- ISWbemPrivilegeSet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 825fbdc18537fa73561f8a662ecc0388ab18be0b9bf26ca2cbfeadd7bfb9b469
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732295"
---
# <a name="swbemprivilegesetremove-method"></a>Método SWbemPrivilegeSet.Remove

El **método Remove** del objeto [**SWbemPrivilegeSet**](swbemprivilegeset.md) elimina un privilegio de la colección.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
SWbemPrivilegeSet.Remove( _
  ByVal iPrivilege _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*iPrivilege* 
</dt> <dd>

Obligatorio. Esta es una de las constantes WMI del [**grupo WbemPrivilegeEnum.**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) Estas constantes son básicamente enteros que representan privilegios específicos. Por ejemplo, para quitar el privilegio que le permite apagar un sistema Windows, use la constante **wbemPrivilegeShutdown** o el equivalente numérico de 0x17.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

Tras la finalización del **método Remove,** el **objeto Err** puede contener uno de los códigos de error de la lista siguiente.

<dl> <dt>

**wbemErrFailed:** 2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrNotFound:** 2147749890 (0x80041002)
</dt> <dd>

El privilegio especificado no existe.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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
</dt> </dl>

 

 




