---
title: LVM_GETUNICODEFORMAT mensaje (Commctrl.h)
description: Recupera la marca de formato de caracteres UNICODE para el control . Puede enviar este mensaje explícitamente o usar la \_ macro ListView GetUnicodeFormat.
ms.assetid: b0598b60-4d0e-4c68-b63a-e614c6268129
keywords:
- LVM_GETUNICODEFORMAT controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b3166d7349bf138fa853523c019a4c1db86e3f1a2d81a6da86c4ef25b5ed405
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019263"
---
# <a name="lvm_getunicodeformat-message"></a>Mensaje \_ GETUNICODEFORMAT de LVM

Recupera la marca de formato de caracteres UNICODE para el control . Puede enviar este mensaje explícitamente o usar la macro [**\_ ListView GetUnicodeFormat.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getunicodeformat)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la marca de formato Unicode del control. Si este valor es distinto de cero, el control usa caracteres Unicode. Si este valor es cero, el control usa caracteres ANSI.

## <a name="remarks"></a>Comentarios

Consulte los comentarios de [**CCM \_ GETUNICODEFORMAT para**](ccm-getunicodeformat.md) obtener una explicación de este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LVM \_ SETUNICODEFORMAT**](lvm-setunicodeformat.md)
</dt> </dl>

 

 





