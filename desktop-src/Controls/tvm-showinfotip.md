---
title: Mensaje de TVM_SHOWINFOTIP (commctrl. h)
description: Muestra el recuadro informativo de un elemento especificado en un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro ShowInfoTip de TreeView.
ms.assetid: ed5a1bda-5754-4bb3-aa22-8faaf1af1268
keywords:
- TVM_SHOWINFOTIP controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905639"
---
# <a name="tvm_showinfotip-message"></a>\_Mensaje de SHOWINFOTIP TVM

Muestra el recuadro informativo de un elemento especificado en un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**\_ ShowInfoTip de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_showinfotip) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* \[ de\]
</dt> <dd>

Identificador del elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero.

## <a name="remarks"></a>Observaciones

La mayoría de las aplicaciones no usan este mensaje. Recuadros informativos se muestran automáticamente. Para obtener más información, vea uso de la vista de árbol recuadros informativos en la información general [sobre los controles de Tree-View](tree-view-controls.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





