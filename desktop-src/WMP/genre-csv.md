---
title: genre.csv
description: genre.csv
ms.assetid: e05517f4-a69b-4db7-943d-3490253b92f3
keywords:
- Windows Media Player tiendas en línea, genre.csv
- tiendas en línea, genre.csv
- Escriba 1 tiendas en línea, genre.csv
- genre.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a077cadccc0b2da318e60ca2e0636d96319e5b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994438"
---
# <a name="genrecsv"></a>genre.csv

Este archivo contiene una entrada para cada género representado en el catálogo. Cada entrada es una fila compuesta por los campos delimitados por tabuladores que se describen en la tabla siguiente. Los campos deben aparecer en el orden mostrado.

Todos los campos de genre.csv son obligatorios.

En la columna formato de la tabla siguiente se describe la forma en que se da formato a cada campo de texto Unicode. No hace referencia al tipo de datos del contenido. Por ejemplo, si se indica Integer en la columna Format, significa que el campo contiene una cadena Unicode que representa un valor entero, en lugar de un entero real.



| Campo             | Formato                                                    | Descripción                                                                                                                                        |
|-------------------|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ID. de género         | Entero no negativo. Ejemplo: 22<br/>               | Identificador del género, único en genre.csv. Debe ser inferior a 2 ^ 32. Es posible un máximo de 64 géneros.                                             |
| GenreTitle        | Cadena Unicode. Ejemplo: Rock<br/>                   | Nombre para mostrar del género.                                                                                                                                |
| FeedsAreAvailable | Booleano. formato: \[ 0 \| 1\]<br/> Ejemplo: 0<br/> | Indica si el comportamiento de reproducción de radio es posible al saltar a una fuente.                                                                          |
| HasComposer       | Booleano. formato: \[ 0 \| 1\]<br/> Ejemplo: 1<br/> | True si este género debe guardar la información del compositor en el catálogo. Si no se establece, la información de compositor se omite y no se compila en el catálogo. |



 

 

 





