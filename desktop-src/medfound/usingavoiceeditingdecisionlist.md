---
description: Usar una lista de decisiones de edición para la codificación de voz
ms.assetid: a3d88483-acc9-47cf-8735-f17bd3b4ad57
title: Usar una lista de decisiones de edición para la codificación de voz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 970cc40bc5749b9edc1017546020fa3806a9730b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666869"
---
# <a name="using-an-editing-decision-list-for-encoding-voice"></a><span data-ttu-id="a0a8b-103">Usar una lista de decisiones de edición para la codificación de voz</span><span class="sxs-lookup"><span data-stu-id="a0a8b-103">Using an Editing Decision List for Encoding Voice</span></span>

<span data-ttu-id="a0a8b-104">Una lista de decisiones de edición (EDL) es un dato dado a un códec que proporciona información sobre cómo se deben codificar determinadas partes del contenido.</span><span class="sxs-lookup"><span data-stu-id="a0a8b-104">An editing decision list (EDL), is data given to a codec that provides information about how specific portions of content should be encoded.</span></span> <span data-ttu-id="a0a8b-105">El códec de voz de Windows Media Audio 9 admite una EDL simple en la que puede especificar las partes de contenido que contienen música.</span><span class="sxs-lookup"><span data-stu-id="a0a8b-105">The Windows Media Audio 9 Voice codec supports a simple EDL in which you can specify the portions of content that contain music.</span></span> <span data-ttu-id="a0a8b-106">De forma predeterminada, el códec detecta los pasajes de música en sí cuando se configura para codificar contenido mixto.</span><span class="sxs-lookup"><span data-stu-id="a0a8b-106">By default, the codec detects passages of music itself when configured to encode mixed content.</span></span> <span data-ttu-id="a0a8b-107">Solo debe usar una EDL si el códec no detecta los tipos de contenido correctamente.</span><span class="sxs-lookup"><span data-stu-id="a0a8b-107">You should use an EDL only if the codec is not detecting the content types correctly.</span></span>

<span data-ttu-id="a0a8b-108">Para usar una EDL, el codificador de voz debe estar establecido para codificar contenido mixto.</span><span class="sxs-lookup"><span data-stu-id="a0a8b-108">To use an EDL, the voice encoder must be set to encode mixed content.</span></span> <span data-ttu-id="a0a8b-109">Configure el modo del códec de voz en "Mixed" estableciendo la propiedad [MFPKEY \_ WMAVOICE \_ enc \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) en 2.</span><span class="sxs-lookup"><span data-stu-id="a0a8b-109">Configure the mode of the voice codec to "mixed" by setting the [MFPKEY\_WMAVOICE\_ENC\_MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) property to 2.</span></span> <span data-ttu-id="a0a8b-110">Establezca la EDL mediante la propiedad [MFPKEY \_ WMAVOICE \_ enc \_ EDL](mfpkey-wmavoice-enc-edlproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="a0a8b-110">Set the EDL using the [MFPKEY\_WMAVOICE\_ENC\_EDL](mfpkey-wmavoice-enc-edlproperty.md) property.</span></span> <span data-ttu-id="a0a8b-111">El valor de esta propiedad es una cadena que contiene una lista delimitada por comas de los intervalos de tiempo en el contenido que se debe codificar como música.</span><span class="sxs-lookup"><span data-stu-id="a0a8b-111">The value of this property is a string containing a comma-delimited list of the time ranges in the content that should be encoded as music.</span></span> <span data-ttu-id="a0a8b-112">El primer elemento de la lista es la versión de la EDL, que es siempre 1.</span><span class="sxs-lookup"><span data-stu-id="a0a8b-112">The first item in the list is the version of the EDL, which is always 1.</span></span> <span data-ttu-id="a0a8b-113">El segundo elemento es el número de secciones de música descritas en la lista.</span><span class="sxs-lookup"><span data-stu-id="a0a8b-113">The second item is the number of music sections described in the list.</span></span> <span data-ttu-id="a0a8b-114">Después del segundo elemento hay un número de pares de valores igual al segundo elemento; cada par de valores describe el punto inicial y final de un pasaje de música en el contenido, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="a0a8b-114">Following the second item are a number of pairs of values equal to the second item; each pair of values describes the starting and ending point of a music passage in the content, in milliseconds.</span></span>

<span data-ttu-id="a0a8b-115">Por ejemplo, la cadena de EDL "1, 4, 1000, 2000, 5000, 6000, 9000, 10000, 13000, 14000" especifica cuatro pasajes musicales, cada uno de los cuales tiene una segunda duración.</span><span class="sxs-lookup"><span data-stu-id="a0a8b-115">For example, the EDL string "1, 4, 1000, 2000, 5000, 6000, 9000, 10000, 13000, 14000" specifies four musical passages, each of which is one second long.</span></span> <span data-ttu-id="a0a8b-116">Si la información de la cadena de EDL no es válida, se omite.</span><span class="sxs-lookup"><span data-stu-id="a0a8b-116">If the information in the EDL string is invalid, it is ignored.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0a8b-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a0a8b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0a8b-118">Usar el códec de voz de Windows Media Audio 9</span><span class="sxs-lookup"><span data-stu-id="a0a8b-118">Using the Windows Media Audio 9 Voice Codec</span></span>](usingthewindowsmediaaudio9voicecodec.md)
</dt> <dt>

[<span data-ttu-id="a0a8b-119">Trabajar con audio</span><span class="sxs-lookup"><span data-stu-id="a0a8b-119">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 



