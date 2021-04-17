---
title: Licencias
description: Licencias
ms.assetid: 74717519-bfd5-4a64-88eb-680d4bdfe74a
keywords:
- SDK de Windows Media Format, administración de derechos digitales (DRM)
- SDK de Windows Media Format, licencias de DRM
- SDK de Windows Media Format, licencias de DRM
- Administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- Administración de derechos digitales (DRM), licencias de archivos protegidos
- DRM (administración de derechos digitales), licencias de archivos protegidos
- licencias, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0fbf2d7c0a25b2b19241d90743f43f46a71d7e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357680"
---
# <a name="licenses"></a><span data-ttu-id="16770-111">Licencias</span><span class="sxs-lookup"><span data-stu-id="16770-111">Licenses</span></span>

<span data-ttu-id="16770-112">Una licencia es un conjunto de datos que describe las condiciones en las que se pueden leer los datos de los archivos protegidos.</span><span class="sxs-lookup"><span data-stu-id="16770-112">A license is a set of data that describes the conditions under which data in protected files can be read.</span></span> <span data-ttu-id="16770-113">Cada licencia se aplica a un identificador de clave, que normalmente se asigna a un solo archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="16770-113">Each license applies to a key identifier, which is typically assigned to a single media file.</span></span> <span data-ttu-id="16770-114">Este identificador es lo que se usa para identificar el contenido protegido en la licencia.</span><span class="sxs-lookup"><span data-stu-id="16770-114">This identifier is what is used to identify the protected content in the license.</span></span>

<span data-ttu-id="16770-115">Cada licencia especifica una o varias acciones que se pueden realizar con el contenido protegido.</span><span class="sxs-lookup"><span data-stu-id="16770-115">Each license specifies one or more actions that can be performed with the protected content.</span></span> <span data-ttu-id="16770-116">Estas acciones, también denominadas derechos, se pueden limitar de varias maneras.</span><span class="sxs-lookup"><span data-stu-id="16770-116">These actions, also called rights, can be limited in a number of ways.</span></span> <span data-ttu-id="16770-117">Mediante la combinación de fechas de inicio, fechas de finalización, recuentos y límites de tiempo, el emisor de la licencia puede crear casi cualquier límite imaginable a la derecha.</span><span class="sxs-lookup"><span data-stu-id="16770-117">By combining start dates, end dates, counts, and time limits, the license issuer can create almost any imaginable limitation on a right.</span></span>

<span data-ttu-id="16770-118">Las licencias las emite un servicio Web.</span><span class="sxs-lookup"><span data-stu-id="16770-118">Licenses are issued by a Web service.</span></span> <span data-ttu-id="16770-119">Cuando se adquiere una licencia, se almacena en el equipo cliente en el almacén de licencias local, que es un archivo protegido que contiene licencias y otros datos DRM.</span><span class="sxs-lookup"><span data-stu-id="16770-119">When a license is acquired, it is stored on the client computer in the local license store, which is a protected file that contains licenses and other DRM data.</span></span> <span data-ttu-id="16770-120">Cuando una aplicación tiene acceso a contenido protegido, el subsistema DRM busca en el almacén de licencias local una licencia que conceda el derecho adecuado.</span><span class="sxs-lookup"><span data-stu-id="16770-120">When protected content is accessed by an application, the DRM subsystem searches the local license store for a license that grants the appropriate right.</span></span> <span data-ttu-id="16770-121">Si no se encuentra ninguna licencia, la aplicación puede adquirir una basada en la información almacenada en el encabezado DRM del archivo.</span><span class="sxs-lookup"><span data-stu-id="16770-121">If no license is found, the application can acquire one based on information stored in the DRM header of the file.</span></span>

<span data-ttu-id="16770-122">Se pueden emitir varias licencias para el mismo archivo protegido.</span><span class="sxs-lookup"><span data-stu-id="16770-122">Multiple licenses can be issued for the same protected file.</span></span> <span data-ttu-id="16770-123">Cuando el subsistema DRM determina si se permite una acción, agrega los derechos de todas las licencias que se aplican.</span><span class="sxs-lookup"><span data-stu-id="16770-123">When the DRM subsystem determines whether an action is allowed, it aggregates the rights from all licenses that apply.</span></span> <span data-ttu-id="16770-124">Se puede asignar una prioridad a cada licencia.</span><span class="sxs-lookup"><span data-stu-id="16770-124">Each license can be assigned a priority.</span></span> <span data-ttu-id="16770-125">Si se aplica más de una licencia a una acción, se comprueba la licencia de prioridad más alta para determinar si es necesario disminuir el número de recuentos.</span><span class="sxs-lookup"><span data-stu-id="16770-125">If more than one license applies to an action, the highest priority license is checked to determine whether counts need to be decremented.</span></span>

## <a name="related-topics"></a><span data-ttu-id="16770-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="16770-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16770-127">**Conceptos**</span><span class="sxs-lookup"><span data-stu-id="16770-127">**Concepts**</span></span>](drmconcepts.md)
</dt> </dl>

 

 




