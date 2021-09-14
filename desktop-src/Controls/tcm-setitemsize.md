---
title: TCM_SETITEMSIZE mensaje (Commctrl.h)
description: Establece el ancho y alto de las pestañas en un control de pestaña de ancho fijo o dibujado por el propietario. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ SetItemSize.
ms.assetid: 3935d686-f8bc-41fb-b025-04120cf03f02
keywords:
- TCM_SETITEMSIZE controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166202"
---
# <a name="tcm_setitemsize-message"></a>Mensaje \_ SETITEMSIZE de TCM

Establece el ancho y alto de las pestañas en un control de pestaña de ancho fijo o dibujado por el propietario. Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ SetItemSize.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemsize)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD es**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) un valor **INT** que especifica el nuevo ancho, en píxeles. [**HIWORD es**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) un valor **INT** que especifica el nuevo alto, en píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el ancho y alto antiguos. El ancho está en el [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) del valor devuelto y el alto está en [**hiword**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).

## <a name="remarks"></a>Observaciones

Si el ancho se establece en un valor menor que el ancho de imagen establecido por [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create), el ancho de la pestaña se establece en el valor más bajo que es mayor que el ancho de la imagen.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

