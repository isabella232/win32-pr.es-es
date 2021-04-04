---
title: Mensaje EM_FINDTEXTW (RichEdit. h)
description: Busca texto Unicode dentro de un control Rich Edit.
ms.assetid: 0c1579f5-3b37-4e28-86a2-f4e03e195f38
keywords:
- EM_FINDTEXTW controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_FINDTEXTW
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73e8bae60269ab3ddb84a17c285c243e00d8117c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803271"
---
# <a name="em_findtextw-message"></a>\_Mensaje FINDTEXTW em

Busca texto Unicode dentro de un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica los parámetros de la operación de búsqueda. Este parámetro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                                     | Significado                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <dt>**Francés \_**</dt> </dl>                               | Si se establece, la operación busca desde el final de la selección actual hasta el final del documento. Si no se establece, la operación busca desde el final de la selección actual hasta el principio del documento.<br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <dt>**MATCHALEFHAMZA de FR \_**</dt> </dl> | De forma predeterminada, los alefs árabe y hebreo con diferentes acentos coinciden con el carácter Alef. Establezca esta marca si desea que la búsqueda distinga entre alefs con distintos acentos.<br/>               |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <dt>**\_MATCHCASE MATCHCASE**</dt> </dl>                | Si se establece, la operación de búsqueda distingue entre mayúsculas y minúsculas. Si no se establece, la operación de búsqueda no distingue entre mayúsculas y minúsculas.<br/>                                                                                                       |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <dt>**FR \_ MATCHDIAC**</dt> </dl>                | De forma predeterminada, se omiten las marcas diacríticas árabe y hebreo. Establezca esta marca si desea que la operación de búsqueda considere las marcas diacríticas.<br/>                                                                  |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <dt>**FR \_ MATCHKASHIDA**</dt> </dl>       | De forma predeterminada, se omiten los kashidas árabe y hebreo. Establezca esta marca si desea que la operación de búsqueda considere kashidas.<br/>                                                                                    |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <dt>**FR \_ WHOLEWORD**</dt> </dl>                | Si se establece, la operación busca solo palabras completas que coincidan con la cadena de búsqueda. Si no se establece, la operación también busca fragmentos de palabras que coincidan con la cadena de búsqueda.<br/>                                  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Estructura [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) que contiene información sobre la operación de búsqueda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se encuentra la cadena de destino, el valor devuelto es la posición de base cero del primer carácter de la coincidencia. Si no se encuentra el destino, el valor devuelto es-1.

## <a name="remarks"></a>Observaciones

**Em \_ FINDTEXTW** usa la estructura [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) , mientras que [**em \_ FINDTEXTEXW**](em-findtextexw.md) usa la estructura [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) . La diferencia es que **FINDTEXTEXW** devuelve el intervalo de texto que se encontró.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_FINDTEXTEXW em**](em-findtextexw.md)
</dt> </dl>

 

 





