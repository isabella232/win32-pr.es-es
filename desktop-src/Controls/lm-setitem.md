---
title: LM_SETITEM mensaje (Commctrl.h)
description: Establece los estados y atributos de un elemento.
ms.assetid: 02a68a31-2541-480e-b768-449d40e5e9e0
keywords:
- LM_SETITEM controles de Windows mensaje
topic_type:
- apiref
api_name:
- LM_SETITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8dccdb37536352c8783f7dd6af6a9475f5bea69111e2f7f09e5395b0ebf25b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062805"
---
# <a name="lm_setitem-message"></a>Mensaje \_ SETITEM de LM

Establece los estados y atributos de un elemento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser **NULL.** </dd> <dt>

*lParam* 
</dt> <dd>Puntero a una <a href="/windows/win32/api/commctrl/ns-commctrl-litem">estructura LITEM</a> que contiene los nuevos estados y atributos deseados para el vínculo. </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si el mensaje establece correctamente los valores y atributos especificados.

## <a name="remarks"></a>Comentarios

Con el [**mensaje \_ LM GETITEM,**](lm-getitem.md) solo se puede acceder a los vínculos a través del índice numérico devuelto en el **miembro iLink** [**de LITEM**](/windows/win32/api/commctrl/ns-commctrl-litem). No se admite el acceso al vínculo a través del nombre de identificador devuelto en **szID.**

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comctl32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





