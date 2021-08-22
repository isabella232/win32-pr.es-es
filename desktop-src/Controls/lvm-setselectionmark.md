---
title: LVM_SETSELECTIONMARK mensaje (Commctrl.h)
description: Establece la marca de selección en un control de vista de lista. Puede enviar este mensaje explícitamente o usar la macro ListView \_ SetSelectionMark.
ms.assetid: 3218f1b3-b934-4083-aaaa-e10ef1dbb6bd
keywords:
- LVM_SETSELECTIONMARK controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_SETSELECTIONMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c80f1392b5bb8b8ae49eaefb639a60213b5d4a7deaf153b99262bf608a770e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119217365"
---
# <a name="lvm_setselectionmark-message"></a>Mensaje \_ SETSELECTIONMARK de LVM

Establece la marca de selección en un control de vista de lista. Puede enviar este mensaje explícitamente o usar la macro [**ListView \_ SetSelectionMark.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setselectionmark)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Índice de base cero de la nueva marca de selección. Si se establece en -1, se quita la marca de selección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la marca de selección anterior o -1 si no hay ninguna marca de selección anterior.

## <a name="remarks"></a>Comentarios

La *marca de selección* es el índice de elemento desde el que se inicia una selección múltiple. Este mensaje no afecta al estado de selección del elemento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LVM \_ GETSELECTIONMARK**](lvm-getselectionmark.md)
</dt> </dl>

 

 





