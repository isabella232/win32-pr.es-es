---
title: EM_GETEXTENDEDSTYLE mensaje (Commctrl.h)
description: Recupera el estilo extendido para un control de edición. Envíe este mensaje explícitamente o mediante la macro \_ Editar GetExtendedStyle.
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- EM_GETEXTENDEDSTYLE controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 77aa5827cc256c040d34ca24574dfa0b12816accaff9e5c0e92b4400195cae2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019673"
---
# <a name="em_getextendedstyle-message-commctrlh"></a>EM_GETEXTENDEDSTYLE mensaje (Commctrl.h)

Recupera el estilo extendido para un control de vista de árbol. Envíe este mensaje explícitamente o mediante la [**macro \_ Editar GetExtendedStyle.**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getextendedstyle)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el valor de estilo extendido. Para obtener más información sobre los estilos, vea [Editar estilos extendidos de control](edit-control-window-extended-styles.md).

## <a name="remarks"></a>Comentarios

Los estilos extendidos para un control de edición no tienen nada que ver con los estilos extendidos usados con la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o la [**función SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10, versión 1809 solo aplicaciones de escritorio\]<br/>                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2019 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

