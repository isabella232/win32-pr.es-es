---
title: HDM_SETBITMAPMARGIN mensaje (Commctrl.h)
description: Establece el ancho del margen, especificado en píxeles, de un mapa de bits en un control de encabezado existente. Puede enviar este mensaje explícitamente o usar la \_ macro SetBitmapMargin de encabezado.
ms.assetid: 5ac04701-18c8-42d4-9850-fe6eb813672c
keywords:
- HDM_SETBITMAPMARGIN controles de Windows mensaje
topic_type:
- apiref
api_name:
- HDM_SETBITMAPMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa2e7c24ea52edc0001cea9f4d7184957c2cfbf50f15769df964351df91e5813
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435955"
---
# <a name="hdm_setbitmapmargin-message"></a>Mensaje \_ SETBITMAPMARGIN de HDM

Establece el ancho del margen, especificado en píxeles, de un mapa de bits en un control de encabezado existente. Puede enviar este mensaje explícitamente o usar la macro [**\_ SetBitmapMargin de**](/windows/desktop/api/Commctrl/nf-commctrl-header_setbitmapmargin) encabezado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Ancho, especificado en píxeles, del margen que rodea un mapa de bits dentro de un control de encabezado existente.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el ancho del margen de mapa de bits, en píxeles. Si no se especificó previamente el margen de mapa de bits, se devuelve el valor predeterminado de 3 \* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) *(SM \_ CXEDGE*).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**HDM \_ GETBITMAPMARGIN**](hdm-getbitmapmargin.md)
</dt> </dl>

 

