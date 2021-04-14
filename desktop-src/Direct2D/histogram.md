---
title: Efecto de histograma
description: Use el efecto histograma para generar un histograma para el mapa de bits de entrada en función del número especificado de ubicaciones.
ms.assetid: 458E2334-F383-41DE-9479-601AC3007BF3
keywords:
- efecto de histograma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b654ffb2b830914b00a59490ceb429b5de9c51cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422230"
---
# <a name="histogram-effect"></a><span data-ttu-id="1db31-104">Efecto de histograma</span><span class="sxs-lookup"><span data-stu-id="1db31-104">Histogram effect</span></span>

<span data-ttu-id="1db31-105">Use el efecto histograma para generar un histograma para el mapa de bits de entrada en función del número especificado de ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="1db31-105">Use the histogram effect to generate a histogram for the input bitmap based on the specified number of bins.</span></span>

<span data-ttu-id="1db31-106">El CLSID para este efecto es CLSID \_ D2D1Histogram.</span><span class="sxs-lookup"><span data-stu-id="1db31-106">The CLSID for this effect is CLSID\_D2D1Histogram.</span></span>

-   [<span data-ttu-id="1db31-107">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1db31-107">Example</span></span>](#example)
-   [<span data-ttu-id="1db31-108">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="1db31-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="1db31-109">Selectores de canal</span><span class="sxs-lookup"><span data-stu-id="1db31-109">Channel selectors</span></span>](#channel-selectors)
-   [<span data-ttu-id="1db31-110">Salida de datos</span><span class="sxs-lookup"><span data-stu-id="1db31-110">Data output</span></span>](#data-output)
-   [<span data-ttu-id="1db31-111">Comentarios:</span><span class="sxs-lookup"><span data-stu-id="1db31-111">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="1db31-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1db31-112">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="1db31-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1db31-113">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="1db31-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1db31-114">Example</span></span>



| <span data-ttu-id="1db31-115">Antes</span><span class="sxs-lookup"><span data-stu-id="1db31-115">Before</span></span>                                                     |
|------------------------------------------------------------|
| ![imagen anterior al efecto.](images/default-before.jpg) |
| <span data-ttu-id="1db31-117">Gráfico de los datos de salida del histograma</span><span class="sxs-lookup"><span data-stu-id="1db31-117">Graph of the histogram output data</span></span>                         |
| ![la imagen después de la transformación.](images/33-histogram.png) |



 


```C++
ComPtr<ID2D1Effect> histogramEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Histogram, &histogramEffect);

histogramEffect->SetInputEffect(0, m_2DAffineTransformEffectRight.Get());
histogramEffect->SetValue(D2D1_HISTOGRAM_PROP_CHANNEL_SELECT, D2D1_CHANNEL_SELECTOR_G);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(histogramEffect.Get());
m_d2dContext->EndDraw();

// The histogram data is only available once the effect has been 'drawn'.
int histogramBinCount;

HRESULT hr = histogramEffect->GetValue(D2D1_HISTOGRAM_PROP_NUM_BINS, &histogramBinCount);

float *histogramData = new float[histogramBinCount];
hr = histogramEffect->GetValue(D2D1_HISTOGRAM_PROP_HISTOGRAM_OUTPUT, 
                               reinterpret_cast<BYTE*>(histogramData), 
                               histogramBinCount * sizeof(float));
```



## <a name="effect-properties"></a><span data-ttu-id="1db31-119">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="1db31-119">Effect properties</span></span>

<span data-ttu-id="1db31-120">Esta es la ecuación para generar la salida.</span><span class="sxs-lookup"><span data-stu-id="1db31-120">Here's the equation to generate the output.</span></span>

![la ecuación para generar el resultado del efecto del histograma.](images/histogram-formula.png)

<span data-ttu-id="1db31-122">*i* se evalúa desde 0 hasta el número de ubicaciones. El efecto genera un histograma para los valores de píxel entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="1db31-122">*i* is evaluated from 0 to the number of bins. The effect generates a histogram for pixel values between 0 and 1.</span></span> <span data-ttu-id="1db31-123">Los valores que se encuentran fuera de este intervalo se fijan al intervalo.</span><span class="sxs-lookup"><span data-stu-id="1db31-123">Values outside of this range are clamped to the range.</span></span> <span data-ttu-id="1db31-124">El intervalo de un depósito determinado depende del número de depósitos.</span><span class="sxs-lookup"><span data-stu-id="1db31-124">The range of a particular bucket depends on the number of buckets.</span></span> <span data-ttu-id="1db31-125">Este efecto funciona en píxeles de mapa de bits directos.</span><span class="sxs-lookup"><span data-stu-id="1db31-125">This effect works on straight bitmap pixels.</span></span> <span data-ttu-id="1db31-126">Los canales de color del mapa de bits de entrada se dividen por el canal alfa para calcular este efecto.</span><span class="sxs-lookup"><span data-stu-id="1db31-126">The color channels of the input bitmap are divided by the alpha channel to compute this effect.</span></span>



| <span data-ttu-id="1db31-127">Enumeración de índice y nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="1db31-127">Display name and index enumeration</span></span>                                             | <span data-ttu-id="1db31-128">Tipo y valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="1db31-128">Type and default value</span></span>                                                   | <span data-ttu-id="1db31-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="1db31-129">Description</span></span>                                                                                                                                                                                   |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1db31-130">NumBins</span><span class="sxs-lookup"><span data-stu-id="1db31-130">NumBins</span></span><br/> <span data-ttu-id="1db31-131">D2D1 \_ de \_ prop número de propiedades de histograma \_ \_</span><span class="sxs-lookup"><span data-stu-id="1db31-131">D2D1\_HISTOGRAM\_PROP\_NUM\_BINS</span></span><br/>                 | <span data-ttu-id="1db31-132">UINT32</span><span class="sxs-lookup"><span data-stu-id="1db31-132">UINT32</span></span><br/> <span data-ttu-id="1db31-133">256</span><span class="sxs-lookup"><span data-stu-id="1db31-133">256</span></span><br/>                                         | <span data-ttu-id="1db31-134">Especifica el número de ubicaciones utilizadas para el histograma.</span><span class="sxs-lookup"><span data-stu-id="1db31-134">Specifies the number of bins used for the histogram.</span></span> <span data-ttu-id="1db31-135">El intervalo de valores de intensidad que se encuentran en un depósito determinado depende del número de depósitos especificados.</span><span class="sxs-lookup"><span data-stu-id="1db31-135">The range of intensity values that fall into a particular bucket depend on the number of specified buckets.</span></span>                              |
| <span data-ttu-id="1db31-136">ChannelSelect</span><span class="sxs-lookup"><span data-stu-id="1db31-136">ChannelSelect</span></span><br/> <span data-ttu-id="1db31-137">\_Selección de \_ canal de prop de histograma D2D1 \_ \_</span><span class="sxs-lookup"><span data-stu-id="1db31-137">D2D1\_HISTOGRAM\_PROP\_CHANNEL\_SELECT</span></span><br/>     | <span data-ttu-id="1db31-138">\_Selector de canal de D2D1 \_</span><span class="sxs-lookup"><span data-stu-id="1db31-138">D2D1\_CHANNEL\_SELECTOR</span></span><br/> <span data-ttu-id="1db31-139">Selector de canal de D2D1 \_ \_ \_ R</span><span class="sxs-lookup"><span data-stu-id="1db31-139">D2D1\_CHANNEL\_SELECTOR\_R</span></span><br/> | <span data-ttu-id="1db31-140">Especifica el canal usado para generar el histograma.</span><span class="sxs-lookup"><span data-stu-id="1db31-140">Specifies the channel used to generate the histogram.</span></span> <span data-ttu-id="1db31-141">Este efecto tiene una única salida de datos correspondiente al canal especificado.</span><span class="sxs-lookup"><span data-stu-id="1db31-141">This effect has a single data output corresponding to the specified channel.</span></span> <span data-ttu-id="1db31-142">Consulte [selectores de canal](#channel-selectors) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="1db31-142">See [Channel selectors](#channel-selectors) for more info.</span></span> |
| <span data-ttu-id="1db31-143">HistogramOutput</span><span class="sxs-lookup"><span data-stu-id="1db31-143">HistogramOutput</span></span><br/> <span data-ttu-id="1db31-144">\_Salida del \_ histograma de prop de histograma D2D1 \_ \_</span><span class="sxs-lookup"><span data-stu-id="1db31-144">D2D1\_HISTOGRAM\_PROP\_HISTOGRAM\_OUTPUT</span></span><br/> | <span data-ttu-id="1db31-145">FLOT\[\]</span><span class="sxs-lookup"><span data-stu-id="1db31-145">FLOAT\[\]</span></span><br/> <span data-ttu-id="1db31-146">Solo propiedad de salida.</span><span class="sxs-lookup"><span data-stu-id="1db31-146">Output property only.</span></span><br/>                    | <span data-ttu-id="1db31-147">Matriz de salida.</span><span class="sxs-lookup"><span data-stu-id="1db31-147">The output array.</span></span>                                                                                                                                                                             |



 

## <a name="channel-selectors"></a><span data-ttu-id="1db31-148">Selectores de canal</span><span class="sxs-lookup"><span data-stu-id="1db31-148">Channel selectors</span></span>



| <span data-ttu-id="1db31-149">Enumeración</span><span class="sxs-lookup"><span data-stu-id="1db31-149">Enumeration</span></span>                | <span data-ttu-id="1db31-150">Descripción</span><span class="sxs-lookup"><span data-stu-id="1db31-150">Description</span></span>                                                           |
|----------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="1db31-151">Selector de canal de D2D1 \_ \_ \_ R</span><span class="sxs-lookup"><span data-stu-id="1db31-151">D2D1\_CHANNEL\_SELECTOR\_R</span></span> | <span data-ttu-id="1db31-152">El efecto genera la salida del histograma en función del canal rojo.</span><span class="sxs-lookup"><span data-stu-id="1db31-152">The effect generates the histogram output based on the red channel.</span></span>   |
| <span data-ttu-id="1db31-153">Selector de canal de D2D1 \_ \_ \_ G</span><span class="sxs-lookup"><span data-stu-id="1db31-153">D2D1\_CHANNEL\_SELECTOR\_G</span></span> | <span data-ttu-id="1db31-154">El efecto genera la salida del histograma en función del canal verde.</span><span class="sxs-lookup"><span data-stu-id="1db31-154">The effect generates the histogram output based on the green channel.</span></span> |
| <span data-ttu-id="1db31-155">Selector de canal de D2D1 \_ \_ \_ B</span><span class="sxs-lookup"><span data-stu-id="1db31-155">D2D1\_CHANNEL\_SELECTOR\_B</span></span> | <span data-ttu-id="1db31-156">El efecto genera la salida del histograma en función del canal azul.</span><span class="sxs-lookup"><span data-stu-id="1db31-156">The effect generates the histogram output based on the blue channel.</span></span>  |
| <span data-ttu-id="1db31-157">\_ \_ Selector de canal \_ de D2D1 A</span><span class="sxs-lookup"><span data-stu-id="1db31-157">D2D1\_CHANNEL\_SELECTOR\_A</span></span> | <span data-ttu-id="1db31-158">El efecto genera la salida del histograma en función del canal alfa.</span><span class="sxs-lookup"><span data-stu-id="1db31-158">The effect generates the histogram output based on the alpha channel.</span></span> |



 

## <a name="data-output"></a><span data-ttu-id="1db31-159">Salida de datos</span><span class="sxs-lookup"><span data-stu-id="1db31-159">Data output</span></span>

<span data-ttu-id="1db31-160">Este efecto da como resultado un \[ \] valor Float, con el número de elementos correspondientes al número de ubicaciones especificadas. Cada elemento de FLOAT \[ \] es float.</span><span class="sxs-lookup"><span data-stu-id="1db31-160">This effect outputs a FLOAT\[\], with the number of elements corresponding to the number of specified bins. Each element in the FLOAT\[\] is a float.</span></span> <span data-ttu-id="1db31-161">El valor del elemento corresponde al número de elementos de esa ubicación.</span><span class="sxs-lookup"><span data-stu-id="1db31-161">The value of the element corresponds to the number of elements in that bin.</span></span>

## <a name="remarks"></a><span data-ttu-id="1db31-162">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1db31-162">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1db31-163">El método [**CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) genera un error si el dispositivo no admite DirectCompute y devuelve HRESULT = D2DERR \_ insuficientes \_ funcionalidades del dispositivo \_ .</span><span class="sxs-lookup"><span data-stu-id="1db31-163">The [**CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) method fails if the device doesn't support DirectCompute and returns HRESULT = D2DERR\_INSUFFICIENT\_DEVICE\_CAPABILITIES.</span></span> <span data-ttu-id="1db31-164">Todas las tarjetas DirectX11 y DirectX10 que admiten DirectCompute pueden usar el efecto.</span><span class="sxs-lookup"><span data-stu-id="1db31-164">All DirectX11 cards and DirectX10 cards that support DirectCompute can use the effect.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1db31-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1db31-165">Requirements</span></span>



| <span data-ttu-id="1db31-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="1db31-166">Requirement</span></span> | <span data-ttu-id="1db31-167">Value</span><span class="sxs-lookup"><span data-stu-id="1db31-167">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1db31-168">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1db31-168">Minimum supported client</span></span> | <span data-ttu-id="1db31-169">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="1db31-169">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="1db31-170">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1db31-170">Minimum supported server</span></span> | <span data-ttu-id="1db31-171">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="1db31-171">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="1db31-172">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1db31-172">Header</span></span>                   | <span data-ttu-id="1db31-173">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="1db31-173">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="1db31-174">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1db31-174">Library</span></span>                  | <span data-ttu-id="1db31-175">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="1db31-175">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="1db31-176">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1db31-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1db31-177">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="1db31-177">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

