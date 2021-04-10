---
description: Curvas de parámetro
ms.assetid: c073e7d0-c119-4c36-a5b2-b31dd6326ac8
title: Curvas de parámetro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc3c482112c8bd76217f5cbdabdf3cda13b09c3e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152501"
---
# <a name="parameter-curves"></a><span data-ttu-id="19aca-103">Curvas de parámetro</span><span class="sxs-lookup"><span data-stu-id="19aca-103">Parameter Curves</span></span>

<span data-ttu-id="19aca-104">Los parámetros multimedia pueden seguir una curva a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="19aca-104">Media parameters are able to follow a curve over time.</span></span> <span data-ttu-id="19aca-105">Cada curva se describe mediante una fórmula matemática y dos puntos de conexión.</span><span class="sxs-lookup"><span data-stu-id="19aca-105">Each curve is described by a mathematical formula and two end-points.</span></span> <span data-ttu-id="19aca-106">Cada extremo se define mediante un tiempo de referencia y el valor de la curva en ese momento.</span><span class="sxs-lookup"><span data-stu-id="19aca-106">Each end-point is defined by a reference time and the value of the curve at that time.</span></span> <span data-ttu-id="19aca-107">La fórmula se usa para calcular valores intermedios entre los puntos y determina la forma de la curva.</span><span class="sxs-lookup"><span data-stu-id="19aca-107">The formula is used to calculate intermediate values between the points, and determines the shape of the curve.</span></span> <span data-ttu-id="19aca-108">Las curvas posibles son:</span><span class="sxs-lookup"><span data-stu-id="19aca-108">The possible curves are:</span></span>

-   <span data-ttu-id="19aca-109">Avanzar</span><span class="sxs-lookup"><span data-stu-id="19aca-109">Jump</span></span>
-   <span data-ttu-id="19aca-110">Lineal</span><span class="sxs-lookup"><span data-stu-id="19aca-110">Linear</span></span>
-   <span data-ttu-id="19aca-111">Square</span><span class="sxs-lookup"><span data-stu-id="19aca-111">Square</span></span>
-   <span data-ttu-id="19aca-112">Cuadrado inverso</span><span class="sxs-lookup"><span data-stu-id="19aca-112">Inverse square</span></span>
-   <span data-ttu-id="19aca-113">Seno</span><span class="sxs-lookup"><span data-stu-id="19aca-113">Sine</span></span>

<span data-ttu-id="19aca-114">"Salto" significa saltar directamente al valor final.</span><span class="sxs-lookup"><span data-stu-id="19aca-114">"Jump" means jump directly to the end value.</span></span> <span data-ttu-id="19aca-115">Las demás curvas se muestran en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="19aca-115">The other curves are shown in the following diagram.</span></span>

![curvas de parámetro](images/param-curves01.png)

<span data-ttu-id="19aca-117">Matemáticamente, las curvas funcionan como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="19aca-117">Mathematically, the curves work as follows.</span></span> <span data-ttu-id="19aca-118">Supongamos que una curva comienza en el momento *t*₀ con un valor de *v*₀ y termina en el tiempo *t*₁ con un valor de *v*₁.</span><span class="sxs-lookup"><span data-stu-id="19aca-118">Suppose that a curve begins at time *t*₀ with a value of *v*₀, and ends at time *t*₁ with a value of *v*₁.</span></span> <span data-ttu-id="19aca-119">Los dos puntos que definen la curva son (*t*₀, *v*₀) and (*t*₁, *v*₁).</span><span class="sxs-lookup"><span data-stu-id="19aca-119">The two points that define the curve are (*t*₀, *v*₀) and (*t*₁, *v*₁).</span></span>

-   <span data-ttu-id="19aca-120">Deje que Δ *t* sea la duración total de la curva, *t*₁ –*t*₀.</span><span class="sxs-lookup"><span data-stu-id="19aca-120">Let Δ *t* be the total duration of the curve, *t*₁–*t*₀.</span></span>
-   <span data-ttu-id="19aca-121">Permita que Δ *v* sea el intervalo entre los valores inicial y final, *v*₁ –*v*₀.</span><span class="sxs-lookup"><span data-stu-id="19aca-121">Let Δ *v* be the interval between the starting and ending values, *v*₁–*v*₀.</span></span>
-   <span data-ttu-id="19aca-122">En cualquier momento *t* como t *₀ <*= *t*  <=  *t*₁, deje Δ *t*' = *t*–*t*₀.</span><span class="sxs-lookup"><span data-stu-id="19aca-122">At any time *t* such that *t*₀ <= *t* <= *t*₁, let Δ *t*' = *t*–*t*₀.</span></span>

