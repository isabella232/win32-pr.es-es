---
title: Complementos de Media Player de Windows
description: Complementos de Media Player de Windows
ms.assetid: 6265084b-e1ff-455b-aca8-dc008d94ed43
keywords:
- Media Player de Windows, Complementos
- Complementos de Media Player de Windows, acerca de
- complementos, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7d666874590f380e6f3828031b297d483ffff7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105714420"
---
# <a name="windows-media-player-plug-ins"></a><span data-ttu-id="c8a88-106">Complementos de Media Player de Windows</span><span class="sxs-lookup"><span data-stu-id="c8a88-106">Windows Media Player Plug-ins</span></span>

<span data-ttu-id="c8a88-107">Microsoft Windows Media Player expone interfaces que permiten ampliar la funcionalidad de varias maneras.</span><span class="sxs-lookup"><span data-stu-id="c8a88-107">Microsoft Windows Media Player exposes interfaces that allow you to extend functionality in several ways.</span></span> <span data-ttu-id="c8a88-108">En las secciones siguientes se describen las arquitecturas de complementos admitidas y el proceso de creación de un complemento:</span><span class="sxs-lookup"><span data-stu-id="c8a88-108">The following sections describe the supported plug-in architectures and the process of building a plug-in:</span></span>



| <span data-ttu-id="c8a88-109">Sección</span><span class="sxs-lookup"><span data-stu-id="c8a88-109">Section</span></span>                                                                                                         | <span data-ttu-id="c8a88-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8a88-110">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c8a88-111">Compilar un complemento</span><span class="sxs-lookup"><span data-stu-id="c8a88-111">Building a Plug-in</span></span>](building-a-plug-in.md)                                                                    | <span data-ttu-id="c8a88-112">Puede crear varios tipos de complementos mediante Visual Studio y el Asistente para complementos de Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="c8a88-112">You can build several types of plug-ins by using Visual Studio and the Windows Media Player plug-in wizard.</span></span>                                                                                                                                                                                             |
| [<span data-ttu-id="c8a88-113">Visualizaciones personalizadas de Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="c8a88-113">Windows Media Player Custom Visualizations</span></span>](windows-media-player-custom-visualizations.md)                    | <span data-ttu-id="c8a88-114">Las visualizaciones de Windows Media Player son objetos del modelo de objetos componentes (COM) que se usan para mostrar imágenes visuales que se sincronizan con la parte de audio de la reproducción multimedia del reproductor.</span><span class="sxs-lookup"><span data-stu-id="c8a88-114">Windows Media Player visualizations are Component Object Model (COM) objects used to display visual imagery that is synchronized to the audio portion of the media playback of the player.</span></span> <span data-ttu-id="c8a88-115">Las visualizaciones personalizadas se pueden crear mediante Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="c8a88-115">Custom visualizations can be created using Microsoft Visual C++.</span></span>                                             |
| [<span data-ttu-id="c8a88-116">Complementos de la interfaz de usuario de Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="c8a88-116">Windows Media Player User Interface Plug-ins</span></span>](windows-media-player-user-interface-plug-ins.md)                | <span data-ttu-id="c8a88-117">Los complementos de la interfaz de usuario de Windows Media Player agregan nuevas funciones al panel **reproducción en curso** del reproductor en modo completo.</span><span class="sxs-lookup"><span data-stu-id="c8a88-117">Windows Media Player user interface plug-ins add new functionality to the **Now Playing** pane of the full mode Player.</span></span> <span data-ttu-id="c8a88-118">Puede crear complementos que usan el área de visualización, una ventana independiente, el área de configuración, el área de metadatos o los complementos de fondo que no exponen ninguna interfaz de usuario visible.</span><span class="sxs-lookup"><span data-stu-id="c8a88-118">You can create plug-ins that use the visualization area, a separate window, the settings area, the metadata area, or background plug-ins that expose no visible user interface.</span></span> |
| [<span data-ttu-id="c8a88-119">Complementos DSP de Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="c8a88-119">Windows Media Player DSP Plug-ins</span></span>](windows-media-player-dsp-plug-ins.md)                                      | <span data-ttu-id="c8a88-120">Los complementos DSP de Windows Media Player modifican o procesan datos de audio y vídeo antes de que los represente el reproductor.</span><span class="sxs-lookup"><span data-stu-id="c8a88-120">Windows Media Player DSP plug-ins modify or process audio and video data before it is rendered by the Player.</span></span> <span data-ttu-id="c8a88-121">Los complementos DSP son objetos multimedia de DirectX (DMO) que se conectan al reproductor a través de interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="c8a88-121">DSP plug-ins are DirectX Media Objects (DMO) that connect to the Player through COM interfaces.</span></span>                                                                                           |
| <span data-ttu-id="c8a88-122">[Complementos de representación de Windows Media Player (desusado)](/previous-versions/windows/desktop/legacy/dd564683(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c8a88-122">[Windows Media Player Rendering Plug-ins (deprecated)](/previous-versions/windows/desktop/legacy/dd564683(v=vs.85))</span></span> | <span data-ttu-id="c8a88-123">Los complementos de representación de Windows Media Player descodifican (si es necesario) y representan los datos personalizados contenidos en una secuencia de formato de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c8a88-123">Windows Media Player rendering plug-ins decode (if necessary) and render custom data contained in a Windows Media format stream.</span></span> <span data-ttu-id="c8a88-124">Los complementos de representación son objetos multimedia de DirectX (DMO) que se conectan al reproductor a través de interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="c8a88-124">Rendering plug-ins are DirectX Media Objects (DMO) that connect to the Player through COM interfaces.</span></span>                                                                  |
| [<span data-ttu-id="c8a88-125">Complementos de conversión de Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="c8a88-125">Windows Media Player Conversion Plug-ins</span></span>](windows-media-player-conversion-plug-ins.md)                        | <span data-ttu-id="c8a88-126">Los complementos de conversión de Windows Media Player convierten archivos multimedia digitales creados con tecnologías no proporcionadas por Microsoft, en formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="c8a88-126">Windows Media Player conversion plug-ins convert digital media files that are created using technologies not provided by Microsoft, into Advanced Systems Format (ASF).</span></span>                                                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="c8a88-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c8a88-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8a88-128">**SDK de Media Player de Windows**</span><span class="sxs-lookup"><span data-stu-id="c8a88-128">**Windows Media Player SDK**</span></span>](windows-media-player-sdk.md)
</dt> </dl>

 

 