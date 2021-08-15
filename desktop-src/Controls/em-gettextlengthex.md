---
title: EM_GETTEXTLENGTHEX mensaje (Richedit.h)
description: Calcula la longitud del texto de varias maneras. Normalmente se llama a antes de crear un búfer para recibir el texto del control .
ms.assetid: 42c89b7b-e48d-4517-9993-ce58ff9e4e40
keywords:
- EM_GETTEXTLENGTHEX controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_GETTEXTLENGTHEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba6cf0a094edc2288dbeae6f735e8c10fb72f943f99f9a41b15fc1ef3136168d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540945"
---
# <a name="em_gettextlengthex-message"></a>Mensaje \_ EM GETTEXTLENGTHEX

Calcula la longitud del texto de varias maneras. Normalmente se llama a antes de crear un búfer para recibir el texto del control .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Puntero a una [**estructura GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) que recibe la información de longitud del texto.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El mensaje devuelve el número de **TCHAR** del control de edición, en función de la configuración de las marcas de la estructura [**GETTEXTLENGTHEX.**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) Si se han establecido marcas incompatibles en el **miembro flags,** el mensaje devuelve E \_ INVALIDARG .

## <a name="remarks"></a>Comentarios

Este mensaje es una manera rápida y sencilla de determinar el número de caracteres de la versión Unicode del control de edición enriqueced. Sin embargo, en el caso de una página de códigos de destino que no sea Unicode, es posible que se convierta en una combinación de caracteres de un solo byte y de doble byte.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex)
</dt> </dl>

 

 





