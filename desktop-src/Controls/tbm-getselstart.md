---
title: TBM_GETSELSTART mensaje (Commctrl.h)
description: Recupera la posición inicial del intervalo de selección actual en una barra de seguimiento.
ms.assetid: 0000df2a-c40d-40c2-b120-e5d4fe6c5016
keywords:
- TBM_GETSELSTART controles de Windows mensaje
topic_type:
- apiref
api_name:
- TBM_GETSELSTART
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a654bfcf8756bee5b39ec9fc97b82ffe84e8e48ba39f4ca2f9fab732d0d1962e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046425"
---
# <a name="tbm_getselstart-message"></a>Mensaje \_ GETSELSTART de TBM

Recupera la posición inicial del intervalo de selección actual en una barra de seguimiento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 32 bits que especifica la posición inicial del intervalo de selección actual.

## <a name="remarks"></a>Comentarios

Una barra de seguimiento solo puede tener un intervalo de selección si especificó el estilo [**\_ ENABLESELRANGE**](trackbar-control-styles.md) de TBS cuando lo creó.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**TBM \_ GETSELEND**](tbm-getselend.md)
</dt> <dt>

[**TBM \_ SETSEL**](tbm-setsel.md)
</dt> <dt>

[**TBM \_ SETSELEND**](tbm-setselend.md)
</dt> <dt>

[**TBM \_ SETSELSTART**](tbm-setselstart.md)
</dt> </dl>

 

 





