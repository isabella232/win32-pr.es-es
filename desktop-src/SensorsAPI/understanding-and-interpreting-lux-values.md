---
description: El tipo de datos del sensor principal para los sensores de luz ambiente se luminancia en lux (lúmenes por metro cuadrado). Los principios descritos en este tema se basan en tomar valores de Lux como entrada y reaccionar a esos datos en un programa.
ms.assetid: 29855779-7c27-4cfe-b8af-b33bc86a1f62
title: Descripción e interpretación de los valores de Lux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8012f983eeac29cc07b18ac2d27918d2df6ed52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082988"
---
# <a name="understanding-and-interpreting-lux-values"></a><span data-ttu-id="dc908-104">Descripción e interpretación de los valores de Lux</span><span class="sxs-lookup"><span data-stu-id="dc908-104">Understanding and Interpreting Lux Values</span></span>

<span data-ttu-id="dc908-105">El tipo de datos del sensor principal para los sensores de luz ambiente se luminancia en lux (lúmenes por metro cuadrado).</span><span class="sxs-lookup"><span data-stu-id="dc908-105">The primary sensor data type for ambient light sensors is illuminance in lux (lumens per square meter).</span></span> <span data-ttu-id="dc908-106">Los principios descritos en este tema se basan en tomar valores de Lux como entrada y reaccionar a esos datos en un programa.</span><span class="sxs-lookup"><span data-stu-id="dc908-106">The principles outlined in this topic are based on taking lux values as input and reacting to that data in a program.</span></span>

<span data-ttu-id="dc908-107">Las lecturas de Lux son directamente proporcionales a la energía por metro cuadrado que se absorbe por segundo.</span><span class="sxs-lookup"><span data-stu-id="dc908-107">Lux readings are directly proportional to the energy per square meter that is absorbed per second.</span></span> <span data-ttu-id="dc908-108">La percepción humana de los niveles de luz no es tan sencilla.</span><span class="sxs-lookup"><span data-stu-id="dc908-108">Human perception of light levels is not so straightforward.</span></span> <span data-ttu-id="dc908-109">La percepción humana de la luz es complicada porque nuestros ojos se están ajustando constantemente y otros procesos biológicos están afectando a nuestra percepción.</span><span class="sxs-lookup"><span data-stu-id="dc908-109">Human perception of light is complicated because our eyes are constantly adjusting and other biological processes are affecting our perception.</span></span> <span data-ttu-id="dc908-110">Sin embargo, podemos pensar en esta percepción desde una perspectiva simplificada creando varios intervalos de interés con umbrales superiores e inferiores conocidos.</span><span class="sxs-lookup"><span data-stu-id="dc908-110">However, we can think of this perception from a simplified perspective by creating several ranges of interest with known upper and lower thresholds.</span></span>

<span data-ttu-id="dc908-111">En el siguiente conjunto de datos de ejemplo se representan umbrales aproximados para las condiciones de iluminación comunes y el paso de iluminación correspondiente.</span><span class="sxs-lookup"><span data-stu-id="dc908-111">The following example data set represents rough thresholds for common lighting conditions, and the corresponding lighting step.</span></span> <span data-ttu-id="dc908-112">En este caso, cada paso de iluminación representa un cambio en el entorno de iluminación.</span><span class="sxs-lookup"><span data-stu-id="dc908-112">Here, each lighting step represents a change in lighting environment.</span></span>

> [!Note]  
> <span data-ttu-id="dc908-113">Este conjunto de datos es para la ilustración y puede que no sea completamente preciso para todos los usuarios o situaciones.</span><span class="sxs-lookup"><span data-stu-id="dc908-113">This data set is for illustration and may not be completely accurate for all users or situations.</span></span>

 



