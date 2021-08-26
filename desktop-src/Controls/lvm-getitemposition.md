---
title: LVM_GETITEMPOSITION mensaje (Commctrl.h)
description: Recupera la posición de un elemento de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro \_ ListView GetItemPosition.
ms.assetid: e5841089-c34e-498e-b94c-45c845bfc747
keywords:
- LVM_GETITEMPOSITION controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETITEMPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92d4f4a55f88b6af9828420871de80117ae492bf53c8a62883e43f928c4f5c70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002625"
---
# <a name="lvm_getitemposition-message"></a>Mensaje \_ GETITEMPOSITION de LVM

Recupera la posición de un elemento de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ ListView GetItemPosition.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemposition)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento list-view.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura POINT**](/previous-versions//dd162805(v=vs.85)) que recibe la posición de la esquina superior izquierda del elemento, en coordenadas de vista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

