---
description: En este tema se enumeran los métodos TransformVectors de la clase Matrix. Para obtener una lista completa de los métodos de la clase Matrix, consulte métodos de matriz.
ms.assetid: 6a2ed6a7-825a-422b-b035-b88746f3ab5d
title: Métodos Matrix. TransformVectors (Gdiplusmatrix. h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3bdb67d839163ffe2d26623a01fc186f8e885ca2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "104987463"
---
# <a name="matrixtransformvectors-methods"></a><span data-ttu-id="294c9-104">Métodos Matrix. TransformVectors</span><span class="sxs-lookup"><span data-stu-id="294c9-104">Matrix.TransformVectors methods</span></span>

<span data-ttu-id="294c9-105">En este tema se enumeran los métodos TransformVectors de la clase [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) .</span><span class="sxs-lookup"><span data-stu-id="294c9-105">This topic lists the TransformVectors methods of the [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) class.</span></span> <span data-ttu-id="294c9-106">Para obtener una lista completa de los métodos de la clase **Matrix** , consulte [métodos de matriz](-gdiplus-class-matrix-methods.md).</span><span class="sxs-lookup"><span data-stu-id="294c9-106">For a complete list of methods for the **Matrix** class, see [Matrix Methods](-gdiplus-class-matrix-methods.md).</span></span>

### <a name="overload-list"></a><span data-ttu-id="294c9-107">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="294c9-107">Overload list</span></span>



| <span data-ttu-id="294c9-108">Método</span><span class="sxs-lookup"><span data-stu-id="294c9-108">Method</span></span>                                                                                                 | <span data-ttu-id="294c9-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="294c9-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
|:-------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="294c9-110">[**TransformVectors (Point \* , int)**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-transformvectors(inoutpoint_inint))</span><span class="sxs-lookup"><span data-stu-id="294c9-110">[**TransformVectors(Point\*,INT)**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-transformvectors(inoutpoint_inint))</span></span>   | <span data-ttu-id="294c9-111">El método [**Matrix:: TransformVectors**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-transformvectors(inoutpoint_inint)) multiplica cada vector de una matriz por esta matriz.</span><span class="sxs-lookup"><span data-stu-id="294c9-111">The [**Matrix::TransformVectors**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-transformvectors(inoutpoint_inint)) method multiplies each vector in an array by this matrix.</span></span> <span data-ttu-id="294c9-112">Los elementos de conversión de esta matriz (tercera fila) se omiten.</span><span class="sxs-lookup"><span data-stu-id="294c9-112">The translation elements of this matrix (third row) are ignored.</span></span> <span data-ttu-id="294c9-113">Cada vector se trata como una matriz de filas.</span><span class="sxs-lookup"><span data-stu-id="294c9-113">Each vector is treated as a row matrix.</span></span> <span data-ttu-id="294c9-114">La multiplicación se realiza con la matriz de filas de la izquierda y esta matriz a la derecha.</span><span class="sxs-lookup"><span data-stu-id="294c9-114">The multiplication is performed with the row matrix on the left and this matrix on the right.</span></span><br/>  |
| <span data-ttu-id="294c9-115">[**TransformVectors (PointF \* , int)**](/previous-versions//ms535319(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="294c9-115">[**TransformVectors(PointF\*,INT)**](/previous-versions//ms535319(v=vs.85))</span></span> | <span data-ttu-id="294c9-116">El método [**Matrix:: TransformVectors**](/previous-versions//ms535319(v=vs.85)) multiplica cada vector de una matriz por esta matriz.</span><span class="sxs-lookup"><span data-stu-id="294c9-116">The [**Matrix::TransformVectors**](/previous-versions//ms535319(v=vs.85)) method multiplies each vector in an array by this matrix.</span></span> <span data-ttu-id="294c9-117">Los elementos de conversión de esta matriz (tercera fila) se omiten.</span><span class="sxs-lookup"><span data-stu-id="294c9-117">The translation elements of this matrix (third row) are ignored.</span></span> <span data-ttu-id="294c9-118">Cada vector se trata como una matriz de filas.</span><span class="sxs-lookup"><span data-stu-id="294c9-118">Each vector is treated as a row matrix.</span></span> <span data-ttu-id="294c9-119">La multiplicación se realiza con la matriz de filas de la izquierda y esta matriz a la derecha.</span><span class="sxs-lookup"><span data-stu-id="294c9-119">The multiplication is performed with the row matrix on the left and this matrix on the right.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="294c9-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="294c9-120">Requirements</span></span>



| <span data-ttu-id="294c9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="294c9-121">Requirement</span></span> | <span data-ttu-id="294c9-122">Value</span><span class="sxs-lookup"><span data-stu-id="294c9-122">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="294c9-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="294c9-123">Header</span></span><br/> | <dl> <span data-ttu-id="294c9-124"><dt>Gdiplusmatrix. h</dt></span><span class="sxs-lookup"><span data-stu-id="294c9-124"><dt>Gdiplusmatrix.h</dt></span></span> </dl> |



 

 
