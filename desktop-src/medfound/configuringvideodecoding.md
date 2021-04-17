---
description: Configuración de la descodificación de vídeo
ms.assetid: 897b8e2d-9827-428d-91ae-632038c4c8c0
title: Configuración de la descodificación de vídeo (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f386e3dbb39d6296756f2fe8eec1b94c5533bff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705420"
---
# <a name="configuring-video-decoding-microsoft-media-foundation"></a><span data-ttu-id="7b886-103">Configuración de la descodificación de vídeo (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="7b886-103">Configuring Video Decoding (Microsoft Media Foundation)</span></span>

<span data-ttu-id="7b886-104">La descodificación es esencialmente la opuesta a la codificación en cuanto a la configuración.</span><span class="sxs-lookup"><span data-stu-id="7b886-104">Decoding is essentially the opposite of encoding in terms of configuration.</span></span> <span data-ttu-id="7b886-105">El descodificador admite muy pocas propiedades y no se requiere ninguna.</span><span class="sxs-lookup"><span data-stu-id="7b886-105">The decoder supports very few properties, and none of them is required.</span></span> <span data-ttu-id="7b886-106">Establezca el tipo de entrada en el tipo que se usa para la salida del descodificador (incluidos los datos privados del códec).</span><span class="sxs-lookup"><span data-stu-id="7b886-106">Set the input type to the type used for the decoder output (including the codec private data).</span></span> <span data-ttu-id="7b886-107">A continuación, establezca la salida en el formato sin comprimir deseado, establezca la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) para que refleje el tamaño de fotograma adecuado y comience a procesar ejemplos.</span><span class="sxs-lookup"><span data-stu-id="7b886-107">Then set the output to the desired uncompressed format, set the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure to reflect the proper frame size, and start processing samples.</span></span>

<span data-ttu-id="7b886-108">Debe proporcionar el descodificador con un tipo de medio que incluya los datos privados del códec situados inmediatamente después de la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="7b886-108">You must supply the decoder with a media type that includes the codec private data positioned immediately after the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span> <span data-ttu-id="7b886-109">El descodificador no puede descodificar el contenido sin estos datos.</span><span class="sxs-lookup"><span data-stu-id="7b886-109">The decoder cannot decode the content without this data.</span></span> <span data-ttu-id="7b886-110">La validación de formato realizada por el descodificador no valida los datos privados.</span><span class="sxs-lookup"><span data-stu-id="7b886-110">The format validation performed by the decoder does not validate the private data.</span></span> <span data-ttu-id="7b886-111">Si los datos privados del códec faltan o son incorrectos, el descodificador responde como si el flujo de bits estuviera dañado.</span><span class="sxs-lookup"><span data-stu-id="7b886-111">If the codec private data is missing or incorrect, the decoder responds as if the bit stream is corrupted.</span></span> <span data-ttu-id="7b886-112">Para obtener más información, consulte [uso de datos privados de códecs de vídeo](usingvideocodecprivatedata.md).</span><span class="sxs-lookup"><span data-stu-id="7b886-112">For more information, see [Using Video Codec Private Data](usingvideocodecprivatedata.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b886-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7b886-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b886-114">Uso de datos privados de códecs de vídeo</span><span class="sxs-lookup"><span data-stu-id="7b886-114">Using Video Codec Private Data</span></span>](usingvideocodecprivatedata.md)
</dt> <dt>

[<span data-ttu-id="7b886-115">Trabajar con vídeo</span><span class="sxs-lookup"><span data-stu-id="7b886-115">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 
