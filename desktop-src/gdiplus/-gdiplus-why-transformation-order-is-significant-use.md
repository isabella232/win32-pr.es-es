---
description: Un objeto de matriz único puede almacenar una transformación única o una secuencia de transformaciones.
ms.assetid: 1dc68ff8-6b17-4934-82da-ab2fc612aafa
title: Importancia del orden de transformación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7350d63456902ff47183faa08170b3b2fef481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984423"
---
# <a name="why-transformation-order-is-significant"></a><span data-ttu-id="72648-103">Importancia del orden de transformación</span><span class="sxs-lookup"><span data-stu-id="72648-103">Why Transformation Order Is Significant</span></span>

<span data-ttu-id="72648-104">Un objeto de [**matriz**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) único puede almacenar una transformación única o una secuencia de transformaciones.</span><span class="sxs-lookup"><span data-stu-id="72648-104">A single [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) object can store a single transformation or a sequence of transformations.</span></span> <span data-ttu-id="72648-105">Esto último se denomina transformación *compuesta*.  </span><span class="sxs-lookup"><span data-stu-id="72648-105">The latter is called a *composite*  *transformation*.</span></span> <span data-ttu-id="72648-106">La matriz de una transformación compuesta se obtiene multiplicando las matrices de las transformaciones individuales.</span><span class="sxs-lookup"><span data-stu-id="72648-106">The matrix of a composite transformation is obtained by multiplying the matrices of the individual transformations.</span></span>

<span data-ttu-id="72648-107">En una transformación compuesta, el orden de las transformaciones individuales es importante.</span><span class="sxs-lookup"><span data-stu-id="72648-107">In a composite transformation, the order of the individual transformations is important.</span></span> <span data-ttu-id="72648-108">Por ejemplo, si primero se gira, después se realiza la escala y después se traduce, se obtiene un resultado diferente que si primero se traslada, después se gira y luego se escala.</span><span class="sxs-lookup"><span data-stu-id="72648-108">For example, if you first rotate, then scale, then translate, you get a different result than if you first translate, then rotate, then scale.</span></span> <span data-ttu-id="72648-109">En GDI+ de Windows, las transformaciones compuestas se crean de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="72648-109">In Windows GDI+, composite transformations are built from left to right.</span></span> <span data-ttu-id="72648-110">Si S, R y T son matrices de escala, rotación y traducción, respectivamente, el producto SRT (en ese orden) es la matriz de la transformación compuesta que se escala primero, luego gira y luego se convierte.</span><span class="sxs-lookup"><span data-stu-id="72648-110">If S, R, and T are scale, rotation, and translation matrices respectively, then the product SRT (in that order) is the matrix of the composite transformation that first scales, then rotates, then translates.</span></span> <span data-ttu-id="72648-111">La matriz generada por el producto SRT es diferente de la que genera el producto de la.</span><span class="sxs-lookup"><span data-stu-id="72648-111">The matrix produced by the product SRT is different from the matrix produced by the product TRS.</span></span>

<span data-ttu-id="72648-112">Un orden de razón es importante es que las transformaciones como la rotación y el escalado se realizan con respecto al origen del sistema de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="72648-112">One reason order is significant is that transformations like rotation and scaling are done with respect to the origin of the coordinate system.</span></span> <span data-ttu-id="72648-113">El escalado de un objeto que está centrado en el origen genera un resultado diferente que el escalado de un objeto que se ha quitado del origen.</span><span class="sxs-lookup"><span data-stu-id="72648-113">Scaling an object that is centered at the origin produces a different result than scaling an object that has been moved away from the origin.</span></span> <span data-ttu-id="72648-114">Del mismo modo, la rotación de un objeto que está centrado en el origen genera un resultado diferente que la rotación de un objeto que se ha quitado del origen.</span><span class="sxs-lookup"><span data-stu-id="72648-114">Similarly, rotating an object that is centered at the origin produces a different result than rotating an object that has been moved away from the origin.</span></span>

