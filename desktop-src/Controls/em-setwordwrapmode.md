---
title: EM_SETWORDWRAPMODE mensaje (Richedit.h)
description: Establece las opciones de ajuste de palabras y separación de palabras para un control de edición enriquecido.
ms.assetid: 43703ac8-6ae5-470b-9156-e60330ef97c4
keywords:
- EM_SETWORDWRAPMODE controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETWORDWRAPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0b5c750bb83f4f3fb0c1acfc82b67677c36094df461d10787186177fc891df2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047985"
---
# <a name="em_setwordwrapmode-message"></a>Mensaje \_ EM SETWORDWRAPMODE

Establece las opciones de ajuste de palabras y separación de palabras para un control de edición enriquecido.

> [!Note]  
> Este mensaje solo se admite en versiones en idioma asiático de Microsoft Rich Edit 1.0. No se admite en versiones posteriores.

 

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica uno o varios de los valores siguientes.



| Value                                                                                                                                                         | Significado                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="WBF_WORDWRAP"></span><span id="wbf_wordwrap"></span><dl> <dt>**WBF \_ WORDWRAP**</dt> </dl>    | Habilita operaciones de ajuste de palabras específicas de Asia, como kinsoku en japonés. <br/>                                 |
| <span id="WBF_WORDBREAK"></span><span id="wbf_wordbreak"></span><dl> <dt>**WBF \_ WORDBREAK**</dt> </dl> | Habilita las operaciones de separación de palabras en inglés en japonés y chino. Habilita la operación de separación de palabras de Hangeul.<br/> |
| <span id="WBF_OVERFLOW"></span><span id="wbf_overflow"></span><dl> <dt>**WBF \_ OVERFLOW**</dt> </dl>    | Reconoce la puntuación de desbordamiento. (No se admite actualmente).<br/>                                                |
| <span id="WBF_LEVEL1"></span><span id="wbf_level1"></span><dl> <dt>**WBF \_ LEVEL1**</dt> </dl>          | Establece la tabla de puntuación de nivel 1 como predeterminada.<br/>                                                         |
| <span id="WBF_LEVEL2"></span><span id="wbf_level2"></span><dl> <dt>**WBF \_ LEVEL2**</dt> </dl>          | Establece la tabla de puntuación de nivel 2 como predeterminada.<br/>                                                         |
| <span id="WBF_CUSTOM"></span><span id="wbf_custom"></span><dl> <dt>**WBF \_ CUSTOM**</dt> </dl>          | Establece la tabla de puntuación definida por la aplicación.<br/>                                                            |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje devuelve las opciones actuales de ajuste de palabras y separación de palabras.

## <a name="remarks"></a>Comentarios

El procedimiento de separación de palabras definido por la aplicación no debe enviar este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 





