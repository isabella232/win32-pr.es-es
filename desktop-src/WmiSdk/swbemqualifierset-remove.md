---
description: El método Remove del objeto SWbemQualifierSet elimina un calificador con nombre de la colección.
ms.assetid: 7d386858-efd1-42e6-9176-9cb4bcfc77d0
ms.tgt_platform: multiple
title: Método SWbemQualifierSet. Remove (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Remove
- ISWbemQualifierSet.Remove
- ISWbemQualifierSet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 39c95f268328bc0cad3f3c0874b633fc36c4f5b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544654"
---
# <a name="swbemqualifiersetremove-method"></a>SWbemQualifierSet. Remove (método)

El método **Remove** del objeto [**SWbemQualifierSet**](swbemqualifierset.md) elimina un calificador con nombre de la colección.

Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
SWbemQualifierSet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*strName* \[ de\]
</dt> <dd>

Obligatorio. Nombre del calificador que se va a quitar.

</dd> <dt>

*iFlags* \[ en, opcional\]
</dt> <dd>

Reservado. El valor predeterminado es 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

Después de completar el método **Remove** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.

<dl> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

El parámetro *iFlags* no era válido.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

El calificador especificado no existe.

</dd> <dt>

**wbemErrInvalidOperation** -2147749910 (0x80041016)
</dt> <dd>

Quitar este calificador no es válido.

</dd> </dl>

## <a name="remarks"></a>Observaciones

No se puede recorrer en iteración una colección mientras se quitan elementos porque cuando se quita un elemento de una colección, el puntero de la colección se mueve al siguiente elemento. Para obtener más información, vea [obtener acceso a una colección](accessing-a-collection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemQualifierSet<br/>                                                     |
| IID<br/>                      | \_ISWBEMQUALIFIERSET IID<br/>                                                      |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemQualifierSet**](swbemqualifierset.md)
</dt> <dt>

[**SWbemQualifierSet. Add**](swbemqualifierset-add.md)
</dt> </dl>

 

 




