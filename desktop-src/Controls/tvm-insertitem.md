---
title: Mensaje de TVM_INSERTITEM (commctrl. h)
description: Inserta un nuevo elemento en un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro InsertItem de TreeView.
ms.assetid: c5e5f88f-6ec8-4b95-89ea-97f6f1fd735e
keywords:
- TVM_INSERTITEM controles de mensajes de Windows
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
ms.openlocfilehash: 719de4c2391ff924c9f6deb8cb4206cfdb56c3ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905102"
---
# <a name="tvm_insertitem-message"></a>Mensaje de error de INSERTITEM de TVM \_

Inserta un nuevo elemento en un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**\_ InsertItem de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_insertitem) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) que especifica los atributos del elemento de vista de árbol.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador **HTREEITEM** para el nuevo elemento si se realiza correctamente, o **null** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TVM \_ INSERTITEMW** (Unicode) y **TVM \_ INSERTITEMA** (ANSI)<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[TVN \_ ENDLABELEDIT](tvn-endlabeledit.md)
</dt> </dl>

 

 





