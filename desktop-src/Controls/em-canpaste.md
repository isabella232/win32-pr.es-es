---
title: EM_CANPASTE mensaje (Richedit.h)
description: Determina si un control de edición enriquecido puede pegar un formato de Portapapeles especificado.
ms.assetid: 1b858ad8-1312-407b-b12a-c63668ba9f72
keywords:
- EM_CANPASTE controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_CANPASTE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24f2d831cd3b3d04fcb7859d2b5936b7354fbb6b638558d605c9f8c5a6ee6333
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916065"
---
# <a name="em_canpaste-message"></a>Mensaje \_ DE EM CANPASTE

Determina si un control de edición enriquecido puede pegar un formato de Portapapeles especificado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica los formatos [del Portapapeles que](/windows/desktop/dataxchg/clipboard-formats) se probarán. Para probar cualquier formato actualmente en el Portapapeles, establezca este parámetro en cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se puede pegar el formato del Portapapeles, el valor devuelto es un valor distinto de cero.

Si no se puede pegar el formato del Portapapeles, el valor devuelto es cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 

