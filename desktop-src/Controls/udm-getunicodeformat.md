---
title: UDM_GETUNICODEFORMAT mensaje (Commctrl.h)
description: 'UDM_GETUNICODEFORMAT mensaje: recupera la marca de formato de caracteres Unicode para el control.'
ms.assetid: 8c09d37b-95a2-49cd-b578-919f9c39fa8b
keywords:
- UDM_GETUNICODEFORMAT controles de Windows mensaje
topic_type:
- apiref
api_name:
- UDM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbce0af6ad559524d7662a0ce386777a5186777a4cb65b4270fc7c4c9bdff70d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957754"
---
# <a name="udm_getunicodeformat-message"></a>Mensaje \_ GETUNICODEFORMAT de UDM

Recupera la marca de formato de caracteres Unicode para el control .

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

[**UDM \_ SETUNICODEFORMAT**](udm-setunicodeformat.md)
</dt> </dl>

 

 





