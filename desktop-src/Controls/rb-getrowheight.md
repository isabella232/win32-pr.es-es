---
title: RB_GETROWHEIGHT mensaje (Commctrl.h)
description: Recupera el alto de una fila especificada en un control rebar.
ms.assetid: 1ff6a32e-b344-4dbc-b4a4-fb13f11a9d8c
keywords:
- RB_GETROWHEIGHT controles de Windows mensaje
topic_type:
- apiref
api_name:
- RB_GETROWHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ac650fb50f1b6594964ec0bf10d23a8c8b6b75ff82e14af44bb63e2c9cf8af8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118409419"
---
# <a name="rb_getrowheight-message"></a>Mensaje \_ GETROWHEIGHT de RB

Recupera el alto de una fila especificada en un control rebar.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de una banda. Se recuperará el alto de la fila que contiene la banda especificada.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor UINT** que representa el alto de la fila, en píxeles.

## <a name="remarks"></a>Comentarios

Para recuperar el número de filas de un control rebar, use el [**mensaje \_ GETROWCOUNT de RB.**](rb-getrowcount.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





