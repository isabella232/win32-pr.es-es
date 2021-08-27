---
title: TBM_GETSELEND mensaje (Commctrl.h)
description: Recupera la posición final del intervalo de selección actual en una barra de seguimiento.
ms.assetid: e365dd4d-eb49-4107-b6d4-cdb558d27fdb
keywords:
- TBM_GETSELEND controles de Windows mensaje
topic_type:
- apiref
api_name:
- TBM_GETSELEND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff24c6b8f22aba0eb8f8f3a52d7de2bc812936525a7754bb1fa0afa4054524e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046435"
---
# <a name="tbm_getselend-message"></a>Mensaje \_ GETSELEND de TBM

Recupera la posición final del intervalo de selección actual en una barra de seguimiento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 32 bits que especifica la posición final del intervalo de selección actual.

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

[**TBM \_ GETSELSTART**](tbm-getselstart.md)
</dt> <dt>

[**TBM \_ SETSEL**](tbm-setsel.md)
</dt> <dt>

[**TBM \_ SETSELEND**](tbm-setselend.md)
</dt> <dt>

[**TBM \_ SETSELSTART**](tbm-setselstart.md)
</dt> </dl>

 

 





