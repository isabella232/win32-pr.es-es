---
title: EM_FINDWORDBREAK mensaje (Richedit.h)
description: Busca el siguiente salto de palabra antes o después de la posición del carácter especificado o recupera información sobre el carácter en esa posición.
ms.assetid: b5df1365-4672-4c82-8ae4-ebf8b60bf871
keywords:
- EM_FINDWORDBREAK controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_FINDWORDBREAK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6533358c0f4f521bc7021e290dfe11d66d4499e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062215"
---
# <a name="em_findwordbreak-message"></a>Mensaje \_ EM FINDWORDBREAK

Busca el siguiente salto de palabra antes o después de la posición del carácter especificado o recupera información sobre el carácter en esa posición.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica la operación de búsqueda. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                  | Significado                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WB_CLASSIFY"></span><span id="wb_classify"></span><dl> <dt>**WB \_ CLASSIFY**</dt> </dl>                | Devuelve la clase de caracteres y las marcas de salto de palabras del carácter en la posición especificada.<br/>                                                                                                                          |
| <span id="WB_ISDELIMITER"></span><span id="wb_isdelimiter"></span><dl> <dt>**WB \_ ISDELIMITER**</dt> </dl>       | Devuelve **TRUE** si el carácter en la posición especificada es un delimitador o **FALSE** en caso contrario.<br/>                                                                                                                   |
| <span id="WB_LEFT"></span><span id="wb_left"></span><dl> <dt>**WB \_ LEFT**</dt> </dl>                            | Busca el carácter más cercano antes de la posición especificada que comienza una palabra.<br/>                                                                                                                                         |
| <span id="WB_LEFTBREAK"></span><span id="wb_leftbreak"></span><dl> <dt>**WB \_ LEFTBREAK**</dt> </dl>             | Busca el siguiente extremo de la palabra antes de la posición especificada. Este valor es el mismo que WB \_ PREVBREAK.<br/>                                                                                                                       |
| <span id="WB_MOVEWORDLEFT"></span><span id="wb_movewordleft"></span><dl> <dt>**WB \_ MOVEWORDLEFT**</dt> </dl>    | Busca el carácter siguiente que comienza una palabra antes de la posición especificada. Este valor se usa durante el procesamiento de teclas CTRL+FLECHA IZQUIERDA. Este valor es similar a WB \_ MOVEWORDPREV. Vea Comentarios para obtener más información.<br/> |
| <span id="WB_MOVEWORDRIGHT"></span><span id="wb_movewordright"></span><dl> <dt>**WB \_ MOVEWORDRIGHT**</dt> </dl> | Busca el carácter siguiente que comienza una palabra después de la posición especificada. Este valor se usa durante el procesamiento de teclas CTRL+derecha. Este valor es similar a WB \_ MOVEWORDNEXT. Vea Comentarios para obtener más información.<br/>           |
| <span id="WB_RIGHT"></span><span id="wb_right"></span><dl> <dt>**WB \_ RIGHT**</dt> </dl>                         | Busca el carácter siguiente que comienza una palabra después de la posición especificada.<br/>                                                                                                                                             |
| <span id="WB_RIGHTBREAK"></span><span id="wb_rightbreak"></span><dl> <dt>**WB \_ RIGHTBREAK**</dt> </dl>          | Busca el siguiente delimitador de fin de palabra después de la posición especificada. Este valor es el mismo que WB \_ NEXTBREAK.<br/>                                                                                                           |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Posición inicial del carácter de base cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El mensaje devuelve un valor basado en el *parámetro wParam.*



| Código devuelto                                                                                    | Descripción                                                                                                            |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Wparam**</dt> </dl>          | Valor devuelto<br/>                                                                                                |
| <dl> <dt>**WB \_ CLASSIFY**</dt> </dl>    | Devuelve la clase de caracteres y las marcas de salto de palabras del carácter en la posición especificada.<br/>                |
| <dl> <dt>**WB \_ ISDELIMITER**</dt> </dl> | Devuelve **TRUE** si el carácter situado en la posición especificada es un delimitador; de lo contrario, **devuelve FALSE.**<br/> |
| <dl> <dt>**Otros**</dt> </dl>          | Devuelve el índice de caracteres de la palabra break.<br/>                                                              |



 

## <a name="remarks"></a>Observaciones

Si *wParam es* WB LEFT y WB RIGHT, el procedimiento de salto de palabras busca saltos de palabras \_ solo después de \_ delimitadores. Esto coincide con la funcionalidad de un control de edición. Si *wParam* es WB \_ MOVEWORDLEFT o WB MOVEWORDRIGHT, el procedimiento de salto de palabras también compara las clases de caracteres y las marcas de salto \_ de palabras.

Para obtener información sobre las clases de caracteres y las marcas de salto de palabras, vea [Word and Line Breaks](using-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 





