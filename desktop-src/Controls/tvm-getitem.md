---
title: Mensaje de TVM_GETITEM (commctrl. h)
description: Recupera algunos o todos los atributos de un elemento de vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro GetItem de TreeView.
ms.assetid: e26ec000-967d-46de-8f71-6ebc36fefe5e
keywords:
- TVM_GETITEM controles de mensajes de Windows
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
ms.openlocfilehash: dff96f4721a3c50eda54792b2b1c003cd808bf11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151250"
---
# <a name="tvm_getitem-message"></a>Mensaje de GETITEM de TVM \_

Recupera algunos o todos los atributos de un elemento de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetItem de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitem) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que especifica la información que se va a recuperar y recibe información sobre el elemento. Con la [versión 4,71](common-control-versions.md) y versiones posteriores, puede usar una estructura [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) en su lugar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Cuando se envía el mensaje, el miembro **hItem** de la estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) o [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) identifica el elemento del que se va a recuperar información y el miembro **Mask** especifica los atributos que se van a recuperar.

Si la \_ marca de texto TVIF se establece en el miembro **Mask** de la estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) o [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) , el miembro **miembros pszText** debe apuntar a un búfer válido y el miembro **cchTextMax** debe establecerse en el número de caracteres de ese búfer.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TVM \_ GETITEMW** (Unicode) y **TVM \_ GETITEMA** (ANSI)<br/>                   |



 

 





