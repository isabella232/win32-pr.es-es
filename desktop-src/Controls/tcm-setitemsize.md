---
title: Mensaje de TCM_SETITEMSIZE (commctrl. h)
description: Establece el ancho y el alto de las pestañas en un control de ficha de ancho fijo o dibujado por el propietario. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ SetItemSize.
ms.assetid: 3935d686-f8bc-41fb-b025-04120cf03f02
keywords:
- TCM_SETITEMSIZE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TCM_SETITEMSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e306af3f6462507a181de91104169c5ac7d6ce14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103904982"
---
# <a name="tcm_setitemsize-message"></a>\_Mensaje SETITEMSIZE de TCM

Establece el ancho y el alto de las pestañas en un control de ficha de ancho fijo o dibujado por el propietario. Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ SetItemSize**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemsize) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es un valor **int** que especifica el nuevo ancho, en píxeles. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) es un valor **int** que especifica el nuevo alto, en píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el ancho y el alto antiguos. El ancho está en el [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) del valor devuelto y el alto está en [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).

## <a name="remarks"></a>Observaciones

Si el ancho se establece en un valor menor que el ancho de imagen establecido por [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create), el ancho de la pestaña se establece en el valor más bajo que sea mayor que el ancho de la imagen.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

