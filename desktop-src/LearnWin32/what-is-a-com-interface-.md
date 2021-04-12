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
# <a name="what-is-a-com-interface"></a><span data-ttu-id="cf1cf-103">¿Qué es una interfaz COM?</span><span class="sxs-lookup"><span data-stu-id="cf1cf-103">What Is a COM Interface?</span></span>

<span data-ttu-id="cf1cf-104">Si conoce C# o Java, las interfaces deberían ser un concepto conocido.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-104">If you know C# or Java, interfaces should be a familiar concept.</span></span> <span data-ttu-id="cf1cf-105">Una *interfaz* define un conjunto de métodos que un objeto puede admitir, sin indicar nada sobre la implementación.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-105">An *interface* defines a set of methods that an object can support, without dictating anything about the implementation.</span></span> <span data-ttu-id="cf1cf-106">La interfaz marca un límite sin cifrar entre el código que llama a un método y el código que implementa el método.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-106">The interface marks a clear boundary between code that calls a method and the code that implements the method.</span></span> <span data-ttu-id="cf1cf-107">En términos de ciencia informática, el autor de la llamada se *desacopla* de la implementación de.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-107">In computer science terms, the caller is *decoupled* from the implementation.</span></span>

![Ilustración que muestra el límite de la interfaz entre un objeto y una aplicación](images/com01.png)

<span data-ttu-id="cf1cf-109">En C++, el equivalente más cercano a una interfaz es una clase virtual pura, es decir, una clase que solo contiene métodos virtuales puros y ningún otro miembro.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-109">In C++, the nearest equivalent to an interface is a pure virtual class—that is, a class that contains only pure virtual methods and no other members.</span></span> <span data-ttu-id="cf1cf-110">Este es un ejemplo hipotético de una interfaz:</span><span class="sxs-lookup"><span data-stu-id="cf1cf-110">Here is a hypothetical example of an interface:</span></span>

```C++
// The following is not actual COM.

// Pseudo-C++:

interface IDrawable
{
    void Draw();
};
```

<span data-ttu-id="cf1cf-111">La idea de este ejemplo es que se pueden dibujar un conjunto de objetos en alguna biblioteca de gráficos.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-111">The idea of this example is that a set of objects in some graphics library are drawable.</span></span> <span data-ttu-id="cf1cf-112">La `IDrawable` interfaz define las operaciones que cualquier objeto dibujable debe admitir.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-112">The `IDrawable` interface defines the operations that any drawable object must support.</span></span> <span data-ttu-id="cf1cf-113">(Por Convención, los nombres de interfaz empiezan por "I"). En este ejemplo, la `IDrawable` interfaz define una única operación: `Draw` .</span><span class="sxs-lookup"><span data-stu-id="cf1cf-113">(By convention, interface names start with "I".) In this example, the `IDrawable` interface defines a single operation: `Draw`.</span></span>

<span data-ttu-id="cf1cf-114">Todas las interfaces son *abstractas*, por lo que un programa no pudo crear una instancia de un `IDrawable` objeto como tal.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-114">All interfaces are *abstract*, so a program could not create an instance of an `IDrawable` object as such.</span></span> <span data-ttu-id="cf1cf-115">Por ejemplo, el código siguiente no se compilaría.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-115">For example, the following code would not compile.</span></span>

```C++
IDrawable draw;
draw.Draw();
```

<span data-ttu-id="cf1cf-116">En su lugar, la biblioteca de gráficos proporciona objetos que *implementan* la `IDrawable` interfaz.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-116">Instead, the graphics library provides objects that *implement* the `IDrawable` interface.</span></span> <span data-ttu-id="cf1cf-117">Por ejemplo, la biblioteca podría proporcionar un objeto de forma para dibujar formas y un objeto de mapa de bits para dibujar imágenes.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-117">For example, the library might provide a shape object for drawing shapes and a bitmap object for drawing images.</span></span> <span data-ttu-id="cf1cf-118">En C++, esto se hace heredando de una clase base abstracta común:</span><span class="sxs-lookup"><span data-stu-id="cf1cf-118">In C++, this is done by inheriting from a common abstract base class:</span></span>

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

