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
ms.openlocfilehash: 76f147253800469a800677a242ff0ab0ccdbdfa4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165606"
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

## <a name="remarks"></a>Observaciones

La mayoría de las aplicaciones no usan este mensaje. La información sobre información se muestra automáticamente. Para obtener más información, vea Using Tree-view Infotips (Uso de información sobre la vista de árbol) en [Información general Tree-View controles.](tree-view-controls.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





