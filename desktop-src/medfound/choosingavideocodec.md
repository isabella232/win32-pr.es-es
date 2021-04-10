---
description: Elección de un códec de vídeo
ms.assetid: 3a4b925a-4fb4-4189-a571-8083454fed0e
title: Elección de un códec de vídeo (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9186c7e7e60f5822ec2e50e3e5c7e16e96b91839
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275145"
---
# <a name="choosing-a-video-codec-microsoft-media-foundation"></a><span data-ttu-id="0a5a8-103">Elección de un códec de vídeo (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="0a5a8-103">Choosing a Video Codec (Microsoft Media Foundation)</span></span>

<span data-ttu-id="0a5a8-104">El codificador de Windows Media Video 9 admite tres categorías de salida codificada: perfil principal, perfil avanzado e imagen.</span><span class="sxs-lookup"><span data-stu-id="0a5a8-104">The Windows Media Video 9 Encoder supports three categories of encoded output: Main Profile, Advanced Profile, and Image.</span></span> <span data-ttu-id="0a5a8-105">La categoría principal de perfil proporciona compresión de vídeo general para contenido de vídeo complejo, como películas o vídeos musicales.</span><span class="sxs-lookup"><span data-stu-id="0a5a8-105">The Main Profile category provides general video compression for complex video content, such as movies or music videos.</span></span> <span data-ttu-id="0a5a8-106">Las características del perfil principal proporcionan una amplia gama de opciones de codificación.</span><span class="sxs-lookup"><span data-stu-id="0a5a8-106">The features of the Main Profile provide for a wide range of encoding settings.</span></span> <span data-ttu-id="0a5a8-107">Puede usar el perfil principal para crear vídeo con velocidades de bits muy bajas para la entrega en dispositivos de mano o, en el otro extremo del espectro, puede usarlo para crear vídeo de alta definición para cine digital.</span><span class="sxs-lookup"><span data-stu-id="0a5a8-107">You can use the Main Profile to create video with very low bit rates for delivery on handheld devices or, at the other end of the spectrum, you can use it to create high-definition video for digital cinema.</span></span>

<span data-ttu-id="0a5a8-108">El énfasis de los algoritmos de codificación en el perfil principal se encuentra en el contenido de vídeo dinámico, pero también es adecuado para otro contenido de vídeo.</span><span class="sxs-lookup"><span data-stu-id="0a5a8-108">The emphasis of the encoding algorithms in the Main Profile is on dynamic video content, but they are suitable for other video content as well.</span></span> <span data-ttu-id="0a5a8-109">El perfil principal debe ser la categoría predeterminada para el contenido de vídeo.</span><span class="sxs-lookup"><span data-stu-id="0a5a8-109">The Main Profile should be your default category for video content.</span></span> <span data-ttu-id="0a5a8-110">Para satisfacer necesidades específicas, puede usar la categoría de perfil avanzado, la categoría de imagen o un codificador independiente denominado codificador de pantalla de Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="0a5a8-110">To meet specific needs, you can use the Advanced Profile category, the Image category, or a separate encoder called the Windows Media Video 9 Screen encoder.</span></span> <span data-ttu-id="0a5a8-111">En la tabla siguiente se enumeran las cuatro opciones.</span><span class="sxs-lookup"><span data-stu-id="0a5a8-111">The following table lists the four options.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0a5a8-112">Propósito</span><span class="sxs-lookup"><span data-stu-id="0a5a8-112">Purpose</span></span></th>
<th><span data-ttu-id="0a5a8-113">Códec</span><span class="sxs-lookup"><span data-stu-id="0a5a8-113">Codec</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0a5a8-114">Codificación de vídeo de uso general</span><span class="sxs-lookup"><span data-stu-id="0a5a8-114">General-purpose video encoding</span></span></td>
<td><span data-ttu-id="0a5a8-115"><a href="windowsmediavideo9encoder.md">Codificador de Windows Media Video 9</a></span><span class="sxs-lookup"><span data-stu-id="0a5a8-115"><a href="windowsmediavideo9encoder.md">Windows Media Video 9 Encoder</a></span></span><dl> <span data-ttu-id="0a5a8-116">Perfil Main</span><span class="sxs-lookup"><span data-stu-id="0a5a8-116">Main Profile</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a5a8-117">Vídeo o vídeo de alta definición de codificación que se ajusta al estándar de SMPTE del perfil avanzado de VC-1</span><span class="sxs-lookup"><span data-stu-id="0a5a8-117">Encoding high definition video or video that conforms to the VC-1 Advanced Profile SMPTE standard</span></span></td>
<td><span data-ttu-id="0a5a8-118"><a href="windowsmediavideo9encoder.md">Codificador de Windows Media Video 9</a></span><span class="sxs-lookup"><span data-stu-id="0a5a8-118"><a href="windowsmediavideo9encoder.md">Windows Media Video 9 Encoder</a></span></span><dl> <span data-ttu-id="0a5a8-119">Perfil avanzado</span><span class="sxs-lookup"><span data-stu-id="0a5a8-119">Advanced Profile</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a5a8-120">Convertir imágenes de mapa Dete en vídeo dinámico</span><span class="sxs-lookup"><span data-stu-id="0a5a8-120">Converting bitmapped images to dynamic video</span></span></td>
<td><span data-ttu-id="0a5a8-121"><a href="windowsmediavideo9encoder.md">Codificador de Windows Media Video 9</a></span><span class="sxs-lookup"><span data-stu-id="0a5a8-121"><a href="windowsmediavideo9encoder.md">Windows Media Video 9 Encoder</a></span></span><dl> <span data-ttu-id="0a5a8-122">Imagen</span><span class="sxs-lookup"><span data-stu-id="0a5a8-122">Image</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a5a8-123">Encoding: vídeo de aplicación (captura de pantalla) u otro vídeo muy estático</span><span class="sxs-lookup"><span data-stu-id="0a5a8-123">Encoding computer-application video (screen capture) or other highly static video</span></span></td>
<td><span data-ttu-id="0a5a8-124"><a href="windowsmediavideo9screenencoder.md"><strong>Codificador de pantalla de Windows Media Video 9</strong></a></span><span class="sxs-lookup"><span data-stu-id="0a5a8-124"><a href="windowsmediavideo9screenencoder.md"><strong>Windows Media Video 9 Screen Encoder</strong></a></span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="0a5a8-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0a5a8-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a5a8-126">Trabajar con vídeo</span><span class="sxs-lookup"><span data-stu-id="0a5a8-126">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 



