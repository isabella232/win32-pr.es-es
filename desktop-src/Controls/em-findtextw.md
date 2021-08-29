---
title: EM_FINDTEXTW mensaje (Richedit.h)
description: 'EM_FINDTEXTW mensaje: busca texto Unicode dentro de un control de edición enriquecido.'
ms.assetid: 0c1579f5-3b37-4e28-86a2-f4e03e195f38
keywords:
- EM_FINDTEXTW controles de Windows mensaje
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
ms.openlocfilehash: 80d7f84f299ad013051dc0f3e183b855f45c4203206d039cec8480a7dcac3bda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697755"
---
# <a name="em_findtextw-message"></a>Mensaje \_ EM FINDTEXTW

Busca texto Unicode dentro de un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica los parámetros de la operación de búsqueda. Este parámetro puede ser uno o varios de los valores siguientes.



| Valor                                                                                                                                                                     | Significado                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <dt>**FR \_ DOWN**</dt> </dl>                               | Si se establece, la operación busca desde el final de la selección actual hasta el final del documento. Si no se establece, la operación busca desde el final de la selección actual hasta el principio del documento.<br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <dt>**FR \_ MATCHALEFHAMZA**</dt> </dl> | De forma predeterminada, los alefs árabe y hebreo con acentos diferentes coinciden con el carácter alef. Establezca esta marca si desea que la búsqueda diferencie entre los alefs con acentos diferentes.<br/>               |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <dt>**FR \_ MATCHCASE**</dt> </dl>                | Si se establece, la operación de búsqueda distingue mayúsculas de minúsculas. Si no se establece, la operación de búsqueda no tiene en cuenta mayúsculas de minúsculas.<br/>                                                                                                       |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <dt>**FR \_ MATCHDIAC**</dt> </dl>                | De forma predeterminada, se omiten las marcas diacríticas en árabe y hebreo. Establezca esta marca si desea que la operación de búsqueda tenga en cuenta las marcas diacríticas.<br/>                                                                  |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <dt>**FR \_ MATCHKASHIDA**</dt> </dl>       | De forma predeterminada, se omiten los kashidas en árabe y hebreo. Establezca esta marca si desea que la operación de búsqueda considere kashidas.<br/>                                                                                    |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <dt>**FR \_ WHOLEWORD**</dt> </dl>                | Si se establece, la operación busca solo palabras enteras que coincidan con la cadena de búsqueda. Si no se establece, la operación también busca fragmentos de palabras que coincidan con la cadena de búsqueda.<br/>                                  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Estructura [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) que contiene información sobre la operación de búsqueda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se encuentra la cadena de destino, el valor devuelto es la posición de base cero del primer carácter de la coincidencia. Si no se encuentra el destino, el valor devuelto es -1.

## <a name="remarks"></a>Comentarios

**EM \_ FINDTEXTW usa** la [**estructura FINDTEXTW,**](/windows/win32/api/richedit/ns-richedit-findtexta) mientras [**que EM \_ FINDTEXTEXW**](em-findtextexw.md) usa la [**estructura FINDTEXTEXW.**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) La diferencia es que **FINDTEXTEXW informa** del intervalo de texto que se encontró.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EM \_ FINDTEXTEXW**](em-findtextexw.md)
</dt> </dl>

 

 





