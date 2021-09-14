---
title: HDM_GETUNICODEFORMAT mensaje (Commctrl.h)
description: Obtiene la marca de formato de caracteres Unicode para el control. Puede enviar este mensaje explícitamente o usar la macro Header \_ GetUnicodeFormat.
ms.assetid: 2b36265a-023c-4083-a755-769461f3804b
keywords:
- HDM_GETUNICODEFORMAT controles de Windows mensaje
topic_type:
- apiref
api_name:
- HDM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce625cc9d4c0ede0c4ce9b54dc852025b22d4870
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061991"
---
# <a name="hdm_getunicodeformat-message"></a>Mensaje \_ GETUNICODEFORMAT de HDM

Obtiene la marca de formato de caracteres Unicode para el control. Puede enviar este mensaje explícitamente o usar la macro [**Header \_ GetUnicodeFormat.**](/windows/desktop/api/Commctrl/nf-commctrl-header_getunicodeformat)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la marca de formato Unicode del control. Si este valor es distinto de cero, el control usa caracteres Unicode. Si este valor es cero, el control usa caracteres ANSI.

## <a name="remarks"></a>Observaciones

Consulte los comentarios de [**CCM \_ GETUNICODEFORMAT para**](ccm-getunicodeformat.md) obtener una explicación de este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**HDM \_ SETUNICODEFORMAT**](hdm-setunicodeformat.md)
</dt> </dl>

 

 





