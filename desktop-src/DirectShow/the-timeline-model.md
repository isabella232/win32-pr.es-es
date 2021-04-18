---
description: Modelo de escala de tiempo
ms.assetid: 53e782a2-0fab-46b4-b029-20017d9905bd
title: Modelo de escala de tiempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac01f90e8ca827bde41f2ad36e1ab32b3d429437
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104569892"
---
# <a name="the-timeline-model"></a><span data-ttu-id="09c68-103">Modelo de escala de tiempo</span><span class="sxs-lookup"><span data-stu-id="09c68-103">The Timeline Model</span></span>

<span data-ttu-id="09c68-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="09c68-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="09c68-105">Una *escala de tiempo* es un objeto que los [servicios de edición de DirectShow](directshow-editing-services.md) (des) usan para representar un proyecto de edición de vídeo.</span><span class="sxs-lookup"><span data-stu-id="09c68-105">A *timeline* is an object that [DirectShow Editing Services](directshow-editing-services.md) (DES) uses to represent a video editing project.</span></span> <span data-ttu-id="09c68-106">Un proyecto de edición se inicia como una colección de clips de origen, tomada de archivos de vídeo, archivos de sonido o archivos de imagen fija.</span><span class="sxs-lookup"><span data-stu-id="09c68-106">An editing project starts as a collection of source clips, taken from video files, sound files, or still image files.</span></span> <span data-ttu-id="09c68-107">Una secuencia lineal de clips forma una *pista*. En los servicios de edición de DirectShow (DES), el audio y el vídeo se colocan en pistas independientes.</span><span class="sxs-lookup"><span data-stu-id="09c68-107">A linear sequence of clips forms a *track*. In DirectShow Editing Services (DES), audio and video are placed in separate tracks.</span></span>

<span data-ttu-id="09c68-108">Las pistas también se pueden colocar en capas.</span><span class="sxs-lookup"><span data-stu-id="09c68-108">Tracks can also be layered.</span></span> <span data-ttu-id="09c68-109">Varias pistas de audio se mezclan juntas y pueden incluir efectos de audio, como fundidos o reverberación.</span><span class="sxs-lookup"><span data-stu-id="09c68-109">Multiple audio tracks are mixed together, and might include audio effects, such as fades or reverb.</span></span> <span data-ttu-id="09c68-110">Se usan varias pistas de vídeo para crear transiciones.</span><span class="sxs-lookup"><span data-stu-id="09c68-110">Multiple video tracks are used to create transitions.</span></span> <span data-ttu-id="09c68-111">Por ejemplo, puede crear un borrado de un clip a otro.</span><span class="sxs-lookup"><span data-stu-id="09c68-111">For example, you can create a wipe from one clip to another.</span></span> <span data-ttu-id="09c68-112">Otro ejemplo es una clave cromada, en la que el fondo de un clip se codifica y se reemplaza por una pista diferente. (El Pronóstico meteorológico delante de una imagen satelite es un ejemplo de generación de claves de croma).</span><span class="sxs-lookup"><span data-stu-id="09c68-112">Another example is a chroma key, in which the background of one clip is keyed out and replaced by a different track. (The weather forecaster in front of a satelite image is an example of chroma keying.)</span></span>

<span data-ttu-id="09c68-113">DES usa una estructura de árbol para representar una edición:</span><span class="sxs-lookup"><span data-stu-id="09c68-113">DES uses a tree structure to represent an editing:</span></span>

