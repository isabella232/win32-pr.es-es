---
title: Entrada y salida de datos
description: Entrada y salida de datos
ms.assetid: a03b5327-65df-4cb9-a639-1e943ac28bfc
keywords:
- Complementos de Windows Media Player, entrada y salida de datos
- complementos, entrada y salida de datos
- Complementos de procesamiento de señal digital, entrada y salida de datos
- Complementos DSP, entrada y salida de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39f66946dc796337d1f1e638cfe3828b3cbfbb6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148813"
---
# <a name="data-input-and-output"></a><span data-ttu-id="5e66d-107">Entrada y salida de datos</span><span class="sxs-lookup"><span data-stu-id="5e66d-107">Data Input and Output</span></span>

<span data-ttu-id="5e66d-108">Windows Media Player proporciona datos de audio o vídeo a los complementos de DSP a través de un búfer de entrada asignado por Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="5e66d-108">Windows Media Player provides audio or video data to DSP plug-ins through an input buffer allocated by Windows Media Player.</span></span> <span data-ttu-id="5e66d-109">Los complementos DSP devuelven datos procesados a Windows Media Player a través de un búfer de salida que también se asigna a Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="5e66d-109">DSP plug-ins return processed data to Windows Media Player through an output buffer that is also allocated by Windows Media Player.</span></span> <span data-ttu-id="5e66d-110">Windows Media Player administra el proceso de pasar datos entre sí mismo y el complemento de DSP llamando a métodos implementados por el complemento.</span><span class="sxs-lookup"><span data-stu-id="5e66d-110">Windows Media Player manages the process of passing data between itself and the DSP plug-in by calling methods implemented by the plug-in.</span></span> <span data-ttu-id="5e66d-111">Para un complemento que actúa como un objeto multimedia de DirectX (DMO), el proceso funciona de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="5e66d-111">For a plug-in acting as a DirectX Media Object (DMO), the process works as follows:</span></span>

1.  <span data-ttu-id="5e66d-112">Windows Media Player llama a **IMediaObject::P rocessinput**, pasando un puntero a un objeto **IMEDIABUFFER** al complemento DSP.</span><span class="sxs-lookup"><span data-stu-id="5e66d-112">Windows Media Player calls **IMediaObject::ProcessInput**, passing a pointer to an **IMediaBuffer** object to the DSP plug-in.</span></span>
2.  <span data-ttu-id="5e66d-113">El complemento DSP mantiene un recuento de referencias en el objeto de búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="5e66d-113">The DSP plug-in keeps a reference count on the input buffer object.</span></span> <span data-ttu-id="5e66d-114">El complemento DSP devuelve un **valor HRESULT** correcto o de error adecuado.</span><span class="sxs-lookup"><span data-stu-id="5e66d-114">The DSP plug-in returns an appropriate success or failure **HRESULT**.</span></span>
3.  <span data-ttu-id="5e66d-115">Windows Media Player llama a **IMediaObject::P rocessoutput**, pasando un puntero a una matriz de estructuras de búfer de datos de salida de DMO (que contienen búferes de salida) al complemento DSP. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5e66d-115">Windows Media Player calls **IMediaObject::ProcessOutput**, passing a pointer to an array of **DMO\_OUTPUT\_DATA\_BUFFER** structures (which contain output buffers) to the DSP plug-in.</span></span>
4.  <span data-ttu-id="5e66d-116">El complemento de DSP procesa los datos en el búfer de entrada y, a continuación, copia los datos en el búfer de salida adecuado.</span><span class="sxs-lookup"><span data-stu-id="5e66d-116">The DSP plug-in processes the data in the input buffer and then copies the data to the appropriate output buffer.</span></span> <span data-ttu-id="5e66d-117">El complemento DSP libera el recuento de referencias en el objeto de búfer de entrada cuando se han procesado todos los datos del búfer.</span><span class="sxs-lookup"><span data-stu-id="5e66d-117">The DSP plug-in releases the reference count on the input buffer object when all the data in the buffer has been processed.</span></span> <span data-ttu-id="5e66d-118">A continuación, el complemento DSP devuelve un **valor HRESULT** de éxito o error adecuado.</span><span class="sxs-lookup"><span data-stu-id="5e66d-118">The DSP plug-in then returns an appropriate success or failure **HRESULT**.</span></span>
5.  <span data-ttu-id="5e66d-119">Windows Media Player representa el contenido en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="5e66d-119">Windows Media Player renders the content in the output buffer.</span></span>

