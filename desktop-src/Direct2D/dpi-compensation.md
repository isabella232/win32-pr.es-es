---
title: Efecto de compensación de PPP
description: Use el efecto de compensación de PPP para ajustar automáticamente un mapa de bits de entrada para que coincida con el PPP del contexto. Esto resulta útil en situaciones en las que un mapa de bits se crea o se carga en un PPP diferente al de la pantalla.
ms.assetid: EA8AD89B-A710-468F-A6F3-474DA29586F1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69a0477d2a57f39738fa9b1ce16c97995c60cf96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905669"
---
# <a name="dpi-compensation-effect"></a><span data-ttu-id="21963-104">Efecto de compensación de PPP</span><span class="sxs-lookup"><span data-stu-id="21963-104">DPI compensation effect</span></span>

<span data-ttu-id="21963-105">Use el efecto de compensación de PPP para ajustar automáticamente un mapa de bits de entrada para que coincida con el PPP del contexto.</span><span class="sxs-lookup"><span data-stu-id="21963-105">Use the DPI compensation effect to automatically adjust an input bitmap to match the DPI of the context.</span></span> <span data-ttu-id="21963-106">Esto resulta útil en situaciones en las que un mapa de bits se crea o se carga en un PPP diferente al de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="21963-106">This is useful for situations where a bitmap is created or loaded at a different DPI than the screen.</span></span>

<span data-ttu-id="21963-107">El CLSID para este efecto es CLSID \_ D2D1DpiCompensation.</span><span class="sxs-lookup"><span data-stu-id="21963-107">The CLSID for this effect is CLSID\_D2D1DpiCompensation.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="21963-108">Propiedades del efecto</span><span class="sxs-lookup"><span data-stu-id="21963-108">Effect properties</span></span>



