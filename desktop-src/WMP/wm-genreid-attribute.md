---
title: Atributo WM/GenreID
description: El atributo WM/GenreID es un identificador de género compatible con la etiqueta TCON en ID3v2.
ms.assetid: 9b68f9be-1f02-4b14-b052-90657b8800e3
keywords:
- Atributo WM/GenreID Reproductor de Windows Media
topic_type:
- apiref
api_name:
- WM/GenreID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52fdb409453bbdc6a30026b5d36cb35bbaeb2a21264e5049c9e5fff520aea08b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118332331"
---
# <a name="wmgenreid-attribute"></a>Atributo WM/GenreID

El **atributo WM/GenreID** es un identificador de género compatible con la etiqueta TCON en ID3v2.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Atributos de archivo multimedia Windows uso frecuente](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Comentarios

Este atributo solo se almacena en el archivo multimedia digital.

La versión 2 de ID3 es una convención de etiquetado que se diseñó originalmente para MP3. Para más información, consulte el sitio web de la organización [ID3.](https://id3.org/)

La constante Windows SDK de formato multimedia para este atributo es g \_ wszGenreID.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 Reproductor de Windows Media 10 o posterior no admite este atributo<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





