---
title: LVM_GETCOUNTPERPAGE mensaje (Commctrl.h)
description: Calcula el número de elementos que pueden caber verticalmente en el área visible de un control de vista de lista cuando se encuentra en la vista de lista o informe. Solo se cuentan los elementos totalmente visibles. Puede enviar este mensaje explícitamente o mediante la macro \_ ListView GetCountPerPage.
ms.assetid: 2ffd2bb1-cddf-4a4a-a4a8-087c9dc3fec0
keywords:
- LVM_GETCOUNTPERPAGE controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETCOUNTPERPAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: deb5e7acf0c3db4add2d986a1821b9a76ae30fc1aec0af369e48e35e2a424f77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968345"
---
# <a name="lvm_getcountperpage-message"></a>Mensaje \_ GETCOUNTPERPAGE de LVM

Calcula el número de elementos que pueden caber verticalmente en el área visible de un control de vista de lista cuando se encuentra en la vista de lista o informe. Solo se cuentan los elementos totalmente visibles. Puede enviar este mensaje explícitamente o mediante la macro [**\_ ListView GetCountPerPage.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcountperpage)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de elementos totalmente visibles si se realiza correctamente. Si la vista actual es icono o vista de icono pequeño, el valor devuelto es el número total de elementos del control list-view.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





