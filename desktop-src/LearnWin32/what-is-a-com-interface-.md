---
title: Qué es una interfaz COM
description: Qué es una interfaz COM
ms.assetid: 36f27a58-cc63-4b67-bdcb-8f9a19650c6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da703569beae7a9aa2fc41bcea0214cc9aa488ad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159926"
---
# <a name="what-is-a-com-interface"></a>¿Qué es una interfaz COM?

Si conoce C# o Java, las interfaces deben ser un concepto conocido. Una *interfaz* define un conjunto de métodos que un objeto puede admitir, sin dictar nada sobre la implementación. La interfaz marca un límite claro entre el código que llama a un método y el código que implementa el método . En términos de informática, el autor de la llamada *se desacopla* de la implementación.

![ilustración que muestra el límite de interfaz entre un objeto y una aplicación](images/com01.png)

En C++, el equivalente más cercano a una interfaz es una clase virtual pura, es decir, una clase que contiene solo métodos virtuales puros y ningún otro miembro. Este es un ejemplo hipotético de una interfaz:

```C++
// The following is not actual COM.

// Pseudo-C++:

interface IDrawable
{
    void Draw();
};
```

La idea de este ejemplo es que se puede dibujar un conjunto de objetos en alguna biblioteca de gráficos. La `IDrawable` interfaz define las operaciones que cualquier objeto drawable debe admitir. (Por convención, los nombres de interfaz comienzan por "I"). En este ejemplo, la `IDrawable` interfaz define una sola operación: `Draw` .

Todas las interfaces son *abstractas,* por lo que un programa no pudo crear una instancia de `IDrawable` un objeto como tal. Por ejemplo, el código siguiente no se compilaría.

```C++
IDrawable draw;
draw.Draw();
```

En su lugar, la biblioteca de gráficos proporciona objetos *que implementan* la `IDrawable` interfaz . Por ejemplo, la biblioteca podría proporcionar un objeto de forma para dibujar formas y un objeto de mapa de bits para dibujar imágenes. En C++, esto se hace heredando de una clase base abstracta común:

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

Las `Shape` clases y definen dos tipos `Bitmap` distintos de objeto drawable. Cada clase hereda de `IDrawable` y proporciona su propia implementación del método `Draw` . Naturalmente, las dos implementaciones pueden diferir considerablemente. Por ejemplo, el método podría rasterizar un conjunto de líneas, mientras que podría `Shape::Draw` `Bitmap::Draw` cortar una matriz de píxeles.

Un programa que usa esta biblioteca de gráficos manipularía objetos y a través de `Shape` `Bitmap` punteros, en lugar de usar `IDrawable` `Shape` `Bitmap` punteros o directamente.

```C++
IDrawable *pDrawable = CreateTriangleShape();

if (pDrawable)
{
    pDrawable->Draw();
}
```

Este es un ejemplo que recorre en bucle una matriz `IDrawable` de punteros. La matriz puede contener una variedad heterogéneo de formas, mapas de bits y otros objetos gráficos, siempre y cuando cada objeto de la matriz herede `IDrawable` .

```C++
void DrawSomeShapes(IDrawable **drawableArray, size_t count)
{
    for (size_t i = 0; i < count; i++)
    {
        drawableArray[i]->Draw();
    }
}
```

Un punto clave sobre COM es que el código de llamada nunca ve el tipo de la clase derivada. En otras palabras, nunca declararía una variable de tipo `Shape` o `Bitmap` en el código. Todas las operaciones en formas y mapas de bits se realizan mediante `IDrawable` punteros. De esta manera, COM mantiene una separación estricta entre la interfaz y la implementación. Los detalles de implementación de las clases y pueden cambiar(por ejemplo, para corregir errores o agregar nuevas funcionalidades) sin cambios `Shape` en el código de `Bitmap` llamada.

En una implementación de C++, las interfaces se declaran mediante una clase o estructura.

> [!Note]  
> Los ejemplos de código de este tema están diseñados para transmitir conceptos generales, no prácticas del mundo real. La definición de nuevas interfaces COM está fuera del ámbito de esta serie, pero no definiría una interfaz directamente en un archivo de encabezado. En su lugar, una interfaz COM se define mediante un lenguaje denominado Lenguaje de definición de interfaz (IDL). Un compilador de IDL procesa el archivo IDL, que genera un archivo de encabezado de C++.

```C++
class IDrawable
{
public:
    virtual void Draw() = 0;
};
```

Cuando se trabaja con COM, es importante recordar que las interfaces no son objetos. Son colecciones de métodos que los objetos deben implementar. Varios objetos pueden implementar la misma interfaz, como se muestra con los `Shape` ejemplos `Bitmap` y . Además, un objeto puede implementar varias interfaces. Por ejemplo, la biblioteca de gráficos podría definir una interfaz denominada `ISerializable` que admita guardar y cargar objetos gráficos. Ahora considere las siguientes declaraciones de clase:

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

En este ejemplo, la `Bitmap` clase implementa `ISerializable` . El programa podría usar este método para guardar o cargar el mapa de bits. Sin embargo, `Shape` la clase no implementa , por lo que no expone esa `ISerializable` funcionalidad. En el diagrama siguiente se muestran las relaciones de herencia en este ejemplo.

![ilustración que muestra la herencia de interfaz, con las clases de forma y mapa de bits que apuntan a idrawable, pero solo mapa de bits que apunta a iserializable](images/com02.png)

En esta sección se ha examinado la base conceptual de las interfaces, pero hasta ahora no hemos visto código COM real. Comenzaremos por lo primero que cualquier aplicación COM debe hacer: Inicializar la biblioteca COM.

## <a name="next"></a>Siguientes

[Inicialización de la biblioteca COM](initializing-the-com-library.md)