---
title: Características del códec
description: Características del códec
ms.assetid: e0bbdf75-2369-4080-ae8e-aabaa8401dcf
keywords:
- SDK de Windows Media Format, características de códecs
- Windows Media Format SDK, características
- códecs, características
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e3623bcb6f338fe11bef3089705801dc3ea047
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268767"
---
# <a name="codec-features"></a><span data-ttu-id="6bf49-106">Características del códec</span><span class="sxs-lookup"><span data-stu-id="6bf49-106">Codec Features</span></span>

<span data-ttu-id="6bf49-107">El SDK de Windows Media Format se entrega con varios códecs de audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="6bf49-107">The Windows Media Format SDK is delivered with several audio and video codecs.</span></span> <span data-ttu-id="6bf49-108">Puede usar los códecs que se proporcionan para comprimir y descomprimir contenido para satisfacer diversas necesidades.</span><span class="sxs-lookup"><span data-stu-id="6bf49-108">You can use the codecs provided to compress and decompress content to suit a variety of needs.</span></span> <span data-ttu-id="6bf49-109">El códec que usa el escritor para comprimir los datos se especifica mediante la información de configuración de la secuencia en el perfil.</span><span class="sxs-lookup"><span data-stu-id="6bf49-109">The codec that is used by the writer to compress data is specified by stream configuration information in the profile.</span></span> <span data-ttu-id="6bf49-110">La información del perfil se almacena en el encabezado del archivo creado por el escritor.</span><span class="sxs-lookup"><span data-stu-id="6bf49-110">Information from the profile is then stored in the header of the file created by the writer.</span></span> <span data-ttu-id="6bf49-111">A continuación, cuando el lector abre el archivo o el lector sincrónico, la información de perfil del encabezado identifica el códec necesario para descomprimir los datos.</span><span class="sxs-lookup"><span data-stu-id="6bf49-111">Then, when the file is opened by the reader or synchronous reader, the profile information in the header identifies the codec needed to decompress the data.</span></span>

<span data-ttu-id="6bf49-112">En esta sección se describen las características siguientes.</span><span class="sxs-lookup"><span data-stu-id="6bf49-112">The following features are discussed in this section.</span></span>

-   [<span data-ttu-id="6bf49-113">Códecs admitidos</span><span class="sxs-lookup"><span data-stu-id="6bf49-113">Supported Codecs</span></span>](supported-codecs.md)
-   [<span data-ttu-id="6bf49-114">Codificación de velocidad de bits constante (CBR)</span><span class="sxs-lookup"><span data-stu-id="6bf49-114">Constant Bit Rate (CBR) Encoding</span></span>](constant-bit-rate--cbr--encoding.md)
-   [<span data-ttu-id="6bf49-115">Codificación de velocidad de bits variable (VBR)</span><span class="sxs-lookup"><span data-stu-id="6bf49-115">Variable Bit Rate (VBR) Encoding</span></span>](variable-bit-rate--vbr--encoding.md)
-   [<span data-ttu-id="6bf49-116">Codificación de dos pasos</span><span class="sxs-lookup"><span data-stu-id="6bf49-116">Two-Pass Encoding</span></span>](two-pass-encoding.md)
-   [<span data-ttu-id="6bf49-117">Compatibilidad con audio de alta resolución</span><span class="sxs-lookup"><span data-stu-id="6bf49-117">High-Resolution Audio Support</span></span>](high-resolution-audio-support.md)
-   [<span data-ttu-id="6bf49-118">Audio con retraso bajo</span><span class="sxs-lookup"><span data-stu-id="6bf49-118">Low-Delay Audio</span></span>](low-delay-audio.md)
-   [<span data-ttu-id="6bf49-119">Salida de audio S/PDIF</span><span class="sxs-lookup"><span data-stu-id="6bf49-119">S/PDIF Audio Output</span></span>](s-pdif-audio-output.md)
-   [<span data-ttu-id="6bf49-120">Imagen de vídeo</span><span class="sxs-lookup"><span data-stu-id="6bf49-120">Video Image</span></span>](video-image.md)
-   [<span data-ttu-id="6bf49-121">Plantillas de conformidad de dispositivos</span><span class="sxs-lookup"><span data-stu-id="6bf49-121">Device Conformance Templates</span></span>](device-conformance-templates.md)
-   [<span data-ttu-id="6bf49-122">Configuración de complejidad de vídeo</span><span class="sxs-lookup"><span data-stu-id="6bf49-122">Video Complexity Settings</span></span>](video-complexity-settings.md)
-   [<span data-ttu-id="6bf49-123">Interpolación de fotogramas</span><span class="sxs-lookup"><span data-stu-id="6bf49-123">Frame Interpolation</span></span>](frame-interpolation.md)

## <a name="related-topics"></a><span data-ttu-id="6bf49-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6bf49-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6bf49-125">**Características**</span><span class="sxs-lookup"><span data-stu-id="6bf49-125">**Features**</span></span>](features.md)
</dt> </dl>

 

 




