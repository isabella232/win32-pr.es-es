---
title: Mensaje EM_FINDTEXTEX (RichEdit. h)
description: Busca texto dentro de un control Rich Edit.
ms.assetid: f1bf925b-2776-40b8-9d05-8484daf8d989
keywords:
- EM_FINDTEXTEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_FINDTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e52f7d51ee7a186a8a9e66f11884d6c2e9bca2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150467"
---
# <a name="em_findtextex-message"></a>\_Mensaje FINDTEXTEX em

Busca texto dentro de un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el comportamiento de la operación de búsqueda. Este parámetro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <dt>**Francés \_**</dt> </dl>                               | Microsoft Rich Edit 2,0 y versiones posteriores: si se establece, la búsqueda se realiza hacia delante desde **FINDTEXTEX. CTA. cpMin**; Si no se establece, la búsqueda se realiza hacia atrás desde **FINDTEXTEX. CTA. cpMin**. <br/> Microsoft Rich Edit 1,0: \_ se omite la marca fr Down. La búsqueda siempre se reenvía.<br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <dt>**MATCHALEFHAMZA de FR \_**</dt> </dl> | Microsoft Rich Edit 3,0 y versiones posteriores: si se establece, la búsqueda distingue entre los alefs árabe y hebreo con diferentes acentos. Si no se establece, todos los alefs solo coinciden con el carácter Alef. <br/>                                                                         |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <dt>**\_MATCHCASE MATCHCASE**</dt> </dl>                | Si se establece, la operación de búsqueda distingue entre mayúsculas y minúsculas. Si no se establece, la operación de búsqueda no distingue entre mayúsculas y minúsculas. <br/>                                                                                                                                                               |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <dt>**FR \_ MATCHDIAC**</dt> </dl>                | Microsoft Rich Edit 3,0 y versiones posteriores: si se establece, la operación de búsqueda tiene en cuenta las marcas diacríticas árabe y hebreo. Si no se establece, se omiten las marcas diacríticas. <br/>                                                                                                           |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <dt>**FR \_ MATCHKASHIDA**</dt> </dl>       | Microsoft Rich Edit 3,0 y versiones posteriores: si se establece, la operación de búsqueda tiene en cuenta los kashidas árabe y hebreo. Si no se establece, se omiten los kashidas. <br/>                                                                                                                             |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <dt>**FR \_ WHOLEWORD**</dt> </dl>                | Si se establece, la operación busca solo palabras completas que coincidan con la cadena de búsqueda. Si no se establece, la operación también busca fragmentos de palabras que coincidan con la cadena de búsqueda.<br/>                                                                                           |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Estructura [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) que contiene información sobre la operación de búsqueda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se encuentra la cadena de destino, el valor devuelto es la posición de base cero del primer carácter de la coincidencia. Si no se encuentra el destino, el valor devuelto es-1.

## <a name="remarks"></a>Observaciones

Use este mensaje para buscar cadenas ANSI. Para Unicode, use [**em \_ FINDTEXTEXW**](em-findtextexw.md).

El miembro **cpMin** de **FINDTEXTEX. CTA** siempre especifica el punto inicial de la búsqueda y **cpMax** especifica el punto final. Al buscar hacia atrás, **cpMin** debe ser igual o mayor que **cpMax**. Al buscar hacia delante, un valor de-1 en **cpMax** extiende el intervalo de búsqueda al final del texto.

Si la operación de búsqueda encuentra una coincidencia, el miembro **chrgText** de la estructura [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) devuelve el intervalo de posiciones de caracteres que contiene el texto coincidente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EM ( \_ textobuscado)**](em-findtext.md)
</dt> </dl>

 

 





