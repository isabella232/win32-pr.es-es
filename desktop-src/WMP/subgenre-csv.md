---
title: subgenre.csv
description: subgenre.csv
ms.assetid: 3ba51cda-0c29-4ce9-9237-8444225349c8
keywords:
- Reproductor de Windows Media en línea, subgenre.csv
- tiendas en línea, subgenre.csv
- tiendas en línea de tipo 1, subgenre.csv
- subgenre.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a10242e955423d75174d04899285dcd3dc20ea2ea4a761d2ab3ba53561c4d41c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122945"
---
# <a name="subgenrecsv"></a>subgenre.csv

Este archivo contiene una entrada para cada subgenes representado en el catálogo. Cada entrada es una fila formada por los campos delimitados por tabulaciones que se describen en la tabla siguiente. Los campos deben aparecer en el orden indicado.

La columna Formato de la tabla siguiente describe la forma en que se formatea cada campo de texto Unicode. No hace referencia al tipo de datos del contenido. Por ejemplo, si integer se indica en la columna Formato, significa que el campo contiene una cadena Unicode que representa un valor entero, en lugar de un entero real.



| Campo             | Requerido | Formato                                                                                            | Descripción                                                                                                                                               |
|-------------------|----------|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| SubGenreID        | Sí      | Entero no negativo.                                                                             | Identificador de subgéneo (id.), único dentro de subgenre.csv. Se permiten hasta 1024 subgéneos.                                                                   |
| SubGenreTitle     | Sí      | Cadena Unicode. Ejemplo: Intelligent Dance Música (IDM)<br/>                                  | Nombre para mostrar del subgéneo.                                                                                                                                    |
| SubGenreSubtitle  | No       | Cadena Unicode. Ejemplo: música electrónica nueva y percutiva que no es del todo pura.<br/> | Describa el significado del nombre para mostrar del subgéneo. Debe tener menos de 64 caracteres.                                                                     |
| FeedsAreAvailable | Sí      | Boolean.Format: \[ 0 \| 1\]<br/> Ejemplo: 0<br/>                                         | Indica si la "reproducción de radio" es posible saltando a una fuente.                                                                                          |
| Id. \_ de género vinculado   | Sí      | Entero no negativo (GenreID). Ejemplo: 12<br/>                                             | El GenreID del género primario. Solo se permite un elemento primario.                                                                                              |
| SortOrderRank     | Sí      | Entero no negativo. Ejemplo: 23<br/>                                                       | Una clasificación, idealmente única, que se usa para ordenar subgéneos en la interfaz de usuario. Si el género primario tiene 10 subgéneos, podría ser un entero de 1 a 10. |



 

 

 





