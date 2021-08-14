---
title: HDM_GETBITMAPMARGIN mensaje (Commctrl.h)
description: Obtiene el ancho del margen de mapa de bits para un control de encabezado. Puede enviar este mensaje explícitamente o usar la \_ macro Header GetBitmapMargin.
ms.assetid: 67794ad4-3c22-4fad-a1d7-7a5d5cc6ad67
keywords:
- HDM_GETBITMAPMARGIN controles de Windows mensaje
topic_type:
- apiref
api_name:
- HDM_GETBITMAPMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 685fb96e2ecf97a33b264de7bb3a6579f0c3480b6a15fdf99929ae879f4b35c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436215"
---
# <a name="hdm_getbitmapmargin-message"></a>Mensaje \_ GETBITMAPMARGIN de HDM

Obtiene el ancho del margen de mapa de bits para un control de encabezado. Puede enviar este mensaje explícitamente o usar la macro [**\_ Header GetBitmapMargin.**](/windows/desktop/api/Commctrl/nf-commctrl-header_getbitmapmargin)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el ancho del margen de mapa de bits en píxeles. Si no se especificó previamente el margen de mapa de bits, se devuelve el valor predeterminado de 3 \* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (SM \_ CXEDGE).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**HDM \_ SETBITMAPMARGIN**](hdm-setbitmapmargin.md)
</dt> </dl>

 

