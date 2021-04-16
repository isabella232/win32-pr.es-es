---
description: .
ms.assetid: 7f339ee8-01e6-4bbb-8563-020ff0e02499
title: Configuración de los Estados de la HD de DXVA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e539796aa5d3997b35739e75c80b438a7b5da50b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715490"
---
# <a name="setting-dxva-hd-states"></a><span data-ttu-id="b3544-103">Configuración de los Estados de la HD de DXVA</span><span class="sxs-lookup"><span data-stu-id="b3544-103">Setting DXVA-HD States</span></span>

<span data-ttu-id="b3544-104">Durante el procesamiento de vídeo, el dispositivo Microsoft DirectX video Acceleration High Definition (DXVA-HD) mantiene un estado persistente de un fotograma a otro.</span><span class="sxs-lookup"><span data-stu-id="b3544-104">During video processing, the Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device maintains a persistent state from one frame to the next.</span></span> <span data-ttu-id="b3544-105">Cada Estado tiene un valor predeterminado documentado.</span><span class="sxs-lookup"><span data-stu-id="b3544-105">Each state has a documented default.</span></span> <span data-ttu-id="b3544-106">Después de configurar el dispositivo, establezca los Estados que desee cambiar con respecto a sus valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="b3544-106">After you configure the device, set any states that you wish to change from their defaults.</span></span> <span data-ttu-id="b3544-107">Antes de procesar cada fotograma, actualice los Estados que deben cambiar.</span><span class="sxs-lookup"><span data-stu-id="b3544-107">Before you process each frame, update any states that should change.</span></span>

> [!Note]  
> <span data-ttu-id="b3544-108">Este diseño es distinto de DXVA-VP.</span><span class="sxs-lookup"><span data-stu-id="b3544-108">This design differs from DXVA-VP.</span></span> <span data-ttu-id="b3544-109">En DXVA-VP, la aplicación debe especificar todos los parámetros VP con cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="b3544-109">In DXVA-VP, the application must specify all of the VP parameters with each frame.</span></span>

 

<span data-ttu-id="b3544-110">Los Estados de los dispositivos se dividen en dos categorías:</span><span class="sxs-lookup"><span data-stu-id="b3544-110">Device states fall into two categories:</span></span>

-   <span data-ttu-id="b3544-111">Los Estados de *secuencia* aplican cada flujo de entrada por separado.</span><span class="sxs-lookup"><span data-stu-id="b3544-111">*Stream* states apply each input stream separately.</span></span> <span data-ttu-id="b3544-112">Puede aplicar diferentes configuraciones a cada flujo.</span><span class="sxs-lookup"><span data-stu-id="b3544-112">You can apply different settings to each stream.</span></span>
-   <span data-ttu-id="b3544-113">Los Estados de *blit* se aplican globalmente a todo el procesamiento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b3544-113">*Blit* states apply globally to the entire video processing blit.</span></span>

<span data-ttu-id="b3544-114">Se definen los siguientes Estados de flujo.</span><span class="sxs-lookup"><span data-stu-id="b3544-114">The following stream states are defined.</span></span>



