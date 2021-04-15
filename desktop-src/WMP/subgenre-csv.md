---
title: subgenre.csv
description: subgenre.csv
ms.assetid: 3ba51cda-0c29-4ce9-9237-8444225349c8
keywords:
- Windows Media Player tiendas en línea, subgenre.csv
- tiendas en línea, subgenre.csv
- Escriba 1 tiendas en línea, subgenre.csv
- subgenre.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98f004eb8cecaaae64a5cc95348ac93e8a7db230
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714220"
---
# <a name="subgenrecsv"></a>subgenre.csv

Este archivo contiene una entrada para cada subgénero representado en el catálogo. Cada entrada es una fila compuesta por los campos delimitados por tabuladores que se describen en la tabla siguiente. Los campos deben aparecer en el orden mostrado.

En la columna formato de la tabla siguiente se describe la forma en que se da formato a cada campo de texto Unicode. No hace referencia al tipo de datos del contenido. Por ejemplo, si se indica Integer en la columna Format, significa que el campo contiene una cadena Unicode que representa un valor entero, en lugar de un entero real.



| Campo             | Obligatorio | Formato                                                                                            | Descripción                                                                                                                                               |
|-------------------|----------|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| SubGenreID        | Sí      | Entero no negativo.                                                                             | Identificador del subgénero (ID.), único dentro de subgenre.csv. Se permiten hasta 1024 subgéneros.                                                                   |
| SubGenreTitle     | Sí      | Cadena Unicode. Ejemplo: música inteligente de baile (IDM)<br/>                                  | Nombre para mostrar del subgénero.                                                                                                                                    |
| SubGenreSubtitle  | No       | Cadena Unicode. Ejemplo: nueva música electrónica de percussive que no es tan pura.<br/> | Describa el significado del nombre para mostrar del subgénero. Debe ser inferior a 64 caracteres.                                                                     |
| FeedsAreAvailable | Sí      | Booleano. formato: \[ 0 \| 1\]<br/> Ejemplo: 0<br/>                                         | Indica si la "reproducción de radio" es posible al saltar a una fuente.                                                                                          |
| GenreID vinculado \_   | Sí      | Entero no negativo (GenreID). Ejemplo: 12<br/>                                             | GenreID del género primario. Solo se permite un elemento primario.                                                                                              |
| SortOrderRank     | Sí      | Entero no negativo. Ejemplo: 23<br/>                                                       | Una clasificación, idealmente única, que se usa para ordenar los subgéneros en la interfaz de usuario. Si el género primario tiene 10 subgéneros, podría ser un entero comprendido entre 1 y 10. |



 

 

 





