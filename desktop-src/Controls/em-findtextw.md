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
ms.openlocfilehash: 325ff948c4c8f03e8051248f15928d8e8c56e52f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126892316"
---
# <a name="em_findtextw-message"></a>Mensaje \_ EM FINDTEXTW

Busca texto Unicode dentro de un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica los parámetros de la operación de búsqueda. Este parámetro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                                     | Significado                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <dt>**FR \_ DOWN**</dt> </dl>                               | Si se establece, la operación busca desde el final de la selección actual hasta el final del documento. Si no se establece, la operación busca desde el final de la selección actual hasta el principio del documento.<br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <dt>**FR \_ MATCHALEFHAMZA**</dt> </dl> | De forma predeterminada, los alefs árabe y hebreo con acentos diferentes coinciden con el carácter alef. Establezca esta marca si desea que la búsqueda diferencie entre los alefs con acentos diferentes.<br/>               |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <dt>**FR \_ MATCHCASE**</dt> </dl>                | Si se establece, la operación de búsqueda distingue mayúsculas de minúsculas. Si no se establece, la operación de búsqueda no tiene en cuenta las mayúsculas y minúsculas.<br/>                                                                                                       |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <dt>**FR \_ MATCHDIAC**</dt> </dl>                | De forma predeterminada, se omiten las marcas diacríticas árabe y hebreo. Establezca esta marca si desea que la operación de búsqueda tenga en cuenta las marcas diacríticas.<br/>                                                                  |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <dt>**FR \_ MATCHKASHIDA**</dt> </dl>       | De forma predeterminada, se omiten las kashidas árabe y hebreo. Establezca esta marca si desea que la operación de búsqueda considere kashidas.<br/>                                                                                    |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <dt>**FR \_ WHOLEWORD**</dt> </dl>                | Si se establece, la operación solo busca palabras enteras que coincidan con la cadena de búsqueda. Si no se establece, la operación también busca fragmentos de palabras que coincidan con la cadena de búsqueda.<br/>                                  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Estructura [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) que contiene información sobre la operación de búsqueda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se encuentra la cadena de destino, el valor devuelto es la posición de base cero del primer carácter de la coincidencia. Si no se encuentra el destino, el valor devuelto es -1.

## <a name="remarks"></a>Observaciones

**EM \_ FINDTEXTW usa** la [**estructura FINDTEXTW,**](/windows/win32/api/richedit/ns-richedit-findtexta) mientras [**que EM \_ FINDTEXTEXW**](em-findtextexw.md) usa la [**estructura FINDTEXTEXW.**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) La diferencia es que **FINDTEXTEXW informa** del intervalo de texto encontrado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**EM \_ FINDTEXTEXW**](em-findtextexw.md)
</dt> </dl>

 

 





