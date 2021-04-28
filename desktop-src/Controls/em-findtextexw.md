---
title: EM_FINDTEXTEXW mensaje (Richedit.h)
description: 'EM_FINDTEXTEXW mensaje: busca texto Unicode dentro de un control de edición enriquecido.'
ms.assetid: 7b90ef06-0395-430e-8b5d-b392481a5f70
keywords:
- EM_FINDTEXTEXW de mensajes controles de Windows
topic_type:
- apiref
api_name:
- EM_FINDTEXTEXW
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5278726ca4d3e4748e96d8095a411bcebd5637ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109813"
---
# <a name="em_findtextexw-message"></a>Mensaje \_ EM FINDTEXTEXW

Busca texto Unicode dentro de un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el comportamiento de la operación de búsqueda. Este parámetro puede ser uno o varios de los valores siguientes.



| Valor                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <dt>**FR \_ DOWN**</dt> </dl>                               | Microsoft Rich Edit 2.0 y versiones posteriores: si se establece, la búsqueda se reenvía desde **FINDTEXTEX.chrg.cpMin**; Si no se establece, la búsqueda se hace hacia atrás desde **FINDTEXTEX.chrg.cpMin**. <br/> Microsoft Rich Edit 1.0: se omite la marca FR \_ DOWN. La búsqueda siempre es hacia delante.<br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <dt>**FR \_ MATCHALEFHAMZA**</dt> </dl> | Si se establece, la búsqueda diferencia entre alefs con acentos diferentes. Si no se establece, los alefs árabe y hebreo con acentos diferentes coinciden con el carácter alef. <br/>                                                                                           |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <dt>**FR \_ MATCHCASE**</dt> </dl>                | Si se establece, la operación de búsqueda distingue mayúsculas de minúsculas. Si no se establece, la operación de búsqueda no tiene en cuenta las mayúsculas y minúsculas.<br/>                                                                                                                                                                |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <dt>**FR \_ MATCHDIAC**</dt> </dl>                | Si se establece, la operación de búsqueda considera marcas diacríticas. Si no se establece, se omiten las marcas diacríticas árabe y hebreo. <br/>                                                                                                                                              |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <dt>**FR \_ MATCHKASHIDA**</dt> </dl>       | Si se establece, la operación de búsqueda tiene en cuenta kashidas. Si no se establece, se omiten los kashidas en árabe y hebreo. <br/>                                                                                                                                                                |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <dt>**FR \_ WHOLEWORD**</dt> </dl>                | Si se establece, la operación busca solo palabras enteras que coincidan con la cadena de búsqueda. Si no se establece, la operación también busca fragmentos de palabras que coincidan con la cadena de búsqueda.<br/>                                                                                           |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Estructura [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) que contiene información sobre la operación de búsqueda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se encuentra la cadena de destino, el valor devuelto es la posición de base cero del primer carácter de la coincidencia. Si no se encuentra el destino, el valor devuelto es -1.

## <a name="remarks"></a>Comentarios

Use este mensaje para buscar cadenas Unicode. Para ANSI;, use [**EM \_ FINDTEXTEX**](em-findtextex.md).

El **miembro cpMin** de **FINDTEXTEX.chrg** siempre especifica el punto inicial de la búsqueda y **cpMax** especifica el punto final. Al buscar hacia atrás, **cpMin** debe ser igual o mayor que **cpMax.** Al buscar hacia delante, un valor de -1 en **cpMax** amplía el intervalo de búsqueda hasta el final del texto.

Si la operación de búsqueda encuentra una coincidencia, el miembro **chrgText** de la estructura [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) devuelve el intervalo de posiciones de caracteres que contiene el texto correspondiente.

**EM \_ FINDTEXTEXW usa** la [**estructura FINDTEXTEXW,**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) mientras [**que EM \_ FINDTEXTW usa**](em-findtextw.md) la estructura [**FINDTEXTW.**](/windows/win32/api/richedit/ns-richedit-findtexta) La diferencia es que **EM \_ FINDTEXTEXW informa** del intervalo de texto que se encontró.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows \[ Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**EM \_ FINDTEXTW**](em-findtextw.md)
</dt> </dl>

 

 





