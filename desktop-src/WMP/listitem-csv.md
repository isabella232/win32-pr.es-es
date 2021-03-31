---
title: listitem.csv
description: listitem.csv
ms.assetid: d8f4bdb3-e7a5-4080-9ae7-555bf3695e9c
keywords:
- Windows Media Player tiendas en línea, listitem.csv
- tiendas en línea, listitem.csv
- Escriba 1 tiendas en línea, listitem.csv
- listitem.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe080c5b9426d5394a7d05c1bd293bba84014b0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418567"
---
# <a name="listitemcsv"></a>listitem.csv

Este archivo contiene entradas para cada elemento que se incluye en una lista. Cada entrada es una fila compuesta por los campos delimitados por tabuladores que se describen en la tabla siguiente. Los campos deben aparecer en el orden mostrado.

Todos los campos son obligatorios.

En la columna formato de la tabla siguiente se describe la forma en que se da formato a cada campo de texto Unicode. No hace referencia al tipo de datos del contenido. Por ejemplo, si se indica Integer en la columna Format, significa que el campo contiene una cadena Unicode que representa un valor entero, en lugar de un entero real.



| Campo              | Formato                                          | Descripción                                                                                                            |
|--------------------|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Vínculo \_ ListID     | Entero no negativo. Ejemplo: 465<br/>    | IDENTIFICADOR de la lista de la que forma parte este elemento.                                                                               |
| ListItem vinculado \_   | Entero no negativo. Ejemplo: 684793<br/> | Identificador del elemento. Puede ser el identificador de una pista, un álbum, un artista, un género, un subgénero, una fuente de radio u otra lista. |
| ItemPositionInList | Entero no negativo. Ejemplo: 5<br/>      | Posición del elemento en su lista. El primer elemento de una lista está en la posición 0.                                   |



 

 

 





