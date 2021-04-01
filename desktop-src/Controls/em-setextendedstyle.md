---
title: Mensaje de EM_SETEXTENDEDSTYLE (commctrl. h)
description: Informa al control de edición para establecer los estilos extendidos. Envíe este mensaje o use la macro Edit \_ SetExtendedStyle.
ms.assetid: 4ca010c3-2c70-41e5-ade4-11e1895fda26
keywords:
- EM_SETEXTENDEDSTYLE controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150916"
---
# <a name="em_setextendedstyle-message"></a>\_Mensaje SETEXTENDEDSTYLE em

Informa al control de edición para establecer los estilos extendidos. Envíe este mensaje o use la macro [**Edit \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setextendedstyle).

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Máscara que se usa para seleccionar los estilos que se van a establecer.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor que indica el estilo extendido. Para obtener más información sobre los estilos, vea [Edit control Extended Styles](edit-control-window-extended-styles.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este mensaje se realiza correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Los estilos extendidos para un control de edición no tienen nada que hacer con los estilos extendidos usados con la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1809 \[\]<br/>                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2019 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

