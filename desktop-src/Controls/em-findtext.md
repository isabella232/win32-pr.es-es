---
title: EM_FINDTEXT mensaje (Richedit.h)
description: 'EM_FINDTEXT mensaje: busca texto dentro de un control de edición enriquecido.'
ms.assetid: f19e19a0-d8dd-4d31-b76d-f1f09577dd2d
keywords:
- EM_FINDTEXT mensaje Controles de Windows
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
ms.openlocfilehash: 452d4e2534fb05cbbbf4c02ac4146f2f8914c9bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109853"
---
# <a name="em_findtext-message"></a>Mensaje \_ EM FINDTEXT

Busca texto dentro de un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifique los parámetros de la operación de búsqueda. Este parámetro puede ser uno o varios de los valores siguientes.



| Valor                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <dt>**FR \_ DOWN**</dt> </dl>                               | Microsoft Rich Edit 2.0 y versiones posteriores: si se establece, la búsqueda va desde el final de la selección actual hasta el final del documento. Si no se establece, la búsqueda es desde el final de la selección actual hasta el principio del documento. <br/> Edición enriquecte de Microsoft 1.0: se omite la marca FR \_ DOWN. La búsqueda siempre está desde el final de la selección actual hasta el final del documento.<br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <dt>**FR \_ MATCHALEFHAMZA**</dt> </dl> | Microsoft Rich Edit 3.0 y versiones posteriores: si se establece, la búsqueda diferencia entre los alefs árabes con acentos diferentes. Si no se establece, el carácter alef coincide solo con todos los alefs. <br/>                                                                                                                                                                                                      |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <dt>**FR \_ MATCHDIAC**</dt> </dl>                | Microsoft Rich Edit 3.0 y versiones posteriores: si se establece, la operación de búsqueda tiene en cuenta las marcas diacríticas en árabe y hebreo. Si no se establece, se omiten las marcas diacríticas. <br/>                                                                                                                                                                                                                             |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <dt>**FR \_ MATCHKASHIDA**</dt> </dl>       | Microsoft Rich Edit 3.0 y versiones posteriores: si se establece, la operación de búsqueda considera kashidas en árabe. Si no se establece, se omiten las kashidas. <br/>                                                                                                                                                                                                                                                          |
| <span id="FR_MATCHWIDTH"></span><span id="fr_matchwidth"></span><dl> <dt>**FR \_ MATCHWIDTH**</dt> </dl>             | Windows 8: si se establece, las versiones de un solo byte y de doble byte del mismo carácter se consideran no iguales.<br/>                                                                                                                                                                                                                                                                          |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <dt>**FR \_ WHOLEWORD**</dt> </dl>                | Si se establece, la operación busca solo palabras enteras que coincidan con la cadena de búsqueda. Si no se establece, la operación también busca fragmentos de palabras que coincidan con la cadena de búsqueda.<br/>                                                                                                                                                                                                             |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Estructura [**FINDTEXT**](/windows/win32/api/richedit/ns-richedit-findtexta) que contiene información sobre la operación de búsqueda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se encuentra la cadena de destino, el valor devuelto es la posición de base cero del primer carácter de la coincidencia. Si no se encuentra el destino, el valor devuelto es -1.

## <a name="remarks"></a>Comentarios

El **miembro cpMin** de **FINDTEXT.chrg** siempre especifica el punto inicial de la búsqueda y **cpMax** especifica el punto final. Al buscar hacia atrás, **cpMin** debe ser igual o mayor que **cpMax**. Al buscar hacia delante, un valor de -1 en **cpMax** amplía el intervalo de búsqueda al final del texto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**FINDTEXT**](/windows/win32/api/richedit/ns-richedit-findtexta)
</dt> </dl>

 

 