![cálculo del parámetro](images/param-curves02.png)

<span data-ttu-id="19aca-124">El valor del parámetro en el momento *t* es:</span><span class="sxs-lookup"><span data-stu-id="19aca-124">The value of the parameter at time *t* is:</span></span>

<span data-ttu-id="19aca-125">*v* = f (Δ *t*'/Δ *t* ) \* Δ *v*  +  *v*₀</span><span class="sxs-lookup"><span data-stu-id="19aca-125">*v* = f( Δ *t*' / Δ *t* ) \* Δ *v* + *v*₀</span></span>

<span data-ttu-id="19aca-126">donde f (x) es una función determinada por el tipo de curva:</span><span class="sxs-lookup"><span data-stu-id="19aca-126">where f(x) is a function determined by the curve type:</span></span>

-   <span data-ttu-id="19aca-127">Lineal: y = x</span><span class="sxs-lookup"><span data-stu-id="19aca-127">Linear: y = x</span></span>
-   <span data-ttu-id="19aca-128">Cuadrado: y = x ^ 2</span><span class="sxs-lookup"><span data-stu-id="19aca-128">Square: y = x^2</span></span>
-   <span data-ttu-id="19aca-129">Cuadrado inverso: y = sqrt (x)</span><span class="sxs-lookup"><span data-stu-id="19aca-129">Inverse square: y = sqrt(x)</span></span>
-   <span data-ttu-id="19aca-130">Seno: y = \[ sin (πx – π/2) + 1 \] /2</span><span class="sxs-lookup"><span data-stu-id="19aca-130">Sine: y = \[ sin(πx – π/2) + 1 \] / 2</span></span>

<span data-ttu-id="19aca-131">Observe que Δ *t*' < Δ t, por lo que el término Δ *t*'/Δ *t* oscila entre *0 y 1*.</span><span class="sxs-lookup"><span data-stu-id="19aca-131">Observe that Δ *t*' < Δ *t*, so the term Δ *t*'/Δ *t* ranges from 0 to 1.</span></span> <span data-ttu-id="19aca-132">Por lo tanto, f (x) también oscila entre 0 y 1, y *v* siempre cae entre *v*₀ y *v*₁.</span><span class="sxs-lookup"><span data-stu-id="19aca-132">Therefore, f(x) also ranges from 0 to 1, and *v* always falls between *v*₀ and *v*₁.</span></span> <span data-ttu-id="19aca-133">Esto es así si *v*₀ < *v*₁ o viceversa.</span><span class="sxs-lookup"><span data-stu-id="19aca-133">This is true whether *v*₀ < *v*₁ or vice versa.</span></span> <span data-ttu-id="19aca-134">En otras palabras, la curva está limitada por el rectángulo (*t*₀, *v*₀, *t*₁, *v*₁).</span><span class="sxs-lookup"><span data-stu-id="19aca-134">In other words, the curve is bounded by the rectangle (*t*₀, *v*₀, *t*₁, *v*₁).</span></span>

<span data-ttu-id="19aca-135">En el caso de la curva sinusoidal, el valor de (πx – π/2) va de – π/2 a π/2, lo que significa que sin (πx – π/2) oscila entre – 1 y 1.</span><span class="sxs-lookup"><span data-stu-id="19aca-135">For the sine curve, the value of (πx – π/2) ranges from –π/2 to π/2, which means that sin(πx – π/2) ranges from –1 to 1.</span></span> <span data-ttu-id="19aca-136">A continuación, el resultado se normaliza de modo que f (x) caiga en el intervalo (0 – 1).</span><span class="sxs-lookup"><span data-stu-id="19aca-136">The result is then normalized so that f(x) falls into the range (0–1).</span></span>

## <a name="related-topics"></a><span data-ttu-id="19aca-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="19aca-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19aca-138">Parámetros multimedia</span><span class="sxs-lookup"><span data-stu-id="19aca-138">Media Parameters</span></span>](media-parameters.md)
</dt> </dl>

 

 



