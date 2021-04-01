---
title: Directivas de control de errores de Direct2D
description: 'En este tema se describen las directivas de control de errores de Direct2D. Contiene las siguientes secciones:'
ms.assetid: b5fa327a-a315-46fa-aa78-8a5733faae01
keywords:
- Direct2D, control de errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fc930e7ee9e5b73b5f676103f45ffe25e4d4e61
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995539"
---
# <a name="direct2d-error-handling-policies"></a><span data-ttu-id="71857-105">Directivas de control de errores de Direct2D</span><span class="sxs-lookup"><span data-stu-id="71857-105">Direct2D Error Handling Policies</span></span>

<span data-ttu-id="71857-106">En este tema se describen las directivas de control de errores de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="71857-106">This topic describes the Direct2D error handling policies.</span></span> <span data-ttu-id="71857-107">Contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="71857-107">It contains the following sections.</span></span>

-   [<span data-ttu-id="71857-108">Uso de HRESULT</span><span class="sxs-lookup"><span data-stu-id="71857-108">Use of HRESULT</span></span>](#use-of-hresult)
-   [<span data-ttu-id="71857-109">Valor devuelto de las funciones por lotes</span><span class="sxs-lookup"><span data-stu-id="71857-109">Return Value of Batched Functions</span></span>](#return-value-of-batched-functions)
-   [<span data-ttu-id="71857-110">Entrada no válida</span><span class="sxs-lookup"><span data-stu-id="71857-110">Invalid Input</span></span>](#invalid-input)
    -   [<span data-ttu-id="71857-111">Puntero de salida</span><span class="sxs-lookup"><span data-stu-id="71857-111">Output Pointer</span></span>](#output-pointer)
    -   [<span data-ttu-id="71857-112">Parámetro obligatorio</span><span class="sxs-lookup"><span data-stu-id="71857-112">Required Parameter</span></span>](#required-parameter)
-   [<span data-ttu-id="71857-113">NaN y RECTÁNGULOs de entrada mal ordenados</span><span class="sxs-lookup"><span data-stu-id="71857-113">NaN and Poorly Ordered Input RECTs</span></span>](#nan-and-poorly-ordered-input-rects)
    -   [<span data-ttu-id="71857-114">NaN como entrada</span><span class="sxs-lookup"><span data-stu-id="71857-114">NaN as Input</span></span>](#nan-as-input)
    -   [<span data-ttu-id="71857-115">RECTÁNGULOs de entrada mal ordenados</span><span class="sxs-lookup"><span data-stu-id="71857-115">Poorly Ordered Input RECTs</span></span>](#poorly-ordered-input-rects)

## <a name="use-of-hresult"></a><span data-ttu-id="71857-116">Uso de HRESULT</span><span class="sxs-lookup"><span data-stu-id="71857-116">Use of HRESULT</span></span>

<span data-ttu-id="71857-117">Si una función no se procesa por lotes y puede tener un error en tiempo de ejecución, debe devolver **HRESULT** para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="71857-117">If a function is not batched and can have a run-time failure, it should return **HRESULT** to indicate a failure.</span></span> <span data-ttu-id="71857-118">Un error en tiempo de ejecución es cualquier error que no se puede evitar en tiempo de diseño, como memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="71857-118">A run-time failure is any failure that cannot be avoided at design time, such as out of memory.</span></span>

## <a name="return-value-of-batched-functions"></a><span data-ttu-id="71857-119">Valor devuelto de las funciones por lotes</span><span class="sxs-lookup"><span data-stu-id="71857-119">Return Value of Batched Functions</span></span>

<span data-ttu-id="71857-120">Las funciones por lotes en Direct2D son las funciones que se procesan como una sola unidad cuando se llama a [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) .</span><span class="sxs-lookup"><span data-stu-id="71857-120">Batched functions in Direct2D are the functions that are processed as a single unit when [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) is called.</span></span> <span data-ttu-id="71857-121">Son los comandos de dibujo entre los comandos [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) y **EndDraw** o de [**GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink).</span><span class="sxs-lookup"><span data-stu-id="71857-121">They are the drawing commands between [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) and **EndDraw** or commands on [**GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink).</span></span> <span data-ttu-id="71857-122">En el caso de estas funciones, se registran errores en el momento en que se completa el lote.</span><span class="sxs-lookup"><span data-stu-id="71857-122">For these functions, errors are reported at the time the batch is completed.</span></span> <span data-ttu-id="71857-123">El error se devuelve después de **EndDraw** para dibujar comandos y después de **Close** para **GeometrySink**.</span><span class="sxs-lookup"><span data-stu-id="71857-123">The error is returned after **EndDraw** for drawing commands, and after **Close** for **GeometrySink**.</span></span>

<span data-ttu-id="71857-124">RenderTargets detener dibujo si se establece un estado de error, pero una aplicación puede llamar a [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) para restablecer el estado de error y reanudar el dibujo.</span><span class="sxs-lookup"><span data-stu-id="71857-124">RenderTargets stop drawing if an error state is set, but an application can call [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) to reset the error state and resume drawing.</span></span>

<span data-ttu-id="71857-125">Las funciones **Get** y **set** no tienen ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="71857-125">**Get** and **Set** functions have no return value.</span></span> <span data-ttu-id="71857-126">Sin embargo, si una función de **conjunto** tiene una entrada no válida, la capa de depuración genera un mensaje.</span><span class="sxs-lookup"><span data-stu-id="71857-126">However, if a **Set** function has an invalid input, the debug layer generates a message.</span></span> <span data-ttu-id="71857-127">En este caso, no se establece ningún estado de error y la función **set** no hace nada.</span><span class="sxs-lookup"><span data-stu-id="71857-127">In this case, no error state is set and the **Set** function does nothing.</span></span>

## <a name="invalid-input"></a><span data-ttu-id="71857-128">Entrada no válida</span><span class="sxs-lookup"><span data-stu-id="71857-128">Invalid Input</span></span>

<span data-ttu-id="71857-129">Direct2D desreferencia los punteros de salida y los parámetros necesarios, lo que da lugar a infracciones de acceso cuando los punteros no son válidos o son **null**.</span><span class="sxs-lookup"><span data-stu-id="71857-129">Direct2D dereferences output pointers and required parameters which result in access violations when the pointers are invalid or **NULL**.</span></span>

### <a name="output-pointer"></a><span data-ttu-id="71857-130">Puntero de salida</span><span class="sxs-lookup"><span data-stu-id="71857-130">Output Pointer</span></span>

<span data-ttu-id="71857-131">Direct2D desreferencia un puntero de salida y lo asigna a **null** inmediatamente al entrar en la función.</span><span class="sxs-lookup"><span data-stu-id="71857-131">Direct2D dereferences an output pointer and assigns it to **NULL** immediately upon entering the function.</span></span> <span data-ttu-id="71857-132">Esto produce una infracción de acceso si un llamador pasa **null** como el puntero al valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="71857-132">This causes an access violation if a caller passes in **NULL** as the pointer to the return value.</span></span> <span data-ttu-id="71857-133">Esta Directiva también se aplica a las matrices de punteros.</span><span class="sxs-lookup"><span data-stu-id="71857-133">This policy also applies to arrays of pointers.</span></span> <span data-ttu-id="71857-134">Para otros parámetros de salida, como un struct, la desreferenciación se produce más tarde y también produce una infracción de acceso.</span><span class="sxs-lookup"><span data-stu-id="71857-134">For other output parameters, such as a struct, the dereference happens later and also results in an access violation.</span></span> <span data-ttu-id="71857-135">Sin embargo, hay algunos métodos que tienen punteros de salida opcionales (es decir, [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw), [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)) que no producirán una infracción de acceso.</span><span class="sxs-lookup"><span data-stu-id="71857-135">However, there are some methods that have optional output pointers (that is, [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw), [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)) that will not cause an access violation.</span></span>

### <a name="required-parameter"></a><span data-ttu-id="71857-136">Parámetro obligatorio</span><span class="sxs-lookup"><span data-stu-id="71857-136">Required Parameter</span></span>

<span data-ttu-id="71857-137">Si se pasa **null** a cualquier función que requiera un valor válido, la función desreferencia el puntero incorrecto y produce una infracción de acceso.</span><span class="sxs-lookup"><span data-stu-id="71857-137">If **NULL** is passed to any function requiring a valid value, the function dereferences the bad pointer early resulting in an access violation.</span></span> <span data-ttu-id="71857-138">En el caso de los parámetros de entrada opcionales, **null** es un valor válido que da como resultado un valor predeterminado razonable.</span><span class="sxs-lookup"><span data-stu-id="71857-138">For optional input parameters, **NULL** is a valid value that results in some reasonable default.</span></span>

## <a name="nan-and-poorly-ordered-input-rects"></a><span data-ttu-id="71857-139">NaN y RECTÁNGULOs de entrada mal ordenados</span><span class="sxs-lookup"><span data-stu-id="71857-139">NaN and Poorly Ordered Input RECTs</span></span>

<span data-ttu-id="71857-140">En Direct2D, NaN se considera una entrada válida y los RECTÁNGULOs de entrada mal ordenados se ordenan.</span><span class="sxs-lookup"><span data-stu-id="71857-140">In Direct2D, NaN is considered a valid input and poorly ordered input RECTs are sorted.</span></span>

### <a name="nan-as-input"></a><span data-ttu-id="71857-141">NaN como entrada</span><span class="sxs-lookup"><span data-stu-id="71857-141">NaN as Input</span></span>

<span data-ttu-id="71857-142">NaN se considera una entrada válida, aunque normalmente da como resultado el primitivo que contiene NaN que no se dibuja.</span><span class="sxs-lookup"><span data-stu-id="71857-142">NaN is considered a valid input, though it typically results in the primitive that contains the NaN not drawing.</span></span> <span data-ttu-id="71857-143">La API de Direct2D no proporciona un filtrado explícito de NaN para validar la entrada.</span><span class="sxs-lookup"><span data-stu-id="71857-143">The Direct2D API does not provide explicit filtering of NaN to validate input.</span></span>

### <a name="poorly-ordered-input-rects"></a><span data-ttu-id="71857-144">RECTÁNGULOs de entrada mal ordenados</span><span class="sxs-lookup"><span data-stu-id="71857-144">Poorly Ordered Input RECTs</span></span>

<span data-ttu-id="71857-145">Los RECTÁNGULOs de entrada mal ordenados se ordenan para que las esquinas superior, izquierda e inferior se especifiquen correctamente.</span><span class="sxs-lookup"><span data-stu-id="71857-145">Poorly ordered input RECTs are sorted so that the top, left and bottom, right corners are correctly specified.</span></span> <span data-ttu-id="71857-146">Para la salida, los rectángulos vacíos tienen el siguiente aspecto: {Infinity, Infinity, FloatMax, FloatMax}.</span><span class="sxs-lookup"><span data-stu-id="71857-146">For output, empty rectangles look like this: {Infinity, Infinity, FloatMax, FloatMax}.</span></span>

 

 