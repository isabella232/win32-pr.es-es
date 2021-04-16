---
description: ¿Por qué un descodificador no acepta el formato de entrada que configuro?
ms.assetid: 19aa5677-bc3f-41d7-ad64-7c75021d907b
title: ¿Por qué un descodificador no acepta el formato de entrada que configuro?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32ae4506fb6ed940bf0b4fffcf82ab78562872d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696857"
---
# <a name="why-does-a-decoder-not-accept-the-input-format-that-i-set"></a><span data-ttu-id="df165-103">¿Por qué un descodificador no acepta el formato de entrada que configuro?</span><span class="sxs-lookup"><span data-stu-id="df165-103">Why does a decoder not accept the input format that I set?</span></span>

<span data-ttu-id="df165-104">Hay muchas razones por las que un descodificador podría rechazar un formato.</span><span class="sxs-lookup"><span data-stu-id="df165-104">There are many reasons why a decoder might reject a format.</span></span> <span data-ttu-id="df165-105">Los datos de formato extendido más comunes faltan o son incorrectos.</span><span class="sxs-lookup"><span data-stu-id="df165-105">The most common is missing or incorrect extended format data.</span></span> <span data-ttu-id="df165-106">Los datos de formato extendido son información específica del códec que se anexa a la estructura que describe el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="df165-106">The extended format data is codec-specific information that is appended to the structure describing the media type.</span></span>

<span data-ttu-id="df165-107">Cuando se enumera un tipo de salida mediante un objeto de codificador, el miembro **pbFormat** de la estructura de [**\_ \_ tipo de medio DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) apuntará a una estructura **WAVEFORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="df165-107">When you enumerate an output type using an encoder object, the **pbFormat** member of the [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure will point to a **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="df165-108">Esta estructura tiene datos de formato extendido anexados y el tamaño de los datos se almacena en el miembro **WAVEFORMATEX. cbSize** .</span><span class="sxs-lookup"><span data-stu-id="df165-108">This structure has extended format data appended to it, and the size of that data is stored in the **WAVEFORMATEX.cbSize** member.</span></span> <span data-ttu-id="df165-109">Independientemente del contenedor utilizado para almacenar los datos comprimidos, debe conservar la estructura **WAVEFORMATEX** y usarlo en el tipo de entrada para el descodificador.</span><span class="sxs-lookup"><span data-stu-id="df165-109">Regardless of the container used to store the compressed data, you must persist the **WAVEFORMATEX** structure and use it in the input type for the decoder.</span></span> <span data-ttu-id="df165-110">Sin los datos de formato extendido, el descodificador no puede descomprimir el contenido.</span><span class="sxs-lookup"><span data-stu-id="df165-110">Without the extended format data, the decoder cannot decompress the content.</span></span>

<span data-ttu-id="df165-111">En el caso de los formatos de vídeo, debe recuperar manualmente los datos de formato extendido y anexarlos a la estructura **VIDEOINFOHEADER** .</span><span class="sxs-lookup"><span data-stu-id="df165-111">For video formats, you must manually retrieve the extended format data and append it to the **VIDEOINFOHEADER** structure.</span></span> <span data-ttu-id="df165-112">Para obtener más información, consulte [uso de datos privados de códecs de vídeo](usingvideocodecprivatedata.md).</span><span class="sxs-lookup"><span data-stu-id="df165-112">For more information, see [Using Video Codec Private Data](usingvideocodecprivatedata.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="df165-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="df165-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df165-114">Preguntas más frecuentes</span><span class="sxs-lookup"><span data-stu-id="df165-114">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 
