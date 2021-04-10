---
description: Ejemplo de EVRPresenter
ms.assetid: 791a9816-4c40-4683-8b32-22f73d7fe84d
title: Ejemplo de EVRPresenter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bde85de152c41f348b1aae74a8c0d67ca746cab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153632"
---
# <a name="evrpresenter-sample"></a><span data-ttu-id="94b32-103">Ejemplo de EVRPresenter</span><span class="sxs-lookup"><span data-stu-id="94b32-103">EVRPresenter Sample</span></span>

<span data-ttu-id="94b32-104">Muestra cómo implementar un presentador personalizado para el [representador de vídeo mejorado](enhanced-video-renderer.md) (EVR).</span><span class="sxs-lookup"><span data-stu-id="94b32-104">Shows how to implement a custom presenter for the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR).</span></span> <span data-ttu-id="94b32-105">El presentador personalizado se puede usar con el filtro EVR de DirectShow o el receptor de EVR de Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="94b32-105">The custom presenter can be used with either the DirectShow EVR filter or the Microsoft Media Foundation EVR sink.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="94b32-106">API mostradas</span><span class="sxs-lookup"><span data-stu-id="94b32-106">APIs Demonstrated</span></span>

<span data-ttu-id="94b32-107">Este ejemplo muestra las siguientes interfaces de Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="94b32-107">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="94b32-108">**IMFClockStateSink**</span><span class="sxs-lookup"><span data-stu-id="94b32-108">**IMFClockStateSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [<span data-ttu-id="94b32-109">**IMFRateSupport**</span><span class="sxs-lookup"><span data-stu-id="94b32-109">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [<span data-ttu-id="94b32-110">**IMFTopologyServiceLookupClient**</span><span class="sxs-lookup"><span data-stu-id="94b32-110">**IMFTopologyServiceLookupClient**</span></span>](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient)
-   [<span data-ttu-id="94b32-111">**IMFVideoDeviceID**</span><span class="sxs-lookup"><span data-stu-id="94b32-111">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)
-   [<span data-ttu-id="94b32-112">**IMFVideoDisplayControl**</span><span class="sxs-lookup"><span data-stu-id="94b32-112">**IMFVideoDisplayControl**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)
-   [<span data-ttu-id="94b32-113">**IMFVideoPresenter**</span><span class="sxs-lookup"><span data-stu-id="94b32-113">**IMFVideoPresenter**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopresenter)

## <a name="usage"></a><span data-ttu-id="94b32-114">Uso</span><span class="sxs-lookup"><span data-stu-id="94b32-114">Usage</span></span>

<span data-ttu-id="94b32-115">En el ejemplo EVRPresenter se crea un archivo DLL que es un servidor COM para el presentador.</span><span class="sxs-lookup"><span data-stu-id="94b32-115">The EVRPresenter sample builds a DLL that is a COM server for the presenter.</span></span> <span data-ttu-id="94b32-116">Antes de usar el presentador personalizado, debe registrar el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="94b32-116">Before using the custom presenter, you must register the DLL.</span></span>

<span data-ttu-id="94b32-117">Para usar este ejemplo en Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="94b32-117">To use this sample in Media Foundation:</span></span>

1.  <span data-ttu-id="94b32-118">Compile el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="94b32-118">Build the sample.</span></span>
2.  <span data-ttu-id="94b32-119">Regsvr32 EvrPresenter.dll.</span><span class="sxs-lookup"><span data-stu-id="94b32-119">Regsvr32 EvrPresenter.dll.</span></span>
3.  <span data-ttu-id="94b32-120">Compile y ejecute el [ejemplo MFPlayer](/previous-versions//bb970516(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="94b32-120">Build and run the [MFPlayer Sample](/previous-versions//bb970516(v=vs.85)).</span></span>
4.  <span data-ttu-id="94b32-121">En el menú **archivo** , seleccione **abrir** archivo.</span><span class="sxs-lookup"><span data-stu-id="94b32-121">From the **File** menu, select **Open** File.</span></span>
5.  <span data-ttu-id="94b32-122">En el cuadro de diálogo **Abrir archivo** , seleccione **presentador EVR personalizado.**</span><span class="sxs-lookup"><span data-stu-id="94b32-122">In the **Open File** dialog box, select **Custom EVR Presenter.**</span></span>
6.  <span data-ttu-id="94b32-123">Seleccione un archivo para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="94b32-123">Select a file for playback.</span></span>

<span data-ttu-id="94b32-124">Para usar este ejemplo en DirectShow:</span><span class="sxs-lookup"><span data-stu-id="94b32-124">To use this sample in DirectShow:</span></span>

1.  <span data-ttu-id="94b32-125">Compile el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="94b32-125">Build the sample.</span></span>
2.  <span data-ttu-id="94b32-126">Registre EvrPresenter.dll.</span><span class="sxs-lookup"><span data-stu-id="94b32-126">Register EvrPresenter.dll.</span></span>
3.  <span data-ttu-id="94b32-127">Compile y ejecute el ejemplo EVRPlayer.</span><span class="sxs-lookup"><span data-stu-id="94b32-127">Build and run the EVRPlayer sample.</span></span> <span data-ttu-id="94b32-128">Este ejemplo se incluye con los ejemplos de DirectShow en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="94b32-128">This sample is included with the DirectShow samples in the Windows SDK.</span></span>
4.  <span data-ttu-id="94b32-129">En el menú **archivo** , seleccione **presentador EVR**.</span><span class="sxs-lookup"><span data-stu-id="94b32-129">From the **File** menu, select **EVR Presenter**.</span></span>
5.  <span data-ttu-id="94b32-130">Seleccione un archivo para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="94b32-130">Select a file for playback.</span></span>

## <a name="requirements"></a><span data-ttu-id="94b32-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94b32-131">Requirements</span></span>



| <span data-ttu-id="94b32-132">Producto</span><span class="sxs-lookup"><span data-stu-id="94b32-132">Product</span></span>                                                        | <span data-ttu-id="94b32-133">Versión</span><span class="sxs-lookup"><span data-stu-id="94b32-133">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="94b32-134">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="94b32-134">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="94b32-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="94b32-135">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="94b32-136">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="94b32-136">Downloading the Sample</span></span>

<span data-ttu-id="94b32-137">Este ejemplo está disponible en el [repositorio de github de ejemplos de Windows clásico](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip).</span><span class="sxs-lookup"><span data-stu-id="94b32-137">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip).</span></span>

## <a name="related-topics"></a><span data-ttu-id="94b32-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="94b32-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94b32-139">Representador de vídeo mejorado</span><span class="sxs-lookup"><span data-stu-id="94b32-139">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> <dt>

[<span data-ttu-id="94b32-140">Cómo escribir un presentador de EVR</span><span class="sxs-lookup"><span data-stu-id="94b32-140">How to Write an EVR Presenter</span></span>](how-to-write-an-evr-presenter.md)
</dt> <dt>

[<span data-ttu-id="94b32-141">Muestras de SDK de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="94b32-141">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> </dl>

 

 