| <span data-ttu-id="b3544-115">Estado de la secuencia</span><span class="sxs-lookup"><span data-stu-id="b3544-115">Stream State</span></span>                                   | <span data-ttu-id="b3544-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3544-116">Description</span></span>                                                                                                     |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3544-117">**DXVAHD \_ Estado de flujo de \_ \_ D3DFORMAT**</span><span class="sxs-lookup"><span data-stu-id="b3544-117">**DXVAHD\_STREAM\_STATE\_D3DFORMAT**</span></span>           | <span data-ttu-id="b3544-118">Formato de vídeo de entrada.</span><span class="sxs-lookup"><span data-stu-id="b3544-118">Input video format.</span></span>                                                                                             |
| <span data-ttu-id="b3544-119">**\_formato de \_ marco de estado de secuencia de DXVAHD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b3544-119">**DXVAHD\_STREAM\_STATE\_FRAME\_FORMAT**</span></span>       | <span data-ttu-id="b3544-120">Entrelaza.</span><span class="sxs-lookup"><span data-stu-id="b3544-120">Interlacing.</span></span>                                                                                                    |
| <span data-ttu-id="b3544-121">**\_espacio de \_ colores de entrada de estado de secuencia de \_ \_ DXVAHD \_**</span><span class="sxs-lookup"><span data-stu-id="b3544-121">**DXVAHD\_STREAM\_STATE\_INPUT\_COLOR\_SPACE**</span></span> | <span data-ttu-id="b3544-122">Espacio de colores de entrada.</span><span class="sxs-lookup"><span data-stu-id="b3544-122">Input color space.</span></span> <span data-ttu-id="b3544-123">Este estado especifica el intervalo de color RGB y la matriz de transferencia YCbCr para el flujo de entrada.</span><span class="sxs-lookup"><span data-stu-id="b3544-123">This state specifies the RGB color range and the YCbCr transfer matrix for the input stream.</span></span> |
| <span data-ttu-id="b3544-124">**\_velocidad de \_ salida de estado de flujo de DXVAHD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b3544-124">**DXVAHD\_STREAM\_STATE\_OUTPUT\_RATE**</span></span>        | <span data-ttu-id="b3544-125">Velocidad de fotogramas de salida.</span><span class="sxs-lookup"><span data-stu-id="b3544-125">Output frame rate.</span></span> <span data-ttu-id="b3544-126">Este estado controla la conversión de velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="b3544-126">This state controls frame-rate conversion.</span></span>                                                   |
| <span data-ttu-id="b3544-127">**\_rectángulo de \_ origen de estado de flujo de DXVAHD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b3544-127">**DXVAHD\_STREAM\_STATE\_SOURCE\_RECT**</span></span>        | <span data-ttu-id="b3544-128">Rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="b3544-128">Source rectangle.</span></span>                                                                                               |
| <span data-ttu-id="b3544-129">**DXVAHD \_ \_ rectángulo de \_ destino de estado de secuencia \_**</span><span class="sxs-lookup"><span data-stu-id="b3544-129">**DXVAHD\_STREAM\_STATE\_DESTINATION\_RECT**</span></span>   | <span data-ttu-id="b3544-130">Rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="b3544-130">Destination rectangle.</span></span>                                                                                          |
| <span data-ttu-id="b3544-131">**DXVAHD \_ Estado de flujo \_ \_ alfa**</span><span class="sxs-lookup"><span data-stu-id="b3544-131">**DXVAHD\_STREAM\_STATE\_ALPHA**</span></span>               | <span data-ttu-id="b3544-132">Alfa plana.</span><span class="sxs-lookup"><span data-stu-id="b3544-132">Planar alpha.</span></span>                                                                                                   |
| <span data-ttu-id="b3544-133">**DXVAHD \_ \_ paleta de estado de flujo \_**</span><span class="sxs-lookup"><span data-stu-id="b3544-133">**DXVAHD\_STREAM\_STATE\_PALETTE**</span></span>             | <span data-ttu-id="b3544-134">Paleta de colores.</span><span class="sxs-lookup"><span data-stu-id="b3544-134">Color palette.</span></span> <span data-ttu-id="b3544-135">Este estado se aplica solo a los formatos de entrada de paleta.</span><span class="sxs-lookup"><span data-stu-id="b3544-135">This state applies only to palettized input formats.</span></span>                                             |
| <span data-ttu-id="b3544-136">**\_clave de \_ luminancia de estado de flujo de DXVAHD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b3544-136">**DXVAHD\_STREAM\_STATE\_LUMA\_KEY**</span></span>           | <span data-ttu-id="b3544-137">Clave de luminancia.</span><span class="sxs-lookup"><span data-stu-id="b3544-137">Luma key.</span></span>                                                                                                       |
| <span data-ttu-id="b3544-138">**\_relación de \_ aspecto de estado de flujo de DXVAHD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b3544-138">**DXVAHD\_STREAM\_STATE\_ASPECT\_RATIO**</span></span>       | <span data-ttu-id="b3544-139">Relación de aspecto de píxeles.</span><span class="sxs-lookup"><span data-stu-id="b3544-139">Pixel aspect ratio.</span></span>                                                                                             |
| <span data-ttu-id="b3544-140">**Filtro de estado de secuencia de DXVAHD \_ \_ \_ \_ xxxx**</span><span class="sxs-lookup"><span data-stu-id="b3544-140">**DXVAHD\_STREAM\_STATE\_FILTER\_Xxxx**</span></span>        | <span data-ttu-id="b3544-141">Configuración del filtro de imágenes.</span><span class="sxs-lookup"><span data-stu-id="b3544-141">Image filter settings.</span></span> <span data-ttu-id="b3544-142">El controlador puede admitir brillo, contraste y otros filtros de imagen.</span><span class="sxs-lookup"><span data-stu-id="b3544-142">The driver can support brightness, contrast, and other image filters.</span></span>                    |



 

