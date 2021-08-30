---
title: LVM_SETITEMPOSITION mensaje (Commctrl.h)
description: Mueve un elemento a una posición especificada en un control de vista de lista (debe estar en la vista de icono o icono pequeño). Puede enviar este mensaje explícitamente o mediante la macro ListView \_ SetItemPosition.
ms.assetid: dfb35af4-e6c3-40fc-9d7c-cf0d68a3ea01
keywords:
- LVM_SETITEMPOSITION controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_SETITEMPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 111f961b668e13fa10fdfb00cdf430aba1bc9d0b1c0b04295e5777a46f5cb9a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915255"
---
# <a name="lvm_setitemposition-message"></a>Mensaje \_ SETITEMPOSITION de LVM

Mueve un elemento a una posición especificada en un control de vista de lista (debe estar en la vista de icono o icono pequeño). Puede enviar este mensaje explícitamente o mediante la macro [**ListView \_ SetItemPosition.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento de vista de lista.

</dd> <dt>

*lParam* 
</dt> <dd>

[**Loword**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica la nueva posición x de la esquina superior izquierda del elemento, en coordenadas de vista. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica la nueva posición y de la esquina superior izquierda del elemento, en coordenadas de vista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="remarks"></a>Comentarios

Si el control de vista de lista tiene el estilo [**LVS \_ AUTOARRANGE,**](list-view-window-styles.md) los elementos del control de vista de lista se organizan después de establecer la posición del elemento.

En Windows Vista, el envío de este mensaje a un control de vista de lista con el estilo [**LVS \_ AUTOARRANGE**](list-view-window-styles.md) no hace nada y el valor devuelto es **FALSE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

