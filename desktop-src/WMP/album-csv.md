---
title: album.csv
description: album.csv
ms.assetid: 7308e849-7227-480e-937a-8e9091bdec98
keywords:
- Reproductor de Windows Media en línea, album.csv
- tiendas en línea, album.csv
- tiendas en línea de tipo 1, album.csv
- album.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 750926a3d01f8d65d7ed11c69436049e39ea3dabf0e446ede8a8c9dcecc53bec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004205"
---
# <a name="albumcsv"></a>album.csv

Este archivo contiene una entrada para cada álbum incluido en el catálogo. Cada entrada es una fila formada por los campos delimitados por tabulaciones que se describen en la tabla siguiente. Los campos deben aparecer en el orden indicado.

Todos los campos de album.csv son obligatorios.

La columna Formato de la tabla siguiente describe la forma en que se formatea cada campo de texto Unicode. No hace referencia al tipo de datos del contenido. Por ejemplo, si integer se indica en la columna Formato, significa que el campo contiene una cadena Unicode que representa un valor entero, en lugar de un entero real.



| Campo             | Formato                                                                   | Descripción                                                                                                                                                                                                                                          |
|-------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AlbumID           | Entero no negativo. Ejemplo: 789456<br/>                          | Identificador del álbum, único dentro de album.csv. Debe ser menor que 2^32.                                                                                                                                                                           |
| AlbumName         | Cadena Unicode. Ejemplo: Grandes aciertos<br/>                         | Título del álbum                                                                                                                                                                                                                                          |
| AlbumArtist       | Entero no negativo. Ejemplo: 34331<br/>                           | ArtistID del intérprete. Solo se permite un valor. Puede ser el identificador de "Varios intérpretes" o similar.                                                                                                                                                    |
| AlbumLabel        | Cadena Unicode. Debe estar vacío.                                         | No se usa en esta versión. Debe estar vacío.                                                                                                                                                                                                           |
| ReleaseDate       | Cadena Unicode, en formato YYYY-MM-DD. Ejemplo: 2005-0-0<br/>        | Fecha de lanzamiento. El valor 0 se permite para el día o el mes.                                                                                                                                                                                               |
| AlbumPrice        | StringExample unicode: 12,49 USD<br/>                                 | Precio del álbum. Se debe incluir el símbolo de moneda. La cadena vacía, 0 y - tienen un significado especial. Una cadena vacía indica un precio desconocido. "0" indica que la pista es libre. Un guión ('-') indica que no se puede comprar el álbum. |
| LinkedGenreID     | Entero no negativo. Ejemplo: 12<br/>                              | Identificador del género principal del álbum. Solo se permite un valor.                                                                                                                                                                                        |
| LinkedSubGenreIDs | Formato: n;n;n; Ejemplo: 32;44;663;<br/>                             | Lista de los iDs de subgenes asociados. Se permite un punto y coma final al final de la lista.                                                                                                                                                             |
| Popularidad        | Puede ser un valor entero o decimal no negativo. Ejemplo: 1256.24<br/> | Clasificación de popularidad determinada por el servicio. Puede ser la clasificación de este álbum en la lista de álbumes ordenados por popularidad. Se permite 0.                                                                                                              |
| IsRecentlyAdded   | booleano. Puede ser 0 o 1.                                                  | Marca para indicar que el álbum se ha agregado recientemente, según lo determinado por el servicio.                                                                                                                                                                    |
| IsFeatured        | booleano. Puede ser 0 o 1.                                                  | Marca para indicar que se trata de un álbum destacado.                                                                                                                                                                                                      |
| EditorialGlyph    | Entero no negativo. Debe ser 0.                                       | No se usa es release. Debe ser 0.                                                                                                                                                                                                                    |
| FeedsAreAvailable | booleano. Puede ser 0 o 1.                                                  | No se usa en esta versión. Debe ser 0.                                                                                                                                                                                                               |



 

 

 





