---
title: EM_GETIMEOPTIONS mensaje (Richedit.h)
description: Recupera las opciones actuales del Editor de métodos de entrada (IME).
ms.assetid: 81ec89b9-dabd-487e-805e-e3c2e58e3068
keywords:
- EM_GETIMEOPTIONS controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_GETIMEOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aea4513189014969dbfdf69a0ad257cbfde6a4ff99c2499f478c4865100a23c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049065"
---
# <a name="em_getimeoptions-message"></a>Mensaje DE EM \_ GETIMEOPTIONS

Recupera las opciones actuales del Editor de métodos de entrada (IME).

> [!Note]  
> Este mensaje solo se admite en las versiones en idioma asiático de Microsoft Rich Edit 1.0. No se admite en versiones posteriores de Rich Edit.

 

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

Este mensaje devuelve uno o varios de los valores de marca de opción de IME descritos en el [**mensaje EM \_ SETIMEOPTIONS.**](em-setimeoptions.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EM \_ SETIMEOPTIONS**](em-setimeoptions.md)
</dt> </dl>

 

 





