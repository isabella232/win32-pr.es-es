---
title: TBM_GETUNICODEFORMAT mensaje (Commctrl.h)
description: 'TBM_GETUNICODEFORMAT mensaje: recupera la marca de formato de caracteres Unicode para el control.'
ms.assetid: cecd7e55-f482-4381-bde8-a60b8c5173eb
keywords:
- TBM_GETUNICODEFORMAT controles de Windows mensaje
topic_type:
- apiref
api_name:
- TBM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82e7424a4e561ee8f8be79135309089fe4bb0bf9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166469"
---
# <a name="tbm_getunicodeformat-message"></a>Mensaje \_ GETUNICODEFORMAT de TBM

Recupera la marca de formato de caracteres Unicode para el control .

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TBM \_ SETUNICODEFORMAT**](tbm-setunicodeformat.md)
</dt> </dl>

 

 





