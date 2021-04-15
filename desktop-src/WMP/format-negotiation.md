---
title: Negociación de formato
description: Negociación de formato
ms.assetid: 7847d4e3-1250-4c35-88e1-52d61bf1553f
keywords:
- Complementos de Windows Media Player, negociación de formato
- complementos, negociación de formato
- Complementos de procesamiento de señal digital, negociación de formato
- Complementos DSP, negociación de formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc805b18d3e2be081e4f85bcc5ed42aded06853
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695424"
---
# <a name="format-negotiation"></a><span data-ttu-id="dbb2d-107">Negociación de formato</span><span class="sxs-lookup"><span data-stu-id="dbb2d-107">Format Negotiation</span></span>

<span data-ttu-id="dbb2d-108">En el caso de Windows Media Player y un complemento DSP para compartir datos, ambos programas deben estar de acuerdo en el formato de los datos que están procesando.</span><span class="sxs-lookup"><span data-stu-id="dbb2d-108">For Windows Media Player and a DSP plug-in to share data, both programs must agree on the format of the data they are processing.</span></span> <span data-ttu-id="dbb2d-109">El complemento DSP implementa los métodos a los que llama el reproductor para determinar los formatos que admite el complemento.</span><span class="sxs-lookup"><span data-stu-id="dbb2d-109">The DSP plug-in implements methods that the Player calls to determine which formats the plug-in supports.</span></span> <span data-ttu-id="dbb2d-110">El complemento también implementa los métodos a los que llama el reproductor para establecer el formato actual.</span><span class="sxs-lookup"><span data-stu-id="dbb2d-110">The plug-in also implements methods that the Player calls to set the current format.</span></span>

<span data-ttu-id="dbb2d-111">Si el complemento está actuando como un objeto multimedia DirextX (DMO), Windows Media Player detecta y establece los formatos multimedia llamando a los métodos de la interfaz **IMediaObject** .</span><span class="sxs-lookup"><span data-stu-id="dbb2d-111">If the plug-in is acting as a DirextX Media Object (DMO), Windows Media Player discovers and sets media formats by calling methods of the **IMediaObject** interface.</span></span> <span data-ttu-id="dbb2d-112">Por ejemplo, el reproductor llama a **IMediaObject:: GetInputType** del complemento varias veces para obtener una lista de todos los formatos de entrada admitidos por el complemento.</span><span class="sxs-lookup"><span data-stu-id="dbb2d-112">For example, the Player calls the plug-in's **IMediaObject::GetInputType** repeatedly to get a list of all input formats supported by the plug-in.</span></span> <span data-ttu-id="dbb2d-113">Los complementos de DMO usan la estructura de **\_ \_ tipo de medio DMO** para organizar la información que especifica un formato de medios.</span><span class="sxs-lookup"><span data-stu-id="dbb2d-113">DMO plug-ins use the **DMO\_MEDIA\_TYPE** structure to organize the information that specifies a media format.</span></span> <span data-ttu-id="dbb2d-114">Para obtener más información acerca de cómo los complementos de DMO y el reproductor negocian el formato, vea [acerca de IMediaObject](about-imediaobject.md).</span><span class="sxs-lookup"><span data-stu-id="dbb2d-114">For more information about how DMO plug-ins and the Player negotiate format, see [About IMediaObject](about-imediaobject.md).</span></span>

<span data-ttu-id="dbb2d-115">Si el complemento actúa como una transformación de Media Foundation (MFT), Windows Media Player detecta y establece los formatos multimedia llamando a los métodos de la interfaz **IMFTransform** .</span><span class="sxs-lookup"><span data-stu-id="dbb2d-115">If the plug-in is acting as a Media Foundation Transform (MFT), Windows Media Player discovers and sets media formats by calling methods of the **IMFTransform** interface.</span></span> <span data-ttu-id="dbb2d-116">Por ejemplo, el reproductor llama a **IMFTransform:: GetInputAvailableType** del complemento varias veces para obtener una lista de todos los formatos de entrada admitidos por el complemento.</span><span class="sxs-lookup"><span data-stu-id="dbb2d-116">For example, the Player calls the plug-in's **IMFTransform::GetInputAvailableType** repeatedly to get a list of all input formats supported by the plug-in.</span></span> <span data-ttu-id="dbb2d-117">Los complementos de MFT y el reproductor usan la interfaz **IMFMediaType** para organizar e intercambiar información de formato.</span><span class="sxs-lookup"><span data-stu-id="dbb2d-117">MFT plug-ins and the Player use the **IMFMediaType** interface to organize and exchange format information.</span></span>

