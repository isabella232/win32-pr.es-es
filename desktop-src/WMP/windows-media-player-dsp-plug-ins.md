---
title: Complementos DSP de Windows Media Player
description: Complementos DSP de Windows Media Player
ms.assetid: 1c7202c4-ca66-491d-9a5f-26032cad1dcc
keywords:
- Media Player de Windows, Complementos
- Media Player de Windows, Complementos DSP
- Complementos de Windows Media Player, procesamiento de señal digital (DSP)
- complementos, procesamiento de señal digital (DSP)
- Complementos de procesamiento de señal digital, acerca de
- Complementos DSP, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 755088bce89530350997d2f543e30872f630e882
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486886"
---
# <a name="windows-media-player-dsp-plug-ins"></a><span data-ttu-id="7f0c4-109">Complementos DSP de Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="7f0c4-109">Windows Media Player DSP Plug-ins</span></span>

<span data-ttu-id="7f0c4-110">Microsoft Windows Media Player proporciona una arquitectura que permite al usuario instalar y activar programas de complementos que agregan funcionalidad de procesamiento de señal digital (DSP).</span><span class="sxs-lookup"><span data-stu-id="7f0c4-110">Microsoft Windows Media Player provides an architecture that enables the user to install and activate plug-in programs that add digital signal processing (DSP) functionality.</span></span> <span data-ttu-id="7f0c4-111">Un complemento de DSP es un objeto Microsoft DirectX media (DMO) o una transformación de Media Foundation (MFT) que se conecta al reproductor mediante interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="7f0c4-111">A DSP plug-in is a Microsoft DirectX Media Object (DMO) or a Media Foundation Transform (MFT) that connects to the Player by using COM interfaces.</span></span> <span data-ttu-id="7f0c4-112">Un complemento DSP típico puede ser un ecualizador de audio o un control de matiz de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7f0c4-112">A typical DSP plug-in might be an audio equalizer or a video tint control.</span></span> <span data-ttu-id="7f0c4-113">Esta sección del SDK proporciona la información de programación que necesita para crear su propio complemento DSP.</span><span class="sxs-lookup"><span data-stu-id="7f0c4-113">This section of the SDK provides the programming information you need to create your own DSP plug-in.</span></span>

<span data-ttu-id="7f0c4-114">La documentación del complemento de DSP está dividida en las tres secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="7f0c4-114">The DSP plug-in documentation is divided into the following three sections.</span></span>



| <span data-ttu-id="7f0c4-115">Sección</span><span class="sxs-lookup"><span data-stu-id="7f0c4-115">Section</span></span>                                                                      | <span data-ttu-id="7f0c4-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="7f0c4-116">Description</span></span>                                                                                                                                     |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7f0c4-117">Acerca de los complementos DSP</span><span class="sxs-lookup"><span data-stu-id="7f0c4-117">About DSP Plug-ins</span></span>](about-dsp-plug-ins.md)                                 | <span data-ttu-id="7f0c4-118">Proporciona información general sobre la arquitectura utilizada para los complementos DSP. Lea esta sección para obtener información sobre los conceptos generales implicados en esta tecnología.</span><span class="sxs-lookup"><span data-stu-id="7f0c4-118">Provides an overview of the architecture used for DSP plug-ins. Read this section to learn the general concepts involved with this technology.</span></span>  |
| [<span data-ttu-id="7f0c4-119">Guía de programación de complementos DSP</span><span class="sxs-lookup"><span data-stu-id="7f0c4-119">DSP Plug-ins Programming Guide</span></span>](dsp-plug-ins-programming-guide.md)         | <span data-ttu-id="7f0c4-120">Explica lo que debe hacer para crear un complemento DSP.</span><span class="sxs-lookup"><span data-stu-id="7f0c4-120">Explains what you need to do to create a DSP plug-in.</span></span> <span data-ttu-id="7f0c4-121">Esta sección contiene código de ejemplo y procedimientos paso a paso.</span><span class="sxs-lookup"><span data-stu-id="7f0c4-121">This section contains example code and step-by-step procedures.</span></span>                           |
| [<span data-ttu-id="7f0c4-122">Referencia de programación de complementos DSP</span><span class="sxs-lookup"><span data-stu-id="7f0c4-122">DSP Plug-ins Programming Reference</span></span>](dsp-plug-ins-programming-reference.md) | <span data-ttu-id="7f0c4-123">Proporciona una referencia detallada de las interfaces, los métodos y los tipos enumerados COM admitidos por el SDK de Windows Media Player para los complementos de DSP.</span><span class="sxs-lookup"><span data-stu-id="7f0c4-123">Provides a detailed reference for the COM interfaces, methods, and enumerated types supported by the Windows Media Player SDK for DSP plug-ins.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7f0c4-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7f0c4-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f0c4-125">**Complementos de Media Player de Windows**</span><span class="sxs-lookup"><span data-stu-id="7f0c4-125">**Windows Media Player Plug-ins**</span></span>](windows-media-player-plug-ins.md)
</dt> </dl>

 

 




