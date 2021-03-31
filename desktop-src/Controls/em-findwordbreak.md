---
title: Mensaje EM_FINDWORDBREAK (RichEdit. h)
description: Busca el siguiente salto de palabra antes o después de la posición del carácter especificado o recupera información sobre el carácter que se encuentra en esa posición.
ms.assetid: b5df1365-4672-4c82-8ae4-ebf8b60bf871
keywords:
- EM_FINDWORDBREAK controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491014"
---
# <a name="em_findwordbreak-message"></a>\_Mensaje FINDWORDBREAK em

Busca el siguiente salto de palabra antes o después de la posición del carácter especificado o recupera información sobre el carácter que se encuentra en esa posición.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica la operación de búsqueda. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                  | Significado                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WB_CLASSIFY"></span><span id="wb_classify"></span><dl> <dt>**\_clasificación WB**</dt> </dl>                | Devuelve la clase de caracteres y las marcas de salto de palabra del carácter que se encuentra en la posición especificada.<br/>                                                                                                                          |
| <span id="WB_ISDELIMITER"></span><span id="wb_isdelimiter"></span><dl> <dt>**WB \_ ISDELIMITER**</dt> </dl>       | Devuelve **true** si el carácter que ocupa la posición especificada es un delimitador o **false** en caso contrario.<br/>                                                                                                                   |
| <span id="WB_LEFT"></span><span id="wb_left"></span><dl> <dt>**WB \_ izquierda**</dt> </dl>                            | Busca el carácter más próximo delante de la posición especificada que comienza una palabra.<br/>                                                                                                                                         |
| <span id="WB_LEFTBREAK"></span><span id="wb_leftbreak"></span><dl> <dt>**WB \_ LEFTBREAK**</dt> </dl>             | Busca la siguiente palabra final antes de la posición especificada. Este valor es el mismo que WB \_ PREVBREAK.<br/>                                                                                                                       |
| <span id="WB_MOVEWORDLEFT"></span><span id="wb_movewordleft"></span><dl> <dt>**WB \_ MOVEWORDLEFT**</dt> </dl>    | Busca el siguiente carácter que comienza una palabra antes de la posición especificada. Este valor se utiliza durante el procesamiento de la tecla CTRL + flecha izquierda. Este valor es similar a WB \_ MOVEWORDPREV. Vea Comentarios para obtener más información.<br/> |
| <span id="WB_MOVEWORDRIGHT"></span><span id="wb_movewordright"></span><dl> <dt>**WB \_ MOVEWORDRIGHT**</dt> </dl> | Busca el siguiente carácter que comienza una palabra después de la posición especificada. Este valor se utiliza durante el procesamiento de la tecla CTRL + flecha derecha. Este valor es similar a WB \_ MOVEWORDNEXT. Vea Comentarios para obtener más información.<br/>           |
| <span id="WB_RIGHT"></span><span id="wb_right"></span><dl> <dt>**WB, \_ derecho**</dt> </dl>                         | Busca el siguiente carácter que comienza una palabra después de la posición especificada.<br/>                                                                                                                                             |
| <span id="WB_RIGHTBREAK"></span><span id="wb_rightbreak"></span><dl> <dt>**WB \_ RIGHTBREAK**</dt> </dl>          | Busca el delimitador de final de palabra siguiente después de la posición especificada. Este valor es el mismo que WB \_ NEXTBREAK.<br/>                                                                                                           |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Posición inicial de carácter de base cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El mensaje devuelve un valor basado en el parámetro *wParam* .



| Código devuelto                                                                                    | Descripción                                                                                                            |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**wParam**</dt> </dl>          | Valor devuelto<br/>                                                                                                |
| <dl> <dt>**\_clasificación WB**</dt> </dl>    | Devuelve la clase de caracteres y las marcas de salto de palabra del carácter que se encuentra en la posición especificada.<br/>                |
| <dl> <dt>**WB \_ ISDELIMITER**</dt> </dl> | Devuelve **true** si el carácter que ocupa la posición especificada es un delimitador; en caso contrario, devuelve **false**.<br/> |
| <dl> <dt>**Otros**</dt> </dl>          | Devuelve el índice de carácter del separador de palabras.<br/>                                                              |



 

## <a name="remarks"></a>Observaciones

Si *wParam* es WB \_ left y WB \_ right, el procedimiento de separación de palabras busca saltos de palabra solo después de los delimitadores. Esto coincide con la funcionalidad de un control de edición. Si *wParam* es WB \_ MOVEWORDLEFT o WB \_ MOVEWORDRIGHT, el procedimiento de separación de palabras también compara las clases de caracteres y las marcas de separación de palabras.

Para obtener información sobre las clases de caracteres y las marcas de salto de línea, vea [Word y saltos de línea](using-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





