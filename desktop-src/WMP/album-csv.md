---
title: album.csv
description: album.csv
ms.assetid: 7308e849-7227-480e-937a-8e9091bdec98
keywords:
- Windows Media Player tiendas en línea, album.csv
- tiendas en línea, album.csv
- Escriba 1 tiendas en línea, album.csv
- album.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8f8b71dc080e6983817d4e6f146249875887ed9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695268"
---
# <a name="albumcsv"></a>album.csv

Este archivo contiene una entrada para cada álbum incluido en el catálogo. Cada entrada es una fila compuesta por los campos delimitados por tabuladores que se describen en la tabla siguiente. Los campos deben aparecer en el orden mostrado.

Todos los campos de album.csv son obligatorios.

En la columna formato de la tabla siguiente se describe la forma en que se da formato a cada campo de texto Unicode. No hace referencia al tipo de datos del contenido. Por ejemplo, si se indica Integer en la columna Format, significa que el campo contiene una cadena Unicode que representa un valor entero, en lugar de un entero real.



| Campo             | Formato                                                                   | Descripción                                                                                                                                                                                                                                          |
|-------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AlbumID           | Entero no negativo. Ejemplo: 789456<br/>                          | Identificador del álbum, único en album.csv. Debe ser inferior a 2 ^ 32.                                                                                                                                                                           |
| Nombre del álbum         | Cadena Unicode. Ejemplo: mayor aciertos<br/>                         | Título del álbum                                                                                                                                                                                                                                          |
| AlbumArtist       | Entero no negativo. Ejemplo: 34331<br/>                           | ArtistID del artista. Solo se permite un valor. Puede ser el identificador de "varios intérpretes" o similar.                                                                                                                                                    |
| AlbumLabel        | Cadena Unicode. Debe estar vacío.                                         | No se usa en esta versión. Debe estar vacío.                                                                                                                                                                                                           |
| ReleaseDate       | Cadena Unicode, en formato AAAA-MM-DD. Ejemplo: 2005-0-0<br/>        | Fecha de lanzamiento. El valor 0 se permite para día o mes.                                                                                                                                                                                               |
| AlbumPrice        | StringExample Unicode: $12,49<br/>                                 | Precio del álbum. Se debe incluir el símbolo de moneda. La cadena vacía, 0 y, tienen un significado especial. Una cadena vacía indica un precio desconocido. "0" indica que la pista es gratuita. Un guion ('-') indica que no se puede comprar el álbum. |
| LinkedGenreID     | Entero no negativo. Ejemplo: 12<br/>                              | IDENTIFICADOR del género principal del álbum. Solo se permite un valor.                                                                                                                                                                                        |
| LinkedSubGenreIDs | Formato: n; n; n; Ejemplo: 32; 44; 663;<br/>                             | Lista de identificadores de subgéneros asociados. Al final de la lista se permite un punto y coma final.                                                                                                                                                             |
| Popularidad        | Puede ser un entero no negativo o un valor decimal. Ejemplo: 1256,24<br/> | Clasificación de popularidad determinada por el servicio. Puede ser la clasificación de este álbum en la lista de álbumes ordenados por popularidad. se permite 0.                                                                                                              |
| IsRecentlyAdded   | booleano. Puede ser 0 o 1.                                                  | Marca que indica que el álbum se ha agregado recientemente, según lo determinado por el servicio.                                                                                                                                                                    |
| IsFeatured        | booleano. Puede ser 0 o 1.                                                  | Marca que indica que se trata de un álbum destacado.                                                                                                                                                                                                      |
| EditorialGlyph    | Entero no negativo. Debe ser 0.                                       | No se usa es Release. Debe ser 0.                                                                                                                                                                                                                    |
| FeedsAreAvailable | booleano. Puede ser 0 o 1.                                                  | No se usa en esta versión. Debe ser 0.                                                                                                                                                                                                               |



 

 

 





