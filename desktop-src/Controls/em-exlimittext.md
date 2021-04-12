---
title: Mensaje EM_EXLIMITTEXT (RichEdit. h)
description: Establece un límite superior para la cantidad de texto que el usuario puede escribir o pegar en un control Rich Edit.
ms.assetid: 66fcdbb9-99ac-4122-b89c-be4aef80fbae
keywords:
- EM_EXLIMITTEXT controles de mensajes de Windows
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
ms.openlocfilehash: 49c4ebb554e3aa3139a66ca63970356e1261a23f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491489"
---
# <a name="em_exlimittext-message"></a>\_Mensaje EXLIMITTEXT em

Establece un límite superior para la cantidad de texto que el usuario puede escribir o pegar en un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica la cantidad máxima de texto que se puede escribir. Si este parámetro es cero, se usa el valor máximo predeterminado, que es de 64 KB. Un objeto COM cuenta como un solo carácter.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El límite de texto establecido por el mensaje **em \_ EXLIMITTEXT** no limita la cantidad de texto que se puede transmitir en un control Rich Edit mediante el [**mensaje \_ secuencia em**](em-streamin.md) con *lParam* establecido en texto SF \_ . Sin embargo, limita la cantidad de texto que se puede transmitir en un control Rich Edit mediante el mensaje **\_ secuencia em** con *lParam* establecido en el \_ formato RTF SF.

Antes de que se llame a **em \_ EXLIMITTEXT** , el límite predeterminado para la cantidad de texto que un usuario puede escribir es de 32.767 caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_secuencia em**](em-streamin.md)
</dt> </dl>

 

 





