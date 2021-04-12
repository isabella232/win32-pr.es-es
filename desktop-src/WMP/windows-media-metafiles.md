---
title: Metaarchivos de Windows Media
description: Metaarchivos de Windows Media
ms.assetid: 77af7d15-52ac-496c-8037-51827adf0250
keywords:
- Metaarchivos de Windows Media, acerca de
- Media Player de Windows, metaarchivos
- Windows Media Player, metaarchivos de Windows Media
- metaarchivos, acerca de
- Windows Media, metaarchivos
- Listas de reproducción de metarchivos de Windows Media, acerca de
- listas de reproducción, acerca de
- listas de reproducción de metarchivos, acerca de
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 385b149e07e9d30df4e11a21f8e7aa4b05e06910
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357116"
---
# <a name="windows-media-metafiles"></a><span data-ttu-id="8db2c-111">Metaarchivos de Windows Media</span><span class="sxs-lookup"><span data-stu-id="8db2c-111">Windows Media Metafiles</span></span>

<span data-ttu-id="8db2c-112">Esta referencia documenta los metaarchivos de Windows Media, que utilizan las extensiones de nombre de archivo. Wax,. wvx,. WMX y. ASX.</span><span class="sxs-lookup"><span data-stu-id="8db2c-112">This reference documents Windows Media metafiles, which use the .wax, .wvx, .wmx, and .asx file name extensions.</span></span> <span data-ttu-id="8db2c-113">Contiene secciones de la guía de programación y de información general, así como una sección de referencia completa de etiquetas de elementos de metarchivo, sus atributos y valores, y condiciones especiales relacionadas con cada elemento.</span><span class="sxs-lookup"><span data-stu-id="8db2c-113">It contains overview and programming guide sections, and a full reference section on metafile element tags, their attributes and values, and special conditions related to each element.</span></span>

<span data-ttu-id="8db2c-114">Un metarchivo es un archivo que contiene información sobre otros archivos.</span><span class="sxs-lookup"><span data-stu-id="8db2c-114">A metafile is a file that contains information about other files.</span></span> <span data-ttu-id="8db2c-115">Se puede usar un metarchivo para mostrar un grupo de archivos de contenido multimedia que se reproducirán en orden.</span><span class="sxs-lookup"><span data-stu-id="8db2c-115">A metafile can be used to list a group of media content files that are to be played in order.</span></span> <span data-ttu-id="8db2c-116">Las listas de reproducción de metarchivos de Windows Media, simplemente denominadas listas de reproducción en este documento de referencia, son una de las características más eficaces de las tecnologías de Microsoft Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8db2c-116">Windows Media metafile playlists, simply referred to as playlists in this reference document, are one of the most powerful features of Microsoft Windows Media Technologies.</span></span> <span data-ttu-id="8db2c-117">Las listas de reproducción le permiten controlar y personalizar el contenido multimedia.</span><span class="sxs-lookup"><span data-stu-id="8db2c-117">Playlists allow you to control and customize your media content.</span></span> <span data-ttu-id="8db2c-118">Por ejemplo, con las listas de reproducción puede programar el contenido para que se reproduzca en sucesión o inserte clips de publicidad o de interés especial en una presentación.</span><span class="sxs-lookup"><span data-stu-id="8db2c-118">For instance, with playlists you can schedule content to play in succession or insert advertising or special interest clips into a presentation.</span></span> <span data-ttu-id="8db2c-119">Una mayor ventaja de las listas de reproducción es que, en lugar de reproducir un flujo, detener, iniciar el siguiente flujo y, a continuación, esperar a que finalice el almacenamiento en búfer, Windows Media Services y Windows Media Player funcionan juntos para reproducir los clips uno tras otro con un tiempo mínimo de almacenamiento en búfer o una interrupción entre ellos.</span><span class="sxs-lookup"><span data-stu-id="8db2c-119">A further advantage of playlists is that instead of playing a stream, stopping, starting the next stream, and then waiting for it to finish buffering, Windows Media Services and Windows Media Player work together to play the clips one after the other with minimal buffering time or interruption between them.</span></span>

<span data-ttu-id="8db2c-120">Las tecnologías de Windows Media y otros productos de Internet proporcionan las herramientas necesarias para comprender los datos demográficos de los usuarios y personalizar dinámicamente una difusión o un mensaje para usuarios individuales.</span><span class="sxs-lookup"><span data-stu-id="8db2c-120">Windows Media Technologies and other Internet products provide you with the tools to understand user demographics and dynamically customize a broadcast or message for individual users.</span></span>

<span data-ttu-id="8db2c-121">Esta referencia se divide en las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="8db2c-121">This reference is divided into the following sections.</span></span>



| <span data-ttu-id="8db2c-122">Sección</span><span class="sxs-lookup"><span data-stu-id="8db2c-122">Section</span></span>                                                                  | <span data-ttu-id="8db2c-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="8db2c-123">Description</span></span>                                                                                                                                                                         |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8db2c-124">Acerca de los metaarchivos de Windows Media</span><span class="sxs-lookup"><span data-stu-id="8db2c-124">About Windows Media Metafiles</span></span>](about-windows-media-metafiles.md)       | <span data-ttu-id="8db2c-125">Presenta los elementos de metarchivo de Windows Media y describe su finalidad.</span><span class="sxs-lookup"><span data-stu-id="8db2c-125">Introduces Windows Media metafile elements and discusses their purpose.</span></span>                                                                                                             |
| [<span data-ttu-id="8db2c-126">Guía de metarchivo de Windows Media</span><span class="sxs-lookup"><span data-stu-id="8db2c-126">Windows Media Metafile Guide</span></span>](windows-media-metafile-guide.md)         | <span data-ttu-id="8db2c-127">Detalla los pasos necesarios para crear los metaarchivos.</span><span class="sxs-lookup"><span data-stu-id="8db2c-127">Details the steps necessary for creating metafiles.</span></span> <span data-ttu-id="8db2c-128">En los ejemplos se muestra cómo usar etiquetas de elementos para tareas específicas.</span><span class="sxs-lookup"><span data-stu-id="8db2c-128">Examples illustrate how to use element tags for specific tasks.</span></span>                                                                 |
| [<span data-ttu-id="8db2c-129">Referencia de metarchivos de Windows Media</span><span class="sxs-lookup"><span data-stu-id="8db2c-129">Windows Media Metafile Reference</span></span>](windows-media-metafile-reference.md) | <span data-ttu-id="8db2c-130">Explica con detalle cada uno de los elementos de metarchivo, sus atributos y valores, y condiciones especiales relacionadas con cada uno de ellos.</span><span class="sxs-lookup"><span data-stu-id="8db2c-130">Explains in detail each of the metafile elements, their attributes and values, and special conditions related to each.</span></span> <span data-ttu-id="8db2c-131">Explica las extensiones de nombre de archivo de metarchivo y su uso correcto.</span><span class="sxs-lookup"><span data-stu-id="8db2c-131">Explains metafile file name extensions and their proper use.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="8db2c-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8db2c-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8db2c-133">**SDK de Media Player de Windows**</span><span class="sxs-lookup"><span data-stu-id="8db2c-133">**Windows Media Player SDK**</span></span>](windows-media-player-sdk.md)
</dt> </dl>

 

 




