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
ms.openlocfilehash: 27ce137eef6168d95abfe493a6f22ab66d58460b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167341"
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

## <a name="remarks"></a>Observaciones

Para recuperar el número de filas de un control rebar, use el [**mensaje \_ GETROWCOUNT de RB.**](rb-getrowcount.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





