---
title: EM_SETEXTENDEDSTYLE mensaje (Commctrl.h)
description: Informa al control de edición para establecer estilos extendidos. Envíe este mensaje o use la macro \_ Editar SetExtendedStyle.
ms.assetid: 4ca010c3-2c70-41e5-ade4-11e1895fda26
keywords:
- EM_SETEXTENDEDSTYLE controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 560b675927b4497810b8d492fd89b5765aa5a2c2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062113"
---
# <a name="em_setextendedstyle-message"></a>Mensaje EM \_ SETEXTENDEDSTYLE

Informa al control de edición para establecer estilos extendidos. Envíe este mensaje o use la macro [**\_ Edit SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setextendedstyle).

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Máscara usada para seleccionar los estilos que se establecerán.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor que indica el estilo extendido. Para obtener más información sobre los estilos, vea [Editar estilos extendidos de control](edit-control-window-extended-styles.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este mensaje se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Los estilos extendidos de un control de edición no tienen nada que ver con los estilos extendidos usados con la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o [**la función SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10, versión 1809 solo aplicaciones de escritorio\]<br/>                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2019 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

