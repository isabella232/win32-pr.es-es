---
title: Editar secuencias
description: Editar secuencias
ms.assetid: 1653ff90-e96a-43fc-b509-6d8ad4ddcd2c
keywords:
- CreateEditableStream función)
- EditStreamCut función)
- EditStreamCopy función)
- EditStreamPaste función)
- EditStreamClone función)
- EditStreamSetInfo función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29eb687eb36ff9dfe0b1d3477bff095bdd78a135
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486894"
---
# <a name="editing-streams"></a><span data-ttu-id="6c08f-109">Editar secuencias</span><span class="sxs-lookup"><span data-stu-id="6c08f-109">Editing Streams</span></span>

<span data-ttu-id="6c08f-110">Puede crear una secuencia que se puede editar mediante la función [**CreateEditableStream**](/windows/desktop/api/Vfw/nf-vfw-createeditablestream) .</span><span class="sxs-lookup"><span data-stu-id="6c08f-110">You can create a stream that you can edit by using the [**CreateEditableStream**](/windows/desktop/api/Vfw/nf-vfw-createeditablestream) function.</span></span> <span data-ttu-id="6c08f-111">Esta función inicializa el entorno para editar una secuencia.</span><span class="sxs-lookup"><span data-stu-id="6c08f-111">This function initializes the environment for editing a stream.</span></span> <span data-ttu-id="6c08f-112">Esto incluye la creación de una interfaz para el nuevo flujo y las tablas de edición internas que realizan el seguimiento de los cambios realizados en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="6c08f-112">This includes creating an interface to the new stream, and internal edit tables that track changes made to the stream.</span></span> <span data-ttu-id="6c08f-113">**CreateEditableStream** devuelve un puntero de secuencia a una secuencia editable que es necesaria para otras funciones de edición de secuencias.</span><span class="sxs-lookup"><span data-stu-id="6c08f-113">**CreateEditableStream** returns a stream pointer to an editable stream that is required by other stream-editing functions.</span></span> <span data-ttu-id="6c08f-114">El puntero de secuencia editable también lo pueden usar otras funciones AVIFile que aceptan punteros de secuencia.</span><span class="sxs-lookup"><span data-stu-id="6c08f-114">The editable stream pointer can also be used by other AVIFile functions that accept stream pointers.</span></span>

<span data-ttu-id="6c08f-115">Puede cortar uno o más ejemplos de una secuencia modificable mediante la función [**EditStreamCut**](/windows/desktop/api/Vfw/nf-vfw-editstreamcut) .</span><span class="sxs-lookup"><span data-stu-id="6c08f-115">You can cut one or more samples from an editable stream by using the [**EditStreamCut**](/windows/desktop/api/Vfw/nf-vfw-editstreamcut) function.</span></span> <span data-ttu-id="6c08f-116">Para quitar ejemplos de la secuencia editable, esta función agrega una entrada a la tabla de edición.</span><span class="sxs-lookup"><span data-stu-id="6c08f-116">To remove samples from the editable stream, this function adds an entry to the edit table.</span></span> <span data-ttu-id="6c08f-117">A continuación, la función coloca una copia de los ejemplos de corte en una nueva secuencia temporal cuyo puntero de interfaz se devuelve en una variable.</span><span class="sxs-lookup"><span data-stu-id="6c08f-117">The function then places a copy of the cut samples in a new temporary stream whose interface pointer is returned in a variable.</span></span>

<span data-ttu-id="6c08f-118">Puede copiar uno o más ejemplos de una secuencia modificable en una secuencia temporal mediante la función [**EditStreamCopy**](/windows/desktop/api/Vfw/nf-vfw-editstreamcopy) .</span><span class="sxs-lookup"><span data-stu-id="6c08f-118">You can copy one or more samples from an editable stream into a temporary stream by using the [**EditStreamCopy**](/windows/desktop/api/Vfw/nf-vfw-editstreamcopy) function.</span></span> <span data-ttu-id="6c08f-119">**EditStreamCopy** coloca copias de los ejemplos en una nueva secuencia temporal cuyo puntero de interfaz se devuelve en una variable.</span><span class="sxs-lookup"><span data-stu-id="6c08f-119">**EditStreamCopy** places copies of the samples in a new temporary stream whose interface pointer is returned in a variable.</span></span>

