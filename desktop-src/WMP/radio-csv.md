---
title: radio.csv
description: radio.csv
ms.assetid: 8b0a1852-b6c9-4598-b1ab-c679362794b3
keywords:
- Reproductor de Windows Media en línea, radio.csv
- tiendas en línea, radio.csv
- tiendas en línea de tipo 1, radio.csv
- radio.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5271f3a87b32d27996f61e444723f537a09cb827
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070948"
---
# <a name="radiocsv"></a>radio.csv

Este archivo contiene entradas para cada fuente de radio incluida en el catálogo. Cada entrada es una fila formada por los campos delimitados por tabulaciones que se describen en la tabla siguiente. Los campos deben aparecer en el orden indicado.

La columna Formato de la tabla siguiente describe la forma en que se formatea cada campo de texto Unicode. No hace referencia al tipo de datos del contenido. Por ejemplo, si integer se indica en la columna Formato, significa que el campo contiene una cadena Unicode que representa un valor entero, en lugar de un entero real.



| Campo              | Obligatorio | Formato                                                                                                               | Descripción                                                                                                                        |
|--------------------|----------|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| RadioID            | Sí      | Entero no negativo.                                                                                                | Identificador de la fuente de radio que es única en radio.csv.                                                                             |
| RadioTitle         | Sí      | Cadena Unicode. Ejemplo: Aciertos esenciales<br/>                                                                    | Título de fuente de radio.                                                                                                                  |
| RadioSubtitle      | No       | Cadena Unicode. Ejemplo: Top 40.                                                                                     | Subtítulo de fuente de radio. A menudo es un nombre de género o subgéneo.                                                                               |
| Programador         | Sí      | Cadena Unicode. Ejemplo: Terri Lee Duffy                                                                             | Nombre del programador de la fuente de radio. Se recomienda que este campo no supere los 32 caracteres.                                     |
| PrimaryGenre       | Sí      | Entero no negativo.                                                                                                | Identificador del género principal. Solo se permite un valor.                                                                            |
| Humor               | Sí      | Cadena Unicode. Ejemplo: divertido; que se puede; y, por tanto, y, por tanto, Exuberante<br/>                                       | Una serie de adjetivos que describen la música. Sin punto y coma final después del último adjetivo.                                    |
| Category           | Sí      | Cadena de Unicode                                                                                                       | No se usa en esta versión. Debe estar vacío.                                                                                         |
| Descripción        | No       | Cadena Unicode. Ejemplo: música animada y fácil de usar de los intérpretes que han probado y verdaderos, que no se van a desaperar.<br/> | Descripción fácil de mostrar en las páginas de propiedades. Se recomienda que este campo no supere los 256 caracteres.                   |
| Popularidad         | Sí      | Valor entero o decimal no negativo. Ejemplo: 31<br/>                                                         | Clasificación de popularidad entre las fuentes de radio. Puede ser 0.                                                                                    |
| StarRating         | No       | Float.Example: 3.21<br/>                                                                                       | Opcional. El valor, normalmente entre 0 y 5, se redondea al 1/4 más cercano para mostrarse en la interfaz de usuario.                   |
| IsSubscriptionOnly | Sí      | booleano. Puede ser 0 o 1.                                                                                              | Indica si la fuente solo está disponible por suscripción.                                                                      |
| IsRecentlyAdded    | Sí      | booleano. Puede ser 0 o 1.                                                                                              | Indica si esta fuente se ha agregado recientemente.                                                                                    |
| IsFeatured         | Sí      | booleano. Puede ser 0 o 1.                                                                                              | Indica si la fuente tiene características.                                                                                            |
| EditorialGlyph     | Sí      | Entero no negativo. Debe ser 0.                                                                                   | No se usa en esta versión. Debe ser 0.                                                                                             |
| SortOrderRank      | Sí      | Entero no negativo.                                                                                                | Se puede usar para determinar el criterio de ordenación cuando todas las estaciones aparecen en la interfaz de usuario. Debe ser 0 si no se usa este campo. |



 

 

 





