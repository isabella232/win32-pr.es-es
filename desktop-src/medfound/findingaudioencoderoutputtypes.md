---
description: Búsqueda de tipos de salida del codificador de audio
ms.assetid: cd47d45b-ea47-4dec-867e-d51145d7f084
title: Búsqueda de tipos de salida del codificador de audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5389274cca1178ebc0ae03e21f7a804f73a5db48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705406"
---
# <a name="finding-audio-encoder-output-types-microsoft-media-foundation"></a><span data-ttu-id="6de07-103">Búsqueda de tipos de salida del codificador de audio (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="6de07-103">Finding Audio Encoder Output Types (Microsoft Media Foundation)</span></span>

<span data-ttu-id="6de07-104">Dado que debe usar un formato de salida de codificador de audio que sea enumerado por el codificador de audio, debe tener una forma de encontrar el formato más adecuado para sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="6de07-104">Because you must use an audio encoder output format that is enumerated by the audio encoder, you need to have a way of finding the format that is most suited to your needs.</span></span> <span data-ttu-id="6de07-105">El número de canales, bits por muestra y la velocidad de muestra de la salida que elija debe coincidir con los valores del contenido que comprime.</span><span class="sxs-lookup"><span data-stu-id="6de07-105">The number of channels, bits per sample, and sample rate of the output that you choose must match the values for the content that you compress.</span></span> <span data-ttu-id="6de07-106">Sin embargo, el codificador puede admitir varios tipos dentro de estas restricciones.</span><span class="sxs-lookup"><span data-stu-id="6de07-106">However, the encoder may support several types within these constraints.</span></span>

<span data-ttu-id="6de07-107">El factor decisivo para elegir un tipo es la velocidad de bits de la secuencia codificada; quiere buscar un tipo de medio que coincida con la entrada y que tenga una velocidad de bits lo más cercana posible a un valor de destino.</span><span class="sxs-lookup"><span data-stu-id="6de07-107">The deciding factor for choosing a type is the bit rate of the encoded stream; you want to find a media type that matches your input and has a bit rate that is as close as possible to a target value.</span></span> <span data-ttu-id="6de07-108">Si está enumerando los tipos de salida VBR de un paso, es el valor de calidad que decidirá el tipo que utiliza.</span><span class="sxs-lookup"><span data-stu-id="6de07-108">If you are enumerating one-pass VBR output types, it is the quality value that will decide the type you use.</span></span> <span data-ttu-id="6de07-109">Para obtener más información sobre los valores de calidad de los tipos de salida enumerados, consulte [enumeración de tipos de audio para modos de codificación específicos](enumeratingaudiotypesforspecificencodingmodes.md).</span><span class="sxs-lookup"><span data-stu-id="6de07-109">For more information about quality values in enumerated output types, see [Enumerating Audio Types for Specific Encoding Modes](enumeratingaudiotypesforspecificencodingmodes.md).</span></span>

> [!Note]  
>    <span data-ttu-id="6de07-110">El codificador de audio enumera algunos tipos que son duplicados de otros tipos de prácticamente todas formas.</span><span class="sxs-lookup"><span data-stu-id="6de07-110">The audio encoder enumerates some types that are duplicates of other types in almost all ways.</span></span> <span data-ttu-id="6de07-111">Estos duplicados existen para formatos en los que el número de paquetes por segundo no cumple los requisitos de almacenamiento en archivos ASF cuando se sincronizan con vídeo.</span><span class="sxs-lookup"><span data-stu-id="6de07-111">These duplicates exist for formats where the number of packets per second does not meet the requirements for storage in ASF files when synchronized with video.</span></span> <span data-ttu-id="6de07-112">El audio sincronizado con vídeo en un archivo ASF debe tener 3 o más paquetes por segundo para velocidades de bits inferiores a 32000 y 5 o más paquetes por segundo para velocidades de bits iguales o superiores a 32000.</span><span class="sxs-lookup"><span data-stu-id="6de07-112">Audio synchronized with video in an ASF file must have 3 or more packets per second for bit rates less than 32000, and 5 or more packets per second for bit rates greater than or equal to 32000.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6de07-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6de07-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6de07-114">Configuración de la codificación de audio</span><span class="sxs-lookup"><span data-stu-id="6de07-114">Configuring Audio Encoding</span></span>](configuringaudioencoding.md)
</dt> <dt>

[<span data-ttu-id="6de07-115">Enumeración de los tipos de audio para los modos de codificación específicos</span><span class="sxs-lookup"><span data-stu-id="6de07-115">Enumerating Audio Types for Specific Encoding Modes</span></span>](enumeratingaudiotypesforspecificencodingmodes.md)
</dt> </dl>

 

 



