---
description: El método Item del objeto SWbemMethodSet devuelve un objeto SWbemMethod con nombre de la colección.
ms.assetid: 4c1bbecc-b38b-4869-9c8c-b9321536b23e
ms.tgt_platform: multiple
title: Método SWbemMethodSet.Item (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethodSet.Item
- ISWbemMethodSet.Item
- ISWbemMethodSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: fd78277be4611507a7f7a488dae0d4edda832afeac8c4a947d4c56277d9af397
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679455"
---
# <a name="swbemmethodsetitem-method"></a>Método SWbemMethodSet.Item

El **método Item** del objeto [**SWbemMethodSet**](swbemmethodset.md) devuelve un objeto [**SWbemMethod**](swbemmethod.md) con nombre de la colección.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
objMethod = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*strName* \[ En\]
</dt> <dd>

Obligatorio. Nombre del método que se recuperará.

</dd> <dt>

*iFlags* \[ in, opcional\]
</dt> <dd>

Reservado. El valor predeterminado es 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, devuelve [**el objeto SWbemMethod**](swbemmethod.md) solicitado.

## <a name="error-codes"></a>Códigos de error

Tras la finalización del **método Item,** el **objeto Err** puede contener uno de los códigos de error de la lista siguiente.

<dl> <dt>

**wbemErrInvalidParameter:** 2147749896 (0x80041008)
</dt> <dd>

El *parámetro iFlags* no era válido.

</dd> <dt>

**wbemErrFailed** : 2147749894
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrNotFound** : 2147749890 (0x80041002)
</dt> <dd>

El método especificado no existe.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemMethodSet<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemMethodSet<br/>                                                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemMethodSet**](swbemmethodset.md)
</dt> <dt>

[**SWbemMethod**](swbemmethod.md)
</dt> </dl>

 

 