<span data-ttu-id="cf1cf-119">Las `Shape` `Bitmap` clases y definen dos tipos distintos de objeto dibujable.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-119">The `Shape` and `Bitmap` classes define two distinct types of drawable object.</span></span> <span data-ttu-id="cf1cf-120">Cada clase hereda de `IDrawable` y proporciona su propia implementación del `Draw` método.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-120">Each class inherits from `IDrawable` and provides its own implementation of the `Draw` method.</span></span> <span data-ttu-id="cf1cf-121">Naturalmente, las dos implementaciones pueden diferir considerablemente.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-121">Naturally, the two implementations might differ considerably.</span></span> <span data-ttu-id="cf1cf-122">Por ejemplo, el `Shape::Draw` método puede rasterizar un conjunto de líneas, mientras que `Bitmap::Draw` podría fundir una matriz de píxeles.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-122">For example, the `Shape::Draw` method might rasterize a set of lines, while `Bitmap::Draw` would blit an array of pixels.</span></span>

<span data-ttu-id="cf1cf-123">Un programa que utiliza esta biblioteca de gráficos manipularía los `Shape` `Bitmap` objetos y a través `IDrawable` de punteros, en lugar de usar `Shape` directamente los `Bitmap` punteros o.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-123">A program using this graphics library would manipulate `Shape` and `Bitmap` objects through `IDrawable` pointers, rather than using `Shape` or `Bitmap` pointers directly.</span></span>

```C++
IDrawable *pDrawable = CreateTriangleShape();

if (pDrawable)
{
    pDrawable->Draw();
}
```

<span data-ttu-id="cf1cf-124">Este es un ejemplo en el que se recorre una matriz de `IDrawable` punteros.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-124">Here is an example that loops over an array of `IDrawable` pointers.</span></span> <span data-ttu-id="cf1cf-125">La matriz puede contener una variedad heterogénea de formas, mapas de bits y otros objetos gráficos, siempre que se herede cada objeto de la matriz `IDrawable` .</span><span class="sxs-lookup"><span data-stu-id="cf1cf-125">The array might contain a heterogeneous assortment of shapes, bitmaps, and other graphics objects, as long as each object in the array inherits `IDrawable`.</span></span>

```C++
void DrawSomeShapes(IDrawable **drawableArray, size_t count)
{
    for (size_t i = 0; i < count; i++)
    {
        drawableArray[i]->Draw();
    }
}
```

<span data-ttu-id="cf1cf-126">Un punto clave sobre COM es que el código de llamada nunca ve el tipo de la clase derivada.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-126">A key point about COM is that the calling code never sees the type of the derived class.</span></span> <span data-ttu-id="cf1cf-127">En otras palabras, nunca se debe declarar una variable de tipo `Shape` o `Bitmap` en el código.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-127">In other words, you would never declare a variable of type `Shape` or `Bitmap` in your code.</span></span> <span data-ttu-id="cf1cf-128">Todas las operaciones realizadas en formas y mapas de bits se realizan mediante `IDrawable` punteros.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-128">All operations on shapes and bitmaps are performed using `IDrawable` pointers.</span></span> <span data-ttu-id="cf1cf-129">De esta forma, COM mantiene una separación estricta entre la interfaz y la implementación.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-129">In this way, COM maintains a strict separation between interface and implementation.</span></span> <span data-ttu-id="cf1cf-130">Los detalles de implementación de `Shape` las `Bitmap` clases y pueden cambiar (por ejemplo, para corregir errores o agregar nuevas capacidades) sin realizar cambios en el código de llamada.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-130">The implementation details of the `Shape` and `Bitmap` classes can change—for example, to fix bugs or add new capabilities—with no changes to the calling code.</span></span>

<span data-ttu-id="cf1cf-131">En una implementación de C++, las interfaces se declaran utilizando una clase o estructura.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-131">In a C++ implementation, interfaces are declared using a class or structure.</span></span>

