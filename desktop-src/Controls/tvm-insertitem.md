---
title: TVM_INSERTITEM mensaje (Commctrl.h)
description: Inserta un nuevo elemento en un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro TreeView \_ InsertItem.
ms.assetid: c5e5f88f-6ec8-4b95-89ea-97f6f1fd735e
keywords:
- TVM_INSERTITEM controles de Windows mensaje
topic_type:
- apiref
api_name:
- TVM_INSERTITEM
- TVM_INSERTITEMA
- TVM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85f8a324613820b94e0bd2c49d8fa78136038471f820dd2b9ed8e38ace15f0cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060195"
---
# <a name="tvm_insertitem-message"></a>Mensaje \_ INSERTITEM de TVM

Inserta un nuevo elemento en un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**TreeView \_ InsertItem.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_insertitem)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) que especifica los atributos del elemento de vista de árbol.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el **identificador HTREEITEM** al nuevo elemento si se realiza correctamente o **NULL** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TVM \_ INSERTITEMW** (Unicode) y **TVM \_ INSERTITEMA** (ANSI)<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[TVN \_ ENDLABELEDIT](tvn-endlabeledit.md)
</dt> </dl>

 

 





