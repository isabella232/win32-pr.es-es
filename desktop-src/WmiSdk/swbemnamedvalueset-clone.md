---
description: El método Clone del objeto SWbemNamedValueSet devuelve un nuevo objeto que es un clon de la colección actual.
ms.assetid: 0e7fab2e-8175-45e5-aa70-1109502e2b3f
ms.tgt_platform: multiple
title: Método SWbemNamedValueSet.Clone (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Clone
- ISWbemNamedValueSet.Clone
- ISWbemNamedValueSet.Clone
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 17678d36a553c84c008f606c647d7ff1fa9dfadc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967095"
---
# <a name="swbemnamedvaluesetclone-method"></a>Método SWbemNamedValueSet.Clone

El **método Clone** del objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) devuelve un nuevo objeto que es un clon de la colección actual.

Para obtener una explicación de esta sintaxis, vea [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxis


```VB
objwbemNamedValueSet = .Clone( _
)
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, se devuelve un nuevo objeto [**SWbemNamedValueSet.**](swbemnamedvalueset.md)

## <a name="error-codes"></a>Códigos de error

Tras la finalización del **método Clone,** el **objeto Err** puede contener uno de los códigos de error siguientes.

<dl> <dt>

**wbemErrFailed:** 2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> <dt>

**wbemErrOutOfMemory:** 2147749894 (0x80041006)
</dt> <dd>

No hay suficiente memoria para clonar el objeto.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Use este método para duplicar una [**colección SWbemNamedValueSet.**](swbemnamedvalueset.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemNamedValueSet<br/>                                                    |
| IID<br/>                      | IID \_ ISWbemNamedValueSet<br/>                                                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SWbemNamedValueSet**](swbemnamedvalueset.md)
</dt> </dl>

 

 




