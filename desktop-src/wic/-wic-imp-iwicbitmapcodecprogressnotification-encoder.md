---
description: Implementación de IWICBitmapCodecProgressNotification (encoder)
ms.assetid: d470ec93-d329-48c0-9556-0c15daece491
title: Implementación de IWICBitmapCodecProgressNotification (encoder)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260fac41068de0695813d569881e4a71938eb83d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911954"
---
# <a name="implementing-iwicbitmapcodecprogressnotification-encoder"></a><span data-ttu-id="4dc88-103">Implementación de IWICBitmapCodecProgressNotification (encoder)</span><span class="sxs-lookup"><span data-stu-id="4dc88-103">Implementing IWICBitmapCodecProgressNotification (Encoder)</span></span>

## <a name="iwicbitmapcodecprogressnotification"></a><span data-ttu-id="4dc88-104">IWICBitmapCodecProgressNotification</span><span class="sxs-lookup"><span data-stu-id="4dc88-104">IWICBitmapCodecProgressNotification</span></span>

<span data-ttu-id="4dc88-105">Aunque la interfaz [**IWICBitmapCodecProgressNotification**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecprogressnotification) es opcional, se recomienda que se implemente en la clase de codificador de nivel de contenedor.</span><span class="sxs-lookup"><span data-stu-id="4dc88-105">Although the [**IWICBitmapCodecProgressNotification**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecprogressnotification) interface is optional, it is recommended that it be implemented on the container-level encoder class.</span></span> <span data-ttu-id="4dc88-106">Esta interfaz se describe con más detalle en [implementación de IWICBitmapCodecProgressNotification (descodificador)](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="4dc88-106">This interface is discussed in more details in [Implementing IWICBitmapCodecProgressNotification (Decoder)](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md).</span></span> <span data-ttu-id="4dc88-107">La implementación es la misma para el descodificador y el codificador.</span><span class="sxs-lookup"><span data-stu-id="4dc88-107">The implementation is the same for either the decoder and the encoder.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4dc88-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4dc88-108">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4dc88-109">**Vista**</span><span class="sxs-lookup"><span data-stu-id="4dc88-109">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4dc88-110">Implementación de IWICBitmapEncoder</span><span class="sxs-lookup"><span data-stu-id="4dc88-110">Implementing IWICBitmapEncoder</span></span>](-wic-imp-iwicbitmapencoder.md)
</dt> <dt>

[<span data-ttu-id="4dc88-111">Implementar IWICBitmapFrameEncode</span><span class="sxs-lookup"><span data-stu-id="4dc88-111">Implementing IWICBitmapFrameEncode</span></span>](-wic-imp-iwicbitmapframeencode.md)
</dt> <dt>

[<span data-ttu-id="4dc88-112">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="4dc88-112">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="4dc88-113">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="4dc88-113">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="4dc88-114">Implementación de IWICBitmapCodecProgressNotification (descodificador)</span><span class="sxs-lookup"><span data-stu-id="4dc88-114">Implementing IWICBitmapCodecProgressNotification (Decoder)</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> </dl>

 

 



