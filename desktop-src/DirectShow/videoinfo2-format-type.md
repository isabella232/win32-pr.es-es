---
description: Tipo de formato VideoInfo2
ms.assetid: edd2013a-f0c5-4176-ba3a-a3af719ce31d
title: Tipo de formato VideoInfo2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74b0f435e0e2a1b5b1d948c42a881f19300a9c6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687166"
---
# <a name="videoinfo2-format-type"></a><span data-ttu-id="f5bbf-103">Tipo de formato VideoInfo2</span><span class="sxs-lookup"><span data-stu-id="f5bbf-103">VideoInfo2 Format Type</span></span>

<span data-ttu-id="f5bbf-104">Un tipo de medio preferido del PIN de vista previa puede ser un tipo con un formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .</span><span class="sxs-lookup"><span data-stu-id="f5bbf-104">A preview pin's preferred media type might be a type with a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format.</span></span> <span data-ttu-id="f5bbf-105">Esta estructura de formato admite características especiales como el vídeo entrelazado y las relaciones de aspecto de la imagen.</span><span class="sxs-lookup"><span data-stu-id="f5bbf-105">This format structure supports special features such as interlaced video and picture aspect ratios.</span></span>

<span data-ttu-id="f5bbf-106">VMR-7 y VMR-9 admiten [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) directamente.</span><span class="sxs-lookup"><span data-stu-id="f5bbf-106">The VMR-7 and the VMR-9 both support [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) directly.</span></span> <span data-ttu-id="f5bbf-107">Al conectar la VMR al descodificador, se negociará el mejor formato.</span><span class="sxs-lookup"><span data-stu-id="f5bbf-107">When you connect the VMR to the decoder, they will negotiate the best format.</span></span> <span data-ttu-id="f5bbf-108">El filtro de representador de vídeo anterior, sin embargo, no es compatible con **VIDEOINFOHEADER2**.</span><span class="sxs-lookup"><span data-stu-id="f5bbf-108">The older Video Renderer filter, however, does not support **VIDEOINFOHEADER2**.</span></span> <span data-ttu-id="f5bbf-109">Para usar los tipos de formato **VIDEOINFOHEADER2** con el filtro de representador de vídeo, debe insertar el filtro de [mezclador de superposición](overlay-mixer-filter.md) en el gráfico.</span><span class="sxs-lookup"><span data-stu-id="f5bbf-109">To use **VIDEOINFOHEADER2** format types with the Video Renderer filter, you must insert the [Overlay Mixer](overlay-mixer-filter.md) filter into the graph.</span></span>

1.  <span data-ttu-id="f5bbf-110">Enumerar los tipos de medios preferidos en el PIN de salida del filtro del descodificador, mediante el método [**IPin:: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="f5bbf-110">Enumerate the preferred media types on the decoder filter's output pin, using the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method.</span></span>
2.  <span data-ttu-id="f5bbf-111">Compruebe el primer tipo de medio en la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="f5bbf-111">Check the first media type in the enumeration sequence.</span></span>
3.  <span data-ttu-id="f5bbf-112">Si el tipo de formato es **format \_ VideoInfo2**, conecte el PIN de salida al mezclador de superposición.</span><span class="sxs-lookup"><span data-stu-id="f5bbf-112">If the format type is **FORMAT\_VideoInfo2**, connect the output pin to the Overlay Mixer.</span></span> <span data-ttu-id="f5bbf-113">A continuación, conecte el mezclador de superposición al representador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f5bbf-113">Then connect the Overlay Mixer to the video renderer.</span></span> <span data-ttu-id="f5bbf-114">(Consulte [pines del puerto de vídeo](video-port-pins.md)).</span><span class="sxs-lookup"><span data-stu-id="f5bbf-114">(See [Video Port Pins](video-port-pins.md).)</span></span>

<span data-ttu-id="f5bbf-115">Si no le importa estas características, no tiene que usar el mezclador de superposición.</span><span class="sxs-lookup"><span data-stu-id="f5bbf-115">If you do not care about these features, you do not have to use the Overlay Mixer.</span></span> <span data-ttu-id="f5bbf-116">Conecte el descodificador directamente al representador de vídeo y se conectará con un formato [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="f5bbf-116">Connect the decoder directly to the Video Renderer, and it will connect with a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) format instead.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5bbf-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f5bbf-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5bbf-118">Temas de captura avanzada</span><span class="sxs-lookup"><span data-stu-id="f5bbf-118">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="f5bbf-119">Usar el mezclador de superposición en la captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="f5bbf-119">Using the Overlay Mixer in Video Capture</span></span>](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



