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
ms.openlocfilehash: 9d31e54805f778a51f345c84654056391ec4052e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466400"
---
# <a name="wmgenreid-attribute"></a>Atributo WM/GenreID

El **atributo WM/GenreID** es un identificador de género compatible con la etiqueta TCON en ID3v2.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Atributos de archivo multimedia Windows uso frecuente](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo solo se almacena en el archivo multimedia digital.

La versión 2 de ID3 es una convención de etiquetado que se diseñó originalmente para MP3. Para más información, consulte el sitio web de la organización [ID3.](https://id3.org/)

La Windows SDK de formato multimedia para este atributo es g \_ wszGenreID.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 Reproductor de Windows Media 10 o posterior no admite este atributo<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