> [!Note]  
> <span data-ttu-id="cf1cf-132">Los ejemplos de código de este tema están diseñados para transmitir conceptos generales, no prácticas del mundo real.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-132">The code examples in this topic are meant to convey general concepts, not real-world practice.</span></span> <span data-ttu-id="cf1cf-133">La definición de nuevas interfaces COM está fuera del ámbito de esta serie, pero no se definió una interfaz directamente en un archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-133">Defining new COM interfaces is beyond the scope of this series, but you would not define an interface directly in a header file.</span></span> <span data-ttu-id="cf1cf-134">En su lugar, se define una interfaz COM mediante un lenguaje denominado lenguaje de definición de interfaz (IDL).</span><span class="sxs-lookup"><span data-stu-id="cf1cf-134">Instead, a COM interface is defined using a language called Interface Definition Language (IDL).</span></span> <span data-ttu-id="cf1cf-135">Un compilador IDL procesa el archivo IDL, que genera un archivo de encabezado de C++.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-135">The IDL file is processed by an IDL compiler, which generates a C++ header file.</span></span>

```C++
class IDrawable
{
public:
    virtual void Draw() = 0;
};
```

<span data-ttu-id="cf1cf-136">Al trabajar con COM, es importante recordar que las interfaces no son objetos.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-136">When you work with COM, it is important to remember that interfaces are not objects.</span></span> <span data-ttu-id="cf1cf-137">Son colecciones de métodos que los objetos deben implementar.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-137">They are collections of methods that objects must implement.</span></span> <span data-ttu-id="cf1cf-138">Varios objetos pueden implementar la misma interfaz, tal y como se muestra en los `Shape` `Bitmap` ejemplos y.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-138">Several objects can implement the same interface, as shown with the `Shape` and `Bitmap` examples.</span></span> <span data-ttu-id="cf1cf-139">Además, un objeto puede implementar varias interfaces.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-139">Moreover, one object can implement several interfaces.</span></span> <span data-ttu-id="cf1cf-140">Por ejemplo, la biblioteca de gráficos puede definir una interfaz denominada `ISerializable` que admita guardar y cargar objetos gráficos.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-140">For example, the graphics library might define an interface named `ISerializable` that supports saving and loading graphics objects.</span></span> <span data-ttu-id="cf1cf-141">Ahora, considere las siguientes declaraciones de clase:</span><span class="sxs-lookup"><span data-stu-id="cf1cf-141">Now consider the following class declarations:</span></span>

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

<span data-ttu-id="cf1cf-142">En este ejemplo, la `Bitmap` clase implementa `ISerializable` .</span><span class="sxs-lookup"><span data-stu-id="cf1cf-142">In this example, the `Bitmap` class implements `ISerializable`.</span></span> <span data-ttu-id="cf1cf-143">El programa podría utilizar este método para guardar o cargar el mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-143">The program could use this method to save or load the bitmap.</span></span> <span data-ttu-id="cf1cf-144">Sin embargo, la `Shape` clase no implementa `ISerializable` , por lo que no expone esa funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-144">However, the `Shape` class does not implement `ISerializable`, so it does not expose that functionality.</span></span> <span data-ttu-id="cf1cf-145">En el diagrama siguiente se muestran las relaciones de herencia en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-145">The following diagram shows the inheritance relations in this example.</span></span>

![Ilustración que muestra la herencia de interfaces, con las clases de forma y mapa de bits que apuntan a idrawable, pero solo mapa de bits que apunta a ISerializable](images/com02.png)

<span data-ttu-id="cf1cf-147">En esta sección se ha examinado la base conceptual de las interfaces, pero hasta ahora no hemos visto el código COM real.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-147">This section has examined the conceptual basis of interfaces, but so far we have not seen actual COM code.</span></span> <span data-ttu-id="cf1cf-148">Comenzaremos con lo primero que cualquier aplicación COM debe hacer: inicializar la biblioteca COM.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-148">We'll start with the first thing that any COM application must do: Initialize the COM library.</span></span>

## <a name="next"></a><span data-ttu-id="cf1cf-149">Siguientes</span><span class="sxs-lookup"><span data-stu-id="cf1cf-149">Next</span></span>

[<span data-ttu-id="cf1cf-150">Inicializar la biblioteca COM</span><span class="sxs-lookup"><span data-stu-id="cf1cf-150">Initializing the COM Library</span></span>](initializing-the-com-library.md)