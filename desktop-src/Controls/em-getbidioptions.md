---
title: EM_GETBIDIOPTIONS mensaje (Richedit.h)
description: Indica el estado actual de las opciones bidireccionales en el control rich edit.
ms.assetid: 055581c0-ae59-4601-a3e9-416705af429a
keywords:
- EM_GETBIDIOPTIONS controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_GETBIDIOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90b377e0fd3a439737fea9efbc403d2ccc64d6cf78eab1c7e31feeffd6c4b0f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019913"
---
# <a name="em_getbidioptions-message"></a>Mensaje \_ EM GETBIDIOPTIONS

Indica el estado actual de las opciones bidireccionales en el control rich edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Estructura [**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) que recibe el estado actual de las opciones bidireccionales en el control de edición enriquecido.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Comentarios

Este mensaje establece los valores de los miembros **wMask** y **wEffects** en el valor del estado actual de las opciones bidireccionales en el control rich edit.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Redistribuible<br/>          | Rich Edit 3.0<br/>                                                              |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions)
</dt> <dt>

[**EM \_ SETBIDIOPTIONS**](em-setbidioptions.md)
</dt> </dl>

 

 