| <span data-ttu-id="21963-109">Enumeración de índice y nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="21963-109">Display name and index enumeration</span></span>                                                       | <span data-ttu-id="21963-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="21963-110">Description</span></span>                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21963-111">InterpolationMode</span><span class="sxs-lookup"><span data-stu-id="21963-111">InterpolationMode</span></span><br/> <span data-ttu-id="21963-112">\_Modo de \_ \_ interpolación de \_ propiedades de D2D1 DPICOMPENSATION</span><span class="sxs-lookup"><span data-stu-id="21963-112">D2D1\_DPICOMPENSATION\_PROP\_INTERPOLATION\_MODE</span></span><br/> | <span data-ttu-id="21963-113">El modo de interpolación que el efecto usa para escalar la imagen.</span><span class="sxs-lookup"><span data-stu-id="21963-113">The interpolation mode the effect uses to scale the image.</span></span><br/> <span data-ttu-id="21963-114">El tipo es D2D1 \_ DPICOMPENSATION \_ modo de interpolación \_ .</span><span class="sxs-lookup"><span data-stu-id="21963-114">The type is D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE.</span></span><br/> <span data-ttu-id="21963-115">El valor predeterminado es D2D1 \_ DPICOMPENSATION \_ modo de interpolación \_ \_ lineal.</span><span class="sxs-lookup"><span data-stu-id="21963-115">The default value is D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_LINEAR .</span></span><br/>                  |
| <span data-ttu-id="21963-116">BorderMode</span><span class="sxs-lookup"><span data-stu-id="21963-116">BorderMode</span></span><br/> <span data-ttu-id="21963-117">D2D1 \_ DPICOMPENSATION \_ \_ modo de borde \_ de la Prop</span><span class="sxs-lookup"><span data-stu-id="21963-117">D2D1\_DPICOMPENSATION\_PROP\_BORDER\_MODE</span></span><br/>               | <span data-ttu-id="21963-118">El modo que se usa para calcular el borde de la imagen, es decir, es flexible o difícil.</span><span class="sxs-lookup"><span data-stu-id="21963-118">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="21963-119">Vea [modos de borde](https://www.bing.com/search?q=Border+modes) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="21963-119">See [Border modes](https://www.bing.com/search?q=Border+modes) for more info.</span></span> <br/> <span data-ttu-id="21963-120">El tipo es D2D1 \_ Border \_ mode.</span><span class="sxs-lookup"><span data-stu-id="21963-120">The type is D2D1\_BORDER\_MODE.</span></span><br/> <span data-ttu-id="21963-121">El valor predeterminado es D2D1 \_ Border \_ Mode \_ .</span><span class="sxs-lookup"><span data-stu-id="21963-121">The default value is D2D1\_BORDER\_MODE\_SOFT.</span></span><br/> |
| <span data-ttu-id="21963-122">InputDpi</span><span class="sxs-lookup"><span data-stu-id="21963-122">InputDpi</span></span><br/> <span data-ttu-id="21963-123">\_PPP de \_ \_ entrada \_ de D2D1 DPICOMPENSATION</span><span class="sxs-lookup"><span data-stu-id="21963-123">D2D1\_DPICOMPENSATION\_PROP\_INPUT\_DPI</span></span><br/>                   | <span data-ttu-id="21963-124">PPP de la imagen de entrada.</span><span class="sxs-lookup"><span data-stu-id="21963-124">The DPI of the input image.</span></span><br/> <span data-ttu-id="21963-125">El tipo es FLOAT.</span><span class="sxs-lookup"><span data-stu-id="21963-125">The type is FLOAT.</span></span><br/> <span data-ttu-id="21963-126">El valor predeterminado es 96.0 f.</span><span class="sxs-lookup"><span data-stu-id="21963-126">The default value is 96.0f.</span></span><br/>                                                                                                                                    |



 

## <a name="interpolation-modes"></a><span data-ttu-id="21963-127">Modos de interpolación</span><span class="sxs-lookup"><span data-stu-id="21963-127">Interpolation modes</span></span>



| <span data-ttu-id="21963-128">Enumeración</span><span class="sxs-lookup"><span data-stu-id="21963-128">Enumeration</span></span>                                                       | <span data-ttu-id="21963-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="21963-129">Description</span></span>                                                                                                                                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21963-130">D2D1 \_ el \_ modo de interpolación DPICOMPENSATION \_ \_ más cercano \_</span><span class="sxs-lookup"><span data-stu-id="21963-130">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_NEAREST\_NEIGHBOR</span></span>     | <span data-ttu-id="21963-131">Muestrea el punto único más cercano y lo usa.</span><span class="sxs-lookup"><span data-stu-id="21963-131">Samples the nearest single point and uses that.</span></span> <span data-ttu-id="21963-132">Este modo utiliza menos tiempo de procesamiento, pero genera la imagen de menor calidad.</span><span class="sxs-lookup"><span data-stu-id="21963-132">This mode uses less processing time, but outputs the lowest quality image.</span></span>                                                                           |
| <span data-ttu-id="21963-133">D2D1 \_ \_ modo de interpolación DPICOMPENSATION \_ \_ lineal</span><span class="sxs-lookup"><span data-stu-id="21963-133">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_LINEAR</span></span>                | <span data-ttu-id="21963-134">Utiliza un ejemplo de cuatro puntos y una interpolación lineal.</span><span class="sxs-lookup"><span data-stu-id="21963-134">Uses a four point sample and linear interpolation.</span></span> <span data-ttu-id="21963-135">Este modo usa más tiempo de procesamiento que el modo vecino más cercano, pero genera una imagen de mayor calidad.</span><span class="sxs-lookup"><span data-stu-id="21963-135">This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.</span></span>                                           |
| <span data-ttu-id="21963-136">D2D1 \_ \_ modo de interpolación DPICOMPENSATION \_ \_ cúbico</span><span class="sxs-lookup"><span data-stu-id="21963-136">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_CUBIC</span></span>                 | <span data-ttu-id="21963-137">Usa un kernel cúbico de ejemplo 16 para la interpolación.</span><span class="sxs-lookup"><span data-stu-id="21963-137">Uses a 16 sample cubic kernel for interpolation.</span></span> <span data-ttu-id="21963-138">Este modo utiliza la mayor parte del tiempo de procesamiento, pero genera una imagen de mayor calidad.</span><span class="sxs-lookup"><span data-stu-id="21963-138">This mode uses the most processing time, but outputs a higher quality image.</span></span>                                                                        |
| <span data-ttu-id="21963-139">D2D1 \_ DPICOMPENSATION \_ modo de interpolación \_ \_ lineal de varios \_ ejemplos \_</span><span class="sxs-lookup"><span data-stu-id="21963-139">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_MULTI\_SAMPLE\_LINEAR</span></span> | <span data-ttu-id="21963-140">Usa 4 muestras lineales dentro de un solo píxel para el suavizado de contorno adecuado.</span><span class="sxs-lookup"><span data-stu-id="21963-140">Uses 4 linear samples within a single pixel for good edge anti-aliasing.</span></span> <span data-ttu-id="21963-141">Este modo es adecuado para reducir verticalmente en pequeñas cantidades de imágenes con pocos píxeles.</span><span class="sxs-lookup"><span data-stu-id="21963-141">This mode is good for scaling down by small amounts on images with few pixels.</span></span>                                              |
| <span data-ttu-id="21963-142">D2D1 \_ \_ modo de interpolación DPICOMPENSATION \_ \_ anisotrópico</span><span class="sxs-lookup"><span data-stu-id="21963-142">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_ANISOTROPIC</span></span>           | <span data-ttu-id="21963-143">Utiliza el filtrado anisotrópico para muestrear un patrón según la forma transformada del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="21963-143">Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.</span></span>                                                                                                     |
| <span data-ttu-id="21963-144">D2D1 \_ DPICOMPENSATION \_ modo de interpolación de \_ \_ alta \_ calidad \_ cúbico</span><span class="sxs-lookup"><span data-stu-id="21963-144">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_HIGH\_QUALITY\_CUBIC</span></span>  | <span data-ttu-id="21963-145">Usa un kernel cúbico de alta calidad de tamaño variable para realizar una downscale previa de la imagen si downscaling está implicado en la matriz de transformación.</span><span class="sxs-lookup"><span data-stu-id="21963-145">Uses a variable size high quality cubic kernel to perform a pre-downscale the image if downscaling is involved in the transform matrix.</span></span> <span data-ttu-id="21963-146">A continuación, usa el modo de interpolación cúbico para la salida final.</span><span class="sxs-lookup"><span data-stu-id="21963-146">Then uses the cubic interpolation mode for the final output.</span></span> |



 

> [!Note]  
> <span data-ttu-id="21963-147">Si no selecciona un modo, el efecto tiene como valor predeterminado el \_ \_ modo de interpolación D2D1 DPICOMPENSTION \_ \_ lineal.</span><span class="sxs-lookup"><span data-stu-id="21963-147">If you don't select a mode, the effect defaults to D2D1\_DPICOMPENSTION\_INTERPOLATION\_MODE\_LINEAR.</span></span>

 

## <a name="border-modes"></a><span data-ttu-id="21963-148">Modos de borde</span><span class="sxs-lookup"><span data-stu-id="21963-148">Border modes</span></span>



| <span data-ttu-id="21963-149">Nombre</span><span class="sxs-lookup"><span data-stu-id="21963-149">Name</span></span>                     | <span data-ttu-id="21963-150">Descripción</span><span class="sxs-lookup"><span data-stu-id="21963-150">Description</span></span>                                                                                                 |
|--------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21963-151">D2D1 \_ modo de borde \_ \_ flexible</span><span class="sxs-lookup"><span data-stu-id="21963-151">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="21963-152">Los píxeles que están fuera de los límites de entrada se generan mediante el [efecto de borde del reflejo](border.md).</span><span class="sxs-lookup"><span data-stu-id="21963-152">Pixels outside of the input boundaries are generated by the [mirror border effect](border.md).</span></span> <br/> |
| <span data-ttu-id="21963-153">D2D1 \_ del \_ modo de borde \_</span><span class="sxs-lookup"><span data-stu-id="21963-153">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="21963-154">Los píxeles que están fuera de los límites de entrada son negros transparentes.</span><span class="sxs-lookup"><span data-stu-id="21963-154">Pixels outside of the input boundaries are transparent black.</span></span><br/>                                    |



 

## <a name="requirements"></a><span data-ttu-id="21963-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21963-155">Requirements</span></span>



| <span data-ttu-id="21963-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="21963-156">Requirement</span></span> | <span data-ttu-id="21963-157">Value</span><span class="sxs-lookup"><span data-stu-id="21963-157">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="21963-158">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="21963-158">Minimum supported client</span></span> | <span data-ttu-id="21963-159">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="21963-159">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="21963-160">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="21963-160">Minimum supported server</span></span> | <span data-ttu-id="21963-161">Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\]</span><span class="sxs-lookup"><span data-stu-id="21963-161">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="21963-162">Encabezado</span><span class="sxs-lookup"><span data-stu-id="21963-162">Header</span></span>                   | <span data-ttu-id="21963-163">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="21963-163">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="21963-164">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="21963-164">Library</span></span>                  | <span data-ttu-id="21963-165">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="21963-165">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="21963-166">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="21963-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21963-167">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="21963-167">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

