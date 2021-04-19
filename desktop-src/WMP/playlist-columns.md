---
title: Lista de reproducción. columnas
description: El atributo Columns define las columnas que aparecen en el elemento de lista de reproducción.
ms.assetid: a805ee06-cf73-4eab-bcda-c374e55cd11a
keywords:
- Lista de reproducción. columnas Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.columns
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcc5f8ef5dc76428ca892d079b60692e6949a5ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708290"
---
# <a name="playlistcolumns"></a>Lista de reproducción. columnas

El atributo **Columns** define las columnas que aparecen en el elemento de **lista de reproducción** .

``` syntax
        elementID.columns
```

## <a name="possible-values"></a>Valores posibles

Este atributo es una **cadena** de lectura/escritura con el siguiente formato:

nombre de la base de BD \_ = \_ nombre descriptivo; nombre de la base de BD \_ = \_ nombre descriptivo;

\_Nombre descriptivo es el valor que se muestra en el encabezado de columna del elemento playlist y DB \_ Name es un valor de la tabla siguiente. Tenga en cuenta que un elemento de lista de reproducción puede ser un elemento multimedia de la biblioteca o de un CD, o puede ser otra **lista de reproducción** que sea creada por el usuario o tomada de un CD. Algunas columnas solo son válidas con determinados elementos de lista de reproducción, como se indica en la columna Descripción.



| Value             | Descripción                                                                                                             |
|-------------------|-------------------------------------------------------------------------------------------------------------------------|
| Álbum             | Nombre del álbum. Se usa solo con elementos multimedia.                                                                      |
| Artistas            | Nombre del intérprete. No se utiliza con listas de reproducción creadas por el usuario.                                                           |
| Autor            | Nombre del intérprete.                                                                                                 |
| Bitrate           | La velocidad de bits del contenido. Solo se usa con elementos multimedia de la biblioteca.                                               |
| CDTrackEnabled    | Indica si la pista del CD está habilitada. Solo se utiliza con elementos multimedia de CD.                                               |
| Activada           | Reservado para uso futuro.                                                                                                |
| Copyright         | Copyright de la lista de reproducción. No se utiliza con listas de reproducción de CD o elementos multimedia.                                               |
| CreationDate      | Fecha y hora en que se creó la entrada en la biblioteca. Solo se usa con elementos de la biblioteca.                     |
| DigitallySecure   | Indica si el elemento está protegido con el administrador de derechos de Windows Media. Solo se usa con elementos multimedia de la biblioteca. |
| Duration          | La duración del elemento multimedia.                                                                                         |
| FileType          | Reservado para uso futuro.                                                                                                |
| Género             | El género de la lista de reproducción. No se utiliza con listas de reproducción de CDs.                                                            |
| MediaAttribute    | Reservado para uso futuro.                                                                                                |
| MediaType         | Tipo del elemento multimedia (audio o vídeo).                                                                            |
| Metadatasource    | El origen de los metadatos de esta pista de CD (AMG, WindowsMedia.com, etc.). Solo se utiliza con elementos multimedia de CD.         |
| ModifiedBy        | Reservado para uso futuro.                                                                                                |
| Nombre              | Nombre de la lista de reproducción.                                                                                               |
| OriginalIndex     | Si es aplicable, el identificador de pista de CD correspondiente. Solo se utiliza con elementos multimedia de CD.                                    |
| PlayCount         | Número de veces que el contenido se ha reproducido hasta el final. Solo se usa con elementos multimedia de la biblioteca.        |
| PlaylistAttribute | Reservado para uso futuro.                                                                                                |
| Rating            | Reservado para uso futuro.                                                                                                |
| SourceURL         | La ruta de acceso o dirección URL del contenido. Solo se usa con elementos multimedia de la biblioteca.                                            |
| Status            | Estado de copia de una pista de CD que se va a copiar. Solo se utiliza con elementos multimedia de CD.                                           |
| Estilo             | Reservado para uso futuro.                                                                                                |
| TABLA DE CONTENIDO               | Si es aplicable, el identificador de la tabla de contenido del CD correspondiente. No se utiliza con listas de reproducción creadas por el usuario.                 |



 

## <a name="remarks"></a>Observaciones

Si una de las columnas no existe en la biblioteca, se deja en blanco.

Se puede especificar un máximo de 31 columnas.

Si especifica una columna duplicada, los datos de la primera columna estarán alineados a la izquierda, pero todas las demás columnas duplicadas estarán alineadas a la derecha. Por ejemplo, si tiene dos columnas de duración, los datos se alinean a la izquierda en la primera y la alineación a la derecha en el segundo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**Lista de reproducción. columnsVisible**](playlist-columnsvisible.md)
</dt> </dl>

 

 





