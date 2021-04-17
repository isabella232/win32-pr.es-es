---
description: Usar el códec y los objetos DSP
ms.assetid: ec571d31-6542-421a-8027-d4c61ce00035
title: Usar el códec y los objetos DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a88670298bfc16ca1dc5053cabeb4f4e631c5c47
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105717369"
---
# <a name="using-the-codec-and-dsp-objects"></a><span data-ttu-id="ac802-103">Usar el códec y los objetos DSP</span><span class="sxs-lookup"><span data-stu-id="ac802-103">Using the Codec and DSP Objects</span></span>

<span data-ttu-id="ac802-104">Hay varias maneras de usar los códecs de Windows Media Audio y vídeo y los DSP para codificar, descodificar o transformar el contenido multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="ac802-104">There are several ways to use the Windows Media Audio and Video codecs and DSPs to encode, decode, or transform your digital media content.</span></span> <span data-ttu-id="ac802-105">El códec de Windows Media Audio y vídeo y la API de DSP están diseñados para los usuarios que necesitan configurar los objetos de códec y DSP manualmente o usarlos fuera del contexto de uno de los SDK de Windows Media, como el SDK de Windows Media Format o el SDK de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="ac802-105">The Windows Media Audio and Video Codec and DSP API is intended for those users who need to configure codec and DSP objects manually or use them outside of the context one of the Windows Media SDKs, such as the Windows Media Format SDK or Media Foundation SDK.</span></span>

<span data-ttu-id="ac802-106">Los creadores de contenido y los usuarios finales pueden utilizar una variedad de herramientas y aplicaciones para codificar el contenido en Windows Media Audio o Windows Media Video flujos.</span><span class="sxs-lookup"><span data-stu-id="ac802-106">Content creators and end users can use a variety of tools and applications to encode content in Windows Media Audio or Windows Media Video streams.</span></span> <span data-ttu-id="ac802-107">Windows Media Encoder, por ejemplo, se ha diseñado específicamente para facilitar el proceso de codificación.</span><span class="sxs-lookup"><span data-stu-id="ac802-107">Windows Media Encoder, for example, is specifically designed to make the encoding process easy.</span></span> <span data-ttu-id="ac802-108">Del mismo modo, Windows Media Player está especialmente diseñado para funcionar bien con los datos multimedia digitales codificados en formatos de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ac802-108">Likewise, Windows Media Player is specially designed to work well with digital media data that is encoded in Windows Media formats.</span></span> <span data-ttu-id="ac802-109">Para muchas aplicaciones, el uso del SDK de Windows Media Encoder o del SDK de Windows Media Player es todo lo que se necesita.</span><span class="sxs-lookup"><span data-stu-id="ac802-109">For many applications, using the Windows Media Encoder SDK or the Windows Media Player SDK is all that is needed.</span></span> <span data-ttu-id="ac802-110">En concreto, estas dos tecnologías son adecuadas para escenarios que se asemejan a la funcionalidad de las herramientas que automatizan.</span><span class="sxs-lookup"><span data-stu-id="ac802-110">In particular, these two technologies are good for scenarios that resemble the functionality of the tools they automate.</span></span>

<span data-ttu-id="ac802-111">Si necesita un mayor control sobre el proceso de codificación o descodificación, pero tiene previsto usar Advanced Systems Format (ASF) como contenedor para los datos multimedia, el SDK de Windows Media Format podría ser una buena opción.</span><span class="sxs-lookup"><span data-stu-id="ac802-111">If you need greater control over the encoding or decoding process, but you still intend to use the Advanced Systems Format (ASF) as a container for your media data, the Windows Media Format SDK might be a good choice.</span></span> <span data-ttu-id="ac802-112">Los objetos del SDK de Windows Media Format proporcionan un marco de trabajo flexible para crear archivos ASF y proporcionan compatibilidad integrada con los códecs de Windows Media Audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="ac802-112">The objects of the Windows Media Format SDK provide a flexible framework for creating ASF files, and provide built-in support for the Windows Media Audio and Video codecs.</span></span>

<span data-ttu-id="ac802-113">El SDK de Media Foundation, que es nuevo en Windows Vista, simplifica considerablemente la codificación y la descodificación proporcionando una canalización multimedia personalizable.</span><span class="sxs-lookup"><span data-stu-id="ac802-113">The Media Foundation SDK, which is new for Windows Vista, greatly simplifies encoding and decoding by providing a customizable media pipeline.</span></span> <span data-ttu-id="ac802-114">Puede establecer las propiedades de los medios de entrada y salida, y el cargador de topología de Media Foundation configurará automáticamente los códecs y los DSP necesarios.</span><span class="sxs-lookup"><span data-stu-id="ac802-114">You can set input and output media properties and the Media Foundation topology loader will configure the necessary codecs and DSPs for you.</span></span>

<span data-ttu-id="ac802-115">La razón principal para usar los objetos de códec directamente es usar los códecs de Windows Media Audio y vídeo fuera del contenedor ASF.</span><span class="sxs-lookup"><span data-stu-id="ac802-115">The primary reason for using the codec objects directly is to use the Windows Media Audio and Video codecs outside of the ASF container.</span></span> <span data-ttu-id="ac802-116">El uso de los objetos codec y DSP también proporciona un nivel de control que no está disponible con ninguna de las tecnologías más abstractas.</span><span class="sxs-lookup"><span data-stu-id="ac802-116">Using the codec and DSP objects also provides a level of control that is unavailable using any of the more abstracted technologies.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac802-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ac802-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac802-118">Códecs de Windows Media</span><span class="sxs-lookup"><span data-stu-id="ac802-118">Windows Media Codecs</span></span>](windows-media-codecs.md)
</dt> </dl>

 

 