-   <span data-ttu-id="09c68-114">Los clips de audio y vídeo forman los nodos hoja, u objetos de *origen* .</span><span class="sxs-lookup"><span data-stu-id="09c68-114">Audio and video clips form the leaf nodes, or *source* objects.</span></span>
-   <span data-ttu-id="09c68-115">Una colección de orígenes con un tipo de medio uniforme (audio o vídeo) es una *pista*.</span><span class="sxs-lookup"><span data-stu-id="09c68-115">A collection of sources with a uniform media type (audio or video) is a *track*.</span></span>
-   <span data-ttu-id="09c68-116">Una colección de pistas es una *composición*.</span><span class="sxs-lookup"><span data-stu-id="09c68-116">A collection of tracks is a *composition*.</span></span> <span data-ttu-id="09c68-117">Una composición se representa como el compuesto de todas las pistas que contiene.</span><span class="sxs-lookup"><span data-stu-id="09c68-117">A composition is rendered as the composite of all the tracks it contains.</span></span> <span data-ttu-id="09c68-118">Las composiciones pueden contener otras composiciones, lo que permite disposiciones complejas de pistas.</span><span class="sxs-lookup"><span data-stu-id="09c68-118">Compositions can contain other compositions, which allows for complex arrangements of tracks.</span></span>
-   <span data-ttu-id="09c68-119">Una colección de nivel superior de composiciones y pistas (que representan el mismo tipo de medio) es un *Grupo*.</span><span class="sxs-lookup"><span data-stu-id="09c68-119">A top-level collection of compositions and tracks (all representing the same media type) is a *group*.</span></span>
-   <span data-ttu-id="09c68-120">Un conjunto de uno o varios grupos forma una *escala de tiempo*.</span><span class="sxs-lookup"><span data-stu-id="09c68-120">A set of one or more groups forms a *timeline*.</span></span> <span data-ttu-id="09c68-121">La escala de tiempo es el nodo raíz del árbol.</span><span class="sxs-lookup"><span data-stu-id="09c68-121">The timeline is the root node in the tree.</span></span>

<span data-ttu-id="09c68-122">Una escala de tiempo debe contener al menos un grupo.</span><span class="sxs-lookup"><span data-stu-id="09c68-122">A timeline must contain at least one group.</span></span> <span data-ttu-id="09c68-123">Cada grupo representa un único flujo en la producción final.</span><span class="sxs-lookup"><span data-stu-id="09c68-123">Each group represents a single stream in the final production.</span></span> <span data-ttu-id="09c68-124">Un proyecto típico incluye un grupo de vídeos y un grupo de audio.</span><span class="sxs-lookup"><span data-stu-id="09c68-124">A typical project includes one video group and one audio group.</span></span> <span data-ttu-id="09c68-125">Las composiciones son opcionales; existen para proporcionar más estructura si es necesario.</span><span class="sxs-lookup"><span data-stu-id="09c68-125">Compositions are optional; they exist to provide more structure if needed.</span></span>

<span data-ttu-id="09c68-126">En la ilustración siguiente se muestran las relaciones de elementos primarios y secundarios que constituyen una escala de tiempo:</span><span class="sxs-lookup"><span data-stu-id="09c68-126">The following illustration shows the child-parent relations that make up a timeline:</span></span>

![estructura del nodo](images/timeline1.png)

<span data-ttu-id="09c68-128">A continuación se muestra una escala de tiempo como una secuencia temporal:</span><span class="sxs-lookup"><span data-stu-id="09c68-128">The following shows a timeline as a temporal sequence:</span></span>

![Ilustración de la escala de tiempo](images/timeline2.png)

<span data-ttu-id="09c68-130">La flecha de la parte superior representa la dirección de la escala de tiempo, empezando por cero de la hora.</span><span class="sxs-lookup"><span data-stu-id="09c68-130">The arrow at the top represents the direction of the timeline, starting from time zero.</span></span> <span data-ttu-id="09c68-131">Dentro del grupo de vídeos, el seguimiento 1 tiene una prioridad más alta que la pista 0.</span><span class="sxs-lookup"><span data-stu-id="09c68-131">Within the video group, track 1 has a higher priority than track 0.</span></span> <span data-ttu-id="09c68-132">Los objetos de origen de Track 1 ocultan los de la pista 0.</span><span class="sxs-lookup"><span data-stu-id="09c68-132">The source objects in track 1 obscure those in track 0.</span></span> <span data-ttu-id="09c68-133">Donde Track 1 está vacío, Track 0 "se muestra a través de".</span><span class="sxs-lookup"><span data-stu-id="09c68-133">Where track 1 is empty, track 0 "shows through."</span></span> <span data-ttu-id="09c68-134">Como se mencionó anteriormente, las pistas de audio se combinan simplemente.</span><span class="sxs-lookup"><span data-stu-id="09c68-134">As mentioned earlier, audio tracks are simply mixed together.</span></span>

## <a name="related-topics"></a><span data-ttu-id="09c68-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="09c68-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09c68-136">Introducción con servicios de edición de DirectShow</span><span class="sxs-lookup"><span data-stu-id="09c68-136">Getting Started with DirectShow Editing Services</span></span>](getting-started-with-directshow-editing-services.md)
</dt> <dt>

[<span data-ttu-id="09c68-137">Construir una escala de tiempo</span><span class="sxs-lookup"><span data-stu-id="09c68-137">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 



