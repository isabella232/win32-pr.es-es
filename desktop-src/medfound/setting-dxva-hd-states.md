---
description: Configuración de estados DXVA-HD
ms.assetid: 7f339ee8-01e6-4bbb-8563-020ff0e02499
title: Configuración de estados DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91766e3eb10399d908ab361e13db4b94fe07b653
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092703"
---
# <a name="setting-dxva-hd-states"></a><span data-ttu-id="eb428-103">Configuración de estados DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="eb428-103">Setting DXVA-HD States</span></span>

<span data-ttu-id="eb428-104">Durante el procesamiento de vídeo, el dispositivo de alta definición de aceleración de vídeo (DXVA-HD) de Microsoft DirectX mantiene un estado persistente de un fotograma al siguiente.</span><span class="sxs-lookup"><span data-stu-id="eb428-104">During video processing, the Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device maintains a persistent state from one frame to the next.</span></span> <span data-ttu-id="eb428-105">Cada estado tiene un valor predeterminado documentado.</span><span class="sxs-lookup"><span data-stu-id="eb428-105">Each state has a documented default.</span></span> <span data-ttu-id="eb428-106">Después de configurar el dispositivo, establezca los estados que quiera cambiar de sus valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="eb428-106">After you configure the device, set any states that you wish to change from their defaults.</span></span> <span data-ttu-id="eb428-107">Antes de procesar cada fotograma, actualice los estados que deben cambiar.</span><span class="sxs-lookup"><span data-stu-id="eb428-107">Before you process each frame, update any states that should change.</span></span>

> [!Note]  
> <span data-ttu-id="eb428-108">Este diseño difiere de DXVA-VP.</span><span class="sxs-lookup"><span data-stu-id="eb428-108">This design differs from DXVA-VP.</span></span> <span data-ttu-id="eb428-109">En DXVA-VP, la aplicación debe especificar todos los parámetros de VP con cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="eb428-109">In DXVA-VP, the application must specify all of the VP parameters with each frame.</span></span>

 

<span data-ttu-id="eb428-110">Los estados del dispositivo se divide en dos categorías:</span><span class="sxs-lookup"><span data-stu-id="eb428-110">Device states fall into two categories:</span></span>

-   <span data-ttu-id="eb428-111">*Los estados* de flujo aplican cada flujo de entrada por separado.</span><span class="sxs-lookup"><span data-stu-id="eb428-111">*Stream* states apply each input stream separately.</span></span> <span data-ttu-id="eb428-112">Puede aplicar diferentes configuraciones a cada secuencia.</span><span class="sxs-lookup"><span data-stu-id="eb428-112">You can apply different settings to each stream.</span></span>
-   <span data-ttu-id="eb428-113">*Los estados de Blit* se aplican globalmente a todo el blit de procesamiento de vídeo.</span><span class="sxs-lookup"><span data-stu-id="eb428-113">*Blit* states apply globally to the entire video processing blit.</span></span>

<span data-ttu-id="eb428-114">Se definen los siguientes estados de secuencia.</span><span class="sxs-lookup"><span data-stu-id="eb428-114">The following stream states are defined.</span></span>



