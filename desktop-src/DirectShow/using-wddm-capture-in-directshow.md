---
description: Usar la captura de WDDM en DirectShow
ms.assetid: 57ee86b0-50bc-4992-94d4-f290f83d2afc
title: Usar la captura de WDDM en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7926af70a3b7f1c4ba67c791d98c9928c3809b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678079"
---
# <a name="using-wddm-capture-in-directshow"></a><span data-ttu-id="8b417-103">Usar la captura de WDDM en DirectShow</span><span class="sxs-lookup"><span data-stu-id="8b417-103">Using WDDM Capture in DirectShow</span></span>

<span data-ttu-id="8b417-104">Este tema se aplica a Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="8b417-104">This topic applies to Windows Vista and later.</span></span>

<span data-ttu-id="8b417-105">Algunas tarjetas de vídeo tienen integrada la funcionalidad de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8b417-105">Some video cards have integrated video capture functionality.</span></span> <span data-ttu-id="8b417-106">En estas tarjetas, los fotogramas de vídeo capturados se colocan en la memoria de vídeo (VRAM).</span><span class="sxs-lookup"><span data-stu-id="8b417-106">On these cards, captured video frames are placed in video memory (VRAM).</span></span> <span data-ttu-id="8b417-107">Antes de Windows Vista, no había ningún mecanismo estándar para procesar los fotogramas mientras permanecían en VRAM.</span><span class="sxs-lookup"><span data-stu-id="8b417-107">Prior to Windows Vista, there was no standard mechanism for processing the frames while they remained in VRAM.</span></span> <span data-ttu-id="8b417-108">En su lugar, los datos tenían que copiarse en la memoria del sistema, procesarse y, a continuación, volver a copiarse en VRAM para su presentación.</span><span class="sxs-lookup"><span data-stu-id="8b417-108">Instead, the data had to be copied into system memory, processed, and then copied back to VRAM for display.</span></span> <span data-ttu-id="8b417-109">En Windows Vista, DirectShow admite ahora un mecanismo para mantener los fotogramas de vídeo en VRAM a lo largo de la canalización de procesamiento, desde la captura que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="8b417-109">In Windows Vista, DirectShow now supports a mechanism for keeping the video frames in VRAM throughout the processing pipeline, from capture to display.</span></span>

<span data-ttu-id="8b417-110">El filtro KsProxy determina si el controlador admite la captura de superficie de VRAM consultando el controlador de la propiedad de la \_ superficie de captura preferida de KSPROPERTY \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8b417-110">The KsProxy filter determines if the driver supports VRAM surface capture by querying the driver for the KSPROPERTY\_PREFERRED\_CAPTURE\_SURFACE property.</span></span> <span data-ttu-id="8b417-111">(Esta propiedad se documenta en la documentación del kit de controladores de Windows). Si el controlador admite la captura de superficie de VRAM, KsProxy asigna un tipo especial de medio de ejemplo que contiene un puntero a una superficie de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="8b417-111">(This property is documented in the Windows Driver Kit documentation.) If the driver supports VRAM surface capture, KsProxy allocates a special kind of media sample that holds a pointer to a Direct3D surface.</span></span>

<span data-ttu-id="8b417-112">A continuación, KsProxy determina si el filtro de bajada es compatible con DirectX video Acceleration (DXVA) 2,0, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8b417-112">Next, KsProxy determines whether the downstream filter supports DirectX Video Acceleration (DXVA) 2.0, as follows:</span></span>

1.  <span data-ttu-id="8b417-113">KsProxy consulta el PIN de entrada de nivel inferior de la interfaz **IMFGetService** .</span><span class="sxs-lookup"><span data-stu-id="8b417-113">KsProxy queries the downstream input pin for the **IMFGetService** interface.</span></span>
2.  <span data-ttu-id="8b417-114">Si el PIN expone **IMFGetService**, KsProxy llama a **IMFGetService:: GetService** para la interfaz **IDirect3DDeviceManager** .</span><span class="sxs-lookup"><span data-stu-id="8b417-114">If the pin exposes **IMFGetService**, KsProxy calls **IMFGetService::GetService** for the **IDirect3DDeviceManager** interface.</span></span> <span data-ttu-id="8b417-115">El servicio identier es el \_ servicio de aceleración de vídeo Mr \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8b417-115">The service identier is MR\_VIDEO\_ACCELERATION\_SERVICE.</span></span>

