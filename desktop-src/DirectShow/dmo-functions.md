---
description: Funciones de DMO
ms.assetid: 0a380dc0-23f0-4ef0-898a-3b5afddf5eaa
title: Funciones de DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70f41750f5e442d93d3cacb2499bf2986a53cda6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494255"
---
# <a name="dmo-functions"></a><span data-ttu-id="b1b28-103">Funciones de DMO</span><span class="sxs-lookup"><span data-stu-id="b1b28-103">DMO Functions</span></span>

<span data-ttu-id="b1b28-104">En esta sección se describen las funciones de Microsoft DirectX media Object (DMO).</span><span class="sxs-lookup"><span data-stu-id="b1b28-104">This section describes the Microsoft DirectX Media Object (DMO) functions.</span></span>



| <span data-ttu-id="b1b28-105">Función</span><span class="sxs-lookup"><span data-stu-id="b1b28-105">Function</span></span>                                             | <span data-ttu-id="b1b28-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1b28-106">Description</span></span>                                                   |
|------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="b1b28-107">**DMOEnum**</span><span class="sxs-lookup"><span data-stu-id="b1b28-107">**DMOEnum**</span></span>](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum)                           | <span data-ttu-id="b1b28-108">Enumera DMOs enumeradas en el registro.</span><span class="sxs-lookup"><span data-stu-id="b1b28-108">Enumerates DMOs listed in the registry.</span></span>                       |
| [<span data-ttu-id="b1b28-109">**DMOGetName**</span><span class="sxs-lookup"><span data-stu-id="b1b28-109">**DMOGetName**</span></span>](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmogetname)                     | <span data-ttu-id="b1b28-110">Recupera el nombre de un DMO del registro.</span><span class="sxs-lookup"><span data-stu-id="b1b28-110">Retrieves the name of a DMO from the registry.</span></span>                |
| [<span data-ttu-id="b1b28-111">**DMOGetTypes**</span><span class="sxs-lookup"><span data-stu-id="b1b28-111">**DMOGetTypes**</span></span>](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmogettypes)                   | <span data-ttu-id="b1b28-112">Recupera los tipos de medios registrados para un DMO.</span><span class="sxs-lookup"><span data-stu-id="b1b28-112">Retrieves the media types registered for a DMO.</span></span>               |
| [<span data-ttu-id="b1b28-113">**DMORegister**</span><span class="sxs-lookup"><span data-stu-id="b1b28-113">**DMORegister**</span></span>](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister)                   | <span data-ttu-id="b1b28-114">Registra un DMO.</span><span class="sxs-lookup"><span data-stu-id="b1b28-114">Registers a DMO.</span></span>                                              |
| [<span data-ttu-id="b1b28-115">**DMOUnregister**</span><span class="sxs-lookup"><span data-stu-id="b1b28-115">**DMOUnregister**</span></span>](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmounregister)               | <span data-ttu-id="b1b28-116">Anula el registro de un DMO.</span><span class="sxs-lookup"><span data-stu-id="b1b28-116">Unregisters a DMO.</span></span>                                            |
| [<span data-ttu-id="b1b28-117">**MoCopyMediaType**</span><span class="sxs-lookup"><span data-stu-id="b1b28-117">**MoCopyMediaType**</span></span>](/previous-versions/windows/desktop/api/Dmort/nf-dmort-mocopymediatype)           | <span data-ttu-id="b1b28-118">Copia una estructura de tipo de medio en otra.</span><span class="sxs-lookup"><span data-stu-id="b1b28-118">Copies one media type structure to another.</span></span>                   |
| [<span data-ttu-id="b1b28-119">**MoCreateMediaType**</span><span class="sxs-lookup"><span data-stu-id="b1b28-119">**MoCreateMediaType**</span></span>](/previous-versions/windows/desktop/api/Dmort/nf-dmort-mocreatemediatype)       | <span data-ttu-id="b1b28-120">Asigna una nueva estructura de tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="b1b28-120">Allocates a new media type structure.</span></span>                         |
| [<span data-ttu-id="b1b28-121">**MoDeleteMediaType**</span><span class="sxs-lookup"><span data-stu-id="b1b28-121">**MoDeleteMediaType**</span></span>](/previous-versions/windows/desktop/api/Dmort/nf-dmort-modeletemediatype)       | <span data-ttu-id="b1b28-122">Elimina una estructura de tipo de medio que se asignó previamente.</span><span class="sxs-lookup"><span data-stu-id="b1b28-122">Deletes a media type structure that was previously allocated.</span></span> |
| [<span data-ttu-id="b1b28-123">**MoDuplicateMediaType**</span><span class="sxs-lookup"><span data-stu-id="b1b28-123">**MoDuplicateMediaType**</span></span>](/previous-versions/windows/desktop/api/Dmort/nf-dmort-moduplicatemediatype) | <span data-ttu-id="b1b28-124">Duplica una estructura de tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="b1b28-124">Duplicates a media type structure.</span></span>                            |
| [<span data-ttu-id="b1b28-125">**MoFreeMediaType**</span><span class="sxs-lookup"><span data-stu-id="b1b28-125">**MoFreeMediaType**</span></span>](/previous-versions/windows/desktop/api/Dmort/nf-dmort-mofreemediatype)           | <span data-ttu-id="b1b28-126">Libera los miembros asignados de una estructura de tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="b1b28-126">Frees the allocated members of a media type structure.</span></span>        |
| [<span data-ttu-id="b1b28-127">**MoInitMediaType**</span><span class="sxs-lookup"><span data-stu-id="b1b28-127">**MoInitMediaType**</span></span>](/previous-versions/windows/desktop/api/Dmort/nf-dmort-moinitmediatype)           | <span data-ttu-id="b1b28-128">Inicializa una estructura de tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="b1b28-128">Initializes a media type structure.</span></span>                           |



 

## <a name="related-topics"></a><span data-ttu-id="b1b28-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b1b28-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1b28-130">Referencia de DMO</span><span class="sxs-lookup"><span data-stu-id="b1b28-130">DMO Reference</span></span>](dmo-reference.md)
</dt> </dl>

 

 