<span data-ttu-id="72648-115">En el ejemplo siguiente se combina el escalado, la rotación y la traslación (en ese orden) para formar una transformación compuesta.</span><span class="sxs-lookup"><span data-stu-id="72648-115">The following example combines scaling, rotation and translation (in that order) to form a composite transformation.</span></span> <span data-ttu-id="72648-116">El argumento [\* \* \* \* MatrixOrderAppend \* \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) \* \* que se pasa al método [**Graphics:: RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform) especifica que el giro seguirá el escalado.</span><span class="sxs-lookup"><span data-stu-id="72648-116">The argument [\*\*\*\*MatrixOrderAppend\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) passed to the [**Graphics::RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform) method specifies that the rotation will follow the scaling.</span></span> <span data-ttu-id="72648-117">Del mismo modo, el argumento \* \* \* \* [MatrixOrderAppend \* \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) \* \* que se pasa al método [**Graphics:: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) especifica que la conversión seguirá a la rotación.</span><span class="sxs-lookup"><span data-stu-id="72648-117">Likewise, the argument [\*\*\*\*MatrixOrderAppend\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) passed to the [**Graphics::TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) method specifies that the translation will follow the rotation.</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.ScaleTransform(1.75f, 0.5f);
graphics.RotateTransform(28.0f, MatrixOrderAppend);
graphics.TranslateTransform(150.0f, 150.0f, MatrixOrderAppend);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="72648-118">En el ejemplo siguiente se realizan las mismas llamadas al método que en el ejemplo anterior, pero se invierte el orden de las llamadas.</span><span class="sxs-lookup"><span data-stu-id="72648-118">The following example makes the same method calls as the previous example, but the order of the calls is reversed.</span></span> <span data-ttu-id="72648-119">El orden resultante de las operaciones se traduce primero, después se gira y luego se escala, lo que genera un resultado muy diferente de la primera escala, y luego gira y, a continuación, traduce:</span><span class="sxs-lookup"><span data-stu-id="72648-119">The resulting order of operations is first translate, then rotate, then scale, which produces a very different result than first scale, then rotate, then translate:</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f);
graphics.RotateTransform(28.0f, MatrixOrderAppend);
graphics.ScaleTransform(1.75f, 0.5f, MatrixOrderAppend);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="72648-120">Una manera de invertir el orden de las transformaciones individuales en una transformación compuesta es invertir el orden de una secuencia de llamadas a métodos.</span><span class="sxs-lookup"><span data-stu-id="72648-120">One way to reverse the order of the individual transformations in a composite transformation is to reverse the order of a sequence of method calls.</span></span> <span data-ttu-id="72648-121">Una segunda manera de controlar el orden de las operaciones es cambiar el argumento de orden de la matriz.</span><span class="sxs-lookup"><span data-stu-id="72648-121">A second way to control the order of operations is to change the matrix order argument.</span></span> <span data-ttu-id="72648-122">El ejemplo siguiente es el mismo que el anterior, salvo que [\* \* \* \* MatrixOrderAppend \* \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) \* \* se ha cambiado a [\* \* \* \* MatrixOrderPrepend \* \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder)\* \*.</span><span class="sxs-lookup"><span data-stu-id="72648-122">The following example is the same as the previous example, except that [\*\*\*\*MatrixOrderAppend\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) has been changed to [\*\*\*\*MatrixOrderPrepend\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder).</span></span> <span data-ttu-id="72648-123">La multiplicación de matrices se realiza en el orden SRT, donde S, R y T son las matrices para la escala, la rotación y la traslación, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="72648-123">The matrix multiplication is done in the order SRT, where S, R, and T are the matrices for scale, rotate, and translate, respectively.</span></span> <span data-ttu-id="72648-124">En primer lugar, el orden de la transformación compuesta es la primera escala, la rotación y la traslación.</span><span class="sxs-lookup"><span data-stu-id="72648-124">The order of the composite transformation is first scale, then rotate, then translate.</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f,MatrixOrderPrepend);
graphics.RotateTransform(28.0f, MatrixOrderPrepend);
graphics.ScaleTransform(1.75f, 0.5f, MatrixOrderPrepend);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="72648-125">El resultado del ejemplo anterior es el mismo resultado que hemos logrado en el primer ejemplo de esta sección.</span><span class="sxs-lookup"><span data-stu-id="72648-125">The result of the preceding example is the same result that we achieved in the first example of this section.</span></span> <span data-ttu-id="72648-126">Esto se debe a que se invirtió el orden de las llamadas al método y el orden de la multiplicación de la matriz.</span><span class="sxs-lookup"><span data-stu-id="72648-126">This is because we reversed both the order of the method calls and the order of the matrix multiplication.</span></span>

 

 



