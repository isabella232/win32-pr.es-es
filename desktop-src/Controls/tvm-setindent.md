---
title: Mensaje de TVM_SETINDENT (commctrl. h)
description: Establece el ancho de la sangría de un control de vista de árbol y vuelve a dibujar el control para reflejar el nuevo ancho. Puede enviar este mensaje explícitamente o mediante la \_ macro SetIndent de TreeView.
ms.assetid: 377da8fe-c8e6-479b-a283-f1811cbc3e58
keywords:
- TVM_SETINDENT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_SETINDENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f85263c7c4330a692dc08949870a0eaa92f2b22c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150452"
---
# <a name="tvm_setindent-message"></a>\_Mensaje de SETINDENT TVM

Establece el ancho de la sangría de un control de vista de árbol y vuelve a dibujar el control para reflejar el nuevo ancho. Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetIndent de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Ancho, en píxeles, de la sangría. Si este parámetro es menor que el ancho mínimo definido por el sistema, el nuevo ancho se establece en el mínimo definido por el sistema.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El valor de sangría mínima definido por el sistema suele ser de cinco píxeles, pero no es fijo. Para recuperar el valor exacto de la sangría mínima en un sistema determinado, envíe un mensaje **TVM \_ SETINDENT** con *wParam* establecido en cero. A continuación, envíe un mensaje [**TVM \_ GETINDENT**](tvm-getindent.md) para recuperar el valor de sangría mínima.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SetIndent de TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent)
</dt> </dl>

 

 





