---
title: EM_GETCTFMODEBIAS mensaje (Richedit.h)
description: Obtiene los valores Text Services Framework de sesgo del modo de actualización para un control Microsoft Rich Edit.
ms.assetid: 2421d37d-169d-480f-a5f7-4c6033ca6c1a
keywords:
- EM_GETCTFMODEBIAS controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_GETCTFMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109d5eabbddca1c13fefae99c29d8c550fbd274e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062197"
---
# <a name="em_getctfmodebias-message"></a>Mensaje \_ EM GETCTFMODEBIAS

Obtiene los valores Text Services Framework de sesgo del modo de actualización para un control Microsoft Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Valor de sesgo Text Services Framework modo actual.

## <a name="remarks"></a>Observaciones

Para obtener el sesgo del modo IME, llame a [**EM \_ GETIMEMODEBIAS**](em-getimemodebias.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de escritorio de SP1 \[\]<br/>                                  |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ SETCTFMODEBIAS**](em-setctfmodebias.md)
</dt> <dt>

[**EM \_ GETIMEMODEBIAS**](em-getimemodebias.md)
</dt> </dl>

 

 





