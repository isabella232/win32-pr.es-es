---
title: TCM_SETITEMSIZE mensaje (Commctrl.h)
description: Establece el ancho y alto de las pestañas en un control de ficha de ancho fijo o dibujado por el propietario. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ SetItemSize.
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
ms.openlocfilehash: 8845aa54cd3cca413f31ee01f4a9583e24dc875a876d1aff691f574214f6f793
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876235"
---
# <a name="tcm_setitemsize-message"></a>Mensaje \_ SETITEMSIZE de TCM

Establece el ancho y alto de las pestañas en un control de ficha de ancho fijo o dibujado por el propietario. Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ SetItemSize.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemsize)

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

## <a name="remarks"></a>Comentarios

Si el ancho se establece en un valor menor que el ancho de imagen establecido por [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create), el ancho de la pestaña se establece en el valor más bajo mayor que el ancho de la imagen.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

