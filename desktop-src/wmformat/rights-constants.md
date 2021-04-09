---
title: Constantes de derechos
description: Constantes de derechos
ms.assetid: fb20dc57-25da-4613-a324-e081ba87df73
keywords:
- SDK de Windows Media Format, constantes
- Administración de derechos digitales (DRM), constantes
- DRM (administración de derechos digitales), constantes
- API extendidas del cliente DRM, constantes
- API extendidas del cliente, constantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1349da53b63b1b7df59c13e0e69f7fdbf47ee3f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148843"
---
# <a name="rights-constants"></a><span data-ttu-id="93efb-108">Constantes de derechos</span><span class="sxs-lookup"><span data-stu-id="93efb-108">Rights Constants</span></span>

<span data-ttu-id="93efb-109">Las constantes que se enumeran en la tabla siguiente se usan para identificar las acciones DRM y generar listas de acciones.</span><span class="sxs-lookup"><span data-stu-id="93efb-109">The constants listed in the following table are used to identify DRM actions and to build lists of actions.</span></span>



| <span data-ttu-id="93efb-110">Constante</span><span class="sxs-lookup"><span data-stu-id="93efb-110">Constant</span></span>                                        | <span data-ttu-id="93efb-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="93efb-111">Description</span></span>                                                                                                                                                                                                                                                    |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93efb-112">g \_ wszWMDRM \_ ACTIONLIST \_ etiqueta</span><span class="sxs-lookup"><span data-stu-id="93efb-112">g\_wszWMDRM\_ACTIONLIST\_TAG</span></span>                    | <span data-ttu-id="93efb-113">Define el nombre del elemento XML para una lista de acciones.</span><span class="sxs-lookup"><span data-stu-id="93efb-113">Defines the XML element name for an action list.</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="93efb-114">\_etiqueta de \_ acción g wszWMDRM \_</span><span class="sxs-lookup"><span data-stu-id="93efb-114">g\_wszWMDRM\_ACTION\_TAG</span></span>                        | <span data-ttu-id="93efb-115">Define el nombre del elemento XML de una entrada de una lista de acciones.</span><span class="sxs-lookup"><span data-stu-id="93efb-115">Defines the XML element name for an entry in an action list.</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="93efb-116">g \_ wszWMDRM \_ la \_ reproducción derecha</span><span class="sxs-lookup"><span data-stu-id="93efb-116">g\_wszWMDRM\_RIGHT\_PLAYBACK</span></span>                    | <span data-ttu-id="93efb-117">Define la cadena de la derecha para reproducir el contenido.</span><span class="sxs-lookup"><span data-stu-id="93efb-117">Defines the string for the right to play content.</span></span>                                                                                                                                                                                                              |
| <span data-ttu-id="93efb-118">g \_ wszWMDRM \_ \_ copia derecha</span><span class="sxs-lookup"><span data-stu-id="93efb-118">g\_wszWMDRM\_RIGHT\_COPY</span></span>                        | <span data-ttu-id="93efb-119">Define la cadena de la derecha para copiar contenido.</span><span class="sxs-lookup"><span data-stu-id="93efb-119">Defines the string for the right to copy content.</span></span>                                                                                                                                                                                                              |
| <span data-ttu-id="93efb-120">g \_ wszWMDRM de la \_ lista de \_ reproducción derecha \_</span><span class="sxs-lookup"><span data-stu-id="93efb-120">g\_wszWMDRM\_RIGHT\_PLAYLIST\_BURN</span></span>              | <span data-ttu-id="93efb-121">Define la cadena de la derecha para grabar contenido en CD como parte de una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="93efb-121">Defines the string for the right to burn content to CD as part of a playlist.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="93efb-122">g \_ wszWMDRM \_ derecha \_ crear \_ imagen en miniatura \_</span><span class="sxs-lookup"><span data-stu-id="93efb-122">g\_wszWMDRM\_RIGHT\_CREATE\_THUMBNAIL\_IMAGE</span></span>    | <span data-ttu-id="93efb-123">Define la cadena de la derecha para crear una imagen en miniatura a partir del contenido de vídeo.</span><span class="sxs-lookup"><span data-stu-id="93efb-123">Defines the string for the right to create a thumbnail image from video content.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="93efb-124">g \_ wszWMDRM \_ \_ copia derecha \_ a \_ CD</span><span class="sxs-lookup"><span data-stu-id="93efb-124">g\_wszWMDRM\_RIGHT\_COPY\_TO\_CD</span></span>                | <span data-ttu-id="93efb-125">Define la cadena de la derecha para copiar contenido en un CD.</span><span class="sxs-lookup"><span data-stu-id="93efb-125">Defines the string for the right to copy content to a CD.</span></span> <span data-ttu-id="93efb-126">Las nuevas licencias no deben usar este derecho.</span><span class="sxs-lookup"><span data-stu-id="93efb-126">New licenses should not use this right.</span></span> <span data-ttu-id="93efb-127">En su lugar, todos los derechos que conceden el permiso para copiar contenido deben estar incluidos en el derecho de copia y en la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="93efb-127">Instead, all rights granting permission to copy content should be covered by the copy right and the playlist burn right.</span></span>                                     |
| <span data-ttu-id="93efb-128">g \_ wszWMDRM \_ la \_ copia derecha \_ en el dispositivo de \_ SDMI \_</span><span class="sxs-lookup"><span data-stu-id="93efb-128">g\_wszWMDRM\_RIGHT\_COPY\_TO\_SDMI\_DEVICE</span></span>      | <span data-ttu-id="93efb-129">Define la cadena de la derecha para copiar contenido en un dispositivo que se ajusta a la iniciativa de música digital segura (SDMI).</span><span class="sxs-lookup"><span data-stu-id="93efb-129">Defines the string for the right to copy content to a device that conforms to the Secure Digital Music Initiative (SDMI).</span></span> <span data-ttu-id="93efb-130">Las nuevas licencias no deben usar este derecho.</span><span class="sxs-lookup"><span data-stu-id="93efb-130">New licenses should not use this right.</span></span> <span data-ttu-id="93efb-131">En su lugar, todos los derechos que conceden el permiso para copiar contenido deben estar incluidos en el derecho de copia.</span><span class="sxs-lookup"><span data-stu-id="93efb-131">Instead, all rights granting permission to copy content should be covered by the copy right.</span></span> |
| <span data-ttu-id="93efb-132">g \_ wszWMDRM \_ la \_ copia derecha \_ en un \_ dispositivo que no es de \_ SDMI \_</span><span class="sxs-lookup"><span data-stu-id="93efb-132">g\_wszWMDRM\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE</span></span> | <span data-ttu-id="93efb-133">Define la cadena de la derecha para copiar en un dispositivo que no se ajusta a la iniciativa de música digital segura (SDMI).</span><span class="sxs-lookup"><span data-stu-id="93efb-133">Defines the string for the right to copy to a device that does not conform to the Secure Digital Music Initiative (SDMI).</span></span> <span data-ttu-id="93efb-134">Las nuevas licencias no deben usar este derecho.</span><span class="sxs-lookup"><span data-stu-id="93efb-134">New licenses should not use this right.</span></span> <span data-ttu-id="93efb-135">En su lugar, todos los derechos que conceden el permiso para copiar contenido deben estar incluidos en el derecho de copia.</span><span class="sxs-lookup"><span data-stu-id="93efb-135">Instead, all rights granting permission to copy content should be covered by the copy right.</span></span> |
| <span data-ttu-id="93efb-136">copia de seguridad de g \_ wszWMDRM \_ derecha \_</span><span class="sxs-lookup"><span data-stu-id="93efb-136">g\_wszWMDRM\_RIGHT\_BACKUP</span></span>                      | <span data-ttu-id="93efb-137">Define la cadena de la derecha para hacer una copia de seguridad de la licencia.</span><span class="sxs-lookup"><span data-stu-id="93efb-137">Defines the string for the right to backup the license.</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="93efb-138">g \_ wszWMDRM de colaboración de la \_ derecha \_ \_</span><span class="sxs-lookup"><span data-stu-id="93efb-138">g\_wszWMDRM\_RIGHT\_COLLABORATIVE\_PLAY</span></span>         | <span data-ttu-id="93efb-139">Define la cadena de la derecha para reproducir contenido a través de una red como parte de una lista de reproducción compartida.</span><span class="sxs-lookup"><span data-stu-id="93efb-139">Defines the string for the right to play content over a network as part of a shared playlist.</span></span>                                                                                                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="93efb-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="93efb-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93efb-141">**Constantes**</span><span class="sxs-lookup"><span data-stu-id="93efb-141">**Constants**</span></span>](constants.md)
</dt> </dl>

 

 