<span data-ttu-id="b3544-143">Se definen los siguientes Estados de blit:</span><span class="sxs-lookup"><span data-stu-id="b3544-143">The following blit states are defined:</span></span>



| <span data-ttu-id="b3544-144">Estado de blit</span><span class="sxs-lookup"><span data-stu-id="b3544-144">Blit State</span></span>                                   | <span data-ttu-id="b3544-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3544-145">Description</span></span>                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="b3544-146">**\_rectángulo de \_ destino de estado \_ \_ de DXVAHD BLT**</span><span class="sxs-lookup"><span data-stu-id="b3544-146">**DXVAHD\_BLT\_STATE\_TARGET\_RECT**</span></span>         | <span data-ttu-id="b3544-147">Rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="b3544-147">Target rectangle.</span></span>                                                            |
| <span data-ttu-id="b3544-148">**\_color de \_ fondo de estado \_ \_ de DXVAHD BLT**</span><span class="sxs-lookup"><span data-stu-id="b3544-148">**DXVAHD\_BLT\_STATE\_BACKGROUND\_COLOR**</span></span>    | <span data-ttu-id="b3544-149">Color de fondo.</span><span class="sxs-lookup"><span data-stu-id="b3544-149">Background color.</span></span>                                                            |
| <span data-ttu-id="b3544-150">**\_espacio de \_ colores de salida de estado \_ \_ de DXVAHD BLT \_**</span><span class="sxs-lookup"><span data-stu-id="b3544-150">**DXVAHD\_BLT\_STATE\_OUTPUT\_COLOR\_SPACE**</span></span> | <span data-ttu-id="b3544-151">Espacio de colores de salida.</span><span class="sxs-lookup"><span data-stu-id="b3544-151">Output color space.</span></span>                                                          |
| <span data-ttu-id="b3544-152">**DXVAHD \_ BLT \_ State \_ alfa \_ Fill**</span><span class="sxs-lookup"><span data-stu-id="b3544-152">**DXVAHD\_BLT\_STATE\_ALPHA\_FILL**</span></span>          | <span data-ttu-id="b3544-153">Modo de relleno alfa.</span><span class="sxs-lookup"><span data-stu-id="b3544-153">Alpha fill mode.</span></span>                                                             |
| <span data-ttu-id="b3544-154">**DXVAHD \_ BLT \_ State \_ CONSTRICTION**</span><span class="sxs-lookup"><span data-stu-id="b3544-154">**DXVAHD\_BLT\_STATE\_CONSTRICTION**</span></span>         | <span data-ttu-id="b3544-155">Constriction.</span><span class="sxs-lookup"><span data-stu-id="b3544-155">Constriction.</span></span> <span data-ttu-id="b3544-156">Este estado controla si el dispositivo downsamples la salida.</span><span class="sxs-lookup"><span data-stu-id="b3544-156">This state controls whether the device downsamples the output.</span></span> |



 