| <span data-ttu-id="dc908-114">Condición de iluminación</span><span class="sxs-lookup"><span data-stu-id="dc908-114">Lighting condition</span></span> | <span data-ttu-id="dc908-115">Desde (Lux)</span><span class="sxs-lookup"><span data-stu-id="dc908-115">From (lux)</span></span> | <span data-ttu-id="dc908-116">A (Lux)</span><span class="sxs-lookup"><span data-stu-id="dc908-116">To (lux)</span></span> | <span data-ttu-id="dc908-117">Valor medio (Lux)</span><span class="sxs-lookup"><span data-stu-id="dc908-117">Mean value (lux)</span></span> | <span data-ttu-id="dc908-118">Paso de iluminación</span><span class="sxs-lookup"><span data-stu-id="dc908-118">Lighting step</span></span> |
|--------------------|------------|----------|------------------|---------------|
| <span data-ttu-id="dc908-119">Tono negro</span><span class="sxs-lookup"><span data-stu-id="dc908-119">Pitch Black</span></span>        | <span data-ttu-id="dc908-120">0</span><span class="sxs-lookup"><span data-stu-id="dc908-120">0</span></span>          | <span data-ttu-id="dc908-121">10</span><span class="sxs-lookup"><span data-stu-id="dc908-121">10</span></span>       | <span data-ttu-id="dc908-122">5</span><span class="sxs-lookup"><span data-stu-id="dc908-122">5</span></span>                | <span data-ttu-id="dc908-123">1</span><span class="sxs-lookup"><span data-stu-id="dc908-123">1</span></span>             |
| <span data-ttu-id="dc908-124">Muy oscuro</span><span class="sxs-lookup"><span data-stu-id="dc908-124">Very Dark</span></span>          | <span data-ttu-id="dc908-125">11</span><span class="sxs-lookup"><span data-stu-id="dc908-125">11</span></span>         | <span data-ttu-id="dc908-126">50</span><span class="sxs-lookup"><span data-stu-id="dc908-126">50</span></span>       | <span data-ttu-id="dc908-127">30</span><span class="sxs-lookup"><span data-stu-id="dc908-127">30</span></span>               | <span data-ttu-id="dc908-128">2</span><span class="sxs-lookup"><span data-stu-id="dc908-128">2</span></span>             |
| <span data-ttu-id="dc908-129">Inpuertas oscuras</span><span class="sxs-lookup"><span data-stu-id="dc908-129">Dark Indoors</span></span>       | <span data-ttu-id="dc908-130">51</span><span class="sxs-lookup"><span data-stu-id="dc908-130">51</span></span>         | <span data-ttu-id="dc908-131">200</span><span class="sxs-lookup"><span data-stu-id="dc908-131">200</span></span>      | <span data-ttu-id="dc908-132">125</span><span class="sxs-lookup"><span data-stu-id="dc908-132">125</span></span>              | <span data-ttu-id="dc908-133">3</span><span class="sxs-lookup"><span data-stu-id="dc908-133">3</span></span>             |
| <span data-ttu-id="dc908-134">Atenuar inpuertas</span><span class="sxs-lookup"><span data-stu-id="dc908-134">Dim Indoors</span></span>        | <span data-ttu-id="dc908-135">201</span><span class="sxs-lookup"><span data-stu-id="dc908-135">201</span></span>        | <span data-ttu-id="dc908-136">400</span><span class="sxs-lookup"><span data-stu-id="dc908-136">400</span></span>      | <span data-ttu-id="dc908-137">300</span><span class="sxs-lookup"><span data-stu-id="dc908-137">300</span></span>              | <span data-ttu-id="dc908-138">4</span><span class="sxs-lookup"><span data-stu-id="dc908-138">4</span></span>             |
| <span data-ttu-id="dc908-139">Interiores normales</span><span class="sxs-lookup"><span data-stu-id="dc908-139">Normal Indoors</span></span>     | <span data-ttu-id="dc908-140">401</span><span class="sxs-lookup"><span data-stu-id="dc908-140">401</span></span>        | <span data-ttu-id="dc908-141">1000</span><span class="sxs-lookup"><span data-stu-id="dc908-141">1000</span></span>     | <span data-ttu-id="dc908-142">700</span><span class="sxs-lookup"><span data-stu-id="dc908-142">700</span></span>              | <span data-ttu-id="dc908-143">5</span><span class="sxs-lookup"><span data-stu-id="dc908-143">5</span></span>             |
| <span data-ttu-id="dc908-144">Indoors brillantes</span><span class="sxs-lookup"><span data-stu-id="dc908-144">Bright Indoors</span></span>     | <span data-ttu-id="dc908-145">1001</span><span class="sxs-lookup"><span data-stu-id="dc908-145">1001</span></span>       | <span data-ttu-id="dc908-146">5000</span><span class="sxs-lookup"><span data-stu-id="dc908-146">5000</span></span>     | <span data-ttu-id="dc908-147">3000</span><span class="sxs-lookup"><span data-stu-id="dc908-147">3000</span></span>             | <span data-ttu-id="dc908-148">6</span><span class="sxs-lookup"><span data-stu-id="dc908-148">6</span></span>             |
| <span data-ttu-id="dc908-149">Atenuar en el exterior</span><span class="sxs-lookup"><span data-stu-id="dc908-149">Dim Outdoors</span></span>       | <span data-ttu-id="dc908-150">5001</span><span class="sxs-lookup"><span data-stu-id="dc908-150">5001</span></span>       | <span data-ttu-id="dc908-151">10 000</span><span class="sxs-lookup"><span data-stu-id="dc908-151">10,000</span></span>   | <span data-ttu-id="dc908-152">7500</span><span class="sxs-lookup"><span data-stu-id="dc908-152">7500</span></span>             | <span data-ttu-id="dc908-153">7</span><span class="sxs-lookup"><span data-stu-id="dc908-153">7</span></span>             |
| <span data-ttu-id="dc908-154">En el exterior de la nube</span><span class="sxs-lookup"><span data-stu-id="dc908-154">Cloudy Outdoors</span></span>    | <span data-ttu-id="dc908-155">10.001</span><span class="sxs-lookup"><span data-stu-id="dc908-155">10,001</span></span>     | <span data-ttu-id="dc908-156">30,000</span><span class="sxs-lookup"><span data-stu-id="dc908-156">30,000</span></span>   | <span data-ttu-id="dc908-157">20 000</span><span class="sxs-lookup"><span data-stu-id="dc908-157">20,000</span></span>           | <span data-ttu-id="dc908-158">8</span><span class="sxs-lookup"><span data-stu-id="dc908-158">8</span></span>             |
| <span data-ttu-id="dc908-159">Luz solar directa</span><span class="sxs-lookup"><span data-stu-id="dc908-159">Direct Sunlight</span></span>    | <span data-ttu-id="dc908-160">30.001</span><span class="sxs-lookup"><span data-stu-id="dc908-160">30,001</span></span>     | <span data-ttu-id="dc908-161">100 000</span><span class="sxs-lookup"><span data-stu-id="dc908-161">100,000</span></span>  | <span data-ttu-id="dc908-162">65.000</span><span class="sxs-lookup"><span data-stu-id="dc908-162">65,000</span></span>           | <span data-ttu-id="dc908-163">9</span><span class="sxs-lookup"><span data-stu-id="dc908-163">9</span></span>             |



 

