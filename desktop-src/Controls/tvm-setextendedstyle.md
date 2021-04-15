---
title: Mensaje de TVM_SETEXTENDEDSTYLE (commctrl. h)
description: Informa al control de vista de árbol para establecer los estilos extendidos. Envíe este mensaje o use la macro TreeView \_ SetExtendedStyle.
ms.assetid: 35cb6ac8-1c1e-4ecd-88b2-878d3f6ccaa5
keywords:
- TVM_SETEXTENDEDSTYLE controles de mensajes de Windows
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
ms.openlocfilehash: 9c450f72f85e40514c35f08284428feec4f7caf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534342"
---
# <a name="tvm_setextendedstyle-message"></a>\_Mensaje de SETEXTENDEDSTYLE TVM

Informa al control de vista de árbol para establecer los estilos extendidos. Envíe este mensaje o use la macro [**TreeView \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setextendedstyle).

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Máscara que se usa para seleccionar los estilos que se van a establecer.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor que indica el estilo extendido. Para obtener más información sobre los estilos, vea los [estilos extendidos del control de vista de árbol](tree-view-control-window-extended-styles.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este mensaje se realiza correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Los estilos extendidos para un control de vista de árbol no tienen nada que ver con los estilos extendidos que se usan con la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