| <span data-ttu-id="eb428-115">Estado de la secuencia</span><span class="sxs-lookup"><span data-stu-id="eb428-115">Stream State</span></span>                                   | <span data-ttu-id="eb428-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb428-116">Description</span></span>                                                                                                     |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb428-117">**DXVAHD \_ STREAM \_ STATE \_ D3DFORMAT**</span><span class="sxs-lookup"><span data-stu-id="eb428-117">**DXVAHD\_STREAM\_STATE\_D3DFORMAT**</span></span>           | <span data-ttu-id="eb428-118">Formato de vídeo de entrada.</span><span class="sxs-lookup"><span data-stu-id="eb428-118">Input video format.</span></span>                                                                                             |
| <span data-ttu-id="eb428-119">**FORMATO DE MARCO \_ DE ESTADO \_ DE FLUJO \_ DXVAHD \_**</span><span class="sxs-lookup"><span data-stu-id="eb428-119">**DXVAHD\_STREAM\_STATE\_FRAME\_FORMAT**</span></span>       | <span data-ttu-id="eb428-120">Entrelazado.</span><span class="sxs-lookup"><span data-stu-id="eb428-120">Interlacing.</span></span>                                                                                                    |
| <span data-ttu-id="eb428-121">**ESPACIO DE COLOR \_ DE ENTRADA DE ESTADO DE \_ FLUJO \_ \_ DXVAHD \_**</span><span class="sxs-lookup"><span data-stu-id="eb428-121">**DXVAHD\_STREAM\_STATE\_INPUT\_COLOR\_SPACE**</span></span> | <span data-ttu-id="eb428-122">Espacio de color de entrada.</span><span class="sxs-lookup"><span data-stu-id="eb428-122">Input color space.</span></span> <span data-ttu-id="eb428-123">Este estado especifica el intervalo de colores RGB y la matriz de transferencia YCbCr para el flujo de entrada.</span><span class="sxs-lookup"><span data-stu-id="eb428-123">This state specifies the RGB color range and the YCbCr transfer matrix for the input stream.</span></span> |
| <span data-ttu-id="eb428-124">**VELOCIDAD DE SALIDA DEL ESTADO DE FLUJO DXVAHD \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="eb428-124">**DXVAHD\_STREAM\_STATE\_OUTPUT\_RATE**</span></span>        | <span data-ttu-id="eb428-125">Velocidad de fotogramas de salida.</span><span class="sxs-lookup"><span data-stu-id="eb428-125">Output frame rate.</span></span> <span data-ttu-id="eb428-126">Este estado controla la conversión de velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="eb428-126">This state controls frame-rate conversion.</span></span>                                                   |
| <span data-ttu-id="eb428-127">**DXVAHD \_ STREAM \_ STATE \_ SOURCE \_ RECT**</span><span class="sxs-lookup"><span data-stu-id="eb428-127">**DXVAHD\_STREAM\_STATE\_SOURCE\_RECT**</span></span>        | <span data-ttu-id="eb428-128">Rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="eb428-128">Source rectangle.</span></span>                                                                                               |
| <span data-ttu-id="eb428-129">**DXVAHD \_ STREAM \_ STATE \_ DESTINATION \_ RECT**</span><span class="sxs-lookup"><span data-stu-id="eb428-129">**DXVAHD\_STREAM\_STATE\_DESTINATION\_RECT**</span></span>   | <span data-ttu-id="eb428-130">Rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="eb428-130">Destination rectangle.</span></span>                                                                                          |
| <span data-ttu-id="eb428-131">**DXVAHD \_ STREAM \_ STATE \_ ALPHA**</span><span class="sxs-lookup"><span data-stu-id="eb428-131">**DXVAHD\_STREAM\_STATE\_ALPHA**</span></span>               | <span data-ttu-id="eb428-132">Alfa plana.</span><span class="sxs-lookup"><span data-stu-id="eb428-132">Planar alpha.</span></span>                                                                                                   |
| <span data-ttu-id="eb428-133">**PALETA DE ESTADO DE FLUJO DXVAHD \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="eb428-133">**DXVAHD\_STREAM\_STATE\_PALETTE**</span></span>             | <span data-ttu-id="eb428-134">Paleta de colores.</span><span class="sxs-lookup"><span data-stu-id="eb428-134">Color palette.</span></span> <span data-ttu-id="eb428-135">Este estado solo se aplica a los formatos de entrada con limitaciones.</span><span class="sxs-lookup"><span data-stu-id="eb428-135">This state applies only to palettized input formats.</span></span>                                             |
| <span data-ttu-id="eb428-136">**DXVAHD \_ STREAM \_ STATE \_ LUMA \_ KEY**</span><span class="sxs-lookup"><span data-stu-id="eb428-136">**DXVAHD\_STREAM\_STATE\_LUMA\_KEY**</span></span>           | <span data-ttu-id="eb428-137">Clave Luma.</span><span class="sxs-lookup"><span data-stu-id="eb428-137">Luma key.</span></span>                                                                                                       |
| <span data-ttu-id="eb428-138">**RELACIÓN DE ASPECTO DEL ESTADO DEL FLUJO DXVAHD \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="eb428-138">**DXVAHD\_STREAM\_STATE\_ASPECT\_RATIO**</span></span>       | <span data-ttu-id="eb428-139">Relación de aspecto de píxeles.</span><span class="sxs-lookup"><span data-stu-id="eb428-139">Pixel aspect ratio.</span></span>                                                                                             |
| <span data-ttu-id="eb428-140">**DXVAHD \_ STREAM \_ STATE \_ FILTER \_ Xxxx**</span><span class="sxs-lookup"><span data-stu-id="eb428-140">**DXVAHD\_STREAM\_STATE\_FILTER\_Xxxx**</span></span>        | <span data-ttu-id="eb428-141">Configuración del filtro de imagen.</span><span class="sxs-lookup"><span data-stu-id="eb428-141">Image filter settings.</span></span> <span data-ttu-id="eb428-142">El controlador puede admitir el brillo, el contraste y otros filtros de imagen.</span><span class="sxs-lookup"><span data-stu-id="eb428-142">The driver can support brightness, contrast, and other image filters.</span></span>                    |



 

