---
title: EM_SETPALETTE mensaje (Richedit.h)
description: Cambia la paleta que usa un control de edición enriquecido para su ventana de presentación.
ms.assetid: c1dc0c24-eaf2-47a8-9bb1-59f37b206feb
keywords:
- EM_SETPALETTE controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETPALETTE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93225a7a550f86bb8b32bf5939a8c7b7aa862ac96c8459bd6bcceb4c6b76e516
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831156"
---
# <a name="em_setpalette-message"></a>Mensaje \_ SETPALETTE DE EM

Cambia la paleta que usa un control de edición enriquecido para su ventana de presentación.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Controle la nueva paleta que usa el control de edición enriquecido.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Comentarios

El control rich edit no comprueba si la nueva paleta es válida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 





