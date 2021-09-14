---
title: EM_GETEXTENDEDSTYLE mensaje (Commctrl.h)
description: Recupera el estilo extendido para un control de edición. Envíe este mensaje explícitamente o mediante la macro \_ Edit GetExtendedStyle .
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
ms.openlocfilehash: 37dc117bccd57b51098a7ca8c19e8b178037bef8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062192"
---
# <a name="em_getextendedstyle-message-commctrlh"></a>EM_GETEXTENDEDSTYLE mensaje (Commctrl.h)

Recupera el estilo extendido para un control de vista de árbol. Envíe este mensaje explícitamente o mediante [**la macro \_ Edit GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getextendedstyle) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el valor de estilo extendido. Para obtener más información sobre los estilos, vea [Editar estilos extendidos de control](edit-control-window-extended-styles.md).

## <a name="remarks"></a>Observaciones

Los estilos extendidos de un control de edición no tienen nada que ver con los estilos extendidos usados con la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o [**la función SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10, versión 1809 solo aplicaciones de escritorio\]<br/>                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2019 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

