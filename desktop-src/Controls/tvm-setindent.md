---
title: TVM_SETINDENT mensaje (Commctrl.h)
description: Establece el ancho de sangría de un control de vista de árbol y vuelve a dibujar el control para reflejar el nuevo ancho. Puede enviar este mensaje explícitamente o mediante la macro TreeView \_ SetIndent.
ms.assetid: 377da8fe-c8e6-479b-a283-f1811cbc3e58
keywords:
- TVM_SETINDENT controles de Windows mensaje
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
ms.openlocfilehash: 538a89439909afe346ae8776d31a2104c7f6014664a33bdd3864bf43b0387e80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669670"
---
# <a name="tvm_setindent-message"></a>Mensaje \_ DE TVM SETINDENT

Establece el ancho de sangría de un control de vista de árbol y vuelve a dibujar el control para reflejar el nuevo ancho. Puede enviar este mensaje explícitamente o mediante la macro [**TreeView \_ SetIndent.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent)

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

El valor mínimo de sangría definido por el sistema suele ser de cinco píxeles, pero no es fijo. Para recuperar el valor exacto de la sangría mínima en un sistema determinado, envíe un mensaje **\_ TVM SETINDENT** con *wParam* establecido en cero. A continuación, [**envíe un mensaje \_ GETINDENT de TVM**](tvm-getindent.md) para recuperar el valor mínimo de sangría.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TreeView \_ SetIndent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent)
</dt> </dl>

 

 





