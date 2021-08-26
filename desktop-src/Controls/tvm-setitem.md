---
title: TVM_SETITEM mensaje (Commctrl.h)
description: El mensaje SETITEM de TVM establece algunos o todos los atributos de un elemento de vista \_ de árbol. Puede enviar este mensaje explícitamente o mediante la macro TreeView \_ SetItem.
ms.assetid: 28d288bf-a557-4fce-870c-ffa368ece5a9
keywords:
- TVM_SETITEM controles de Windows mensaje
topic_type:
- apiref
api_name:
- TVM_SETITEM
- TVM_SETITEMA
- TVM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9521bc67766dbb503fc205e966d6ce72e674a4050b6c0d237c885dcb4a8f4b68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913945"
---
# <a name="tvm_setitem-message"></a>Mensaje \_ SETITEM de TVM

El **mensaje \_ SETITEM de TVM** establece algunos o todos los atributos de un elemento de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**TreeView \_ SetItem.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contiene los nuevos atributos de elemento. Con [la versión 4.71](common-control-versions.md) y posteriores, puede usar una [**estructura TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) en su lugar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="remarks"></a>Comentarios

El **miembro hItem** de la estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) o [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) identifica el elemento y el miembro **mask** especifica qué atributos se establecerán.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TVM \_ SETITEMW** (Unicode) y **TVM \_ SETITEMA** (ANSI)<br/>                   |



 

 





