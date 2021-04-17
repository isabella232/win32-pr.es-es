---
description: Configuración del descodificador para Windows Media Center Edition
ms.assetid: 019b063f-f215-44d8-a916-3125bee6af93
title: Configuración del descodificador para Windows Media Center Edition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f66b5107fa0316f6ce2547e1f5f066165ed598
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105660007"
---
# <a name="decoder-settings-for-windows-media-center-edition"></a><span data-ttu-id="c709b-103">Configuración del descodificador para Windows Media Center Edition</span><span class="sxs-lookup"><span data-stu-id="c709b-103">Decoder Settings for Windows Media Center Edition</span></span>

<span data-ttu-id="c709b-104">Windows XP Media Center Edition 2005 y versiones posteriores usan la interfaz [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) para configurar el filtro de descodificador de audio para la reproducción de televisión y DVD.</span><span class="sxs-lookup"><span data-stu-id="c709b-104">Windows XP Media Center Edition 2005 and later uses the [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) interface to configure the audio decoder filter for television and DVD playback.</span></span> <span data-ttu-id="c709b-105">Se admiten las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="c709b-105">The following properties are supported.</span></span>



| <span data-ttu-id="c709b-106">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="c709b-106">Property GUID</span></span>                   | <span data-ttu-id="c709b-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="c709b-107">Description</span></span>                                      |
|---------------------------------|--------------------------------------------------|
| <span data-ttu-id="c709b-108">\_formato de \_ salida de audio CODECAPI \_</span><span class="sxs-lookup"><span data-stu-id="c709b-108">CODECAPI\_AUDIO\_OUTPUT\_FORMAT</span></span> | <span data-ttu-id="c709b-109">Configura el formato de salida de audio.</span><span class="sxs-lookup"><span data-stu-id="c709b-109">Configures the audio output format.</span></span> <span data-ttu-id="c709b-110">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="c709b-110">See Remarks.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c709b-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c709b-111">Remarks</span></span>

<span data-ttu-id="c709b-112">El valor de la \_ propiedad CODECAPI audio \_ Output \_ Format es una representación de cadena de un GUID, que se almacena como un valor **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="c709b-112">The value of the CODECAPI\_AUDIO\_OUTPUT\_FORMAT property is a string representation of a GUID, stored as a **BSTR** value.</span></span> <span data-ttu-id="c709b-113">Se definen los siguientes GUID.</span><span class="sxs-lookup"><span data-stu-id="c709b-113">The following GUIDs are defined.</span></span>



| <span data-ttu-id="c709b-114">GUID</span><span class="sxs-lookup"><span data-stu-id="c709b-114">GUID</span></span>                                                        | <span data-ttu-id="c709b-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="c709b-115">Description</span></span>                                                                                                                                                                                                    |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c709b-116">\_formato de salida de audio CODECAPI \_ \_ \_ PCM \_ estéreo \_ MATRIXENCODED</span><span class="sxs-lookup"><span data-stu-id="c709b-116">CODECAPI\_AUDIO\_OUTPUT\_FORMAT\_PCM\_STEREO\_MATRIXENCODED</span></span> | <span data-ttu-id="c709b-117">El filtro de audio de software debe realizar la descodificación de software y generar una secuencia de audio estéreo con la matriz de audio multicanal codificada en los dos canales.</span><span class="sxs-lookup"><span data-stu-id="c709b-117">The software audio filter should perform software decoding and output a stereo audio stream, with the multichannel audio matrix encoded to the two channels.</span></span>                                                   |
| <span data-ttu-id="c709b-118">\_formato de salida de audio CODECAPI \_ \_ \_ PCM \_ Stereo</span><span class="sxs-lookup"><span data-stu-id="c709b-118">CODECAPI\_AUDIO\_OUTPUT\_FORMAT\_PCM\_STEREO</span></span>                | <span data-ttu-id="c709b-119">El filtro de audio de software debe realizar la descodificación de software y generar una secuencia de audio estéreo.</span><span class="sxs-lookup"><span data-stu-id="c709b-119">The software audio filter should perform software decoding and output a stereo audio stream.</span></span>                                                                                                                   |
| <span data-ttu-id="c709b-120">\_formato de salida de audio CODECAPI \_ \_ \_ \_ PCM SPDIF</span><span class="sxs-lookup"><span data-stu-id="c709b-120">CODECAPI\_AUDIO\_OUTPUT\_FORMAT\_SPDIF\_PCM</span></span>                 | <span data-ttu-id="c709b-121">El filtro de audio de software debe realizar la descodificación de audio de software, aunque la salida física del equipo puede ser una interfaz digital, como S/PDIF.</span><span class="sxs-lookup"><span data-stu-id="c709b-121">The software audio filter should perform software audio decoding, even though the physical output from the PC may be a digital interface, such as S/PDIF.</span></span>                                                      |
| <span data-ttu-id="c709b-122">\_formato de salida de audio CODECAPI \_ \_ \_ SPDIF \_ fragmentada</span><span class="sxs-lookup"><span data-stu-id="c709b-122">CODECAPI\_AUDIO\_OUTPUT\_FORMAT\_SPDIF\_BITSTREAM</span></span>           | <span data-ttu-id="c709b-123">El filtro de audio de software no debe realizar la descodificación de audio de software, pero debe pasar el fragmentada de audio digital sin procesar para el procesamiento externo por un dispositivo conectado a un vínculo de audio digital, como S/PDIF.</span><span class="sxs-lookup"><span data-stu-id="c709b-123">The software audio filter should not perform software audio decoding, but should pass the raw digital audio bitstream for external processing by a device connected with a digital audio link, such as S/PDIF.</span></span> |
| <span data-ttu-id="c709b-124">formato de salida de audio CODECAPI- \_ \_ \_ \_ \_ auriculares PCM</span><span class="sxs-lookup"><span data-stu-id="c709b-124">CODECAPI\_AUDIO\_OUTPUT\_FORMAT\_PCM\_HEADPHONES</span></span>            | <span data-ttu-id="c709b-125">El filtro de audio de software debe realizar la descodificación de audio de software y debe aplicar el procesamiento de propiedad para optimizar los auriculares.</span><span class="sxs-lookup"><span data-stu-id="c709b-125">The software audio filter should perform software audio decoding and should apply proprietary processing to optimize for headphones.</span></span> <span data-ttu-id="c709b-126">La compatibilidad con esta configuración es opcional.</span><span class="sxs-lookup"><span data-stu-id="c709b-126">Support for this setting is optional.</span></span>                                     |



 

> [!Note]  
> <span data-ttu-id="c709b-127">La interfaz **ICodecAPI** almacena las propiedades de códec como pares clave-valor, donde la clave es un GUID y el valor es un tipo **Variant** .</span><span class="sxs-lookup"><span data-stu-id="c709b-127">The **ICodecAPI** interface stores codec properties as key/value pairs, where the key is a GUID and the value is a **VARIANT** type.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c709b-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c709b-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c709b-129">Desarrollo del codificador y descodificador</span><span class="sxs-lookup"><span data-stu-id="c709b-129">Encoder and Decoder Development</span></span>](encoder-and-decoder-development.md)
</dt> </dl>

 

 



