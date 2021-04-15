---
title: Atributo WM/GenreID
description: El atributo WM/GenreID es un identificador de género compatible con la etiqueta TCON en ID3v2.
ms.assetid: 9b68f9be-1f02-4b14-b052-90657b8800e3
keywords:
- Media Player de Windows de atributos de WM/GenreID
topic_type:
- apiref
api_name:
- WM/GenreID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d31e54805f778a51f345c84654056391ec4052e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708719"
---
# <a name="wmgenreid-attribute"></a>Atributo WM/GenreID

El atributo **WM/GenreID** es un identificador de género compatible con la etiqueta TCON en ID3v2.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Atributos de archivo de Windows Media de uso frecuente](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo solo se almacena en el archivo multimedia digital.

ID3 versión 2 es una Convención de etiquetado que se diseñó originalmente para MP3. Para obtener más información, consulte el [sitio web de la organización ID3](https://id3.org/).

La constante del SDK de Windows Media Format para este atributo es g \_ wszGenreID.

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series Windows Media Player 10 o posterior no admite este atributo<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





