---
title: Mensaje EM_SETWORDWRAPMODE (RichEdit. h)
description: Establece las opciones de ajuste de palabras y de separación de palabras para un control Rich Edit.
ms.assetid: 43703ac8-6ae5-470b-9156-e60330ef97c4
keywords:
- EM_SETWORDWRAPMODE controles de mensajes de Windows
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
ms.openlocfilehash: cf1dc6f064f52bf2a5f58c71db099f38b9350e63
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079485"
---
# <a name="em_setwordwrapmode-message"></a>\_Mensaje SETWORDWRAPMODE em

Establece las opciones de ajuste de palabras y de separación de palabras para un control Rich Edit.

> [!Note]  
> Este mensaje solo se admite en las versiones en idioma asiático de Microsoft Rich Edit 1,0. No se admite en las versiones posteriores.

 

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica uno o varios de los valores siguientes.



| Value                                                                                                                                                         | Significado                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="WBF_WORDWRAP"></span><span id="wbf_wordwrap"></span><dl> <dt>**WBF \_ WORDWRAP**</dt> </dl>    | Habilita operaciones de ajuste de palabras específicas de Asia, como Kinsoku en japonés. <br/>                                 |
| <span id="WBF_WORDBREAK"></span><span id="wbf_wordbreak"></span><dl> <dt>**WBF \_ WORDBREAK**</dt> </dl> | Habilita las operaciones de división de palabras en inglés en japonés y chino. Habilita la operación de separación de palabras de Hangeul.<br/> |
| <span id="WBF_OVERFLOW"></span><span id="wbf_overflow"></span><dl> <dt>**desbordamiento de WBF \_**</dt> </dl>    | Reconoce la puntuación de desbordamiento. (Actualmente no se admite).<br/>                                                |
| <span id="WBF_LEVEL1"></span><span id="wbf_level1"></span><dl> <dt>**WBF \_ Level1**</dt> </dl>          | Establece la tabla de puntuación de nivel 1 como valor predeterminado.<br/>                                                         |
| <span id="WBF_LEVEL2"></span><span id="wbf_level2"></span><dl> <dt>**WBF \_ LEVEL2**</dt> </dl>          | Establece la tabla de puntuación de nivel 2 como valor predeterminado.<br/>                                                         |
| <span id="WBF_CUSTOM"></span><span id="wbf_custom"></span><dl> <dt>**WBF \_ personalizado**</dt> </dl>          | Establece la tabla de puntuación definida por la aplicación.<br/>                                                            |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje devuelve las opciones actuales de ajuste de palabras y de separación de palabras.

## <a name="remarks"></a>Observaciones

Este mensaje no se debe enviar mediante el procedimiento de separación de palabras definido por la aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





