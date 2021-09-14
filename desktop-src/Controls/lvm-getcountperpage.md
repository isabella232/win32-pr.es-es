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
ms.openlocfilehash: 734d460754f9ae8a11c3a42d8eacebf31d0b6fc0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061854"
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

Devuelve el número de elementos totalmente visibles si se realiza correctamente. Si la vista actual es icono o vista de icono pequeña, el valor devuelto es el número total de elementos del control list-view.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





