---
description: El método DeleteAll del objeto SWbemNamedValueSet quita todos los valores con nombre de la colección, con lo que se vacía.
ms.assetid: db5d2e68-028e-4902-ad42-0b46e1a96bcb
ms.tgt_platform: multiple
title: Método SWbemNamedValueSet. DeleteAll (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.DeleteAll
- ISWbemNamedValueSet.DeleteAll
- ISWbemNamedValueSet.DeleteAll
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9df7b08dddf4cf9f1a687a262721452c0780267a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277322"
---
# <a name="swbemnamedvaluesetdeleteall-method"></a>SWbemNamedValueSet. DeleteAll, método

El método **DeleteAll** del objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) quita todos los valores con nombre de la colección, con lo que se vacía.

## <a name="syntax"></a>Sintaxis


```VB
SWbemNamedValueSet.DeleteAll()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

Al completarse el método **DeleteAll** , el objeto **Err** puede contener el código de error siguiente.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Error no especificado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemNamedValueSet<br/>                                                    |
| IID<br/>                      | \_ISWBEMNAMEDVALUESET IID<br/>                                                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SWbemNamedValueSet**](swbemnamedvalueset.md)
</dt> <dt>

[**SWbemNamedValueSet. Remove**](swbemnamedvalueset-remove.md)
</dt> </dl>

 

 




