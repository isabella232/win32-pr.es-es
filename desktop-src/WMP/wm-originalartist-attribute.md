---
title: Atributo WM/OriginalArtist
description: El atributo WM/OriginalArtist es el nombre del artista que generó originalmente el contenido.
ms.assetid: b00e8a1f-0f6a-4ef4-b1bc-01a4d0a28c19
keywords:
- Media Player de Windows de atributos de WM/OriginalArtist
topic_type:
- apiref
api_name:
- WM/OriginalArtist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e7b78bb8b36db22dca1a616c1bdeffc3186b1f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718989"
---
# <a name="wmoriginalartist-attribute"></a>Atributo WM/OriginalArtist

El atributo **WM/OriginalArtist** es el nombre del artista que generó originalmente el contenido.

## <a name="applies-to"></a>Se aplica a

-   [Archivos de música](music-file-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo solo se almacena en un archivo de música que no está en la biblioteca.

La constante del SDK de Windows Media Format para este atributo es g \_ wszWMOriginalArtist.

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





