---
title: Interface Pointers and Interfaces (Punteros de interfaz e interfaces)
description: Interface Pointers and Interfaces (Punteros de interfaz e interfaces)
ms.assetid: 8a8671fe-f0b2-4698-8c98-89753fffce0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa23d53f529c43fa7529d657108cc75cb6a23b15
ms.sourcegitcommit: d482e4276cc06515e9fade2f253a257ffc418ce5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/24/2019
ms.locfileid: "105704559"
---
# <a name="interface-pointers-and-interfaces"></a>Interface Pointers and Interfaces (Punteros de interfaz e interfaces)

Una instancia de una implementación de interfaz es, en realidad, un puntero a una matriz de punteros a métodos, es decir, una tabla de funciones que hace referencia a una implementación de todos los métodos especificados en la interfaz. Los objetos con varias interfaces pueden proporcionar punteros a más de una tabla de funciones. Cualquier código que tenga un puntero a través del que pueda tener acceso a la matriz puede llamar a los métodos de esa interfaz.

Hablar precisamente sobre este direccionamiento indirecto no es práctico, por lo que en su lugar, el puntero a la tabla de la función de interfaz que otro objeto debe tener para llamar a sus métodos se llama simplemente un *puntero de interfaz*. Puede crear tablas de funciones de forma manual en una aplicación de C o casi automáticamente mediante Visual C++ (u otros lenguajes orientados a objetos que admitan COM).

Con la compatibilidad del compilador adecuada (que es inherente en C y C++), un cliente puede llamar a un método de interfaz a través de su nombre, no su posición en la matriz. Dado que una interfaz es un tipo, el compilador, dados los nombres de los métodos, puede comprobar los tipos de parámetros y valores devueltos de cada llamada al método de interfaz. En cambio, si un cliente utiliza un esquema de llamada basado en la posición, esta comprobación de tipos no está disponible, ni siquiera en C o C++.

Cada interfaz es un contrato inmutable de un grupo funcional de métodos. Se hace referencia a una interfaz en tiempo de ejecución con un identificador de interfaz único global (IID). Este IID, que es una instancia específica de un identificador único global (GUID) compatible con COM, permite a un cliente preguntar a un objeto con precisión si admite la semántica de la interfaz, sin una sobrecarga innecesaria y sin que la confusión que podría surgir en un sistema tenga varias versiones de la misma interfaz con el mismo nombre.

En Resumen, es importante comprender qué es una interfaz COM y qué no:

-   Una interfaz COM no es lo mismo que una clase de C++. La definición virtual pura no tiene ninguna implementación. Si es un programador de C++, puede definir la implementación de una interfaz como una clase, pero se encuentra en el encabezado de los detalles de implementación, que COM no especifica. Se debe crear una instancia de un objeto que implementa una interfaz para que la interfaz exista realmente. Además, las distintas clases de objeto pueden implementar una interfaz de forma diferente, pero se pueden usar indistintamente en formato binario, siempre y cuando el comportamiento se ajuste a la definición de la interfaz.
-   Una interfaz COM no es un objeto. Es simplemente un grupo relacionado de funciones y es el estándar binario a través del cual se comunican los clientes y los objetos. Siempre y cuando pueda proporcionar punteros a métodos de interfaz, el objeto se puede implementar en cualquier lenguaje con cualquier representación de estado interno.
-   Las interfaces COM están fuertemente tipadas. Cada interfaz tiene su propio identificador de interfaz (un GUID), que elimina la posibilidad de que se produzcan duplicaciones con cualquier otro esquema de nomenclatura.
-   Las interfaces COM son inmutables. No se puede definir una nueva versión de una interfaz antigua y asignarle el mismo identificador. Al agregar o quitar métodos de una interfaz o cambiar la semántica, se crea una nueva interfaz, no una nueva versión de una interfaz antigua. Por lo tanto, una nueva interfaz no puede entrar en conflicto con una interfaz antigua. Sin embargo, los objetos pueden admitir varias interfaces simultáneamente y pueden exponer interfaces que son revisiones sucesivas de una interfaz, con identificadores diferentes. Por lo tanto, cada interfaz es un contrato independiente y no es necesario que los objetos del sistema en todo el sistema estén relacionados con si la versión de la interfaz a la que se está llamando es la esperada. El identificador de interfaz (IID) define el contrato de la interfaz de forma explícita y exclusiva.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos e interfaces COM](com-objects-and-interfaces.md)
</dt> </dl>

 

 