<span data-ttu-id="8b417-116">Ambas interfaces se documentan en la documentación del SDK de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8b417-116">Both of these interfaces are documented in the Media Foundation SDK documentation.</span></span>

<span data-ttu-id="8b417-117">Si el filtro de nivel inferior no admite DXVA 2,0, KsProxy asigna un búfer de memoria del sistema adicional.</span><span class="sxs-lookup"><span data-stu-id="8b417-117">If the downstream filter does not support DXVA 2.0, KsProxy allocates an additional system memory buffer.</span></span> <span data-ttu-id="8b417-118">Usa este búfer para copiar los fotogramas de vídeo de VRAM a la memoria del sistema.</span><span class="sxs-lookup"><span data-stu-id="8b417-118">It uses this buffer to copy the video frames from VRAM to system memory.</span></span> <span data-ttu-id="8b417-119">El método [**IMediaSample:: GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) del ejemplo multimedia devuelve un puntero a este búfer de memoria del sistema.</span><span class="sxs-lookup"><span data-stu-id="8b417-119">The media sample's [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) method returns a pointer to this system memory buffer.</span></span>

<span data-ttu-id="8b417-120">Sin embargo, si el filtro de nivel inferior admite DXVA 2,0, KsProxy no asignará un búfer de memoria del sistema.</span><span class="sxs-lookup"><span data-stu-id="8b417-120">However, if the downstream filter does support DXVA 2.0, then KsProxy does not allocate a system memory buffer.</span></span> <span data-ttu-id="8b417-121">En ese caso, el método **GetPointer** devuelve E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="8b417-121">In that case, the **GetPointer** method returns E\_NOTIMPL.</span></span> <span data-ttu-id="8b417-122">En su lugar, se espera que el filtro de nivel inferior acceda directamente a la superficie de Direct3D del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="8b417-122">Instead, the downstream filter is expected to access the sample's Direct3D surface directly.</span></span> <span data-ttu-id="8b417-123">Hay dos maneras de que el filtro de nivel inferior obtenga un puntero a la superficie, ambos equivalentes:</span><span class="sxs-lookup"><span data-stu-id="8b417-123">There are two ways for the downstream filter to get a pointer to the surface, both of them equivalent:</span></span>

-   <span data-ttu-id="8b417-124">Consulte el ejemplo de la interfaz **IMFGetService** y llame a **GetService** para la interfaz **IDirect3DSurface9** .</span><span class="sxs-lookup"><span data-stu-id="8b417-124">Query the sample for the **IMFGetService** interface and call **GetService** for the **IDirect3DSurface9** interface.</span></span> <span data-ttu-id="8b417-125">El identificador de servicio es el \_ servicio de búfer Mr \_ .</span><span class="sxs-lookup"><span data-stu-id="8b417-125">The service identifier is MR\_BUFFER\_SERVICE.</span></span>
-   <span data-ttu-id="8b417-126">Consulte el ejemplo de la interfaz [**IMediaSample2Config**](/windows/desktop/api/Strmif/nn-strmif-imediasample2config) y llame a [**IMediaSample2Config:: GetSurface**](/windows/desktop/api/Strmif/nf-strmif-imediasample2config-getsurface).</span><span class="sxs-lookup"><span data-stu-id="8b417-126">Query the sample for the [**IMediaSample2Config**](/windows/desktop/api/Strmif/nn-strmif-imediasample2config) interface and call [**IMediaSample2Config::GetSurface**](/windows/desktop/api/Strmif/nf-strmif-imediasample2config-getsurface).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b417-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8b417-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b417-128">Temas de captura avanzada</span><span class="sxs-lookup"><span data-stu-id="8b417-128">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> </dl>

 

 



