---
title: TVM_GETITEM mensaje (Commctrl.h)
description: Recupera algunos o todos los atributos de un elemento de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro TreeView \_ GetItem.
ms.assetid: e26ec000-967d-46de-8f71-6ebc36fefe5e
keywords:
- TVM_GETITEM controles de Windows mensaje
topic_type:
- apiref
api_name:
- TVM_GETITEM
- TVM_GETITEMA
- TVM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 425b0200df62b1cfcbc18556ad12513e43cebadf6e5742b36880464fad195fb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984895"
---
# <a name="tvm_getitem-message"></a>Mensaje \_ GETITEM de TVM

Recupera algunos o todos los atributos de un elemento de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**TreeView \_ GetItem.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitem)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que especifica la información que se debe recuperar y recibe información sobre el elemento. Con [la versión 4.71](common-control-versions.md) y versiones posteriores, puede usar una [**estructura TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) en su lugar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="remarks"></a>Comentarios

Cuando se envía el mensaje, el **miembro hItem** de la estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) o [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) identifica el elemento sobre el que se va a recuperar información y el miembro **mask** especifica los atributos que se recuperarán.

Si la marca TEXT de TVIF se establece en el miembro mask de la estructura \_ [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) o [**TVITEMEX,**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) el miembro **pszText** debe apuntar a un búfer válido y el miembro **cchTextMax** debe establecerse en el número de caracteres de ese búfer. 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TVM \_ GETITEMW** (Unicode) y **TVM \_ GETITEMA** (ANSI)<br/>                   |



 

 





