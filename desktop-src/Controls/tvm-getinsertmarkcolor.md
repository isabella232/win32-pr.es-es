---
title: TVM_GETINSERTMARKCOLOR mensaje (Commctrl.h)
description: Recupera el color utilizado para dibujar la marca de inserción de la vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro \_ TreeView GetInsertMarkColor.
ms.assetid: d1fba4bb-1bdb-44e0-8083-b564cdafc055
keywords:
- TVM_GETINSERTMARKCOLOR controles de Windows mensaje
topic_type:
- apiref
api_name:
- TVM_GETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61416a428fed88ece8f50ca640dd9a05ec131614
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165746"
---
# <a name="tvm_getinsertmarkcolor-message"></a>Mensaje \_ DE TVM GETINSERTMARKCOLOR

Recupera el color utilizado para dibujar la marca de inserción de la vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**\_ TreeView GetInsertMarkColor.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getinsertmarkcolor)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un [**valor COLORREF**](/windows/desktop/gdi/colorref) que contiene el color de la marca de inserción actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TVM \_ SETINSERTMARKCOLOR**](tvm-setinsertmarkcolor.md)
</dt> </dl>

 