<span data-ttu-id="dc908-164">Si visualizamos estos datos mediante los valores medios de esta tabla, vemos que la relación de lux a iluminación-paso no es lineal, tal como se muestra en el gráfico siguiente.</span><span class="sxs-lookup"><span data-stu-id="dc908-164">If we visualize this data by using the mean values from this table, we see that the lux-to-lighting-step relationship is not linear, as show in the following graph.</span></span>

![gráfico luminancia lineal](images/luxtostep.png)

<span data-ttu-id="dc908-166">Sin embargo, si vemos estos datos con una escala logarítmica en el eje x, podemos ver que emerge una relación lineal aproximadamente.</span><span class="sxs-lookup"><span data-stu-id="dc908-166">However, if we view this data by using a logarithmic scale on the x-axis, we can see that a roughly linear relationship emerges.</span></span>

![gráfico luminancia logarítmico](images/luxlogtostep.png)

### <a name="an-example-transform"></a><span data-ttu-id="dc908-168">Transformación de ejemplo</span><span class="sxs-lookup"><span data-stu-id="dc908-168">An Example Transform</span></span>

<span data-ttu-id="dc908-169">En función del conjunto de datos de ejemplo para los sensores de luz ambiente que se proporcionaron anteriormente, podría llegar a la siguiente ecuación para asignar valores lux a la percepción humana.</span><span class="sxs-lookup"><span data-stu-id="dc908-169">Based on the sample data set for ambient light sensors previously provided, you could arrive at the following equation to map lux values to human perception.</span></span> <span data-ttu-id="dc908-170">En este ejemplo, los valores esperados van de 0 lux a 1 millón Lux.</span><span class="sxs-lookup"><span data-stu-id="dc908-170">In this example, the expected values range from 0 lux to 1,000,000 lux.</span></span>

![ecuación de valor Lux](images/sensor-lux-equation.jpg)

<span data-ttu-id="dc908-172">Esta ecuación produce valores que varían en un modo lineal aproximadamente entre 0,0 y 1,0.</span><span class="sxs-lookup"><span data-stu-id="dc908-172">This equation results in values that vary in a roughly linear fashion between 0.0 and 1.0.</span></span> <span data-ttu-id="dc908-173">Este resultado indica cómo cambió la iluminación percibida por el usuario en función del conjunto de datos de ejemplo que se mostró anteriormente.</span><span class="sxs-lookup"><span data-stu-id="dc908-173">This result indicates how human-perceived lighting changed based on the example data set that was shown previously.</span></span>

 

 



