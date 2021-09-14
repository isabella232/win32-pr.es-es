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
ms.openlocfilehash: 9375dd4a333f0e29d5e8f2721409244cf80f1233
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062154"
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



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**REPASTESPECIAL**](/windows/desktop/api/Richedit/ns-richedit-repastespecial)
</dt> </dl>

 

