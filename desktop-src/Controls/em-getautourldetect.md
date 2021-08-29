---
title: EM_GETAUTOURLDETECT mensaje (Richedit.h)
description: Indica si la detección automática de direcciones URL está activada en el control de edición enriquecido.
ms.assetid: f723f15c-bf8f-41ab-aef0-bd8f2c0b9e5d
keywords:
- EM_GETAUTOURLDETECT controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_GETAUTOURLDETECT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d60fc8efdc6e554e379a9381239920cf70ef07ffca22240e62cfc6892ca2e636
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019954"
---
# <a name="em_getautourldetect-message"></a>Mensaje \_ EM GETAUTOURLDETECT

Indica si la detección automática de direcciones URL está activada en el control de edición enriquecido.

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

Si la detección automática de direcciones URL está activa, el valor devuelto es 1.

Si la detección automática de direcciones URL está inactiva, el valor devuelto es 0.

## <a name="remarks"></a>Comentarios

Cuando la detección automática de direcciones URL está activa, Microsoft Rich Edit comprueba constantemente el texto escrito para una dirección URL válida. Rich Edit reconoce las direcciones URL que comienzan con estos prefijos:

-   http:
-   file:
-   mailto:
-   Ftp:
-   https:
-   Gopher:
-   Nntp:
-   Prospero:
-   Telnet:
-   Noticias:
-   Wais:
-   Outlook:

Rich Edit también reconoce los nombres de ruta de acceso estándar que comienzan por \\ \\ . Cuando Rich Edit busca una dirección URL, cambia el color del texto de la dirección URL, subraya el texto y notifica al cliente mediante [EN \_ LINK](en-link.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[VÍNCULO \_ DE EN](en-link.md)
</dt> </dl>

 

 





