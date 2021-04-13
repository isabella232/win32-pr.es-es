---
title: Mensaje de EM_GETEXTENDEDSTYLE (commctrl. h)
description: Recupera el estilo extendido de un control de edición. Envíe este mensaje explícitamente o mediante la \_ macro Edit GetExtendedStyle.
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- EM_GETEXTENDEDSTYLE controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491813"
---
# <a name="em_getextendedstyle-message-commctrlh"></a>Mensaje de EM_GETEXTENDEDSTYLE (commctrl. h)

Recupera el estilo extendido para un control de vista de árbol. Envíe este mensaje explícitamente o mediante la macro [**Edit \_ GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getextendedstyle) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el valor de estilo extendido. Para obtener más información sobre los estilos, vea [Edit control Extended Styles](edit-control-window-extended-styles.md).

## <a name="remarks"></a>Observaciones

Los estilos extendidos para un control de edición no tienen nada que hacer con los estilos extendidos usados con la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1809 \[\]<br/>                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2019 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

