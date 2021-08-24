---
title: TVM_SETEXTENDEDSTYLE mensaje (Commctrl.h)
description: Informa al control de vista de árbol para establecer estilos extendidos. Envíe este mensaje o use la macro TreeView \_ SetExtendedStyle.
ms.assetid: 35cb6ac8-1c1e-4ecd-88b2-878d3f6ccaa5
keywords:
- TVM_SETEXTENDEDSTYLE controles de Windows mensaje
topic_type:
- apiref
api_name:
- TVM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d13d99a2f7a27475c30867f007f45d7525118d3077ebdce235c6bd33e1f8aafe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750965"
---
# <a name="tvm_setextendedstyle-message"></a>Mensaje \_ DE TVM SETEXTENDEDSTYLE

Informa al control de vista de árbol para establecer estilos extendidos. Envíe este mensaje o use la macro [**TreeView \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setextendedstyle).

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Máscara usada para seleccionar los estilos que se establecerán.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor que indica el estilo extendido. Para obtener más información sobre los estilos, vea [Estilos extendidos del control De vista de árbol.](tree-view-control-window-extended-styles.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este mensaje se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Los estilos extendidos de un control de vista de árbol no tienen nada que ver con los estilos extendidos usados con la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o [**la función SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

