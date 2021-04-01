---
title: Mensaje EM_FINDTEXTEXW (RichEdit. h)
description: Busca texto Unicode dentro de un control Rich Edit.
ms.assetid: 7b90ef06-0395-430e-8b5d-b392481a5f70
keywords:
- EM_FINDTEXTEXW controles de mensajes de Windows
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
ms.openlocfilehash: aaf0857e47c6e98f4be6867ca66baef3472766a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996930"
---
# <a name="em_findtextexw-message"></a>\_Mensaje FINDTEXTEXW em

Busca texto Unicode dentro de un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el comportamiento de la operación de búsqueda. Este parámetro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <dt>**Francés \_**</dt> </dl>                               | Microsoft Rich Edit 2,0 y versiones posteriores: si se establece, la búsqueda se realiza hacia delante desde **FINDTEXTEX. CTA. cpMin**; Si no se establece, la búsqueda se realiza hacia atrás desde **FINDTEXTEX. CTA. cpMin**. <br/> Microsoft Rich Edit 1,0: \_ se omite la marca fr Down. La búsqueda siempre se reenvía.<br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <dt>**MATCHALEFHAMZA de FR \_**</dt> </dl> | Si se establece, la búsqueda distingue entre alefs con diferentes acentos. Si no se establece, el carácter Alef coincide con los alefs árabes y hebreos con acentos diferentes. <br/>                                                                                           |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <dt>**\_MATCHCASE MATCHCASE**</dt> </dl>                | Si se establece, la operación de búsqueda distingue entre mayúsculas y minúsculas. Si no se establece, la operación de búsqueda no distingue entre mayúsculas y minúsculas.<br/>                                                                                                                                                                |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <dt>**FR \_ MATCHDIAC**</dt> </dl>                | Si se establece, la operación de búsqueda tiene en cuenta las marcas diacríticas. Si no se establece, se omiten las marcas diacríticas árabe y hebreo. <br/>                                                                                                                                              |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <dt>**FR \_ MATCHKASHIDA**</dt> </dl>       | Si se establece, la operación de búsqueda tiene en cuenta kashidas. Si no se establece, se omiten los kashidas en árabe y hebreo. <br/>                                                                                                                                                                |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <dt>**FR \_ WHOLEWORD**</dt> </dl>                | Si se establece, la operación busca solo palabras completas que coincidan con la cadena de búsqueda. Si no se establece, la operación también busca fragmentos de palabras que coincidan con la cadena de búsqueda.<br/>                                                                                           |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Estructura [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) que contiene información sobre la operación de búsqueda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se encuentra la cadena de destino, el valor devuelto es la posición de base cero del primer carácter de la coincidencia. Si no se encuentra el destino, el valor devuelto es-1.

## <a name="remarks"></a>Observaciones

Use este mensaje para buscar cadenas Unicode. Para ANSI;, use [**em \_ FINDTEXTEX**](em-findtextex.md).

El miembro **cpMin** de **FINDTEXTEX. CTA** siempre especifica el punto inicial de la búsqueda y **cpMax** especifica el punto final. Al buscar hacia atrás, **cpMin** debe ser igual o mayor que **cpMax**. Al buscar hacia delante, un valor de-1 en **cpMax** extiende el intervalo de búsqueda al final del texto.

Si la operación de búsqueda encuentra una coincidencia, el miembro **chrgText** de la estructura [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) devuelve el intervalo de posiciones de caracteres que contiene el texto coincidente.

**Em \_ FINDTEXTEXW** usa la estructura [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) , mientras que [**em \_ FINDTEXTW**](em-findtextw.md) usa la estructura [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) . La diferencia es que **em \_ FINDTEXTEXW** informa del intervalo de texto que se encontró.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_FINDTEXTW em**](em-findtextw.md)
</dt> </dl>

 

 





