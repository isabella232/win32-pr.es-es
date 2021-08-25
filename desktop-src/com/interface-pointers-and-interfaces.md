---
title: Interface Pointers and Interfaces (Punteros de interfaz e interfaces)
description: Interface Pointers and Interfaces (Punteros de interfaz e interfaces)
ms.assetid: 8a8671fe-f0b2-4698-8c98-89753fffce0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abeb6040c2e55168fee1aa2c73db0056de557d0ddafaed6499e7da048dfc56de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854375"
---
# <a name="interface-pointers-and-interfaces"></a>Interface Pointers and Interfaces (Punteros de interfaz e interfaces)

Una instancia de una implementación de interfaz es realmente un puntero a una matriz de punteros a métodos, es decir, una tabla de funciones que hace referencia a una implementación de todos los métodos especificados en la interfaz. Los objetos con varias interfaces pueden proporcionar punteros a más de una tabla de funciones. Cualquier código que tenga un puntero a través del cual pueda acceder a la matriz puede llamar a los métodos de esa interfaz.

Hablar con precisión sobre este direccionamiento indirecto múltiple no es conveniente, por lo que en su lugar, el puntero a la tabla de funciones de interfaz que otro objeto debe tener para llamar a sus métodos se denomina simplemente un puntero de *interfaz*. Puede crear manualmente tablas de funciones en una aplicación de C o casi automáticamente mediante Visual C++ (u otros lenguajes orientados a objetos que admitan COM).

Con la compatibilidad del compilador adecuada (que es inherente a C y C++), un cliente puede llamar a un método de interfaz a través de su nombre, no su posición en la matriz. Dado que una interfaz es un tipo, el compilador, dados los nombres de métodos, puede comprobar los tipos de parámetros y los valores devueltos de cada llamada de método de interfaz. Por el contrario, si un cliente usa un esquema de llamada basado en la posición, dicha comprobación de tipos no está disponible, ni siquiera en C o C++.

Cada interfaz es un contrato inmutable de un grupo funcional de métodos. Se hace referencia a una interfaz en tiempo de ejecución con un identificador de interfaz único global (IID). Este IID, que es una instancia específica de un identificador único global (GUID) compatible con COM, permite a un cliente preguntar a un objeto exactamente si admite la semántica de la interfaz, sin sobrecarga innecesaria y sin la confusión que podría surgir en un sistema al tener varias versiones de la misma interfaz con el mismo nombre.

En resumen, es importante comprender qué es una interfaz COM y no:

-   Una interfaz COM no es lo mismo que una clase de C++. La definición virtual pura no lleva ninguna implementación. Si es programador de C++, puede definir la implementación de una interfaz como una clase, pero esto se encuentra bajo el encabezado de detalles de implementación, que COM no especifica. Se debe crear una instancia de un objeto que implemente una interfaz para que exista realmente la interfaz. Además, las distintas clases de objeto pueden implementar una interfaz de forma diferente, pero se pueden usar indistintamente en formato binario, siempre que el comportamiento se ajuste a la definición de la interfaz.
-   Una interfaz COM no es un objeto . Es simplemente un grupo relacionado de funciones y es el estándar binario a través del cual se comunican los clientes y los objetos. Siempre que pueda proporcionar punteros a métodos de interfaz, el objeto se puede implementar en cualquier lenguaje con cualquier representación de estado interna.
-   Las interfaces COM tienen un fuerte tipo. Cada interfaz tiene su propio identificador de interfaz (un GUID), lo que elimina la posibilidad de que se produzca una duplicación con cualquier otro esquema de nomenclatura.
-   Las interfaces COM son inmutables. No se puede definir una nueva versión de una interfaz antigua y asignarle el mismo identificador. Al agregar o quitar métodos de una interfaz o cambiar la semántica, se crea una nueva interfaz, no una nueva versión de una interfaz antigua. Por lo tanto, una nueva interfaz no puede estar en conflicto con una interfaz antigua. Sin embargo, los objetos pueden admitir varias interfaces simultáneamente y pueden exponer interfaces que son revisiones sucesivas de una interfaz, con identificadores diferentes. Por lo tanto, cada interfaz es un contrato independiente y los objetos de todo el sistema no tienen que preocuparse de si la versión de la interfaz a la que llaman es la que esperan. El identificador de interfaz (IID) define el contrato de interfaz de forma explícita y única.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos COM e interfaces](com-objects-and-interfaces.md)
</dt> </dl>

 

 




