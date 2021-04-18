---
title: 'Apéndice: Transformaciones de matriz'
description: En este tema se proporciona una introducción matemática de transformaciones de matriz para gráficos 2D.
ms.assetid: 8cc01f45-dd84-4f3e-a5f2-26edc5cbdfa1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5a9b09f75b17e4baf8afe5e7fde8643c06982f
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/28/2021
ms.locfileid: "104555992"
---
# <a name="appendix-matrix-transforms"></a><span data-ttu-id="6e39f-103">Apéndice: transformaciones de matriz</span><span class="sxs-lookup"><span data-stu-id="6e39f-103">Appendix: Matrix Transforms</span></span>

<span data-ttu-id="6e39f-104">En este tema se proporciona una introducción matemática de transformaciones de matriz para gráficos 2D.</span><span class="sxs-lookup"><span data-stu-id="6e39f-104">This topic provides a mathematical overview of matrix transforms for 2-D graphics.</span></span> <span data-ttu-id="6e39f-105">Sin embargo, no es necesario conocer la aritmética de matrices para usar transformaciones en Direct2D.</span><span class="sxs-lookup"><span data-stu-id="6e39f-105">However, you don't need to know matrix math in order to use transforms in Direct2D.</span></span> <span data-ttu-id="6e39f-106">Lea este tema si está interesado en las matemáticas; de lo contrario, no dude en omitir este tema.</span><span class="sxs-lookup"><span data-stu-id="6e39f-106">Read this topic if you are interested in the math; otherwise, feel free to skip this topic.</span></span>

