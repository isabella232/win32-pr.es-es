---
title: Información general de los metaarchivos de Windows Media
description: Información general de los metaarchivos de Windows Media
ms.assetid: 5b7742c0-f416-4bf4-ae03-9554b51fe620
keywords:
- Metaarchivos de Windows Media, acerca de
- Media Player de Windows, metaarchivos
- Windows Media Player, metaarchivos de Windows Media
- metaarchivos, acerca de
- Windows Media, metaarchivos
- Listas de reproducción de metarchivos de Windows Media, acerca de
- listas de reproducción, acerca de
- Metaarchivos de Windows Media, sintaxis
- metaarchivos, sintaxis
- listas de reproducción de metarchivos, acerca de
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e7ed86cca023103c044f28141e0212542d83d200
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714171"
---
# <a name="windows-media-metafiles-overview"></a><span data-ttu-id="6c7f7-113">Información general de los metaarchivos de Windows Media</span><span class="sxs-lookup"><span data-stu-id="6c7f7-113">Windows Media Metafiles Overview</span></span>

<span data-ttu-id="6c7f7-114">La parte más importante del uso correcto de metarchivos de Windows Media es usar la sintaxis correcta para los elementos de metarchivo.</span><span class="sxs-lookup"><span data-stu-id="6c7f7-114">The most important part of successfully using Windows Media metafiles is using the correct syntax for the metafile elements.</span></span> <span data-ttu-id="6c7f7-115">Los errores de sintaxis de un metarchivo de Windows Media pueden provocar que se supere el uso de un solo atributo, que el metarchivo no se reconoce como válido y no funciona.</span><span class="sxs-lookup"><span data-stu-id="6c7f7-115">Syntax errors in a Windows Media metafile can cause anything from a single attribute being overlooked, to the metafile not being recognized as valid and failing to work.</span></span>

<span data-ttu-id="6c7f7-116">Casi tan importante es el orden en el que aparecen los elementos en un metarchivo de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="6c7f7-116">Almost as important is the order in which the elements appear in a Windows Media metafile.</span></span> <span data-ttu-id="6c7f7-117">Los atributos de algunos elementos invalidan temporalmente los atributos de elementos similares en distintas secciones del metarchivo.</span><span class="sxs-lookup"><span data-stu-id="6c7f7-117">The attributes of some elements temporarily override the attributes of similar elements in different sections of the metafile.</span></span> <span data-ttu-id="6c7f7-118">Hay un [orden de prioridad](order-of-precedence.md)definido.</span><span class="sxs-lookup"><span data-stu-id="6c7f7-118">There is a defined [Order of Precedence](order-of-precedence.md).</span></span>

<span data-ttu-id="6c7f7-119">Las listas de reproducción de metarchivos de Windows Media son metarchivos de Windows Media que proporcionan información que Windows Media Player usa para recibir secuencias de unidifusión, secuencias de multidifusión y otros medios admitidos desde una intranet o Internet.</span><span class="sxs-lookup"><span data-stu-id="6c7f7-119">Windows Media metafile playlists are Windows Media metafiles that provide information that Windows Media Player uses to receive unicast streams, multicast streams, and other supported media from an intranet or the Internet.</span></span> <span data-ttu-id="6c7f7-120">Una lista de reproducción de metarchivo es básicamente un acceso directo al contenido multimedia.</span><span class="sxs-lookup"><span data-stu-id="6c7f7-120">A metafile playlist is basically a shortcut to media content.</span></span> <span data-ttu-id="6c7f7-121">Se puede enviar una lista de reproducción de metarchivo como correo electrónico, que se usa como referencia de vínculo en una página web, que se crea dinámicamente con Active Server páginas (ASP) o como un archivo independiente en una unidad de disco local.</span><span class="sxs-lookup"><span data-stu-id="6c7f7-121">A metafile playlist can be sent as email, used as a link reference on a webpage, created dynamically using Active Server Pages (ASP), or exist as a stand-alone file on a local disk drive.</span></span> <span data-ttu-id="6c7f7-122">Una lista de reproducción de metarchivo puede hacer referencia a otra lista de reproducción de metarchivo, una página ASP o un archivo de estación de Windows Media (con la extensión de nombre de archivo. NSC).</span><span class="sxs-lookup"><span data-stu-id="6c7f7-122">A metafile playlist can reference another metafile playlist, an ASP page, or a Windows Media station file (with an .nsc file name extension).</span></span> <span data-ttu-id="6c7f7-123">Un archivo. NSC se usa para definir una estación de Windows Media a Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6c7f7-123">An .nsc file is used to define a Windows Media station to Windows Media Player.</span></span> <span data-ttu-id="6c7f7-124">El proceso de control básico es el mismo para cada caso.</span><span class="sxs-lookup"><span data-stu-id="6c7f7-124">The basic handling process is the same for each case.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6c7f7-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6c7f7-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c7f7-126">**Acerca de los metaarchivos de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="6c7f7-126">**About Windows Media Metafiles**</span></span>](about-windows-media-metafiles.md)
</dt> </dl>

 

 