<span data-ttu-id="dbb2d-118">Windows Media Player usará un complemento de DSP de audio solo si el complemento admite la misma profundidad de bits que el audio digital que se reproduce.</span><span class="sxs-lookup"><span data-stu-id="dbb2d-118">Windows Media Player will use an audio DSP plug-in only if the plug-in supports the same bit depth as the digital audio being played.</span></span> <span data-ttu-id="dbb2d-119">Por ejemplo, si el audio digital es de 20 bits, el complemento debe estar escrito para procesar audio de 20 bits.</span><span class="sxs-lookup"><span data-stu-id="dbb2d-119">For instance, if the digital audio is 20-bit, the plug-in must be written to process 20-bit audio.</span></span> <span data-ttu-id="dbb2d-120">En el caso de audio de CD, los complementos DSP deben admitir el procesamiento de 20 bits.</span><span class="sxs-lookup"><span data-stu-id="dbb2d-120">For CD audio, DSP plug-ins must support 20-bit processing.</span></span>

<span data-ttu-id="dbb2d-121">Durante la negociación de formato del contenido de varios canales en un equipo configurado para su uso con altavoces estéreo, Windows Media Player primero intenta conectarse a un complemento de DSP de audio con el formato de entrada y salida existente mediante una llamada a **IMediaObject:: SetInputType** y **IMediaObject:: SetOutputType**.</span><span class="sxs-lookup"><span data-stu-id="dbb2d-121">During format negotiation of multi-channel content on a computer configured for use with stereo speakers, Windows Media Player first attempts to connect to an audio DSP plug-in using the existing input and output format by calling **IMediaObject::SetInputType** and **IMediaObject::SetOutputType**.</span></span> <span data-ttu-id="dbb2d-122">Una vez que se produce esta negociación inicial, el reproductor enumera los formatos que admite el complemento e intenta negociar la mejor combinación de formato para el reproductor y el complemento.</span><span class="sxs-lookup"><span data-stu-id="dbb2d-122">Once this initial negotiation occurs, the Player then enumerates the formats the plug-in supports and attempts to negotiate the best format combination for the Player and the plug-in.</span></span> <span data-ttu-id="dbb2d-123">Si el complemento acepta audio estéreo (definido por una estructura **WAVEFORMATEX** ) como formato de entrada durante la negociación inicial y, a continuación, acepta únicamente audio de canal múltiple (definido por una estructura **WAVEFORMATEXTENSIBLE** ), el reproductor proporcionará audio de varios canales como formato de entrada al complemento.</span><span class="sxs-lookup"><span data-stu-id="dbb2d-123">If the plug-in accepts stereo audio (defined by a **WAVEFORMATEX** structure) as the input format during the initial negotiation, and then subsequently accepts only multi-channel audio (defined by a **WAVEFORMATEXTENSIBLE** structure), the Player will provide multi-channel audio as the input format to the plug-in.</span></span> <span data-ttu-id="dbb2d-124">Este comportamiento durante la negociación de formato está disponible para su uso en el sistema operativo Microsoft Windows XP.</span><span class="sxs-lookup"><span data-stu-id="dbb2d-124">This behavior during format negotiation is available for use in the Microsoft Windows XP operating system.</span></span> <span data-ttu-id="dbb2d-125">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="dbb2d-125">It may be altered or unavailable in subsequent versions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dbb2d-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dbb2d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dbb2d-127">**Introducción al desarrollador de complementos de DSP**</span><span class="sxs-lookup"><span data-stu-id="dbb2d-127">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




