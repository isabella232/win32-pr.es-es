---
title: Establecimiento fuerte de tipos
description: C es un lenguaje débilmente tipado, es decir, el compilador permite operaciones como la asignación y la comparación entre variables de tipos diferentes.
ms.assetid: 5f52adcc-22b9-4b4f-b921-5996d278b10e
keywords:
- RPC llamada a procedimiento remoto, descripción, escritura de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea859e2d5c160048d79e3c371b47af2bc55e0a65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994570"
---
# <a name="strong-typing"></a>Establecimiento fuerte de tipos

C es un lenguaje débilmente tipado, es decir, el compilador permite operaciones como la asignación y la comparación entre variables de tipos diferentes. Por ejemplo, C permite que el valor de una variable se convierta en otro tipo. La capacidad de usar variables de tipos diferentes en la misma expresión promueve la flexibilidad y la eficacia.

Un lenguaje fuertemente tipado impone restricciones en las operaciones entre variables de tipos diferentes. En esos casos, el compilador emite un error que prohíbe la operación. Estas instrucciones estrictas relacionadas con los tipos de datos están diseñadas para evitar posibles errores.

La dificultad de usar un lenguaje débilmente tipado, como C para llamadas a procedimientos remotos, es que las aplicaciones distribuidas se pueden ejecutar en varios equipos con compiladores de C diferentes y arquitecturas diferentes. Cuando una aplicación se ejecuta en un solo equipo, no tiene que preocuparse por el formato de datos interno, ya que los datos se administran de forma coherente. Sin embargo, en un entorno de computación distribuida, distintos equipos pueden usar definiciones diferentes para sus tipos de datos base. Por ejemplo, algunos equipos definen el tipo **int** , por lo que su representación interna es de 16 bits, mientras que otros usan 32 bits. Una arquitectura de equipo, conocida como "little endian", asigna el byte menos significativo de los datos a la dirección de memoria más baja y el byte más significativo a la dirección más alta. Otra arquitectura, conocida como "big endian", asigna el byte menos significativo a la dirección de memoria más alta asociada a esos datos.

Las llamadas a procedimientos remotos requieren un control estricto sobre los tipos de parámetro. Para controlar la transmisión y la conversión de datos a través de la red, MIDL exige estrictamente las restricciones de tipos para los datos transferidos a través de la red. Por esta razón, MIDL incluye un conjunto de [tipos base](base-types.md)bien definidos. MIDL exige el establecimiento fuerte de tipos, ya que exige el uso de palabras clave que definen sin ambigüedad el tamaño y el tipo de datos. El efecto más visible de los tipos fuertes es que MIDL no permite variables del tipo **void \***.

En los temas siguientes, en esta sección se describen las características del lenguaje MIDL que aplican tipos de datos seguros:

-   [Tipos base](base-types.md)
-   [Tipos con signo y sin signo](signed-and-unsigned-types.md)
-   [Tipos de caracteres anchos](wide-character-types.md)
-   [Estructuras](structures.md)
-   [Uniones](unions.md)
-   [Tipos enumerados](enumerated-types.md)
-   [Matrices](arrays.md)
-   [Atributos de función](function-attributes.md)
-   [Atributos de campo](field-attributes.md)
-   [Tres tipos de puntero](three-pointer-types.md)
-   [Atributos de tipo](type-attributes.md)

 

 




