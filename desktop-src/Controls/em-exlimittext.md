---
title: EM_EXLIMITTEXT mensaje (Richedit.h)
description: Establece un límite superior en la cantidad de texto que el usuario puede escribir o pegar en un control de edición enriquecido.
ms.assetid: 66fcdbb9-99ac-4122-b89c-be4aef80fbae
keywords:
- EM_EXLIMITTEXT controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_EXLIMITTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98f9879323f3feade3ece536cd130b274b423c98aebedd6b6f5ef1497d995d07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915685"
---
# <a name="em_exlimittext-message"></a>Mensaje \_ EM EXLIMITTEXT

Establece un límite superior en la cantidad de texto que el usuario puede escribir o pegar en un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica la cantidad máxima de texto que se puede especificar. Si este parámetro es cero, se usa el máximo predeterminado, que es de 64 000 caracteres. Un objeto COM cuenta como un solo carácter.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Comentarios

El límite de texto establecido por el mensaje **EM \_ EXLIMITTEXT** no limita la cantidad de texto que se puede transmitir a un control de edición enriquecido mediante el mensaje [**EM \_ STREAMIN**](em-streamin.md) con *lParam* establecido en SF \_ TEXT. Sin embargo, limita la cantidad de texto que se puede transmitir a un control de edición enriquecido mediante el mensaje **\_ EM STREAMIN** con *lParam* establecido en SF \_ RTF.

Antes de llamar a **EM \_ EXLIMITTEXT,** el límite predeterminado para la cantidad de texto que un usuario puede escribir es de 32 767 caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EM \_ STREAMIN**](em-streamin.md)
</dt> </dl>

 

 





