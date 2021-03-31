---
title: Mensaje EM_FINDTEXT (RichEdit. h)
description: Busca texto dentro de un control Rich Edit.
ms.assetid: f19e19a0-d8dd-4d31-b76d-f1f09577dd2d
keywords:
- EM_FINDTEXT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_FINDTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e50034337f05d2df17af777986136881c503d05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996568"
---
# <a name="em_findtext-message"></a>\_Mensaje TEXTOBUSCADO em

Busca texto dentro de un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifique los parámetros de la operación de búsqueda. Este parámetro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <dt>**Francés \_**</dt> </dl>                               | Microsoft Rich Edit 2,0 y versiones posteriores: si se establece, la búsqueda se realiza desde el final de la selección actual hasta el final del documento. Si no se establece, la búsqueda se realiza desde el final de la selección actual hasta el principio del documento. <br/> Microsoft Rich Edit 1,0: \_ se omite la marca fr Down. La búsqueda siempre va desde el final de la selección actual hasta el final del documento.<br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <dt>**MATCHALEFHAMZA de FR \_**</dt> </dl> | Microsoft Rich Edit 3,0 y versiones posteriores: si se establece, la búsqueda distingue entre alefs árabes con diferentes acentos. Si no se establece, todos los alefs solo coinciden con el carácter Alef. <br/>                                                                                                                                                                                                      |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <dt>**FR \_ MATCHDIAC**</dt> </dl>                | Microsoft Rich Edit 3,0 y versiones posteriores: si se establece, la operación de búsqueda tiene en cuenta las marcas diacríticas árabe y hebreo. Si no se establece, se omiten las marcas diacríticas. <br/>                                                                                                                                                                                                                             |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <dt>**FR \_ MATCHKASHIDA**</dt> </dl>       | Microsoft Rich Edit 3,0 y versiones posteriores: si se establece, la operación de búsqueda considera kashidas árabes. Si no se establece, se omiten los kashidas. <br/>                                                                                                                                                                                                                                                          |
| <span id="FR_MATCHWIDTH"></span><span id="fr_matchwidth"></span><dl> <dt>**FR \_ MATCHWIDTH**</dt> </dl>             | Windows 8: si se establece, se considera que las versiones de un solo byte y de doble byte del mismo carácter no son iguales.<br/>                                                                                                                                                                                                                                                                          |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <dt>**FR \_ WHOLEWORD**</dt> </dl>                | Si se establece, la operación busca solo palabras completas que coincidan con la cadena de búsqueda. Si no se establece, la operación también busca fragmentos de palabras que coincidan con la cadena de búsqueda.<br/>                                                                                                                                                                                                             |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Una estructura [**FINDTEXT**](/windows/win32/api/richedit/ns-richedit-findtexta) que contiene información sobre la operación de búsqueda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se encuentra la cadena de destino, el valor devuelto es la posición de base cero del primer carácter de la coincidencia. Si no se encuentra el destino, el valor devuelto es-1.

## <a name="remarks"></a>Observaciones

El miembro **cpMin** de **FINDTEXT. CTA** siempre especifica el punto inicial de la búsqueda y **cpMax** especifica el punto final. Al buscar hacia atrás, **cpMin** debe ser igual o mayor que **cpMax**. Al buscar hacia delante, un valor de-1 en **cpMax** extiende el intervalo de búsqueda al final del texto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**FINDTEXT**](/windows/win32/api/richedit/ns-richedit-findtexta)
</dt> </dl>

 

 





