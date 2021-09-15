---
title: Escritura fuerte
description: C es un lenguaje débilmente con tipo, es decir, el compilador permite operaciones como la asignación y la comparación entre variables de distintos tipos.
ms.assetid: 5f52adcc-22b9-4b4f-b921-5996d278b10e
keywords:
- Llamada a procedimiento remoto RPC, descrita, escritura de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea859e2d5c160048d79e3c371b47af2bc55e0a65
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473490"
---
# <a name="strong-typing"></a>Escritura fuerte

C es un lenguaje débilmente con tipo, es decir, el compilador permite operaciones como la asignación y la comparación entre variables de distintos tipos. Por ejemplo, C permite convertir el valor de una variable a otro tipo. La capacidad de usar variables de distintos tipos en la misma expresión promueve la flexibilidad y la eficacia.

Un lenguaje fuertemente con tipo impone restricciones en las operaciones entre variables de distintos tipos. En esos casos, el compilador emite un error que prohíbe la operación. Estas directrices estrictas con respecto a los tipos de datos están diseñadas para evitar posibles errores.

La dificultad de usar un lenguaje débilmente con tipo, como C, para las llamadas a procedimientos remotos es que las aplicaciones distribuidas se pueden ejecutar en varios equipos diferentes con compiladores de C diferentes y arquitecturas diferentes. Cuando una aplicación se ejecuta en un solo equipo, no tiene que preocuparse del formato de datos interno porque los datos se controlan de forma coherente. Sin embargo, en un entorno informático distribuido, los distintos equipos pueden usar definiciones diferentes para sus tipos de datos base. Por ejemplo, algunos equipos definen el tipo **int,** por lo que su representación interna es de 16 bits, mientras que otros equipos usan 32 bits. Una arquitectura de equipo, conocida como "little endian", asigna el byte menos significativo de datos a la dirección de memoria más baja y el byte más significativo a la dirección más alta. Otra arquitectura, conocida como "big endian", asigna el byte menos significativo a la dirección de memoria más alta asociada a los datos.

Las llamadas a procedimientos remotos requieren un control estricto sobre los tipos de parámetro. Para controlar la transmisión y conversión de datos a través de la red, MIDL aplica estrictamente restricciones de tipo para los datos transferidos a través de la red. Por esta razón, MIDL incluye un conjunto de tipos [base bien definidos.](base-types.md) MIDL exige la escritura fuerte al exigir el uso de palabras clave que definen inequívocamente el tamaño y el tipo de datos. El efecto más visible de la escritura fuerte es que MIDL no permite variables del tipo **void. \***

En los temas siguientes, en esta sección se tratan las características del lenguaje MIDL que aplican la escritura segura de datos:

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

 

 




