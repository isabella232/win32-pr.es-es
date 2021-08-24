---
title: TVM_GETEXTENDEDSTYLE mensaje (Commctrl.h)
description: Recupera el estilo extendido para un control de vista de árbol. Envíe este mensaje explícitamente o mediante la macro \_ TreeView GetExtendedStyle.
ms.assetid: adc74cc5-e741-4966-bf49-a4b0c67e645a
keywords:
- TVM_GETEXTENDEDSTYLE controles de Windows mensaje
topic_type:
- apiref
api_name:
- TVM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a93eb22b3dfdbe05365d28a7c93bfa9df3619796f9b4ae9ec603c74da252c5a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119834205"
---
# <a name="tvm_getextendedstyle-message-commctrlh"></a>TVM_GETEXTENDEDSTYLE mensaje (Commctrl.h)

Recupera el estilo extendido para un control de vista de árbol. Envíe este mensaje explícitamente o mediante la macro [**\_ TreeView GetExtendedStyle.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getextendedstyle)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el valor de estilo extendido. Para obtener más información sobre los estilos, vea [Estilos extendidos del control De vista de árbol](tree-view-control-window-extended-styles.md).

## <a name="remarks"></a>Comentarios

Los estilos extendidos de un control de vista de árbol no tienen nada que ver con los estilos extendidos usados con la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o [**la función SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

