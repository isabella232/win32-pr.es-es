---
title: Qué es una interfaz COM
description: Qué es una interfaz COM
ms.assetid: 36f27a58-cc63-4b67-bdcb-8f9a19650c6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da703569beae7a9aa2fc41bcea0214cc9aa488ad
ms.sourcegitcommit: 8eac40ea4d87a85e036ed5bbffec7b7a3dab39ec
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2019
ms.locfileid: "104419223"
---
# <a name="what-is-a-com-interface"></a>¿Qué es una interfaz COM?

Si conoce C# o Java, las interfaces deberían ser un concepto conocido. Una *interfaz* define un conjunto de métodos que un objeto puede admitir, sin indicar nada sobre la implementación. La interfaz marca un límite sin cifrar entre el código que llama a un método y el código que implementa el método. En términos de ciencia informática, el autor de la llamada se *desacopla* de la implementación de.

![Ilustración que muestra el límite de la interfaz entre un objeto y una aplicación](images/com01.png)

En C++, el equivalente más cercano a una interfaz es una clase virtual pura, es decir, una clase que solo contiene métodos virtuales puros y ningún otro miembro. Este es un ejemplo hipotético de una interfaz:

```C++
// The following is not actual COM.

// Pseudo-C++:

interface IDrawable
{
    void Draw();
};
```

La idea de este ejemplo es que se pueden dibujar un conjunto de objetos en alguna biblioteca de gráficos. La `IDrawable` interfaz define las operaciones que cualquier objeto dibujable debe admitir. (Por Convención, los nombres de interfaz empiezan por "I"). En este ejemplo, la `IDrawable` interfaz define una única operación: `Draw` .

Todas las interfaces son *abstractas*, por lo que un programa no pudo crear una instancia de un `IDrawable` objeto como tal. Por ejemplo, el código siguiente no se compilaría.

```C++
IDrawable draw;
draw.Draw();
```

En su lugar, la biblioteca de gráficos proporciona objetos que *implementan* la `IDrawable` interfaz. Por ejemplo, la biblioteca podría proporcionar un objeto de forma para dibujar formas y un objeto de mapa de bits para dibujar imágenes. En C++, esto se hace heredando de una clase base abstracta común:

```C++
class Shape : public IDrawable
{
public:
    virtual void Draw();    // Override Draw and provide implementation.
};

class Bitmap : public IDrawable
{
public:
    virtual void Draw();    // Override Draw and provide implementation.
};
```

Las `Shape` `Bitmap` clases y definen dos tipos distintos de objeto dibujable. Cada clase hereda de `IDrawable` y proporciona su propia implementación del `Draw` método. Naturalmente, las dos implementaciones pueden diferir considerablemente. Por ejemplo, el `Shape::Draw` método puede rasterizar un conjunto de líneas, mientras que `Bitmap::Draw` podría fundir una matriz de píxeles.

Un programa que utiliza esta biblioteca de gráficos manipularía los `Shape` `Bitmap` objetos y a través `IDrawable` de punteros, en lugar de usar `Shape` directamente los `Bitmap` punteros o.

```C++
IDrawable *pDrawable = CreateTriangleShape();

if (pDrawable)
{
    pDrawable->Draw();
}
```

Este es un ejemplo en el que se recorre una matriz de `IDrawable` punteros. La matriz puede contener una variedad heterogénea de formas, mapas de bits y otros objetos gráficos, siempre que se herede cada objeto de la matriz `IDrawable` .

```C++
void DrawSomeShapes(IDrawable **drawableArray, size_t count)
{
    for (size_t i = 0; i < count; i++)
    {
        drawableArray[i]->Draw();
    }
}
```

Un punto clave sobre COM es que el código de llamada nunca ve el tipo de la clase derivada. En otras palabras, nunca se debe declarar una variable de tipo `Shape` o `Bitmap` en el código. Todas las operaciones realizadas en formas y mapas de bits se realizan mediante `IDrawable` punteros. De esta forma, COM mantiene una separación estricta entre la interfaz y la implementación. Los detalles de implementación de `Shape` las `Bitmap` clases y pueden cambiar (por ejemplo, para corregir errores o agregar nuevas capacidades) sin realizar cambios en el código de llamada.

En una implementación de C++, las interfaces se declaran utilizando una clase o estructura.

> [!Note]  
> Los ejemplos de código de este tema están diseñados para transmitir conceptos generales, no prácticas del mundo real. La definición de nuevas interfaces COM está fuera del ámbito de esta serie, pero no se definió una interfaz directamente en un archivo de encabezado. En su lugar, se define una interfaz COM mediante un lenguaje denominado lenguaje de definición de interfaz (IDL). Un compilador IDL procesa el archivo IDL, que genera un archivo de encabezado de C++.

```C++
class IDrawable
{
public:
    virtual void Draw() = 0;
};
```

Al trabajar con COM, es importante recordar que las interfaces no son objetos. Son colecciones de métodos que los objetos deben implementar. Varios objetos pueden implementar la misma interfaz, tal y como se muestra en los `Shape` `Bitmap` ejemplos y. Además, un objeto puede implementar varias interfaces. Por ejemplo, la biblioteca de gráficos puede definir una interfaz denominada `ISerializable` que admita guardar y cargar objetos gráficos. Ahora, considere las siguientes declaraciones de clase:

```C++
// An interface for serialization.
class ISerializable
{
public:
    virtual void Load(PCWSTR filename) = 0;    // Load from file.
    virtual void Save(PCWSTR filename) = 0;    // Save to file.
};

// Declarations of drawable object types.

class Shape : public IDrawable
{
    ...
};

class Bitmap : public IDrawable, public ISerializable
{
    ...
};
```

En este ejemplo, la `Bitmap` clase implementa `ISerializable` . El programa podría utilizar este método para guardar o cargar el mapa de bits. Sin embargo, la `Shape` clase no implementa `ISerializable` , por lo que no expone esa funcionalidad. En el diagrama siguiente se muestran las relaciones de herencia en este ejemplo.

![Ilustración que muestra la herencia de interfaces, con las clases de forma y mapa de bits que apuntan a idrawable, pero solo mapa de bits que apunta a ISerializable](images/com02.png)

En esta sección se ha examinado la base conceptual de las interfaces, pero hasta ahora no hemos visto el código COM real. Comenzaremos con lo primero que cualquier aplicación COM debe hacer: inicializar la biblioteca COM.

## <a name="next"></a>Siguientes

[Inicializar la biblioteca COM](initializing-the-com-library.md)