---
title: EM_PASTESPECIAL mensaje (Richedit.h)
description: Pega un formato específico del Portapapeles en un control de edición enriquecido.
ms.assetid: b4b9c1a7-943d-4dc8-bcb9-054c984b82ba
keywords:
- EM_PASTESPECIAL controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_PASTESPECIAL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc1af4dd0566cdf8e256b34f87fcc52ea855bc521c87cbe390e02b8b1cf7b06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412806"
---
# <a name="em_pastespecial-message"></a>MENSAJE \_ PASTESPECIAL DE EM

Pega un formato específico del Portapapeles en un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica los formatos [del Portapapeles.](/windows/desktop/dataxchg/clipboard-formats)

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura REPASTESPECIAL**](/windows/desktop/api/Richedit/ns-richedit-repastespecial) o **NULL.** Si se pega un objeto, la **estructura REPASTESPECIAL** se rellena con el aspecto de presentación deseado. Si *lParam es* **NULL o** el **miembro dwAspect** es cero, el aspecto de presentación utilizado será el contenido del descriptor del objeto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**REPASTESPECIAL**](/windows/desktop/api/Richedit/ns-richedit-repastespecial)
</dt> </dl>

 

