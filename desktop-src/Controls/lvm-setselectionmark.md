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
ms.openlocfilehash: 3efc01068f22585061cae5a6f2c5c0c841810f52
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362667"
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

## <a name="remarks"></a>Observaciones

La *marca de selección* es el índice de elemento desde el que se inicia una selección múltiple. Este mensaje no afecta al estado de selección del elemento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**LVM \_ GETSELECTIONMARK**](lvm-getselectionmark.md)
</dt> </dl>

 

 





