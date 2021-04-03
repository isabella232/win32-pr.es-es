---
title: Mensaje de HDM_SETBITMAPMARGIN (commctrl. h)
description: Establece el ancho del margen, especificado en píxeles, de un mapa de bits en un control de encabezado existente. Puede enviar este mensaje explícitamente o utilizar la \_ macro header SetBitmapMargin.
ms.assetid: 5ac04701-18c8-42d4-9850-fe6eb813672c
keywords:
- HDM_SETBITMAPMARGIN controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905478"
---
# <a name="hdm_setbitmapmargin-message"></a>HDM \_ SETBITMAPMARGIN

Establece el ancho del margen, especificado en píxeles, de un mapa de bits en un control de encabezado existente. Puede enviar este mensaje explícitamente o utilizar la macro [**Header \_ SetBitmapMargin**](/windows/desktop/api/Commctrl/nf-commctrl-header_setbitmapmargin) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Ancho, especificado en píxeles, del margen que rodea un mapa de bits dentro de un control de encabezado existente.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el ancho del margen del mapa de bits, en píxeles. Si no se especificó previamente el margen del mapa de bits, se devuelve el valor predeterminado de 3 \* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (*SM \_ CXEDGE*).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**HDM \_ GETBITMAPMARGIN**](hdm-getbitmapmargin.md)
</dt> </dl>

 

