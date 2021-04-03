---
title: Mensaje de LVM_SETITEMPOSITION (commctrl. h)
description: Mueve un elemento a una posición especificada en un control de vista de lista (debe estar en el icono o en la vista de iconos pequeños). Puede enviar este mensaje explícitamente o mediante la \_ macro SetItemPosition de ListView.
ms.assetid: dfb35af4-e6c3-40fc-9d7c-cf0d68a3ea01
keywords:
- LVM_SETITEMPOSITION controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905291"
---
# <a name="lvm_setitemposition-message"></a>\_Mensaje SETITEMPOSITION LVM

Mueve un elemento a una posición especificada en un control de vista de lista (debe estar en el icono o en la vista de iconos pequeños). Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetItemPosition de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento de vista de lista.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica la nueva posición x de la esquina superior izquierda del elemento, en coordenadas de la vista. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica la nueva posición y de la esquina superior izquierda del elemento, en coordenadas de la vista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Si el control de vista de lista tiene el estilo [**LVS \_ AutoArrange**](list-view-window-styles.md) , los elementos del control de vista de lista se organizan una vez establecida la posición del elemento.

En Windows Vista, el envío de este mensaje a un control de vista de lista con el estilo [**LVS \_ AutoArrange**](list-view-window-styles.md) no hace nada y el valor devuelto es **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

