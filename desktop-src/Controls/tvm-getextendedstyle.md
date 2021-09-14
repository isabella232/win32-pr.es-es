---
title: TVM_GETEXTENDEDSTYLE mensaje (Commctrl.h)
description: Recupera el estilo extendido para un control de vista de árbol. Envíe este mensaje explícitamente o mediante la \_ macro TreeView GetExtendedStyle.
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
ms.openlocfilehash: 579a00e125389ff56c7ff93370ab71945598dba7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165758"
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

Devuelve el valor de estilo extendido. Para obtener más información sobre los estilos, vea [Estilos extendidos del control De vista de árbol.](tree-view-control-window-extended-styles.md)

## <a name="remarks"></a>Observaciones

Los estilos extendidos de un control de vista de árbol no tienen nada que ver con los estilos extendidos usados con la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o [**la función SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