<span data-ttu-id="5e66d-120">Para un complemento que actúa como una transformación de Media Foundation (MFT), el proceso funciona de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="5e66d-120">For a plug-in acting as a Media Foundation Transform (MFT), the process works as follows:</span></span>

-   <span data-ttu-id="5e66d-121">Windows Media Player llama a **IMFTransform::P rocessinput**, pasando un puntero a un objeto de interfaz **IMFSAMPLE** al complemento DSP.</span><span class="sxs-lookup"><span data-stu-id="5e66d-121">Windows Media Player calls **IMFTransform::ProcessInput**, passing a pointer to an **IMFSample** interface object to the DSP plug-in.</span></span>
    1.  <span data-ttu-id="5e66d-122">El complemento DSP mantiene un recuento de referencias en la interfaz **IMFSample** .</span><span class="sxs-lookup"><span data-stu-id="5e66d-122">The DSP plug-in keeps a reference count on the **IMFSample** interface.</span></span> <span data-ttu-id="5e66d-123">El complemento DSP devuelve un **valor HRESULT** correcto o de error adecuado.</span><span class="sxs-lookup"><span data-stu-id="5e66d-123">The DSP plug-in returns an appropriate success or failure **HRESULT**.</span></span>
    2.  <span data-ttu-id="5e66d-124">Windows Media Player llama a **IMFTransform::P rocessoutput**, pasando un puntero a una matriz de estructuras de búfer de datos de salida de MFT (que contienen búferes de salida) al complemento DSP. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5e66d-124">Windows Media Player calls **IMFTransform::ProcessOutput**, passing a pointer to an array of **MFT\_OUTPUT\_DATA\_BUFFER** structures (which contain output buffers) to the DSP plug-in.</span></span>
    3.  <span data-ttu-id="5e66d-125">El complemento de DSP procesa los datos en el búfer de entrada y, a continuación, copia los datos en el búfer de salida adecuado.</span><span class="sxs-lookup"><span data-stu-id="5e66d-125">The DSP plug-in processes the data in the input buffer and then copies the data to the appropriate output buffer.</span></span> <span data-ttu-id="5e66d-126">El complemento DSP libera el recuento de referencias en el objeto de búfer de entrada cuando se han procesado todos los datos del búfer.</span><span class="sxs-lookup"><span data-stu-id="5e66d-126">The DSP plug-in releases the reference count on the input buffer object when all the data in the buffer has been processed.</span></span> <span data-ttu-id="5e66d-127">A continuación, el complemento DSP devuelve un **valor HRESULT** de éxito o error adecuado.</span><span class="sxs-lookup"><span data-stu-id="5e66d-127">The DSP plug-in then returns an appropriate success or failure **HRESULT**.</span></span>
    4.  <span data-ttu-id="5e66d-128">Windows Media Player representa el contenido en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="5e66d-128">Windows Media Player renders the content in the output buffer.</span></span>

<span data-ttu-id="5e66d-129">Este proceso se repite continuamente mientras el complemento está habilitado y Windows Media Player tiene contenido para representarlo.</span><span class="sxs-lookup"><span data-stu-id="5e66d-129">This process repeats continuously while the plug-in is enabled and Windows Media Player has content to render.</span></span>

> [!Note]  
> <span data-ttu-id="5e66d-130">No Escriba código que escriba datos en el búfer de entrada o que lea los datos del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="5e66d-130">Do not write code that writes data to the input buffer or reads data from the output buffer.</span></span> <span data-ttu-id="5e66d-131">El acceso incorrecto a los búferes de datos puede producir resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="5e66d-131">Incorrectly accessing data buffers may yield unexpected results.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5e66d-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5e66d-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e66d-133">**Introducción al desarrollador de complementos de DSP**</span><span class="sxs-lookup"><span data-stu-id="5e66d-133">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




