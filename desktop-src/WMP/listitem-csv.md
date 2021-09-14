---
title: listitem.csv
description: listitem.csv
ms.assetid: d8f4bdb3-e7a5-4080-9ae7-555bf3695e9c
keywords:
- Reproductor de Windows Media en línea, listitem.csv
- tiendas en línea, listitem.csv
- tiendas en línea de tipo 1, listitem.csv
- listitem.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe080c5b9426d5394a7d05c1bd293bba84014b0e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967588"
---
# <a name="listitemcsv"></a>listitem.csv

Este archivo contiene entradas para cada elemento incluido en una lista. Cada entrada es una fila compuesta de los campos delimitados por tabulaciones que se describen en la tabla siguiente. Los campos deben aparecer en el orden indicado.

Todos los campos son obligatorios.

La columna Formato de la tabla siguiente describe la forma en que se formatea cada campo de texto Unicode. No hace referencia al tipo de datos del contenido. Por ejemplo, si entero se indica en la columna Formato , significa que el campo contiene una cadena Unicode que representa un valor entero, en lugar de un entero real.



| Campo              | Formato                                          | Descripción                                                                                                            |
|--------------------|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Id. \_ de lista vinculado     | Entero no negativo. Ejemplo: 465<br/>    | Identificador de la lista de la que forma parte este elemento.                                                                               |
| Linked \_ ListItem   | Entero no negativo. Ejemplo: 684793<br/> | Identificador del elemento. Puede ser el identificador de una pista, un álbum, un intérprete, un género, un subgéneo, una fuente de radio u otra lista. |
| ItemPositionInList | Entero no negativo. Ejemplo: 5<br/>      | Posición del elemento dentro de su lista. El primer elemento de una lista está en la posición 0.                                   |



 

 

 





