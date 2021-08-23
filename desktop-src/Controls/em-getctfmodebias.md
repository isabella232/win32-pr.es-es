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
ms.openlocfilehash: 60d6e030e3080ec9bf3d801583b9ade182483ba8560b3eccb2fb9813be7d39cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019753"
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

## <a name="remarks"></a>Comentarios

Para obtener el sesgo del modo IME, llame a [**EM \_ GETIMEMODEBIAS**](em-getimemodebias.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de escritorio de SP1 \[\]<br/>                                  |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ SETCTFMODEBIAS**](em-setctfmodebias.md)
</dt> <dt>

[**EM \_ GETIMEMODEBIAS**](em-getimemodebias.md)
</dt> </dl>

 

 





