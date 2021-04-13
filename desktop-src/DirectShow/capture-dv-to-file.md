---
description: Capturar DV en archivo
ms.assetid: f7a8bcbb-a744-43c4-a226-354ae2d94df8
title: Capturar DV en archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 713e49eba3016b353362c541ba31ffd6a1ae5de7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104359982"
---
# <a name="capture-dv-to-file"></a><span data-ttu-id="2e0ed-103">Capturar DV en archivo</span><span class="sxs-lookup"><span data-stu-id="2e0ed-103">Capture DV to File</span></span>

<span data-ttu-id="2e0ed-104">En esta sección se describe cómo capturar vídeo digital (DV) desde una cámara DV o desde una cinta VTR.</span><span class="sxs-lookup"><span data-stu-id="2e0ed-104">This section describes how to capture digital video (DV) from a DV camera or from a VTR tape.</span></span>

1.  <span data-ttu-id="2e0ed-105">Cree una instancia del filtro del [controlador MSDV](msdv-driver.md) .</span><span class="sxs-lookup"><span data-stu-id="2e0ed-105">Create an instance of the [MSDV Driver](msdv-driver.md) filter.</span></span> <span data-ttu-id="2e0ed-106">Para obtener más información, consulte [seleccionar un dispositivo de captura](selecting-a-capture-device.md).</span><span class="sxs-lookup"><span data-stu-id="2e0ed-106">For more information, see [Selecting a Capture Device](selecting-a-capture-device.md).</span></span>
2.  <span data-ttu-id="2e0ed-107">Inicialice el generador de gráficos de captura, tal y como se describe en [el generador de gráficos de captura](about-the-capture-graph-builder.md).</span><span class="sxs-lookup"><span data-stu-id="2e0ed-107">Initialize the Capture Graph Builder, as described in [About the Capture Graph Builder](about-the-capture-graph-builder.md).</span></span>
3.  <span data-ttu-id="2e0ed-108">Cree el gráfico de captura, en función del tipo de archivo de destino:</span><span class="sxs-lookup"><span data-stu-id="2e0ed-108">Build the capture graph, depending on the target file type:</span></span>
    -   [<span data-ttu-id="2e0ed-109">Capturar un archivo de tipo 1 DV</span><span class="sxs-lookup"><span data-stu-id="2e0ed-109">Capture a Type-1 DV File</span></span>](capture-a-type-1-dv-file.md)
    -   [<span data-ttu-id="2e0ed-110">Capturar un archivo de tipo-2 DV</span><span class="sxs-lookup"><span data-stu-id="2e0ed-110">Capture a Type-2 DV File</span></span>](capture-a-type-2-dv-file.md)
    -   [<span data-ttu-id="2e0ed-111">Capturar DV en RGB sin comprimir</span><span class="sxs-lookup"><span data-stu-id="2e0ed-111">Capture DV to Uncompressed RGB</span></span>](capture-dv-to-uncompressed-rgb.md)
4.  <span data-ttu-id="2e0ed-112">Ejecute el gráfico.</span><span class="sxs-lookup"><span data-stu-id="2e0ed-112">Run the graph.</span></span>

<span data-ttu-id="2e0ed-113">La captura de una cinta VTR funciona igual que la captura de vídeo en directo desde la cámara, salvo que se debe reproducir la cinta, tal como se describe en [controlar una videocámara DV](controlling-a-dv-camcorder.md).</span><span class="sxs-lookup"><span data-stu-id="2e0ed-113">Capturing from a VTR tape works just like capturing live video from the camera, except that you must play the tape, as described in [Controlling a DV Camcorder](controlling-a-dv-camcorder.md).</span></span> <span data-ttu-id="2e0ed-114">Para evitar la pérdida de fotogramas, ejecute primero el gráfico y, a continuación, reproduzca la cinta.</span><span class="sxs-lookup"><span data-stu-id="2e0ed-114">To avoid losing any frames, run the graph first, and then play the tape.</span></span> <span data-ttu-id="2e0ed-115">Cuando haya terminado de transmitir, detenga primero la cinta y, a continuación, detenga el gráfico.</span><span class="sxs-lookup"><span data-stu-id="2e0ed-115">When you are done transmitting, stop the tape first and then stop the graph.</span></span>

> [!Note]  
> <span data-ttu-id="2e0ed-116">El camascopio debe estar en modo VTR.</span><span class="sxs-lookup"><span data-stu-id="2e0ed-116">The camcorder must be in VTR mode.</span></span> <span data-ttu-id="2e0ed-117">Vea [modo de dispositivo](device-mode.md).</span><span class="sxs-lookup"><span data-stu-id="2e0ed-117">See [Device Mode](device-mode.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="2e0ed-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2e0ed-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e0ed-119">Vídeo digital en DirectShow</span><span class="sxs-lookup"><span data-stu-id="2e0ed-119">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="2e0ed-120">Archivos AVI de tipo 1 frente a-2</span><span class="sxs-lookup"><span data-stu-id="2e0ed-120">Type-1 vs. Type-2 DV AVI Files</span></span>](type-1-vs--type-2-dv-avi-files.md)
</dt> <dt>

[<span data-ttu-id="2e0ed-121">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="2e0ed-121">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



