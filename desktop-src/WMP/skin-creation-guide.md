---
title: Guía de creación de máscaras
description: Guía de creación de máscaras
ms.assetid: 86c77764-5c8c-4493-ac2d-15268c1ba564
keywords:
- Media Player de Windows, máscaras
- Aspectos de Windows Media Player, guía de creación
- máscaras, guía de creación
- crear máscaras, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7214accedf24bd80449bf8952bc9268f9b9bf49d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704633"
---
# <a name="skin-creation-guide"></a><span data-ttu-id="de036-107">Guía de creación de máscaras</span><span class="sxs-lookup"><span data-stu-id="de036-107">Skin Creation Guide</span></span>

<span data-ttu-id="de036-108">Esta guía es una serie de explicaciones detalladas sobre cómo crear diferentes tipos de máscaras.</span><span class="sxs-lookup"><span data-stu-id="de036-108">This guide is a series of detailed explanations of how to create different kinds of skins.</span></span> <span data-ttu-id="de036-109">Para obtener más información general sobre las máscaras, vea acerca de las [máscaras](about-skins.md).</span><span class="sxs-lookup"><span data-stu-id="de036-109">For more general information on skins, see [About Skins](about-skins.md).</span></span> <span data-ttu-id="de036-110">Para obtener detalles específicos sobre todos los atributos, métodos y eventos utilizados en las máscaras, vea la [referencia de programación](skin-programming-reference.md)de la máscara.</span><span class="sxs-lookup"><span data-stu-id="de036-110">For specific details about every attribute, method, and event used in skins, see the [Skin Programming Reference](skin-programming-reference.md).</span></span> <span data-ttu-id="de036-111">A medida que lo hace más en la programación de la máscara, puede que desee leer la parte de este SDK que abarca el [modelo de objetos de Windows Media Player](windows-media-player-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="de036-111">As you get more involved in the programming of your skin, you may want to read the part of this SDK covering the [Windows Media Player Object Model](windows-media-player-object-model.md).</span></span>

<span data-ttu-id="de036-112">En esta guía, se proporcionarán instrucciones para crear la imagen para Adobe Photoshop 5,5, un conocido programa de manipulación de imágenes.</span><span class="sxs-lookup"><span data-stu-id="de036-112">In this guide, instructions for creating the art will be given for Adobe Photoshop 5.5, a popular art manipulation program.</span></span> <span data-ttu-id="de036-113">Las instrucciones específicas pueden ser diferentes si tiene un programa de arte similar, como Jasc Paint Shop Pro o Sonic Foundry viscosidad, pero los conceptos son los mismos.</span><span class="sxs-lookup"><span data-stu-id="de036-113">The specific instructions may be different if you have a similar art program such as Jasc Paint Shop Pro or Sonic Foundry Viscosity, but the concepts will be the same.</span></span> <span data-ttu-id="de036-114">Photoshop se eligió por dos motivos: es un conocido programa de arte para artistas comerciales y funciona con capas.</span><span class="sxs-lookup"><span data-stu-id="de036-114">Photoshop was chosen for two reasons: it is a popular art program for commercial artists, and it works with layers.</span></span> <span data-ttu-id="de036-115">Como verá en los tutoriales, las capas son muy útiles para la creación de máscaras.</span><span class="sxs-lookup"><span data-stu-id="de036-115">As you will see in the tutorials, layers are very useful for skin creation.</span></span>

<span data-ttu-id="de036-116">En esta guía se tratan las siguientes tareas.</span><span class="sxs-lookup"><span data-stu-id="de036-116">This guide will cover the following tasks.</span></span>



| <span data-ttu-id="de036-117">Tarea</span><span class="sxs-lookup"><span data-stu-id="de036-117">Task</span></span>                                                     | <span data-ttu-id="de036-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="de036-118">Description</span></span>                                                                                     |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="de036-119">Creación de la primera máscara</span><span class="sxs-lookup"><span data-stu-id="de036-119">Building Your First Skin</span></span>](building-your-first-skin.md) | <span data-ttu-id="de036-120">Un tutorial de una máscara simple que inicia y detiene Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="de036-120">A walk-through of a simple skin that starts and stops Windows Media Player.</span></span>                     |
| [<span data-ttu-id="de036-121">Agregar una lista de reproducción</span><span class="sxs-lookup"><span data-stu-id="de036-121">Adding a Playlist</span></span>](adding-a-playlist.md)               | <span data-ttu-id="de036-122">Cómo usar una lista de reproducción simple.</span><span class="sxs-lookup"><span data-stu-id="de036-122">How to use a simple playlist.</span></span>                                                                   |
| [<span data-ttu-id="de036-123">Elegir archivos</span><span class="sxs-lookup"><span data-stu-id="de036-123">Choosing Files</span></span>](choosing-files.md)                     | <span data-ttu-id="de036-124">Cómo seleccionar archivos con un cuadro de diálogo Abrir archivo.</span><span class="sxs-lookup"><span data-stu-id="de036-124">How to pick files with an open file dialog box.</span></span>                                                 |
| [<span data-ttu-id="de036-125">Agregar vídeo</span><span class="sxs-lookup"><span data-stu-id="de036-125">Adding Video</span></span>](adding-video.md)                         | <span data-ttu-id="de036-126">Cómo colocar una ventana de vídeo en la máscara.</span><span class="sxs-lookup"><span data-stu-id="de036-126">How to put a video window into your skin.</span></span>                                                       |
| [<span data-ttu-id="de036-127">Agregar visualizaciones</span><span class="sxs-lookup"><span data-stu-id="de036-127">Adding Visualizations</span></span>](adding-visualizations.md)       | <span data-ttu-id="de036-128">Cómo agregar visualizaciones.</span><span class="sxs-lookup"><span data-stu-id="de036-128">How to add visualizations.</span></span>                                                                      |
| [<span data-ttu-id="de036-129">Agregar un control deslizante</span><span class="sxs-lookup"><span data-stu-id="de036-129">Adding a Slider</span></span>](adding-a-slider.md)                   | <span data-ttu-id="de036-130">Cómo usar un control deslizante para realizar un seguimiento del progreso del contenido multimedia... y deje que el usuario cambie.</span><span class="sxs-lookup"><span data-stu-id="de036-130">How to use a slider to track the progress of your media content ... and let the user change it!</span></span> |
| [<span data-ttu-id="de036-131">Crear controles deslizantes personalizados</span><span class="sxs-lookup"><span data-stu-id="de036-131">Creating Custom Sliders</span></span>](creating-custom-sliders.md)   | <span data-ttu-id="de036-132">Cómo controlar el volumen con un control deslizante personalizado.</span><span class="sxs-lookup"><span data-stu-id="de036-132">How to control the volume with a custom slider.</span></span>                                                 |
| [<span data-ttu-id="de036-133">Otros ejemplos de máscara</span><span class="sxs-lookup"><span data-stu-id="de036-133">Other Skin Samples</span></span>](other-skin-samples.md)             | <span data-ttu-id="de036-134">Vea la sección de ejemplos del SDK.</span><span class="sxs-lookup"><span data-stu-id="de036-134">See the samples section of the SDK.</span></span>                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="de036-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="de036-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de036-136">**Máscaras de Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="de036-136">**Windows Media Player Skins**</span></span>](windows-media-player-skins.md)
</dt> </dl>

 

 