<span data-ttu-id="b3544-157">Para establecer un estado de flujo, llame al método [**IDXVAHD de \_ videoprocesador:: SetVideoProcessStreamState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate) .</span><span class="sxs-lookup"><span data-stu-id="b3544-157">To set a stream state, call the [**IDXVAHD\_VideoProcessor::SetVideoProcessStreamState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate) method.</span></span> <span data-ttu-id="b3544-158">Para establecer un estado de Blit, llame al método [**IDXVAHD de \_ videoprocesador:: SetVideoProcessBltState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate) .</span><span class="sxs-lookup"><span data-stu-id="b3544-158">To set a blit state, call the [**IDXVAHD\_VideoProcessor::SetVideoProcessBltState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate) method.</span></span> <span data-ttu-id="b3544-159">En ambos métodos, un valor de enumeración especifica el estado que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="b3544-159">In both of these methods, an enumeration value specifies the state to set.</span></span> <span data-ttu-id="b3544-160">Los datos de estado se proporcionan mediante una estructura de datos específica del estado, que la aplicación convierte en un tipo **void \*** .</span><span class="sxs-lookup"><span data-stu-id="b3544-160">The state data is given using a state-specific data structure, which the application casts to a **void\*** type.</span></span>

<span data-ttu-id="b3544-161">En el ejemplo de código siguiente se establece el formato de entrada y el rectángulo de destino para la secuencia 0, y se establece el color de fondo en negro.</span><span class="sxs-lookup"><span data-stu-id="b3544-161">The following code example sets the input format and destination rectangle for stream 0, and sets the background color to black.</span></span>


```C++
HRESULT SetDXVAHDStates(HWND hwnd, D3DFORMAT inputFormat)
{
    // Set the initial stream states.

    // Set the format of the input stream

    DXVAHD_STREAM_STATE_D3DFORMAT_DATA d3dformat = { inputFormat };

    HRESULT hr = g_pDXVAVP->SetVideoProcessStreamState(
        0,  // Stream index
        DXVAHD_STREAM_STATE_D3DFORMAT,
        sizeof(d3dformat),
        &d3dformat
        );

    if (SUCCEEDED(hr))
    { 
        // For this example, the input stream contains progressive frames.

        DXVAHD_STREAM_STATE_FRAME_FORMAT_DATA frame_format = { DXVAHD_FRAME_FORMAT_PROGRESSIVE };
        
        hr = g_pDXVAVP->SetVideoProcessStreamState(
            0, // Stream index
            DXVAHD_STREAM_STATE_FRAME_FORMAT,
            sizeof(frame_format),
            &frame_format
            );
    }

    if (SUCCEEDED(hr))
    { 
        // Compute the letterbox area.

        RECT rcDest;
        GetClientRect(hwnd, &rcDest);

        RECT rcSrc;
        SetRect(&rcSrc, 0, 0, VIDEO_WIDTH, VIDEO_HEIGHT);

        rcDest = LetterBoxRect(rcSrc, rcDest);

        // Set the destination rectangle, so the frame is displayed within the 
        // letterbox area. Otherwise, the frame is stretched to cover the 
        // entire surface.

        DXVAHD_STREAM_STATE_DESTINATION_RECT_DATA DstRect = { TRUE, rcDest };

        hr = g_pDXVAVP->SetVideoProcessStreamState(
            0, // Stream index 
            DXVAHD_STREAM_STATE_DESTINATION_RECT,
            sizeof(DstRect),
            &DstRect
            );
    }

    if (SUCCEEDED(hr))
    { 
        DXVAHD_COLOR_RGBA rgbBackground = { 0.0f, 0.0f, 0.0f, 1.0f };  // RGBA

        DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA background = { FALSE, rgbBackground };

        hr = g_pDXVAVP->SetVideoProcessBltState(
            DXVAHD_BLT_STATE_BACKGROUND_COLOR,
            sizeof (background),
            &background
            );
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="b3544-162">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b3544-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3544-163">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="b3544-163">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



