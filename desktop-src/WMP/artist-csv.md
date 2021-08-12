---
title: artist.csv
description: artist.csv
ms.assetid: 50cf2fbc-28cc-4b13-988e-4c02eb821cfd
keywords:
- Reproductor de Windows Media en línea, artist.csv
- tiendas en línea, artist.csv
- tiendas en línea de tipo 1, artist.csv
- artist.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4192d0817740ac872d1c08989f2f57b4715d65fea6b9a6c9a199dcdabe267e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583062"
---
# <a name="artistcsv"></a>artist.csv

Este archivo contiene una entrada para cada intérprete del catálogo. Cada entrada es una fila formada por los campos delimitados por tabulaciones que se describen en la tabla siguiente. Los campos deben aparecer en el orden indicado.

Todos los campos de artist.csv son obligatorios.

La columna Formato de la tabla siguiente describe la forma en que se formatea cada campo de texto Unicode. No hace referencia al tipo de datos del contenido. Por ejemplo, si Integer se indica en la columna Formato, significa que el campo contiene una cadena Unicode que representa un valor entero, en lugar de un entero real.



| Campo                  | Formato                                            | Descripción                                                                                                |
|------------------------|---------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| ArtistID               | Entero no negativo. Ejemplo: 65832              | Identificador único del intérprete, único dentro de artist.csv. Debe ser menor que 2^32.                        |
| ArtistName             | Cadena Unicode. Ejemplo: Don Don<br/>       | Nombre para mostrar del intérprete.                                                                               |
| LinkedGenreID          | Entero no negativo. Ejemplo: 313<br/>      | GenreID del género principal del intérprete. Debe ser un género principal y no un subgéneo. Solo se permite un valor. |
| LinkedSimilarArtistIDs | N/D                                               | No se usa en esta versión. Debe estar vacío.                                                                 |
| Popularidad             | Puede ser un valor entero o decimal. Ejemplo: 1252.25 | Clasificación de popularidad. Puede ser la posición de la lista cuando se ordena por popularidad.                             |
| FeedsAvailable         | booleano. Formato: \[ 0 \| 1 \] Ejemplo: 0<br/>    | No se usa en esta versión. Debe estar vacío.                                                                 |



 

 

 





