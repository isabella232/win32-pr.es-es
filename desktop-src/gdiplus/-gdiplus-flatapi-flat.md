---
description: Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones. Microsoft .NET Framework proporciona un conjunto de clases contenedoras de código administrado para GDI+.
ms.assetid: afd8cf81-8a20-4592-bd0a-46341742cc9b
title: API plana de GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65f91c3c925b7de31f27e91c70cbd1bf0cbbb2a4
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394990"
---
# <a name="gdi-flat-api"></a><span data-ttu-id="45f18-104">API plana de GDI+</span><span class="sxs-lookup"><span data-stu-id="45f18-104">GDI+ Flat API</span></span>

<span data-ttu-id="45f18-105">Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones, que se implementan en Gdiplus.dll y se declaran en Gdiplusflat.h.</span><span class="sxs-lookup"><span data-stu-id="45f18-105">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="45f18-106">Las funciones de la API plana de GDI+ están encapsuladas por una colección de aproximadamente 40 clases de C++.</span><span class="sxs-lookup"><span data-stu-id="45f18-106">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="45f18-107">Se recomienda no llamar directamente a las funciones de la API plana.</span><span class="sxs-lookup"><span data-stu-id="45f18-107">It is recommended that you do not directly call the functions in the flat API.</span></span> <span data-ttu-id="45f18-108">Siempre que realice llamadas a GDI+, debe hacerlo llamando a los métodos y funciones proporcionados por los contenedores de C++.</span><span class="sxs-lookup"><span data-stu-id="45f18-108">Whenever you make calls to GDI+, you should do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="45f18-109">Los Servicios de soporte técnico de Microsoft no proporcionarán compatibilidad con el código que llama directamente a la API plana.</span><span class="sxs-lookup"><span data-stu-id="45f18-109">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span>

<span data-ttu-id="45f18-110">Como alternativa a los contenedores de C++, Microsoft .NET Framework proporciona un conjunto de clases contenedoras de código administrado para GDI+.</span><span class="sxs-lookup"><span data-stu-id="45f18-110">As an alternative to the C++ wrappers, the Microsoft .NET Framework provides a set of managed-code wrapper classes for GDI+.</span></span> <span data-ttu-id="45f18-111">Los contenedores de código administrado para GDI+ pertenecen a los siguientes espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="45f18-111">The managed-code wrappers for GDI+ belong to the following namespaces.</span></span>

