---
title: EM_GETBIDIOPTIONS mensaje (Richedit.h)
description: Indica el estado actual de las opciones bidireccionales en el control de edición enriquecido.
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
ms.openlocfilehash: 7fade63ac94007bedbf58642dc7a9451eb158fc3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062210"
---
# <a name="em_getbidioptions-message"></a>Mensaje \_ EM GETBIDIOPTIONS

Indica el estado actual de las opciones bidireccionales en el control de edición enriquecido.

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

## <a name="remarks"></a>Observaciones

Este mensaje establece los valores de los miembros **wMask** y **wEffects** en el valor del estado actual de las opciones bidireccionales en el control de edición enriquecido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Redistribuible<br/>          | Rich Edit 3.0<br/>                                                              |
| Encabezado<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions)
</dt> <dt>

[**EM \_ SETBIDIOPTIONS**](em-setbidioptions.md)
</dt> </dl>

 

 