<span data-ttu-id="eb428-143">Se definen los siguientes estados blit:</span><span class="sxs-lookup"><span data-stu-id="eb428-143">The following blit states are defined:</span></span>



| <span data-ttu-id="eb428-144">Estado de Blit</span><span class="sxs-lookup"><span data-stu-id="eb428-144">Blit State</span></span>                                   | <span data-ttu-id="eb428-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb428-145">Description</span></span>                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="eb428-146">**DXVAHD \_ BLT \_ STATE \_ TARGET \_ RECT**</span><span class="sxs-lookup"><span data-stu-id="eb428-146">**DXVAHD\_BLT\_STATE\_TARGET\_RECT**</span></span>         | <span data-ttu-id="eb428-147">Rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="eb428-147">Target rectangle.</span></span>                                                            |
| <span data-ttu-id="eb428-148">**COLOR DE FONDO DEL \_ ESTADO BLT DE DXVAHD \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="eb428-148">**DXVAHD\_BLT\_STATE\_BACKGROUND\_COLOR**</span></span>    | <span data-ttu-id="eb428-149">Color de fondo.</span><span class="sxs-lookup"><span data-stu-id="eb428-149">Background color.</span></span>                                                            |
| <span data-ttu-id="eb428-150">**ESPACIO DE COLOR DE SALIDA DEL \_ ESTADO BLT DE DXVAHD \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="eb428-150">**DXVAHD\_BLT\_STATE\_OUTPUT\_COLOR\_SPACE**</span></span> | <span data-ttu-id="eb428-151">Espacio de color de salida.</span><span class="sxs-lookup"><span data-stu-id="eb428-151">Output color space.</span></span>                                                          |
| <span data-ttu-id="eb428-152">**RELLENO ALFA DE \_ ESTADO BLT DE DXVAHD \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="eb428-152">**DXVAHD\_BLT\_STATE\_ALPHA\_FILL**</span></span>          | <span data-ttu-id="eb428-153">Modo de relleno alfa.</span><span class="sxs-lookup"><span data-stu-id="eb428-153">Alpha fill mode.</span></span>                                                             |
| <span data-ttu-id="eb428-154">**CONSTRICCIÓN DEL \_ ESTADO \_ BLT DE DXVAHD \_**</span><span class="sxs-lookup"><span data-stu-id="eb428-154">**DXVAHD\_BLT\_STATE\_CONSTRICTION**</span></span>         | <span data-ttu-id="eb428-155">Constricción.</span><span class="sxs-lookup"><span data-stu-id="eb428-155">Constriction.</span></span> <span data-ttu-id="eb428-156">Este estado controla si el dispositivo reduce el muestreo de la salida.</span><span class="sxs-lookup"><span data-stu-id="eb428-156">This state controls whether the device downsamples the output.</span></span> |



 

<span data-ttu-id="eb428-157">Para establecer un estado de secuencia, llame al [**método IDXVAHD \_ VideoProcessor::SetVideoProcessStreamState.**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate)</span><span class="sxs-lookup"><span data-stu-id="eb428-157">To set a stream state, call the [**IDXVAHD\_VideoProcessor::SetVideoProcessStreamState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate) method.</span></span> <span data-ttu-id="eb428-158">Para establecer un estado blit, llame al [**método IDXVAHD \_ VideoProcessor::SetVideoProcessBltState.**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate)</span><span class="sxs-lookup"><span data-stu-id="eb428-158">To set a blit state, call the [**IDXVAHD\_VideoProcessor::SetVideoProcessBltState**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate) method.</span></span> <span data-ttu-id="eb428-159">En ambos métodos, un valor de enumeración especifica el estado que se debe establecer.</span><span class="sxs-lookup"><span data-stu-id="eb428-159">In both of these methods, an enumeration value specifies the state to set.</span></span> <span data-ttu-id="eb428-160">Los datos de estado se entregan mediante una estructura de datos específica del estado, que la aplicación convierte a un **tipo void. \***</span><span class="sxs-lookup"><span data-stu-id="eb428-160">The state data is given using a state-specific data structure, which the application casts to a **void\*** type.</span></span>

<span data-ttu-id="eb428-161">En el ejemplo de código siguiente se establece el formato de entrada y el rectángulo de destino para la secuencia 0 y el color de fondo en negro.</span><span class="sxs-lookup"><span data-stu-id="eb428-161">The following code example sets the input format and destination rectangle for stream 0, and sets the background color to black.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="eb428-162">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="eb428-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb428-163">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="eb428-163">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



