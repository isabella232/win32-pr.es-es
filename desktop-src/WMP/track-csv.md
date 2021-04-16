---
title: track.csv
description: track.csv
ms.assetid: 5ce782b7-5fb8-4e6e-80cb-fa1dd7c47716
keywords:
- Windows Media Player tiendas en línea, track.csv
- tiendas en línea, track.csv
- Escriba 1 tiendas en línea, track.csv
- track.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9826dbcc7b553caba89b2288057b643cdb0712bf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357268"
---
# <a name="trackcsv"></a>track.csv

Este archivo contiene una entrada para cada pista en el catálogo. Cada entrada es una fila compuesta por los campos delimitados por tabuladores que se describen en la tabla siguiente. Los campos deben aparecer en el orden mostrado.

En la columna formato de la tabla siguiente se describe la forma en que se da formato a cada campo de texto Unicode. No hace referencia al tipo de datos del contenido. Por ejemplo, si se indica Integer en la columna Format, significa que el campo contiene una cadena Unicode que representa un valor entero, en lugar de un entero real.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Campo</th>
<th>Obligatorio</th>
<th>Formato</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Elemento TrackID</td>
<td>Sí</td>
<td>Entero no negativo. Ejemplo: 32789<br/></td>
<td>Identificador único proporcionado por el proveedor de contenido. Debe ser inferior a 2 ^ 32. sugerencia de rendimiento: si se numeran consecutivamente los identificadores asignados a las pistas del mismo álbum, la compresión del catálogo será más eficaz. Sin embargo, no se requiere la numeración consecutiva de las pistas de álbum.<br/></td>
</tr>
<tr class="even">
<td>TrackTitle</td>
<td>Sí</td>
<td>Cadena Unicode. Ejemplo: Raygun le Robbers ' Blues '</td>
<td>Nombre de la pista.</td>
</tr>
<tr class="odd">
<td>Duration</td>
<td>Sí</td>
<td>Entero no negativo. Ejemplo: 543<br/></td>
<td>Duración de la pista en segundos.</td>
</tr>
<tr class="even">
<td>TrackNumber</td>
<td>Sí</td>
<td>Entero no negativo. Ejemplo: 7<br/></td>
<td>Número de pista en el álbum de la pista. Los números de seguimiento comienzan en 1 y aumentan entre conjuntos de discos. El número de pista debe ser inferior a 256. Un número de pista mayor o igual que 256 producirá un comportamiento inesperado en Windows Media Player.</td>
</tr>
<tr class="odd">
<td>TrackPrice</td>
<td>Sí</td>
<td>Cadena Unicode. Ejemplo: $0,99.</td>
<td>Precio de seguimiento. Se debe incluir el símbolo de moneda. La cadena vacía, 0 y, tienen un significado especial. Una cadena vacía indica que se desconoce el precio. Un cero en este campo significa que la pista es gratuita y un guión (-) indica que no se puede comprar la pista.</td>
</tr>
<tr class="even">
<td>CanStream</td>
<td>Sí</td>
<td>booleano. Puede ser 0 o 1. ejemplo: 0<br/></td>
<td>Indica si se puede transmitir por secuencias la pista.</td>
</tr>
<tr class="odd">
<td>CanDownload</td>
<td>Sí</td>
<td>booleano. Puede ser 0 o 1. ejemplo: 0<br/></td>
<td>Indica si se puede descargar la pista.</td>
</tr>
<tr class="even">
<td>HasPreviewClip</td>
<td>Sí</td>
<td>booleano. Puede ser 0 o 1. ejemplo: 0<br/></td>
<td>Indica si la pista tiene un clip de vista previa.</td>
</tr>
<tr class="odd">
<td>HasVideoClip</td>
<td>Sí</td>
<td>booleano. Puede ser 0 o 1. ejemplo: 0<br/></td>
<td>Indica si la pista tiene un clip de vídeo.</td>
</tr>
<tr class="even">
<td>ParentalRating</td>
<td>Sí</td>
<td>Enumeración. Puede ser N, E o C. ejemplo: N<br/></td>
<td>Indica la clasificación del Asesor parental. Los valores N, E y C tienen como valor normal, Explicit y Clean.</td>
</tr>
<tr class="odd">
<td>LinkedAlbumID</td>
<td>Sí</td>
<td>Entero no negativo. Debe ser el identificador de un álbum. Ejemplo: 32423</td>
<td>IDENTIFICADOR del álbum que contiene esta pista.
<blockquote>
[!Note]<br />
Cada pista debe pertenecer a un álbum. Es decir, para cada pista, el campo LinkedAlbumID debe ser igual a uno de los identificadores de álbum del archivo album.csv.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>LinkedTrackArtist_ArtistIDs</td>
<td>Sí</td>
<td>Lista de enteros. La lista contiene los identificadores de intérprete, separados por punto y coma. Ejemplo: 41322; 12321; 82123;</td>
<td>Una lista de identificadores que corresponden a los artistas contribuyentes.</td>
</tr>
<tr class="odd">
<td>Composer</td>
<td>No</td>
<td>Cadena Unicode. Ejemplo: Beethoven</td>
<td>Compositor de la pista. Si el género de la pista no tiene establecido el campo HasComposer, se omitirá el valor del campo compositor. Normalmente solo se usa para pistas jazz o clásicas.</td>
</tr>
<tr class="even">
<td>Popularidad</td>
<td>Sí</td>
<td>Entero no negativo o float. ejemplo: 1252,6<br/></td>
<td>Determina la posición de la pista en la lista cuando se ordena por popularidad. Un número menor indica una mayor popularidad.</td>
</tr>
<tr class="odd">
<td>StarRating</td>
<td>No</td>
<td>Float. ejemplo: 4,21<br/></td>
<td>La clasificación por estrellas se redondeará al 1/4 de Media Player Windows más cercano antes de mostrarse en la interfaz de usuario de Windows Media Player.</td>
</tr>
</tbody>
</table>



 

 

 





