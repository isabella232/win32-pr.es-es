---
title: TVM_SHOWINFOTIP mensaje (Commctrl.h)
description: Muestra la información sobre un elemento especificado en un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro TreeView ShowInfoTip.
ms.assetid: ed5a1bda-5754-4bb3-aa22-8faaf1af1268
keywords:
- TVM_SHOWINFOTIP controles de Windows mensaje
topic_type:
- apiref
api_name:
- TVM_SHOWINFOTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e1cf61511e8c9e69c42d89f99fc4ddae90de78701e5e75170ff1b793671120
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913925"
---
# <a name="tvm_showinfotip-message"></a>Mensaje \_ SHOWINFOTIP de TVM

Muestra la información sobre un elemento especificado en un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**\_ TreeView ShowInfoTip.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_showinfotip)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* \[ En\]
</dt> <dd>

Identificador del elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero.

## <a name="remarks"></a>Comentarios

La mayoría de las aplicaciones no usan este mensaje. La información se muestra automáticamente. Para obtener más información, vea Using Tree-view Infotips (Información sobre el uso de información sobre la vista de árbol) en about Tree-View Controls overview (Información general [sobre Tree-View controles).](tree-view-controls.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





