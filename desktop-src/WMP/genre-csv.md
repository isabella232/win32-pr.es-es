---
title: genre.csv
description: genre.csv
ms.assetid: e05517f4-a69b-4db7-943d-3490253b92f3
keywords:
- Reproductor de Windows Media en línea, genre.csv
- tiendas en línea, genre.csv
- tiendas en línea de tipo 1, genre.csv
- genre.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a077cadccc0b2da318e60ca2e0636d96319e5b0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068431"
---
# <a name="genrecsv"></a>genre.csv

Este archivo contiene una entrada para cada género representado en el catálogo. Cada entrada es una fila formada por los campos delimitados por tabulaciones que se describen en la tabla siguiente. Los campos deben aparecer en el orden indicado.

Todos los campos de genre.csv son obligatorios.

La columna Formato de la tabla siguiente describe la forma en que se formatea cada campo de texto Unicode. No hace referencia al tipo de datos del contenido. Por ejemplo, si integer se indica en la columna Formato, significa que el campo contiene una cadena Unicode que representa un valor entero, en lugar de un entero real.



| Campo             | Formato                                                    | Descripción                                                                                                                                        |
|-------------------|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de \_ género         | Entero no negativo. Ejemplo: 22<br/>               | Identificador de género, único dentro de genre.csv. Debe ser menor que 2^32. Es posible un máximo de 64 géneros.                                             |
| GenreTitle        | Cadena Unicode. Ejemplo: Rock<br/>                   | Nombre para mostrar del género.                                                                                                                                |
| FeedsAreAvailable | Boolean.Format: \[ 0 \| 1\]<br/> Ejemplo: 0<br/> | Indica si el comportamiento de "radio play" es posible saltando a una fuente.                                                                          |
| HasComposer       | Boolean.Format: \[ 0 \| 1\]<br/> Ejemplo: 1<br/> | True si este género debe guardar la información del compositor en el catálogo. Si no se establece, la información del compositor se omite y no se compila en el catálogo. |



 

 

 





