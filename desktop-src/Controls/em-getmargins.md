---
title: EM_GETMARGINS mensaje (Winuser.h)
description: Obtiene los anchos de los márgenes izquierdo y derecho de un control de edición.
ms.assetid: 2482354b-aae0-4abd-8287-65c423f30abb
keywords:
- EM_GETMARGINS controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_GETMARGINS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33746bc44a7b1b0aadd11c573675fedd51e565a557da7601ebe35a4442ddc96c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119541075"
---
# <a name="em_getmargins-message"></a>Mensaje \_ EM GETMARGINS

Obtiene los anchos de los márgenes izquierdo y derecho de un control de edición.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el ancho del margen izquierdo en el LOWORD y el ancho del margen derecho en hiword.

## <a name="remarks"></a>Comentarios

**Edición enriquecte:** No **se admite el mensaje EM \_ GETMARGINS.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EM \_ SETMARGINS**](em-setmargins.md)
</dt> </dl>

 

 





