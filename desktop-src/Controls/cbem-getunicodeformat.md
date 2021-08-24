---
title: CBEM_GETUNICODEFORMAT mensaje (Commctrl.h)
description: Obtiene la marca de formato de caracteres UNICODE para el control.
ms.assetid: 854ff8d5-6e2f-4918-a6c5-91356a4454af
keywords:
- CBEM_GETUNICODEFORMAT controles de Windows mensaje
topic_type:
- apiref
api_name:
- CBEM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4665877c3a9cae9fc559c55040d1972128dbb7404f59e5c61a5739829aca629
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119699275"
---
# <a name="cbem_getunicodeformat-message"></a>Mensaje \_ GETUNICODEFORMAT de CBEM

Obtiene la marca de formato de caracteres UNICODE para el control.

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



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBEM \_ SETUNICODEFORMAT**](cbem-setunicodeformat.md)
</dt> </dl>

 

 





