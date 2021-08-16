---
description: El método Item del objeto SWbemQualifierSet devuelve un objeto SWbemQualifier con nombre de la colección. Este es el método predeterminado de este objeto .
ms.assetid: 5ed3a336-c06f-446d-85d4-243daddc82a5
ms.tgt_platform: multiple
title: Método SWbemQualifierSet.Item (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Item
- ISWbemQualifierSet.Item
- ISWbemQualifierSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 99b735f52ac4d311af6e35f7e214322c55345e4c029e73a342baa52dfa72de6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312996"
---
# <a name="swbemqualifiersetitem-method"></a>Método SWbemQualifierSet.Item

El **método Item** del objeto [**SWbemQualifierSet**](swbemqualifierset.md) devuelve un objeto [**SWbemQualifier**](swbemqualifier.md) con nombre de la colección. Este es el método predeterminado de este objeto .

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
objQualifier = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*strName* \[ En\]
</dt> <dd>

Obligatorio. Nombre del calificador que se recuperará.

</dd> <dt>

*iFlags* \[ in, opcional\]
</dt> <dd>

Reservado. El valor predeterminado es 0 (cero).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, se devuelve el objeto [**SWbemQualifier**](swbemqualifier.md) solicitado.

## <a name="error-codes"></a>Códigos de error

Después de completar el **método Item,** el **objeto Err** puede contener uno de los códigos de error de la lista siguiente.

<dl> <dt>

**wbemErrInvalidParameter:** 2147749896 (0x80041008)
</dt> <dd>

El *parámetro iFlags* no era válido.

</dd> <dt>

**wbemErrFailed:** 2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrNotFound** : 2147749890 (0x80041002)
</dt> <dd>

El calificador especificado no existe.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemQualifierSet<br/>                                                     |
| IID<br/>                      | IID \_ ISWbemQualifierSet<br/>                                                      |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SWbemQualifierSet**](swbemqualifierset.md)
</dt> <dt>

[**SWbemQualifier**](swbemqualifier.md)
</dt> </dl>

 

 




