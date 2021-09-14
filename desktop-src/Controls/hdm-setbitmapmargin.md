---
title: HDM_SETBITMAPMARGIN mensaje (Commctrl.h)
description: Establece el ancho del margen, especificado en píxeles, de un mapa de bits en un control de encabezado existente. Puede enviar este mensaje explícitamente o usar la macro \_ Header SetBitmapMargin.
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
ms.openlocfilehash: d2a5384151a63918a5828608b0aa8e829df61cad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061976"
---
# <a name="hdm_setbitmapmargin-message"></a>Mensaje \_ SETBITMAPMARGIN de HDM

Establece el ancho del margen, especificado en píxeles, de un mapa de bits en un control de encabezado existente. Puede enviar este mensaje explícitamente o usar la macro [**\_ Header SetBitmapMargin.**](/windows/desktop/api/Commctrl/nf-commctrl-header_setbitmapmargin)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Ancho, especificado en píxeles, del margen que rodea un mapa de bits dentro de un control de encabezado existente.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el ancho del margen de mapa de bits, en píxeles. Si no se especificó previamente el margen de mapa de bits, se devuelve el valor predeterminado de 3 \* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (*SM \_ CXEDGE*).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**HDM \_ GETBITMAPMARGIN**](hdm-getbitmapmargin.md)
</dt> </dl>

 

