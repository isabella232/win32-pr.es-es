---
title: PLAYLIST.columns
description: El atributo columns define las columnas que aparecen en el elemento PLAYLIST.
ms.assetid: a805ee06-cf73-4eab-bcda-c374e55cd11a
keywords:
- LISTA DE REPRODUCCIÓN.columnas Reproductor de Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.columns
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcc5f8ef5dc76428ca892d079b60692e6949a5ca
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359518"
---
# <a name="playlistcolumns"></a>PLAYLIST.columns

El **atributo columns** define las columnas que aparecen en el elemento **PLAYLIST.**

``` syntax
        elementID.columns
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una cadena de **lectura** y escritura en el formato siguiente:

DB \_ NAME=FRIENDLY \_ NAME;DB \_ NAME=FRIENDLY \_ NAME;

FRIENDLY NAME es el valor que se muestra en el encabezado de columna del elemento \_ PLAYLIST y DB NAME es un valor de la tabla \_ siguiente. Tenga en cuenta que un elemento de lista de reproducción puede ser  un elemento multimedia de la biblioteca o de un CD, o puede ser otra lista de reproducción creada por el usuario o tomada de un CD. Algunas columnas solo son válidas con determinados elementos de lista de reproducción, como se indica en la columna Descripción.



| Value             | Descripción                                                                                                             |
|-------------------|-------------------------------------------------------------------------------------------------------------------------|
| Álbum             | Nombre del álbum. Se usa solo con elementos multimedia.                                                                      |
| Artista            | Nombre del intérprete. No se usa con listas de reproducción creadas por el usuario.                                                           |
| Autor            | Nombre del intérprete.                                                                                                 |
| Bitrate           | Velocidad de bits del contenido. Se usa solo con elementos multimedia de la biblioteca.                                               |
| CDTrackEnabled    | Indica si la pista de CD está habilitada. Solo se usa con elementos multimedia de CD.                                               |
| Activada           | Reservado para uso futuro.                                                                                                |
| Copyright         | El copyright de la lista de reproducción. No se usa con listas de reproducción de CD ni elementos multimedia.                                               |
| CreationDate      | Fecha y hora en que se creó la entrada de la biblioteca. Solo se usa con elementos de la biblioteca.                     |
| DigitallySecure   | Indica si el elemento está protegido con Windows Media Rights Manager. Se usa solo con elementos multimedia de la biblioteca. |
| Duration          | Duración del elemento multimedia.                                                                                         |
| FileType          | Reservado para uso futuro.                                                                                                |
| Género             | Género de la lista de reproducción. No se usa con listas de reproducción de CDs.                                                            |
| MediaAttribute    | Reservado para uso futuro.                                                                                                |
| MediaType         | Tipo del elemento multimedia (audio o vídeo).                                                                            |
| MetadataSource    | Origen de los metadatos de esta pista de CD (AMG, WindowsMedia.com, y así sucesivamente). Solo se usa con elementos multimedia de CD.         |
| ModifiedBy        | Reservado para uso futuro.                                                                                                |
| Nombre              | Nombre de la lista de reproducción.                                                                                               |
| OriginalIndex     | Si procede, el identificador de seguimiento de CD correspondiente. Solo se usa con elementos multimedia de CD.                                    |
| PlayCount         | Número de veces que se ha reproducido el contenido hasta el final. Se usa solo con elementos multimedia de la biblioteca.        |
| PlaylistAttribute | Reservado para uso futuro.                                                                                                |
| Rating            | Reservado para uso futuro.                                                                                                |
| SourceURL         | Ruta de acceso o dirección URL al contenido. Se usa solo con elementos multimedia de la biblioteca.                                            |
| Status            | El estado de copia de una pista de CD que se va a copiar. Solo se usa con elementos multimedia de CD.                                           |
| Estilo             | Reservado para uso futuro.                                                                                                |
| TABLA DE CONTENIDO               | Si procede, el identificador de tabla de contenido de CD correspondiente. No se usa con listas de reproducción creadas por el usuario.                 |



 

## <a name="remarks"></a>Observaciones

Si una de las columnas no existe en la biblioteca, se deja en blanco.

Se puede especificar un máximo de 31 columnas.

Si especifica una columna duplicada, los datos de la primera columna se alinearán a la izquierda, pero todas las demás columnas duplicadas estarán alineadas a la derecha. Por ejemplo, si tiene dos columnas de duración, los datos se alinearán a la izquierda en la primera y a la derecha en la segunda.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ELEMENTO PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.columnsVisible**](playlist-columnsvisible.md)
</dt> </dl>

 

 





