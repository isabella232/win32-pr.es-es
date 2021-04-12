---
description: Atributos de secuencia
ms.assetid: 83b64ad8-2552-41d1-bc61-20361831020b
title: Atributos de secuencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a25de9ae6cf769268b3868d36bac2e293cfd8d60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543790"
---
# <a name="stream-attributes"></a><span data-ttu-id="5e732-103">Atributos de secuencia</span><span class="sxs-lookup"><span data-stu-id="5e732-103">Stream Attributes</span></span>

<span data-ttu-id="5e732-104">Los siguientes atributos se aplican a las secuencias de multimedia.</span><span class="sxs-lookup"><span data-stu-id="5e732-104">The following attributes apply to media streams.</span></span> <span data-ttu-id="5e732-105">Para obtener los atributos de un ejemplo multimedia, use el método [**IMFMediaSourceEx:: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) .</span><span class="sxs-lookup"><span data-stu-id="5e732-105">To get the attributes from a media sample, use the [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) method.</span></span>



| <span data-ttu-id="5e732-106">Atributo</span><span class="sxs-lookup"><span data-stu-id="5e732-106">Attribute</span></span>                                                                                   | <span data-ttu-id="5e732-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e732-107">Description</span></span>                                   |
|---------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="5e732-108">MFStreamExtension \_ CameraExtrinsics</span><span class="sxs-lookup"><span data-stu-id="5e732-108">MFStreamExtension\_CameraExtrinsics</span></span>](mfstreamextension-cameraextrinsics.md)               | <span data-ttu-id="5e732-109">La cámara extrinsics para la secuencia.</span><span class="sxs-lookup"><span data-stu-id="5e732-109">The camera extrinsics for the stream.</span></span>         |
| [<span data-ttu-id="5e732-110">MFStreamExtension \_ PinholeCameraIntrinsics</span><span class="sxs-lookup"><span data-stu-id="5e732-110">MFStreamExtension\_PinholeCameraIntrinsics</span></span>](mfstreamextension-pinholecameraintrinsics.md) | <span data-ttu-id="5e732-111">La cámara pinhole intrínseco para la secuencia.</span><span class="sxs-lookup"><span data-stu-id="5e732-111">The pinhole camera intrinsics for the stream.</span></span> |



 

<span data-ttu-id="5e732-112">No todas las secuencias de medios contienen todos los atributos que se enumeran aquí.</span><span class="sxs-lookup"><span data-stu-id="5e732-112">Not every media stream contains every attribute listed here.</span></span> <span data-ttu-id="5e732-113">En algunos casos, un atributo solo se aplica a determinados tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="5e732-113">In some cases, an attribute applies only to certain kinds of data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5e732-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5e732-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e732-115">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="5e732-115">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[<span data-ttu-id="5e732-116">Atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5e732-116">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5e732-117">Ejemplos de medios</span><span class="sxs-lookup"><span data-stu-id="5e732-117">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 