-   [<span data-ttu-id="6e39f-107">Introducción a las matrices</span><span class="sxs-lookup"><span data-stu-id="6e39f-107">Introduction to Matrices</span></span>](#introduction-to-matrices)
    -   [<span data-ttu-id="6e39f-108">Operaciones de matriz</span><span class="sxs-lookup"><span data-stu-id="6e39f-108">Matrix Operations</span></span>](#matrix-operations)
-   [<span data-ttu-id="6e39f-109">Transformaciones afines</span><span class="sxs-lookup"><span data-stu-id="6e39f-109">Affine Transforms</span></span>](#affine-transforms)
    -   [<span data-ttu-id="6e39f-110">Transformación de traslación</span><span class="sxs-lookup"><span data-stu-id="6e39f-110">Translation Transform</span></span>](#translation-transform)
    -   [<span data-ttu-id="6e39f-111">Transformación de escala</span><span class="sxs-lookup"><span data-stu-id="6e39f-111">Scaling Transform</span></span>](#scaling-transform)
    -   [<span data-ttu-id="6e39f-112">Giro alrededor del origen</span><span class="sxs-lookup"><span data-stu-id="6e39f-112">Rotation Around the Origin</span></span>](#rotation-around-the-origin)
    -   [<span data-ttu-id="6e39f-113">Giro alrededor de un punto arbitrario</span><span class="sxs-lookup"><span data-stu-id="6e39f-113">Rotation Around an Arbitrary Point</span></span>](#rotation-around-an-arbitrary-point)
    -   [<span data-ttu-id="6e39f-114">Sesgar transformación</span><span class="sxs-lookup"><span data-stu-id="6e39f-114">Skew Transform</span></span>](#skew-transform)
-   [<span data-ttu-id="6e39f-115">Representar transformaciones en Direct2D</span><span class="sxs-lookup"><span data-stu-id="6e39f-115">Representing Transforms in Direct2D</span></span>](#representing-transforms-in-direct2d)
-   [<span data-ttu-id="6e39f-116">Siguiente</span><span class="sxs-lookup"><span data-stu-id="6e39f-116">Next</span></span>](#next)

## <a name="introduction-to-matrices"></a><span data-ttu-id="6e39f-117">Introducción a las matrices</span><span class="sxs-lookup"><span data-stu-id="6e39f-117">Introduction to Matrices</span></span>

<span data-ttu-id="6e39f-118">Una matriz es una matriz rectangular de números reales.</span><span class="sxs-lookup"><span data-stu-id="6e39f-118">A matrix is a rectangular array of real numbers.</span></span> <span data-ttu-id="6e39f-119">El *orden* de la matriz es el número de filas y columnas.</span><span class="sxs-lookup"><span data-stu-id="6e39f-119">The *order* of the matrix is the number of rows and columns.</span></span> <span data-ttu-id="6e39f-120">Por ejemplo, si la matriz tiene 3 filas y dos columnas, el orden es 3 × 2.</span><span class="sxs-lookup"><span data-stu-id="6e39f-120">For example, if the matrix has 3 rows and 2 columns, the order is 3 × 2.</span></span> <span data-ttu-id="6e39f-121">Las matrices se suelen mostrar con los elementos de la matriz entre corchetes:</span><span class="sxs-lookup"><span data-stu-id="6e39f-121">Matrices are usually shown with the matrix elements enclosed in square brackets:</span></span>

![matriz 3 x 2.](images/matrix01.png)

<span data-ttu-id="6e39f-123">Notación: una matriz se designa con una letra mayúscula.</span><span class="sxs-lookup"><span data-stu-id="6e39f-123">Notation: A matrix is designated by a capital letter.</span></span> <span data-ttu-id="6e39f-124">Los elementos se designan con letras minúsculas.</span><span class="sxs-lookup"><span data-stu-id="6e39f-124">Elements are designated by lowercase letters.</span></span> <span data-ttu-id="6e39f-125">Los subíndices indican el número de fila y columna de un elemento.</span><span class="sxs-lookup"><span data-stu-id="6e39f-125">Subscripts indicate the row and column number of an element.</span></span> <span data-ttu-id="6e39f-126">Por ejemplo, un *ij* es el elemento de la fila i i y la columna j'th de la matriz a.</span><span class="sxs-lookup"><span data-stu-id="6e39f-126">For example, a *ij* is the element at the i'th row and j'th column of the matrix A.</span></span>

<span data-ttu-id="6e39f-127">En el diagrama siguiente se muestra una matriz i × j, con los elementos individuales en cada celda de la matriz.</span><span class="sxs-lookup"><span data-stu-id="6e39f-127">The following diagram shows an i × j matrix, with the individual elements in each cell of the matrix.</span></span>

![matriz con i filas y j columnas.](images/matrix15.png)

### <a name="matrix-operations"></a><span data-ttu-id="6e39f-129">Operaciones de matriz</span><span class="sxs-lookup"><span data-stu-id="6e39f-129">Matrix Operations</span></span>

<span data-ttu-id="6e39f-130">En esta sección se describen las operaciones básicas definidas en las matrices.</span><span class="sxs-lookup"><span data-stu-id="6e39f-130">This section describes the basic operations defined on matrices.</span></span>

<span data-ttu-id="6e39f-131">*Adición*.</span><span class="sxs-lookup"><span data-stu-id="6e39f-131">*Addition*.</span></span> <span data-ttu-id="6e39f-132">La suma A + B de dos matrices se obtiene agregando los elementos correspondientes de A y B:</span><span class="sxs-lookup"><span data-stu-id="6e39f-132">The sum A + B of two matrices is obtained by adding the corresponding elements of A and B:</span></span>

<dl> <span data-ttu-id="6e39f-133">A + b = \[ a *ij* \]  +  \[ B *ij* \]  =  \[ a *ij* + b *ij*\]</span><span class="sxs-lookup"><span data-stu-id="6e39f-133">A + B = \[ a *ij* \] + \[ b *ij* \] = \[ a *ij* + b *ij* \]</span></span>
</dl>

<span data-ttu-id="6e39f-134">*Multiplicación escalar*.</span><span class="sxs-lookup"><span data-stu-id="6e39f-134">*Scalar multiplication*.</span></span> <span data-ttu-id="6e39f-135">Esta operación multiplica una matriz por un número real.</span><span class="sxs-lookup"><span data-stu-id="6e39f-135">This operation multiplies a matrix by a real number.</span></span> <span data-ttu-id="6e39f-136">Dado un número *k* real, el producto escalar Ka se obtiene multiplicando todos los elementos de a por *k*.</span><span class="sxs-lookup"><span data-stu-id="6e39f-136">Given a real number *k*, the scalar product kA is obtained by multiplying every element of A by *k*.</span></span>

<dl> <span data-ttu-id="6e39f-137">Ka = k \[ a *ij* \]  =  \[ k × a *ij*\]</span><span class="sxs-lookup"><span data-stu-id="6e39f-137">kA = k\[ a *ij* \] = \[ k × a *ij* \]</span></span>
</dl>

<span data-ttu-id="6e39f-138">*Multiplicación de matrices*.</span><span class="sxs-lookup"><span data-stu-id="6e39f-138">*Matrix multiplication*.</span></span> <span data-ttu-id="6e39f-139">Dadas dos matrices A y B con Order (m × n) y (n × p), el producto C = A × B es una matriz con Order (m × p), definida de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="6e39f-139">Given two matrices A and B with order (m × n) and (n × p), the product C = A × B is a matrix with order (m × p), defined as follows:</span></span>

![Muestra una fórmula para la multiplicación de matrices.](images/matrix02.png)

<span data-ttu-id="6e39f-141">o, de forma equivalente:</span><span class="sxs-lookup"><span data-stu-id="6e39f-141">or, equivalently:</span></span>

<dl> <span data-ttu-id="6e39f-142">c *ij* = a *i* 1 x B1 *j* + a *i* 2 x B2 *j* +... + a *in* + b *NJ*  
</span><span class="sxs-lookup"><span data-stu-id="6e39f-142">c *ij* = a *i* 1 x b1 *j* + a *i* 2 x b2 *j* + ... + a *in* + b *nj*  
</span></span></dl>

<span data-ttu-id="6e39f-143">Es decir, para calcular cada elemento c *ij*, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="6e39f-143">That is, to compute each element c *ij*, do the following:</span></span>

1.  <span data-ttu-id="6e39f-144">Tome la fila i i de y la columna j'th de B.</span><span class="sxs-lookup"><span data-stu-id="6e39f-144">Take the i'th row of A and the j'th column of B.</span></span>
2.  <span data-ttu-id="6e39f-145">Multiplica cada par de elementos de la fila y la columna: la primera entrada de la primera columna, la segunda entrada de la fila en la segunda entrada de la columna, etc.</span><span class="sxs-lookup"><span data-stu-id="6e39f-145">Multiply each pair of elements in the row and column: the first row entry by the first column entry, the second row entry by the second column entry, and so forth.</span></span>
3.  <span data-ttu-id="6e39f-146">Suma el resultado.</span><span class="sxs-lookup"><span data-stu-id="6e39f-146">Sum the result.</span></span>

<span data-ttu-id="6e39f-147">Este es un ejemplo de la multiplicación de una matriz (2 × 2) por una matriz (2 × 3).</span><span class="sxs-lookup"><span data-stu-id="6e39f-147">Here is an example of multiplying a (2 × 2) matrix by a (2 × 3) matrix.</span></span>

![multiplicación de matrices.](images/matrix03.png)

<span data-ttu-id="6e39f-149">La multiplicación de matrices no es conmutativa.</span><span class="sxs-lookup"><span data-stu-id="6e39f-149">Matrix multiplication is not commutative.</span></span> <span data-ttu-id="6e39f-150">Es decir, A × B ≠ B × A. Además, a partir de la definición se sigue que no todos los pares de matrices se pueden multiplicar.</span><span class="sxs-lookup"><span data-stu-id="6e39f-150">That is, A × B ≠ B × A. Also, from the definition it follows that not every pair of matrices can be multiplied.</span></span> <span data-ttu-id="6e39f-151">El número de columnas de la matriz de la izquierda debe ser igual al número de filas de la matriz de la derecha.</span><span class="sxs-lookup"><span data-stu-id="6e39f-151">The number of columns in the left-hand matrix must equal the number of rows in the right-hand matrix.</span></span> <span data-ttu-id="6e39f-152">De lo contrario, no se define el operador ×.</span><span class="sxs-lookup"><span data-stu-id="6e39f-152">Otherwise, the × operator is not defined.</span></span>

<span data-ttu-id="6e39f-153">*Identifique la matriz*.</span><span class="sxs-lookup"><span data-stu-id="6e39f-153">*Identify matrix*.</span></span> <span data-ttu-id="6e39f-154">Una matriz de identidad, designada como I, es una matriz cuadrada definida de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="6e39f-154">An identity matrix, designated I, is a square matrix defined as follows:</span></span>

<dl> <span data-ttu-id="6e39f-155">I *ij* = 1 si *i*  =  *j* o 0 en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6e39f-155">I *ij* = 1 if *i* = *j*, or 0 otherwise.</span></span>  
</dl>

<span data-ttu-id="6e39f-156">En otras palabras, una matriz de identidad contiene 1 para cada elemento donde el número de fila es igual al número de columna y cero para todos los demás elementos.</span><span class="sxs-lookup"><span data-stu-id="6e39f-156">In other words, an identity matrix contains 1 for each element where the row number equals the column number, and zero for all other elements.</span></span> <span data-ttu-id="6e39f-157">Por ejemplo, esta es la matriz de identidad 3 × 3.</span><span class="sxs-lookup"><span data-stu-id="6e39f-157">For example, here is the 3 × 3 identity matrix.</span></span>

![matriz de identidad.](images/matrix04.png)

<span data-ttu-id="6e39f-159">La siguiente es la igualdad de la matriz M.</span><span class="sxs-lookup"><span data-stu-id="6e39f-159">The following equalities hold for any matrix M.</span></span>

<dl> <span data-ttu-id="6e39f-160">M x I = M</span><span class="sxs-lookup"><span data-stu-id="6e39f-160">M x I = M</span></span>  
<span data-ttu-id="6e39f-161">I x M = M</span><span class="sxs-lookup"><span data-stu-id="6e39f-161">I x M = M</span></span>  
</dl>

## <a name="affine-transforms"></a><span data-ttu-id="6e39f-162">Transformaciones afines</span><span class="sxs-lookup"><span data-stu-id="6e39f-162">Affine Transforms</span></span>

<span data-ttu-id="6e39f-163">Una *transformación afín* es una operación matemática que asigna un espacio de coordenadas a otro.</span><span class="sxs-lookup"><span data-stu-id="6e39f-163">An *affine transform* is a mathematical operation that maps one coordinate space to another.</span></span> <span data-ttu-id="6e39f-164">En otras palabras, asigna un conjunto de puntos a otro conjunto de puntos.</span><span class="sxs-lookup"><span data-stu-id="6e39f-164">In other words, it maps one set of points to another set of points.</span></span> <span data-ttu-id="6e39f-165">Las transformaciones afines tienen algunas características que las hacen útiles en los gráficos de los equipos.</span><span class="sxs-lookup"><span data-stu-id="6e39f-165">Affine transforms have some features that make them useful in computer graphics.</span></span>

-   <span data-ttu-id="6e39f-166">Las transformaciones afines conservan la *colinealidad*.</span><span class="sxs-lookup"><span data-stu-id="6e39f-166">Affine transforms preserve *collinearity*.</span></span> <span data-ttu-id="6e39f-167">Si tres o más puntos se encuentran en una línea, seguirán formando una línea después de la transformación.</span><span class="sxs-lookup"><span data-stu-id="6e39f-167">If three or more points fall on a line, they still form a line after the transformation.</span></span> <span data-ttu-id="6e39f-168">Las líneas rectas permanecen rectas.</span><span class="sxs-lookup"><span data-stu-id="6e39f-168">Straight lines remain straight.</span></span>
-   <span data-ttu-id="6e39f-169">La composición de dos transformaciones afines es una transformación afín.</span><span class="sxs-lookup"><span data-stu-id="6e39f-169">The composition of two affine transforms is an affine transform.</span></span>

<span data-ttu-id="6e39f-170">Las transformaciones afines para el espacio 2D tienen el formato siguiente.</span><span class="sxs-lookup"><span data-stu-id="6e39f-170">Affine transforms for 2-D space have the following form.</span></span>

![Muestra una transformación afín para el espacio 2D.](images/matrix05.png)

<span data-ttu-id="6e39f-172">Si aplica la definición de la multiplicación de matrices proporcionada anteriormente, puede mostrar que el producto de dos transformaciones afines es otra transformación afín.</span><span class="sxs-lookup"><span data-stu-id="6e39f-172">If you apply the definition of matrix multiplication given earlier, you can show that the product of two affine transforms is another affine transform.</span></span> <span data-ttu-id="6e39f-173">Para transformar un punto 2D mediante una transformación afín, el punto se representa como una matriz de 1 × 3.</span><span class="sxs-lookup"><span data-stu-id="6e39f-173">To transform a 2D point using an affine transform, the point is represented as a 1 × 3 matrix.</span></span>

<dl> <span data-ttu-id="6e39f-174">P = \| x y 1 \|</span><span class="sxs-lookup"><span data-stu-id="6e39f-174">P = \| x y 1 \|</span></span>  
</dl>

<span data-ttu-id="6e39f-175">Los dos primeros elementos contienen las coordenadas x e y del punto.</span><span class="sxs-lookup"><span data-stu-id="6e39f-175">The first two elements contain the x and y coordinates of the point.</span></span> <span data-ttu-id="6e39f-176">El 1 se coloca en el tercer elemento para que las operaciones matemáticas funcionen correctamente.</span><span class="sxs-lookup"><span data-stu-id="6e39f-176">The 1 is placed in the third element to make the math work out correctly.</span></span> <span data-ttu-id="6e39f-177">Para aplicar la transformación, multiplique las dos matrices como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="6e39f-177">To apply the transform, multiply the two matrices as follows.</span></span>

<dl> <span data-ttu-id="6e39f-178">P ' = P × M</span><span class="sxs-lookup"><span data-stu-id="6e39f-178">P' = P × M</span></span>  
</dl>

<span data-ttu-id="6e39f-179">Se expande a lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="6e39f-179">This expands to the following.</span></span>

![transformación afín.](images/matrix06.png)

<span data-ttu-id="6e39f-181">where</span><span class="sxs-lookup"><span data-stu-id="6e39f-181">where</span></span>

<dl> <span data-ttu-id="6e39f-182">x ' = AX + CY + e</span><span class="sxs-lookup"><span data-stu-id="6e39f-182">x' = ax + cy + e</span></span>  
<span data-ttu-id="6e39f-183">y ' = BX + DY + f</span><span class="sxs-lookup"><span data-stu-id="6e39f-183">y' = bx + dy + f</span></span>  
</dl>

<span data-ttu-id="6e39f-184">Para obtener el punto transformado, tome los dos primeros elementos de la matriz P '.</span><span class="sxs-lookup"><span data-stu-id="6e39f-184">To get the transformed point, take the first two elements of matrix P'.</span></span>

<dl> <span data-ttu-id="6e39f-185">p = (x ', y ') = (AX + CY + e, BX + DY + f)</span><span class="sxs-lookup"><span data-stu-id="6e39f-185">p = (x', y') = (ax + cy + e, bx + dy + f)</span></span>  
</dl>

> [!Note]  
> <span data-ttu-id="6e39f-186">Una matriz de 1 × *n* se denomina *Vector de fila*.</span><span class="sxs-lookup"><span data-stu-id="6e39f-186">A 1 × *n* matrix is called a *row vector*.</span></span> <span data-ttu-id="6e39f-187">Tanto Direct2D como Direct3D usan vectores de filas para representar puntos en el espacio 2D o 3D.</span><span class="sxs-lookup"><span data-stu-id="6e39f-187">Direct2D and Direct3D both use row vectors to represent points in 2D or 3D space.</span></span> <span data-ttu-id="6e39f-188">Puede obtener un resultado equivalente mediante el uso de un vector de columna (*n* × 1) y transponer la matriz de transformación.</span><span class="sxs-lookup"><span data-stu-id="6e39f-188">You can get an equivalent result by using a column vector (*n* × 1) and transposing the transform matrix.</span></span> <span data-ttu-id="6e39f-189">La mayoría de los textos gráficos usan el formato de vector de columna.</span><span class="sxs-lookup"><span data-stu-id="6e39f-189">Most graphics texts use the column vector form.</span></span> <span data-ttu-id="6e39f-190">En este tema se presenta el formato de vector de fila para mantener la coherencia con Direct2D y Direct3D.</span><span class="sxs-lookup"><span data-stu-id="6e39f-190">This topic presents the row vector form for consistency with Direct2D and Direct3D.</span></span>

 

<span data-ttu-id="6e39f-191">En las siguientes secciones se derivan las transformaciones básicas.</span><span class="sxs-lookup"><span data-stu-id="6e39f-191">The next several sections derive the basic transforms.</span></span>

### <a name="translation-transform"></a><span data-ttu-id="6e39f-192">Transformación de traslación</span><span class="sxs-lookup"><span data-stu-id="6e39f-192">Translation Transform</span></span>

<span data-ttu-id="6e39f-193">La matriz de transformación de traslación tiene el formato siguiente.</span><span class="sxs-lookup"><span data-stu-id="6e39f-193">The translation transform matrix has the following form.</span></span>

![transformación de traslación.](images/matrix07.png)

<span data-ttu-id="6e39f-195">La conexión de un punto *P* a esta ecuación produce:</span><span class="sxs-lookup"><span data-stu-id="6e39f-195">Plugging a point *P* into this equation yields:</span></span>

<dl> <span data-ttu-id="6e39f-196">P ' = (*x*  +  *DX*, *y*  +  *DY*)</span><span class="sxs-lookup"><span data-stu-id="6e39f-196">P' = (*x* + *dx*, *y* + *dy*)</span></span>
</dl>

<span data-ttu-id="6e39f-197">que corresponde al punto (x, y) traducido por *DX* en el eje x y *DY* en el eje y.</span><span class="sxs-lookup"><span data-stu-id="6e39f-197">which corresponds to the point (x, y) translated by *dx* in the X-axis and *dy* in the Y-axis.</span></span>

![diagrama que muestra la conversión de dos puntos.](images/graphics22.png)

### <a name="scaling-transform"></a><span data-ttu-id="6e39f-199">Transformación de escala</span><span class="sxs-lookup"><span data-stu-id="6e39f-199">Scaling Transform</span></span>

<span data-ttu-id="6e39f-200">La matriz de transformación de escala tiene el formato siguiente.</span><span class="sxs-lookup"><span data-stu-id="6e39f-200">The scaling transform matrix has the following form.</span></span>

![transformación de escalado.](images/matrix09.png)

<span data-ttu-id="6e39f-202">La conexión de un punto *P* a esta ecuación produce:</span><span class="sxs-lookup"><span data-stu-id="6e39f-202">Plugging a point *P* into this equation yields:</span></span>

<dl> <span data-ttu-id="6e39f-203">P ' = (*x* enviada *DX*, *y* enviada *DY*)</span><span class="sxs-lookup"><span data-stu-id="6e39f-203">P' = (*x* ∙ *dx*, *y* ∙ *dy*)</span></span>
</dl>

<span data-ttu-id="6e39f-204">que corresponde al punto (x, y) escalado por *DX* y *DY*.</span><span class="sxs-lookup"><span data-stu-id="6e39f-204">which corresponds to the point (x,y) scaled by *dx* and *dy*.</span></span>

![diagrama que muestra el escalado de dos puntos.](images/graphics23.png)

### <a name="rotation-around-the-origin"></a><span data-ttu-id="6e39f-206">Giro alrededor del origen</span><span class="sxs-lookup"><span data-stu-id="6e39f-206">Rotation Around the Origin</span></span>

<span data-ttu-id="6e39f-207">La matriz para girar un punto alrededor del origen tiene el formato siguiente.</span><span class="sxs-lookup"><span data-stu-id="6e39f-207">The matrix to rotate a point around the origin has the following form.</span></span>

![Muestra una fórmula para una transformación de giro.](images/matrix11.png)

<span data-ttu-id="6e39f-209">El punto transformado es:</span><span class="sxs-lookup"><span data-stu-id="6e39f-209">The transformed point is:</span></span>

<dl> <span data-ttu-id="6e39f-210">P ' = (*x* CosΘ – ysinΘ, *x* sinΘ + *y* cosΘ)</span><span class="sxs-lookup"><span data-stu-id="6e39f-210">P' = (*x* cosΘ – ysinΘ, *x* sinΘ + *y* cosΘ)</span></span>
</dl>

<span data-ttu-id="6e39f-211">Justificar.</span><span class="sxs-lookup"><span data-stu-id="6e39f-211">Proof.</span></span> <span data-ttu-id="6e39f-212">Para mostrar que P ' representa una rotación, considere el siguiente diagrama.</span><span class="sxs-lookup"><span data-stu-id="6e39f-212">To show that P' represents a rotation, consider the following diagram.</span></span>

![diagrama que muestra el giro alrededor del origen.](images/graphics24.png)

<span data-ttu-id="6e39f-214">Con estas premisas:</span><span class="sxs-lookup"><span data-stu-id="6e39f-214">Given:</span></span>

<dl> <dt>

<span data-ttu-id="6e39f-215"><span id="P____x_y_"></span><span id="p____x_y_"></span><span id="P____X_Y_"></span>P = (x, y)</span><span class="sxs-lookup"><span data-stu-id="6e39f-215"><span id="P____x_y_"></span><span id="p____x_y_"></span><span id="P____X_Y_"></span>P = (x,y)</span></span>
</dt> <dd>

<span data-ttu-id="6e39f-216">Punto original que se va a transformar.</span><span class="sxs-lookup"><span data-stu-id="6e39f-216">The original point to transform.</span></span>

</dd> <dt>

<span data-ttu-id="6e39f-217">Φ</span><span class="sxs-lookup"><span data-stu-id="6e39f-217">Φ</span></span>
</dt> <dd>

<span data-ttu-id="6e39f-218">El ángulo formado por la línea (0,0) a P.</span><span class="sxs-lookup"><span data-stu-id="6e39f-218">The angle formed by the line (0,0) to P.</span></span>

</dd> <dt>

<span data-ttu-id="6e39f-219">Θ</span><span class="sxs-lookup"><span data-stu-id="6e39f-219">Θ</span></span>
</dt> <dd>

<span data-ttu-id="6e39f-220">Ángulo por el que se va a girar (x, y) el origen.</span><span class="sxs-lookup"><span data-stu-id="6e39f-220">The angle by which to rotate (x,y) about the origin.</span></span>

</dd> <dt>

<span data-ttu-id="6e39f-221"><span id="P_____x__y__"></span><span id="p_____x__y__"></span><span id="P_____X__Y__"></span>P ' = (x ', y ')</span><span class="sxs-lookup"><span data-stu-id="6e39f-221"><span id="P_____x__y__"></span><span id="p_____x__y__"></span><span id="P_____X__Y__"></span>P' = (x',y')</span></span>
</dt> <dd>

<span data-ttu-id="6e39f-222">Punto transformado.</span><span class="sxs-lookup"><span data-stu-id="6e39f-222">The transformed point.</span></span>

</dd> <dt>

<span data-ttu-id="6e39f-223"><span id="R"></span><span id="r"></span>C</span><span class="sxs-lookup"><span data-stu-id="6e39f-223"><span id="R"></span><span id="r"></span>R</span></span>
</dt> <dd>

<span data-ttu-id="6e39f-224">Longitud de la línea (0,0) a P. También es el radio del círculo de rotación.</span><span class="sxs-lookup"><span data-stu-id="6e39f-224">The length of the line (0,0) to P. Also the radius of the circle of rotation.</span></span>

</dd> </dl>

> [!Note]  
> <span data-ttu-id="6e39f-225">En este diagrama se usa el sistema de coordenadas estándar que se usa en Geometry, donde el eje y positivo apunta hacia arriba.</span><span class="sxs-lookup"><span data-stu-id="6e39f-225">This diagram uses the standard coordinate system used in geometry, where the positive y-axis points up.</span></span> <span data-ttu-id="6e39f-226">Direct2D usa el sistema de coordenadas de Windows, donde el eje y positivo apunta hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="6e39f-226">Direct2D uses the Windows coordinate system, where the positive y-axis points down.</span></span>

 

<span data-ttu-id="6e39f-227">El ángulo entre el eje x y la línea (0,0) a P ' es Φ + Θ.</span><span class="sxs-lookup"><span data-stu-id="6e39f-227">The angle between the x-axis and the line (0,0) to P' is Φ + Θ.</span></span> <span data-ttu-id="6e39f-228">Las siguientes identidades contienen:</span><span class="sxs-lookup"><span data-stu-id="6e39f-228">The following identities hold:</span></span>

<dl> <span data-ttu-id="6e39f-229">x = R cosΦ</span><span class="sxs-lookup"><span data-stu-id="6e39f-229">x = R cosΦ</span></span>  
<span data-ttu-id="6e39f-230">y = R sinΦ</span><span class="sxs-lookup"><span data-stu-id="6e39f-230">y = R sinΦ</span></span>  
<span data-ttu-id="6e39f-231">x ' = R cos (Φ + Θ)</span><span class="sxs-lookup"><span data-stu-id="6e39f-231">x' = R cos(Φ + Θ)</span></span>  
<span data-ttu-id="6e39f-232">y ' = R sin (Φ + Θ)</span><span class="sxs-lookup"><span data-stu-id="6e39f-232">y' = R sin(Φ+ Θ)</span></span>  
</dl>

<span data-ttu-id="6e39f-233">Ahora se resuelve para x ' e y ' en términos de Θ.</span><span class="sxs-lookup"><span data-stu-id="6e39f-233">Now solve for x' and y' in terms of Θ.</span></span> <span data-ttu-id="6e39f-234">Por las fórmulas de suma trigonométrica:</span><span class="sxs-lookup"><span data-stu-id="6e39f-234">By the trigonometric addition formulas:</span></span>

<dl> <span data-ttu-id="6e39f-235">x ' = R (cosΦcosΘ – sinΦsinΘ) = RcosΦcosΘ – RsinΦsinΘ</span><span class="sxs-lookup"><span data-stu-id="6e39f-235">x' = R(cosΦcosΘ – sinΦsinΘ) = RcosΦcosΘ – RsinΦsinΘ</span></span>  
<span data-ttu-id="6e39f-236">y ' = R (sinΦcosΘ + cosΦsinΘ) = RsinΦcosΘ + RcosΦsinΘ</span><span class="sxs-lookup"><span data-stu-id="6e39f-236">y' = R(sinΦcosΘ + cosΦsinΘ) = RsinΦcosΘ + RcosΦsinΘ</span></span>  
</dl>

<span data-ttu-id="6e39f-237">Sustituyendo:</span><span class="sxs-lookup"><span data-stu-id="6e39f-237">Substituting, we get:</span></span>

<dl> <span data-ttu-id="6e39f-238">x ' = xcosΘ – ysinΘ</span><span class="sxs-lookup"><span data-stu-id="6e39f-238">x' = xcosΘ – ysinΘ</span></span>  
<span data-ttu-id="6e39f-239">y ' = xsinΘ + ycosΘ</span><span class="sxs-lookup"><span data-stu-id="6e39f-239">y' = xsinΘ + ycosΘ</span></span>  
</dl>

<span data-ttu-id="6e39f-240">que corresponde al punto P ' transformado que se mostró anteriormente.</span><span class="sxs-lookup"><span data-stu-id="6e39f-240">which corresponds to the transformed point P' shown earlier.</span></span>

### <a name="rotation-around-an-arbitrary-point"></a><span data-ttu-id="6e39f-241">Giro alrededor de un punto arbitrario</span><span class="sxs-lookup"><span data-stu-id="6e39f-241">Rotation Around an Arbitrary Point</span></span>

<span data-ttu-id="6e39f-242">Para girar alrededor de un punto (x, y) que no sea el origen, se usa la matriz siguiente.</span><span class="sxs-lookup"><span data-stu-id="6e39f-242">To rotate around a point (x,y) other than the origin, the following matrix is used.</span></span>

![transformación de giro.](images/matrix13.png)

<span data-ttu-id="6e39f-244">Puede derivar esta matriz tomando el punto (x, y) como el origen.</span><span class="sxs-lookup"><span data-stu-id="6e39f-244">You can derive this matrix by taking the point (x,y) to be the origin.</span></span>

![diagrama que muestra la rotación alrededor de un punto.](images/graphics25.png)

<span data-ttu-id="6e39f-246">Let (x1, Y1) es el punto que es el resultado de girar el punto (x0, Y0) alrededor del punto (x, y).</span><span class="sxs-lookup"><span data-stu-id="6e39f-246">Let (x1, y1) be the point that results from rotating the point (x0, y0) around the point (x,y).</span></span> <span data-ttu-id="6e39f-247">Se puede derivar x1 como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="6e39f-247">We can derive x1 as follows.</span></span>

<dl> <span data-ttu-id="6e39f-248">x1 = (x0 – x) cosΘ – (Y0 – y) sinΘ + x</span><span class="sxs-lookup"><span data-stu-id="6e39f-248">x1 = (x0 – x)cosΘ– (y0 – y)sinΘ + x</span></span>  
<span data-ttu-id="6e39f-249">x1 = x0cosΘ – y0sinΘ + \[ (1 – cosΘ) + ysinΘ \]</span><span class="sxs-lookup"><span data-stu-id="6e39f-249">x1 = x0cosΘ – y0sinΘ + \[ (1 – cosΘ) + ysinΘ \]</span></span>  
</dl>

<span data-ttu-id="6e39f-250">A continuación, vuelva a conectar esta ecuación a la matriz de transformación con la fórmula x1 = aX0 + cy0 + e anterior.</span><span class="sxs-lookup"><span data-stu-id="6e39f-250">Now plug this equation back into the transform matrix, using the formula x1 = ax0 + cy0 + e from earlier.</span></span> <span data-ttu-id="6e39f-251">Use el mismo procedimiento para derivar Y1.</span><span class="sxs-lookup"><span data-stu-id="6e39f-251">Use the same procedure to derive y1.</span></span>

### <a name="skew-transform"></a><span data-ttu-id="6e39f-252">Sesgar transformación</span><span class="sxs-lookup"><span data-stu-id="6e39f-252">Skew Transform</span></span>

<span data-ttu-id="6e39f-253">La transformación de sesgo se define mediante cuatro parámetros:</span><span class="sxs-lookup"><span data-stu-id="6e39f-253">The skew transform is defined by four parameters:</span></span>

-   <span data-ttu-id="6e39f-254">Θ: la cantidad que se va a sesgar a lo largo del eje x, medida como un ángulo desde el eje y.</span><span class="sxs-lookup"><span data-stu-id="6e39f-254">Θ: The amount to skew along the x-axis, measured as an angle from the y-axis.</span></span>
-   <span data-ttu-id="6e39f-255">Φ: la cantidad que se va a sesgar a lo largo del eje y, medida como un ángulo del eje x.</span><span class="sxs-lookup"><span data-stu-id="6e39f-255">Φ: The amount to skew along the y-axis, measured as an angle from the x-axis.</span></span>
-   <span data-ttu-id="6e39f-256">(*PX*, *py*): las coordenadas x e y del punto sobre el que se realiza el sesgo.</span><span class="sxs-lookup"><span data-stu-id="6e39f-256">(*px*, *py*): The x- and y-coordinates of the point about which the skew is performed.</span></span>

<span data-ttu-id="6e39f-257">La transformación de sesgo utiliza la matriz siguiente.</span><span class="sxs-lookup"><span data-stu-id="6e39f-257">The skew transform uses the following matrix.</span></span>

![transformación de sesgo.](images/matrix14.png)

<span data-ttu-id="6e39f-259">El punto transformado es:</span><span class="sxs-lookup"><span data-stu-id="6e39f-259">The transformed point is:</span></span>

<dl> <span data-ttu-id="6e39f-260">P ' = (*x*  +  *y* tanΘ – *py* tanΘ, *y*  +  *x* tanΦ) – *py* tanΦ</span><span class="sxs-lookup"><span data-stu-id="6e39f-260">P' = (*x* + *y* tanΘ – *py* tanΘ, *y* + *x* tanΦ) – *py* tanΦ</span></span>
</dl>

<span data-ttu-id="6e39f-261">o equivalente:</span><span class="sxs-lookup"><span data-stu-id="6e39f-261">or equivalently:</span></span>

<dl> <span data-ttu-id="6e39f-262">P ' = (*x* + (*y* – *py*) tanΘ, *y* + (*x* – *PX*) tanΦ)</span><span class="sxs-lookup"><span data-stu-id="6e39f-262">P' = (*x* + (*y* – *py*)tanΘ, *y* + (*x* – *px*)tanΦ)</span></span>
</dl>

<span data-ttu-id="6e39f-263">Para ver cómo funciona esta transformación, considere cada componente individualmente.</span><span class="sxs-lookup"><span data-stu-id="6e39f-263">To see how this transform works, consider each component individually.</span></span> <span data-ttu-id="6e39f-264">El parámetro Θ mueve cada punto en la dirección x en una cantidad igual a tanΘ.</span><span class="sxs-lookup"><span data-stu-id="6e39f-264">The Θ parameter moves every point in the x direction by an amount equal to tanΘ.</span></span> <span data-ttu-id="6e39f-265">En el diagrama siguiente se muestra la relación entre Θ y el sesgo del eje x.</span><span class="sxs-lookup"><span data-stu-id="6e39f-265">The following diagram shows the relation between Θ and the x-axis skew.</span></span>

![Diagrama que muestra el sesgo a lo largo del eje x.](images/graphics26.png)

<span data-ttu-id="6e39f-267">Este es el mismo sesgo aplicado a un rectángulo:</span><span class="sxs-lookup"><span data-stu-id="6e39f-267">Here is the same skew applied to a rectangle:</span></span>

![Diagrama que muestra el sesgo a lo largo del eje x cuando se aplica a un rectángulo.](images/graphics27.png)

<span data-ttu-id="6e39f-269">El parámetro Φ tiene el mismo efecto, pero a lo largo del eje y:</span><span class="sxs-lookup"><span data-stu-id="6e39f-269">The Φ parameter has the same effect, but along the y-axis:</span></span>

![Diagrama que muestra el sesgo a lo largo del eje y.](images/graphics28.png)

<span data-ttu-id="6e39f-271">En el siguiente diagrama se muestra el sesgo del eje y aplicado a un rectángulo.</span><span class="sxs-lookup"><span data-stu-id="6e39f-271">The next diagram shows y-axis skew applied to a rectangle.</span></span>

![Diagrama que muestra el sesgo a lo largo del eje y cuando se aplica a un rectángulo.](images/graphics29.png)

<span data-ttu-id="6e39f-273">Por último, los parámetros *PX* y *py* desplazan el punto central para el sesgo a lo largo de los ejes x e y.</span><span class="sxs-lookup"><span data-stu-id="6e39f-273">Finally, the parameters *px* and *py* shift the center point for the skew along the x- and y-axes.</span></span>

## <a name="representing-transforms-in-direct2d"></a><span data-ttu-id="6e39f-274">Representar transformaciones en Direct2D</span><span class="sxs-lookup"><span data-stu-id="6e39f-274">Representing Transforms in Direct2D</span></span>

<span data-ttu-id="6e39f-275">Todas las transformaciones de Direct2D son transformaciones afines.</span><span class="sxs-lookup"><span data-stu-id="6e39f-275">All Direct2D transforms are affine transforms.</span></span> <span data-ttu-id="6e39f-276">Direct2D no admite transformaciones no afines.</span><span class="sxs-lookup"><span data-stu-id="6e39f-276">Direct2D does not support non-affine transforms.</span></span> <span data-ttu-id="6e39f-277">Las transformaciones se representan mediante la estructura D2D1 de la [**\_ matriz de \_ 3x2 \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) .</span><span class="sxs-lookup"><span data-stu-id="6e39f-277">Transforms are represented by the [**D2D1\_MATRIX\_3X2\_F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) structure.</span></span> <span data-ttu-id="6e39f-278">Esta estructura define una matriz de 3 × 2.</span><span class="sxs-lookup"><span data-stu-id="6e39f-278">This structure defines a 3 × 2 matrix.</span></span> <span data-ttu-id="6e39f-279">Dado que la tercera columna de una transformación afín siempre es la misma ( \[ 0, 0, 1 \] ) y dado que Direct2D no admite transformaciones no afines, no es necesario especificar toda la matriz de 3 × 3.</span><span class="sxs-lookup"><span data-stu-id="6e39f-279">Because the third column of an affine transform is always the same (\[0, 0, 1\]), and because Direct2D does not support non-affine transforms, there is no need to specify the entire 3 × 3 matrix.</span></span> <span data-ttu-id="6e39f-280">Internamente, Direct2D usa 3 × 3 matrices para calcular las transformaciones.</span><span class="sxs-lookup"><span data-stu-id="6e39f-280">Internally, Direct2D uses 3 × 3 matrices to compute the transforms.</span></span>

<span data-ttu-id="6e39f-281">A los miembros de [**la \_ matriz D2D1 \_ 3x2 \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) se les asigna un nombre según su posición de índice: el miembro **\_ 11** es Element (1,1), el miembro **\_ 12** es Element (1, 2), etc.</span><span class="sxs-lookup"><span data-stu-id="6e39f-281">The members of the [**D2D1\_MATRIX\_3X2\_F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) are named according to their index position: the **\_11** member is element (1,1), the **\_12** member is element (1,2), and so forth.</span></span> <span data-ttu-id="6e39f-282">Aunque puede inicializar los miembros de la estructura directamente, se recomienda usar la clase [**D2D1:: Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) .</span><span class="sxs-lookup"><span data-stu-id="6e39f-282">Although you can initialize the structure members directly, it is recommended to use the [**D2D1::Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) class.</span></span> <span data-ttu-id="6e39f-283">Esta clase hereda **D2D1 \_ Matrix \_ 3x2 \_ F** y proporciona métodos auxiliares para crear cualquiera de las transformaciones afines básicas.</span><span class="sxs-lookup"><span data-stu-id="6e39f-283">This class inherits **D2D1\_MATRIX\_3X2\_F** and provides helper methods for creating any of the basic affine transforms.</span></span> <span data-ttu-id="6e39f-284">La clase también define [**Operator \* ()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) para crear dos o más transformaciones, como se describe en [aplicar transformaciones en Direct2D](applying-transforms-in-direct2d.md).</span><span class="sxs-lookup"><span data-stu-id="6e39f-284">The class also defines [**operator\*()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) for composing two or more transforms, as described in [Applying Transforms in Direct2D](applying-transforms-in-direct2d.md).</span></span>

## <a name="next"></a><span data-ttu-id="6e39f-285">Siguientes</span><span class="sxs-lookup"><span data-stu-id="6e39f-285">Next</span></span>

[<span data-ttu-id="6e39f-286">Módulo 4. Datos proporcionados por el usuario</span><span class="sxs-lookup"><span data-stu-id="6e39f-286">Module 4. User Input</span></span>](module-4--user-input.md)

 

 