-   [<span data-ttu-id="45f18-112">System.Drawing</span><span class="sxs-lookup"><span data-stu-id="45f18-112">System.Drawing</span></span>](/dotnet/api/system.drawing?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [<span data-ttu-id="45f18-113">System.Drawing.Drawing2D</span><span class="sxs-lookup"><span data-stu-id="45f18-113">System.Drawing.Drawing2D</span></span>](/dotnet/api/system.drawing.drawing2d?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [<span data-ttu-id="45f18-114">System.Drawing.Imaging</span><span class="sxs-lookup"><span data-stu-id="45f18-114">System.Drawing.Imaging</span></span>](/dotnet/api/system.drawing.imaging?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [<span data-ttu-id="45f18-115">System.Drawing.Text</span><span class="sxs-lookup"><span data-stu-id="45f18-115">System.Drawing.Text</span></span>](/dotnet/api/system.drawing.text?view=dotnet-plat-ext-3.1&preserve-view=true)

<span data-ttu-id="45f18-116">Ambos conjuntos de contenedores (C++ y código administrado) usan un enfoque orientado a objetos, por lo que hay algunas diferencias entre la forma en que se pasan los parámetros a los métodos contenedor y la forma en que se pasan los parámetros a las funciones de la API plana.</span><span class="sxs-lookup"><span data-stu-id="45f18-116">Both sets of wrappers (C++ and managed code) use an object-oriented approach, so there are some differences between the way parameters are passed to the wrapper methods and the way parameters are passed to functions in the flat API.</span></span> <span data-ttu-id="45f18-117">Por ejemplo, uno de los contenedores de C++ es la [**clase Matrix.**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix)</span><span class="sxs-lookup"><span data-stu-id="45f18-117">For example, one of the C++ wrappers is the [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) class.</span></span> <span data-ttu-id="45f18-118">Cada **objeto Matrix** tiene un campo, **nativeMatrix**, que apunta a una variable interna de tipo **GpMatrix**.</span><span class="sxs-lookup"><span data-stu-id="45f18-118">Each **Matrix** object has a field, **nativeMatrix**, that points to an internal variable of type **GpMatrix**.</span></span> <span data-ttu-id="45f18-119">Cuando se pasan parámetros a un método de un objeto **Matrix,** ese método pasa esos parámetros (o un conjunto de parámetros relacionados) a una de las funciones de la API plana de GDI+.</span><span class="sxs-lookup"><span data-stu-id="45f18-119">When you pass parameters to a method of a **Matrix** object, that method passes those parameters (or a set of related parameters) along to one of the functions in the GDI+ flat API.</span></span> <span data-ttu-id="45f18-120">Pero ese método también pasa el **campo nativeMatrix** (como parámetro de entrada) a la función de API plana.</span><span class="sxs-lookup"><span data-stu-id="45f18-120">But that method also passes the **nativeMatrix** field (as an input parameter) to the flat API function.</span></span> <span data-ttu-id="45f18-121">El código siguiente muestra cómo el método [**Matrix::Shear**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear) llama a la función **GdipS disposeMatrix(matriz GpMatrix, \* REAL shearX, REAL shearY, GpMatrixOrder order).**</span><span class="sxs-lookup"><span data-stu-id="45f18-121">The following code shows how the [**Matrix::Shear**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear) method calls the **GdipShearMatrix(GpMatrix \*matrix, REAL shearX, REAL shearY, GpMatrixOrder order)** function.</span></span>


```
Status Shear(
      IN REAL shearX, 
      IN REAL shearY,
      IN MatrixOrder order = MatrixOrderPrepend)
{
   ...
   GdipShearMatrix(nativeMatrix, shearX, shearY, order);
   ...
}
```



<span data-ttu-id="45f18-122">Los constructores [**matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) pasan la dirección de una variable de puntero **GpMatrix** (como parámetro de salida) a la **función GdipCreateMatrix(GpMatrix \* \* matrix).**</span><span class="sxs-lookup"><span data-stu-id="45f18-122">The [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) constructors pass the address of a **GpMatrix** pointer variable (as an output parameter) to the **GdipCreateMatrix(GpMatrix \*\*matrix)** function.</span></span> <span data-ttu-id="45f18-123">**GdipCreateMatrix** crea e inicializa una variable **GpMatrix** interna y, a continuación, asigna la dirección de **GpMatrix** a la variable de puntero.</span><span class="sxs-lookup"><span data-stu-id="45f18-123">**GdipCreateMatrix** creates and initializes an internal **GpMatrix** variable and then assigns the address of the **GpMatrix** to the pointer variable.</span></span> <span data-ttu-id="45f18-124">A continuación, el constructor copia el valor del puntero en el **campo nativeMatrix.**</span><span class="sxs-lookup"><span data-stu-id="45f18-124">Then the constructor copies the value of the pointer to the **nativeMatrix** field.</span></span>


```
Matrix()
{
   GpMatrix *matrix = NULL;
   lastResult = DllExports::GdipCreateMatrix(&matrix);
   SetNativeMatrix(matrix);
}

VOID SetNativeMatrix(GpMatrix *nativeMatrix)
{
   this->nativeMatrix = nativeMatrix;
}
```



<span data-ttu-id="45f18-125">Los métodos de clonación de las clases contenedoras no reciben ningún parámetro, pero a menudo pasan dos parámetros a la función subyacente en la API plana de GDI+.</span><span class="sxs-lookup"><span data-stu-id="45f18-125">Clone methods in the wrapper classes receive no parameters but often pass two parameters to the underlying function in the GDI+ flat API.</span></span> <span data-ttu-id="45f18-126">Por ejemplo, el método [**Matrix::Clone**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-clone) pasa **nativeMatrix** (como parámetro de entrada) y la dirección de una variable de puntero **GpMatrix** (como parámetro de salida) a la función **GdipCloneMatrix.**</span><span class="sxs-lookup"><span data-stu-id="45f18-126">For example, the [**Matrix::Clone**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-clone) method passes **nativeMatrix** (as an input parameter) and the address of a **GpMatrix** pointer variable (as an output parameter) to the **GdipCloneMatrix** function.</span></span> <span data-ttu-id="45f18-127">El código siguiente muestra cómo el método **Matrix::Clone** llama a la función **GdipCloneMatrix(GpMatrix \* matrix, GpMatrix \* \* cloneMatrix).**</span><span class="sxs-lookup"><span data-stu-id="45f18-127">The following code shows how the **Matrix::Clone** method calls the **GdipCloneMatrix(GpMatrix \*matrix, GpMatrix \*\*cloneMatrix)** function.</span></span>


```
Matrix *Clone() const
{
   GpMatrix *cloneMatrix = NULL;
   ...
   GdipCloneMatrix(nativeMatrix, &cloneMatrix));
   ...
   return new Matrix(cloneMatrix);
 }
```



<span data-ttu-id="45f18-128">Las funciones de la API plana devuelven un valor de tipo GpStatus.</span><span class="sxs-lookup"><span data-stu-id="45f18-128">The functions in the flat API return a value of type GpStatus.</span></span> <span data-ttu-id="45f18-129">La enumeración GpStatus es idéntica a la [**enumeración Status**](/windows/win32/api/Gdiplustypes/ne-gdiplustypes-status) utilizada por los métodos contenedores.</span><span class="sxs-lookup"><span data-stu-id="45f18-129">The GpStatus enumeration is identical to the [**Status**](/windows/win32/api/Gdiplustypes/ne-gdiplustypes-status) enumeration used by the wrapper methods.</span></span> <span data-ttu-id="45f18-130">En GdiplusGpStubs.h, GpStatus se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="45f18-130">In GdiplusGpStubs.h, GpStatus is defined as follows:</span></span>

`typedef Status GpStatus;`

<span data-ttu-id="45f18-131">La mayoría de los métodos de las clases contenedoras devuelven un valor de estado que indica si el método se ha hecho correctamente.</span><span class="sxs-lookup"><span data-stu-id="45f18-131">Most of the methods in the wrapper classes return a status value that indicates whether the method succeeded.</span></span> <span data-ttu-id="45f18-132">Sin embargo, algunos de los métodos contenedor devuelven valores de estado.</span><span class="sxs-lookup"><span data-stu-id="45f18-132">However, some of the wrapper methods return state values.</span></span> <span data-ttu-id="45f18-133">Cuando se llama a un método contenedor que devuelve un valor de estado, el método contenedor pasa los parámetros adecuados a la función subyacente en la API plana de GDI+.</span><span class="sxs-lookup"><span data-stu-id="45f18-133">When you call a wrapper method that returns a state value, the wrapper method passes the appropriate parameters to the underlying function in the GDI+ flat API.</span></span> <span data-ttu-id="45f18-134">Por ejemplo, la clase [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) tiene un método [**Matrix::IsInvertible**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-isinvertible) que pasa el campo **nativeMatrix** y la dirección de una variable **BOOL** (como parámetro de salida) a la función **GdipIsMatrixInvertible.**</span><span class="sxs-lookup"><span data-stu-id="45f18-134">For example, the [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) class has an [**Matrix::IsInvertible**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-isinvertible) method that passes the **nativeMatrix** field and and the address of a **BOOL** variable (as an output parameter) to the **GdipIsMatrixInvertible** function.</span></span> <span data-ttu-id="45f18-135">El código siguiente muestra cómo el método **Matrix::IsInvertible** llama a la función **GdipIsMatrixInvertible(matriz GDIPCONST GpMatrix, resultado \* BOOL). \***</span><span class="sxs-lookup"><span data-stu-id="45f18-135">The following code shows how the **Matrix::IsInvertible** method calls the **GdipIsMatrixInvertible(GDIPCONST GpMatrix \*matrix, BOOL \*result)** function.</span></span>


```
BOOL IsInvertible() const
{
   BOOL result = FALSE;
   ...
   GdipIsMatrixInvertible(nativeMatrix, &result);
   return result;
}
```



<span data-ttu-id="45f18-136">Otro de los contenedores es la [**clase Color.**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color)</span><span class="sxs-lookup"><span data-stu-id="45f18-136">Another one of the wrappers is the [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) class.</span></span> <span data-ttu-id="45f18-137">Un **objeto Color** tiene un único campo de tipo **ARGB**, que se define como **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="45f18-137">A **Color** object has a single field of type **ARGB**, which is defined as a **DWORD**.</span></span> <span data-ttu-id="45f18-138">Cuando se pasa un **objeto Color** a uno de los métodos contenedor, ese método pasa el **campo ARGB** junto con la función subyacente en la API plana de GDI+.</span><span class="sxs-lookup"><span data-stu-id="45f18-138">When you pass a **Color** object to one of the wrapper methods, that method passes the **ARGB** field along to the underlying function in the GDI+ flat API.</span></span> <span data-ttu-id="45f18-139">El código siguiente muestra cómo el [**método Pen::SetColor**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setcolor) llama a la función **GdipSetPenColor(GpPen \* pen, ARGB argb).**</span><span class="sxs-lookup"><span data-stu-id="45f18-139">The following code shows how the [**Pen::SetColor**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setcolor) method calls the **GdipSetPenColor(GpPen \*pen, ARGB argb)** function.</span></span> <span data-ttu-id="45f18-140">El [**método Color::GetValue**](/windows/win32/api/Gdipluscolor/nf-gdipluscolor-color-getvalue) devuelve el valor del **campo ARGB.**</span><span class="sxs-lookup"><span data-stu-id="45f18-140">The [**Color::GetValue**](/windows/win32/api/Gdipluscolor/nf-gdipluscolor-color-getvalue) method returns the value of the **ARGB** field.</span></span>


```
Status SetColor(IN const Color& color)
{
   ...
   GdipSetPenColor(nativePen, color.GetValue());
}
```



<span data-ttu-id="45f18-141">En los temas siguientes se muestra la relación entre la API plana de GDI+ y los métodos contenedor de C++.</span><span class="sxs-lookup"><span data-stu-id="45f18-141">The following topics show the relationship between the GDI+ flat API and the C++ wrapper methods.</span></span>

-   [<span data-ttu-id="45f18-142">Funciones AdjustableArrowCap</span><span class="sxs-lookup"><span data-stu-id="45f18-142">AdjustableArrowCap Functions</span></span>](-gdiplus-adjustablearrowcap-flat.md)
-   [<span data-ttu-id="45f18-143">Funciones de mapa de bits</span><span class="sxs-lookup"><span data-stu-id="45f18-143">Bitmap Functions</span></span>](-gdiplus-bitmap-flat.md)
-   [<span data-ttu-id="45f18-144">Funciones de pincel</span><span class="sxs-lookup"><span data-stu-id="45f18-144">Brush Functions</span></span>](-gdiplus-brush-flat.md)
-   [<span data-ttu-id="45f18-145">Funciones CachedBitmap</span><span class="sxs-lookup"><span data-stu-id="45f18-145">CachedBitmap Functions</span></span>](-gdiplus-cachedbitmap-flat.md)
-   [<span data-ttu-id="45f18-146">CustomLineCap (Funciones)</span><span class="sxs-lookup"><span data-stu-id="45f18-146">CustomLineCap Functions</span></span>](-gdiplus-customlinecap-flat.md)
-   [<span data-ttu-id="45f18-147">Funciones de fuente</span><span class="sxs-lookup"><span data-stu-id="45f18-147">Font Functions</span></span>](-gdiplus-font-flat.md)
-   [<span data-ttu-id="45f18-148">FontFamilyFunctions</span><span class="sxs-lookup"><span data-stu-id="45f18-148">FontFamilyFunctions</span></span>](-gdiplus-fontfamily-flat.md)
-   [<span data-ttu-id="45f18-149">Funciones de gráficos</span><span class="sxs-lookup"><span data-stu-id="45f18-149">Graphics Functions</span></span>](-gdiplus-graphics-flat.md)
-   [<span data-ttu-id="45f18-150">Funciones GraphicsPath</span><span class="sxs-lookup"><span data-stu-id="45f18-150">GraphicsPath Functions</span></span>](-gdiplus-graphicspath-flat.md)
-   [<span data-ttu-id="45f18-151">Funciones de Objeto HatchBrush</span><span class="sxs-lookup"><span data-stu-id="45f18-151">HatchBrush Functions</span></span>](-gdiplus-hatchbrush-flat.md)
-   [<span data-ttu-id="45f18-152">Funciones de imagen</span><span class="sxs-lookup"><span data-stu-id="45f18-152">Image Functions</span></span>](-gdiplus-image-flat.md)
-   [<span data-ttu-id="45f18-153">Funciones ImageAttributes</span><span class="sxs-lookup"><span data-stu-id="45f18-153">ImageAttributes Functions</span></span>](-gdiplus-imageattributes-flat.md)
-   [<span data-ttu-id="45f18-154">Funciones LinearGradientBrush</span><span class="sxs-lookup"><span data-stu-id="45f18-154">LinearGradientBrush Functions</span></span>](-gdiplus-lineargradientbrush-flat.md)
-   [<span data-ttu-id="45f18-155">Funciones de matriz</span><span class="sxs-lookup"><span data-stu-id="45f18-155">Matrix Functions</span></span>](-gdiplus-matrix-flat.md)
-   [<span data-ttu-id="45f18-156">Funciones de memoria</span><span class="sxs-lookup"><span data-stu-id="45f18-156">Memory Functions</span></span>](-gdiplus-memory-flat.md)
-   [<span data-ttu-id="45f18-157">Funciones de notificación</span><span class="sxs-lookup"><span data-stu-id="45f18-157">Notification Functions</span></span>](-gdiplus-notification-flat.md)
-   [<span data-ttu-id="45f18-158">Funciones PathGradientBrush</span><span class="sxs-lookup"><span data-stu-id="45f18-158">PathGradientBrush Functions</span></span>](-gdiplus-pathgradientbrush-flat.md)
-   [<span data-ttu-id="45f18-159">Funciones pathIterator</span><span class="sxs-lookup"><span data-stu-id="45f18-159">PathIterator Functions</span></span>](-gdiplus-pathiterator-flat.md)
-   [<span data-ttu-id="45f18-160">Funciones de lápiz</span><span class="sxs-lookup"><span data-stu-id="45f18-160">Pen Functions</span></span>](-gdiplus-pen-flat.md)
-   [<span data-ttu-id="45f18-161">Funciones de región</span><span class="sxs-lookup"><span data-stu-id="45f18-161">Region Functions</span></span>](-gdiplus-region-flat.md)
-   [<span data-ttu-id="45f18-162">Funciones solidBrush</span><span class="sxs-lookup"><span data-stu-id="45f18-162">SolidBrush Functions</span></span>](-gdiplus-solidbrush-flat.md)
-   [<span data-ttu-id="45f18-163">Funciones de formato de cadena</span><span class="sxs-lookup"><span data-stu-id="45f18-163">String Format Functions</span></span>](-gdiplus-stringformat-flat.md)
-   [<span data-ttu-id="45f18-164">Funciones de texto</span><span class="sxs-lookup"><span data-stu-id="45f18-164">Text Functions</span></span>](-gdiplus-text-flat.md)
-   [<span data-ttu-id="45f18-165">Funciones de pincel de textura</span><span class="sxs-lookup"><span data-stu-id="45f18-165">Texture Brush Functions</span></span>](-gdiplus-texturebrush-flat.md)

 

 
