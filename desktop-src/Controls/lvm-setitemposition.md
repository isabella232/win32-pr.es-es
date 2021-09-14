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
ms.openlocfilehash: b95fcf2949f1e19677bd445c0f6c5f762db078d1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362691"
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

## <a name="remarks"></a>Observaciones

Si el control de vista de lista tiene el estilo [**LVS \_ AUTOARRANGE,**](list-view-window-styles.md) los elementos del control de vista de lista se organizan después de establecer la posición del elemento.

En Windows Vista, el envío de este mensaje a un control de vista de lista con el estilo [**LVS \_ AUTOARRANGE**](list-view-window-styles.md) no hace nada y el valor devuelto es **FALSE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

