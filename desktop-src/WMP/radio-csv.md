---
title: radio.csv
description: radio.csv
ms.assetid: 8b0a1852-b6c9-4598-b1ab-c679362794b3
keywords:
- Windows Media Player tiendas en línea, radio.csv
- tiendas en línea, radio.csv
- Escriba 1 tiendas en línea, radio.csv
- radio.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5271f3a87b32d27996f61e444723f537a09cb827
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357437"
---
# <a name="radiocsv"></a>radio.csv

Este archivo contiene entradas para cada fuente de radio incluida en el catálogo. Cada entrada es una fila compuesta por los campos delimitados por tabuladores que se describen en la tabla siguiente. Los campos deben aparecer en el orden mostrado.

En la columna formato de la tabla siguiente se describe la forma en que se da formato a cada campo de texto Unicode. No hace referencia al tipo de datos del contenido. Por ejemplo, si se indica Integer en la columna Format, significa que el campo contiene una cadena Unicode que representa un valor entero, en lugar de un entero real.



| Campo              | Obligatorio | Formato                                                                                                               | Descripción                                                                                                                        |
|--------------------|----------|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| RadioID            | Sí      | Entero no negativo.                                                                                                | IDENTIFICADOR de la fuente de radio que es única dentro de radio.csv.                                                                             |
| Radiotítulo         | Sí      | Cadena Unicode. Ejemplo: aciertos esenciales<br/>                                                                    | Título de la fuente de radio.                                                                                                                  |
| Radiosubtítulos      | No       | Cadena Unicode. Ejemplo: Top 40.                                                                                     | Subtítulo de la fuente de radio. Suele ser un género o un nombre de subgénero.                                                                               |
| Programmer's         | Sí      | Cadena Unicode. Ejemplo: Terri Lee Duffy                                                                             | Nombre del programador de fuentes de radio. Se recomienda que este campo no supere los 32 caracteres.                                     |
| PrimaryGenre       | Sí      | Entero no negativo.                                                                                                | IDENTIFICADOR del género principal. Solo se permite un valor.                                                                            |
| Ánimo               | Sí      | Cadena Unicode. Ejemplo: divertido; amiable; condiciona sofisticación exuberant<br/>                                       | Serie de adjetivos que describen la música. No hay un punto y coma final después del último adjetivo.                                    |
| Category           | Sí      | Cadena de Unicode                                                                                                       | No se usa en esta versión. Debe estar vacío.                                                                                         |
| Descripción        | No       | Cadena Unicode. Ejemplo: realice una mejora en la música de los intérpretes probados y verdaderos que no disappoint.<br/> | Descripción detallada para la presentación en páginas de propiedades. Se recomienda que este campo no supere los 256 caracteres.                   |
| Popularidad         | Sí      | Entero no negativo o valor decimal. Ejemplo: 31<br/>                                                         | Clasificación de popularidad entre fuentes de radio. Puede ser 0.                                                                                    |
| StarRating         | No       | Float. ejemplo: 3,21<br/>                                                                                       | Opcional. El valor, normalmente entre 0 y 5, se redondea al 1/4 más próximo para su presentación en la interfaz de usuario.                   |
| IsSubscriptionOnly | Sí      | booleano. Puede ser 0 o 1.                                                                                              | Indica si la fuente solo está disponible por suscripción.                                                                      |
| IsRecentlyAdded    | Sí      | booleano. Puede ser 0 o 1.                                                                                              | Indica si esta fuente se ha agregado recientemente.                                                                                    |
| IsFeatured         | Sí      | booleano. Puede ser 0 o 1.                                                                                              | Indica si la fuente está destacada.                                                                                            |
| EditorialGlyph     | Sí      | Entero no negativo. Debe ser 0.                                                                                   | No se usa en esta versión. Debe ser 0.                                                                                             |
| SortOrderRank      | Sí      | Entero no negativo.                                                                                                | Se puede usar para determinar el criterio de ordenación cuando todas las estaciones se enumeran en la interfaz de usuario. Debe ser 0 si no se utiliza este campo. |



 

 

 