<span data-ttu-id="6c08f-120">Puede copiar uno o más ejemplos de una secuencia y pegarlos en una secuencia modificable mediante la función [**EditStreamPaste**](/windows/desktop/api/Vfw/nf-vfw-editstreampaste) .</span><span class="sxs-lookup"><span data-stu-id="6c08f-120">You can copy one or more samples from a stream and paste them into an editable stream by using the [**EditStreamPaste**](/windows/desktop/api/Vfw/nf-vfw-editstreampaste) function.</span></span> <span data-ttu-id="6c08f-121">Para insertar los ejemplos en la posición especificada, esta función agrega una entrada en la tabla de edición de la secuencia modificable de destino.</span><span class="sxs-lookup"><span data-stu-id="6c08f-121">To insert the samples at the specified position, this function adds an entry in the edit table of the target editable stream.</span></span>

<span data-ttu-id="6c08f-122">Puede duplicar una secuencia modificable mediante la función [**EditStreamClone**](/windows/desktop/api/Vfw/nf-vfw-editstreamclone) .</span><span class="sxs-lookup"><span data-stu-id="6c08f-122">You can duplicate an editable stream by using the [**EditStreamClone**](/windows/desktop/api/Vfw/nf-vfw-editstreamclone) function.</span></span> <span data-ttu-id="6c08f-123">Esta función devuelve un puntero a la interfaz de flujo de la nueva secuencia.</span><span class="sxs-lookup"><span data-stu-id="6c08f-123">This function returns a pointer to the stream interface of the new stream.</span></span> <span data-ttu-id="6c08f-124">Puede copiar estos flujos en el portapapeles o utilizarlos para mantener un rastro de las ediciones realizadas en un flujo.</span><span class="sxs-lookup"><span data-stu-id="6c08f-124">You can copy these streams to the clipboard or use them to maintain a trail of edits made to a stream.</span></span>

<span data-ttu-id="6c08f-125">Puede cambiar algunas de las características de una secuencia modificable mediante la función [**EditStreamSetInfo**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetinfoa) .</span><span class="sxs-lookup"><span data-stu-id="6c08f-125">You can change several of the characteristics of an editable stream by using the [**EditStreamSetInfo**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetinfoa) function.</span></span> <span data-ttu-id="6c08f-126">Esta función actualiza la configuración de prioridad, el idioma, la escala y la velocidad, la hora de inicio, la configuración de calidad, las coordenadas y las dimensiones del rectángulo de destino, y la descripción textual de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="6c08f-126">This function updates the priority setting, language, scale and rate, starting time, quality setting, destination rectangle dimensions and coordinates, and the textual description of the stream.</span></span> <span data-ttu-id="6c08f-127">Estos elementos se almacenan en la estructura [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) asociada al flujo modificable.</span><span class="sxs-lookup"><span data-stu-id="6c08f-127">These items are stored in the [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) structure associated with the editable stream.</span></span>

<span data-ttu-id="6c08f-128">También puede cambiar la descripción textual de una secuencia modificable mediante la función [**EditStreamSetName**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetnamea) .</span><span class="sxs-lookup"><span data-stu-id="6c08f-128">You can also change the textual description of an editable stream by using the [**EditStreamSetName**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetnamea) function.</span></span> <span data-ttu-id="6c08f-129">Esta función actualiza el miembro **szName** de la estructura **AVISTREAMINFO** asociada al flujo modificable.</span><span class="sxs-lookup"><span data-stu-id="6c08f-129">This function updates the **szName** member of the **AVISTREAMINFO** structure associated with the editable stream.</span></span>

<span data-ttu-id="6c08f-130">Las funciones de edición funcionan en secuencias.</span><span class="sxs-lookup"><span data-stu-id="6c08f-130">The editing functions work on streams.</span></span> <span data-ttu-id="6c08f-131">Debe cortar y pegar cada flujo individualmente y, a continuación, usar la función [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) para crear un nuevo puntero de archivo.</span><span class="sxs-lookup"><span data-stu-id="6c08f-131">You need to cut and paste each stream individually, and then use the [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) function to create a new file pointer.</span></span>

> [!Note]  
> <span data-ttu-id="6c08f-132">Las tablas de edición de una secuencia modificable mantienen todos los cambios de una secuencia.</span><span class="sxs-lookup"><span data-stu-id="6c08f-132">The edit tables in an editable stream maintain all the changes for a stream.</span></span> <span data-ttu-id="6c08f-133">La secuencia de origen nunca cambia.</span><span class="sxs-lookup"><span data-stu-id="6c08f-133">The source stream is never changed.</span></span>

 

 

 




