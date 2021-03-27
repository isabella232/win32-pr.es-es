---
description: Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones, que se implementan en Gdiplus.dll y se declaran en Gdiplusflat. h.
ms.assetid: afd8cf81-8a20-4592-bd0a-46341742cc9b
title: API plana de GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 450f89439b6ead3b8cd9a49f52a6620571f6db54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997492"
---
# <a name="gdi-flat-api"></a>API plana de GDI+

Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones, que se implementan en Gdiplus.dll y se declaran en Gdiplusflat. h. Las funciones de la API plana GDI+ se incluyen en una colección de aproximadamente 40 clases de C++. Se recomienda no llamar directamente a las funciones de la API plana. Siempre que realice llamadas a GDI+, debe hacerlo mediante una llamada a los métodos y las funciones proporcionados por los contenedores de C++. Los servicios de soporte técnico de Microsoft no proporcionarán soporte técnico para el código que llama directamente a la API plana.

Como alternativa a los contenedores de C++, el marco de Microsoft .NET proporciona un conjunto de clases contenedoras de código administrado para GDI+. Los contenedores de código administrado para GDI+ pertenecen a los siguientes espacios de nombres.

-   [System.Drawing](/dotnet/api/system.drawing?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [System. Drawing. Drawing2D](/dotnet/api/system.drawing.drawing2d?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [System. Drawing. Imaging](/dotnet/api/system.drawing.imaging?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [System. Drawing. Text](/dotnet/api/system.drawing.text?view=dotnet-plat-ext-3.1&preserve-view=true)

Ambos conjuntos de contenedores (C++ y código administrado) usan un enfoque orientado a objetos, por lo que hay algunas diferencias entre la manera en que se pasan los parámetros a los métodos de contenedor y la manera en que se pasan los parámetros a las funciones de la API plana. Por ejemplo, uno de los contenedores de C++ es la clase [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) . Cada objeto de **matriz** tiene un campo, **nativeMatrix**, que apunta a una variable interna de tipo **GpMatrix**. Al pasar parámetros a un método de un objeto **Matrix** , ese método pasa esos parámetros (o un conjunto de parámetros relacionados) a una de las funciones de la API plana GDI+. Pero ese método también pasa el campo **nativeMatrix** (como parámetro de entrada) a la función de API plana. En el código siguiente se muestra cómo el método [**Matrix:: distorsión**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear) llama a la función **GdipShearMatrix (GPMATRIX \* Matrix, real SHEARX, imtorsión real, GpMatrixOrder Order)** .


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



Los constructores de [**matriz**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) pasan la dirección de una variable de puntero **GpMatrix** (como parámetro de salida) a la función **GdipCreateMatrix (GpMatrix \* \* Matrix)** . **GdipCreateMatrix** crea e inicializa una variable interna de **GpMatrix** y, a continuación, asigna la dirección de **GpMatrix** a la variable de puntero. Después, el constructor copia el valor del puntero en el campo **nativeMatrix** .


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



Los métodos Clone de las clases contenedoras no reciben parámetros pero, a menudo, pasan dos parámetros a la función subyacente en la API plana GDI+. Por ejemplo, el método [**Matrix:: Clone**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-clone) pasa **nativeMatrix** (como parámetro de entrada) y la dirección de una variable de puntero **GpMatrix** (como parámetro de salida) a la función **GdipCloneMatrix** . En el código siguiente se muestra cómo el método **Matrix:: Clone** llama a la función **GdipCloneMatrix (GpMatrix \* Matrix, GpMatrix \* \* cloneMatrix)** .


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



Las funciones de la API plana devuelven un valor de tipo GpStatus. La enumeración GpStatus es idéntica a la enumeración [**status**](/windows/win32/api/Gdiplustypes/ne-gdiplustypes-status) que usan los métodos contenedores. En GdiplusGpStubs. h, GpStatus se define de la siguiente manera:

`typedef Status GpStatus;`

La mayoría de los métodos de las clases contenedoras devuelven un valor de estado que indica si el método se realizó correctamente. Sin embargo, algunos de los métodos de contenedor devuelven valores de estado. Cuando se llama a un método contenedor que devuelve un valor de estado, el método contenedor pasa los parámetros adecuados a la función subyacente en la API plana GDI+. Por ejemplo, la [**clase Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) tiene un [**método Matrix:: IsInvertible**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-isinvertible) que pasa el campo **nativeMatrix** y la dirección de una variable **bool** (como parámetro Output) a la función **GdipIsMatrixInvertible** . En el código siguiente se muestra cómo el método **Matrix:: IsInvertible** llama a la función **GdipIsMatrixInvertible (GDIPCONST GPMATRIX \* Matrix, bool \* result)** .


```
BOOL IsInvertible() const
{
   BOOL result = FALSE;
   ...
   GdipIsMatrixInvertible(nativeMatrix, &result);
   return result;
}
```



Otro de los contenedores es la clase de [**color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) . Un objeto de **color** tiene un único campo de tipo **ARGB**, que se define como un **valor DWORD**. Cuando se pasa un objeto de **color** a uno de los métodos de contenedor, ese método pasa el campo **ARGB** junto a la función subyacente en la API plana de GDI+. En el código siguiente se muestra cómo el método [**Pen:: SetColor**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setcolor) llama a la función **GdipSetPenColor (GPPEN \* Pen, ARGB ARGB)** . El método [**color:: GetValue**](/windows/win32/api/Gdipluscolor/nf-gdipluscolor-color-getvalue) devuelve el valor del campo **ARGB** .


```
Status SetColor(IN const Color& color)
{
   ...
   GdipSetPenColor(nativePen, color.GetValue());
}
```



En los temas siguientes se muestra la relación entre la API plana de GDI+ y los métodos de contenedor de C++.

-   [Funciones de AdjustableArrowCap](-gdiplus-adjustablearrowcap-flat.md)
-   [Funciones de mapa de bits](-gdiplus-bitmap-flat.md)
-   [Funciones de pincel](-gdiplus-brush-flat.md)
-   [Funciones de CachedBitmap](-gdiplus-cachedbitmap-flat.md)
-   [Funciones de CustomLineCap](-gdiplus-customlinecap-flat.md)
-   [Funciones de fuente](-gdiplus-font-flat.md)
-   [FontFamilyFunctions](-gdiplus-fontfamily-flat.md)
-   [Funciones de gráficos](-gdiplus-graphics-flat.md)
-   [Funciones GraphicsPath](-gdiplus-graphicspath-flat.md)
-   [Funciones HatchBrush](-gdiplus-hatchbrush-flat.md)
-   [Funciones de imagen](-gdiplus-image-flat.md)
-   [Funciones ImageAttributes](-gdiplus-imageattributes-flat.md)
-   [Funciones LinearGradientBrush](-gdiplus-lineargradientbrush-flat.md)
-   [Funciones de matriz](-gdiplus-matrix-flat.md)
-   [Funciones de memoria](-gdiplus-memory-flat.md)
-   [Funciones de notificación](-gdiplus-notification-flat.md)
-   [PathGradientBrush (funciones)](-gdiplus-pathgradientbrush-flat.md)
-   [Funciones PathIterator](-gdiplus-pathiterator-flat.md)
-   [Funciones de lápiz](-gdiplus-pen-flat.md)
-   [Funciones de región](-gdiplus-region-flat.md)
-   [SolidBrush (funciones)](-gdiplus-solidbrush-flat.md)
-   [Funciones de formato de cadena](-gdiplus-stringformat-flat.md)
-   [Funciones de texto](-gdiplus-text-flat.md)
-   [Funciones de pincel de textura](-gdiplus-texturebrush-flat.md)

 

 
