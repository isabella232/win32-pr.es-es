---
title: artist.csv
description: artist.csv
ms.assetid: 50cf2fbc-28cc-4b13-988e-4c02eb821cfd
keywords:
- Windows Media Player tiendas en línea, artist.csv
- tiendas en línea, artist.csv
- Escriba 1 tiendas en línea, artist.csv
- artist.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f548c419f01d23b76172c44cd6e50263c4e9197
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357710"
---
# <a name="artistcsv"></a>artist.csv

Este archivo contiene una entrada para cada artista en el catálogo. Cada entrada es una fila compuesta por los campos delimitados por tabuladores que se describen en la tabla siguiente. Los campos deben aparecer en el orden mostrado.

Todos los campos de artist.csv son obligatorios.

En la columna formato de la tabla siguiente se describe la forma en que se da formato a cada campo de texto Unicode. No hace referencia al tipo de datos del contenido. Por ejemplo, si se indica Integer en la columna Format, significa que el campo contiene una cadena Unicode que representa un valor entero, en lugar de un entero real.



| Campo                  | Formato                                            | Descripción                                                                                                |
|------------------------|---------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| ArtistID               | Entero no negativo. Ejemplo: 65832              | Identificador único para el artista, único en artist.csv. Debe ser inferior a 2 ^ 32.                        |
| ArtistName             | Cadena Unicode. Ejemplo: Don funk<br/>       | Nombre para mostrar del intérprete.                                                                               |
| LinkedGenreID          | Entero no negativo. Ejemplo: 313<br/>      | GenreID del género principal del artista. Debe ser un género principal y no un subgénero. Solo se permite un valor. |
| LinkedSimilarArtistIDs | N/D                                               | No se usa en esta versión. Debe estar vacío.                                                                 |
| Popularidad             | Puede ser un valor entero o decimal. Ejemplo: 1252,25 | Clasificación de popularidad. Puede ser la posición en la lista cuando se ordene por popularidad.                             |
| FeedsAvailable         | booleano. Formato: \[ 0 \| 1 \] ejemplo: 0<br/>    | No se usa en esta versión. Debe estar vacío.                                                                 |



 

 

 





