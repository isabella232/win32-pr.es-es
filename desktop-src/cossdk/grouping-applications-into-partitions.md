---
description: Agrupar aplicaciones en particiones
ms.assetid: bdfe2428-9769-4bcb-b74e-a141ba67a67e
title: Agrupar aplicaciones en particiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b35c726662d7dbe2cf039678ba5cdb4f94eeea
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677243"
---
# <a name="grouping-applications-into-partitions"></a><span data-ttu-id="1a9e1-103">Agrupar aplicaciones en particiones</span><span class="sxs-lookup"><span data-stu-id="1a9e1-103">Grouping Applications into Partitions</span></span>

<span data-ttu-id="1a9e1-104">A la hora de decidir cómo agrupar las aplicaciones en particiones, los administradores deben tener en cuenta ciertas reglas y restricciones, entre las que se incluyen las siguientes:</span><span class="sxs-lookup"><span data-stu-id="1a9e1-104">When deciding how to group applications into partitions, administrators need to be aware of certain rules and restrictions, including the following:</span></span>

-   <span data-ttu-id="1a9e1-105">Una aplicación se puede instalar en una o varias particiones.</span><span class="sxs-lookup"><span data-stu-id="1a9e1-105">An application can be installed into one or more partitions.</span></span>
-   <span data-ttu-id="1a9e1-106">Solo puede existir una instancia de un componente determinado en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="1a9e1-106">Only one instance of a given component can exist in an application.</span></span>

## <a name="public-and-private-components"></a><span data-ttu-id="1a9e1-107">Componentes públicos y privados</span><span class="sxs-lookup"><span data-stu-id="1a9e1-107">Public and Private Components</span></span>

<span data-ttu-id="1a9e1-108">Existen otras restricciones a la hora de decidir cómo agrupar aplicaciones COM+.</span><span class="sxs-lookup"><span data-stu-id="1a9e1-108">Other restrictions exist when deciding how to group COM+ applications.</span></span> <span data-ttu-id="1a9e1-109">Estas restricciones se aplican a los componentes públicos y privados dentro de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="1a9e1-109">These restrictions pertain to public versus private components within an application.</span></span> <span data-ttu-id="1a9e1-110">Los componentes de la aplicación generalmente pueden ser públicos o privados.</span><span class="sxs-lookup"><span data-stu-id="1a9e1-110">Application components can generally be either public or private.</span></span> <span data-ttu-id="1a9e1-111">Sin embargo, al agrupar las aplicaciones en particiones, los administradores deben tener en cuenta algunas restricciones en relación con los componentes públicos y privados.</span><span class="sxs-lookup"><span data-stu-id="1a9e1-111">However, when grouping applications into partitions, administrators should be aware of some restrictions around public and private components.</span></span> <span data-ttu-id="1a9e1-112">En la tabla siguiente se enumeran estas restricciones.</span><span class="sxs-lookup"><span data-stu-id="1a9e1-112">The following table lists these restrictions.</span></span>



| <span data-ttu-id="1a9e1-113">Si una aplicación es:</span><span class="sxs-lookup"><span data-stu-id="1a9e1-113">If an application is:</span></span>              | <span data-ttu-id="1a9e1-114">A continuación, los componentes de una partición pueden:</span><span class="sxs-lookup"><span data-stu-id="1a9e1-114">Then components in a partition can be:</span></span>                                                                                   |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a9e1-115">Una aplicación de servidor</span><span class="sxs-lookup"><span data-stu-id="1a9e1-115">A server application</span></span><br/>    | <span data-ttu-id="1a9e1-116">Público y privado.</span><span class="sxs-lookup"><span data-stu-id="1a9e1-116">Public and private.</span></span><br/>                                                                                           |
| <span data-ttu-id="1a9e1-117">Una aplicación de biblioteca</span><span class="sxs-lookup"><span data-stu-id="1a9e1-117">A library application</span></span><br/>   | <span data-ttu-id="1a9e1-118">Solo público.</span><span class="sxs-lookup"><span data-stu-id="1a9e1-118">Public only.</span></span> <span data-ttu-id="1a9e1-119">De lo contrario, la aplicación llamadores podría tener los mismos componentes, lo que crearía ambigüedad.</span><span class="sxs-lookup"><span data-stu-id="1a9e1-119">Otherwise, the callers application could have the same components, which would create ambiguity.</span></span><br/> |
| <span data-ttu-id="1a9e1-120">En la partición global</span><span class="sxs-lookup"><span data-stu-id="1a9e1-120">In the global partition</span></span><br/> | <span data-ttu-id="1a9e1-121">Solo público.</span><span class="sxs-lookup"><span data-stu-id="1a9e1-121">Public only.</span></span> <span data-ttu-id="1a9e1-122">Esto garantiza la compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="1a9e1-122">This ensures backward compatibility.</span></span><br/>                                                             |



 

## <a name="application-ids"></a><span data-ttu-id="1a9e1-123">Identificadores de aplicación</span><span class="sxs-lookup"><span data-stu-id="1a9e1-123">Application IDs</span></span>

<span data-ttu-id="1a9e1-124">Todas las aplicaciones COM+ instaladas en un equipo tienen un identificador de aplicación único.</span><span class="sxs-lookup"><span data-stu-id="1a9e1-124">Every COM+ application installed on a computer has a unique application ID.</span></span> <span data-ttu-id="1a9e1-125">Sin embargo, los nombres de aplicación solo deben ser únicos en una sola partición y no en todo el equipo.</span><span class="sxs-lookup"><span data-stu-id="1a9e1-125">However, application names need only be unique within a single partition and not on the entire computer.</span></span>

<span data-ttu-id="1a9e1-126">En la tabla siguiente se muestra lo que sucede con el identificador de la aplicación cuando una aplicación se importa en una partición o se exporta desde una partición.</span><span class="sxs-lookup"><span data-stu-id="1a9e1-126">The following table shows what happens to the application ID when an application is imported into a partition or exported from a partition.</span></span>



| <span data-ttu-id="1a9e1-127">Si una aplicación es:</span><span class="sxs-lookup"><span data-stu-id="1a9e1-127">If an application is:</span></span>                                              | <span data-ttu-id="1a9e1-128">Después, el identificador de la aplicación:</span><span class="sxs-lookup"><span data-stu-id="1a9e1-128">Then the application ID:</span></span>                    |
|--------------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="1a9e1-129">Importado a la partición global</span><span class="sxs-lookup"><span data-stu-id="1a9e1-129">Imported to the global partition</span></span><br/>                        | <span data-ttu-id="1a9e1-130">Sigue siendo el mismo</span><span class="sxs-lookup"><span data-stu-id="1a9e1-130">Remains the same</span></span><br/>                 |
| <span data-ttu-id="1a9e1-131">Importado a una partición distinta de la partición global</span><span class="sxs-lookup"><span data-stu-id="1a9e1-131">Imported to a partition other than the global partition</span></span><br/> | <span data-ttu-id="1a9e1-132">Cambiado</span><span class="sxs-lookup"><span data-stu-id="1a9e1-132">Is changed</span></span><br/>                       |
| <span data-ttu-id="1a9e1-133">Exportado</span><span class="sxs-lookup"><span data-stu-id="1a9e1-133">Exported</span></span><br/>                                                | <span data-ttu-id="1a9e1-134">Se incluye en el archivo exportado</span><span class="sxs-lookup"><span data-stu-id="1a9e1-134">Is included in the exported file</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="1a9e1-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1a9e1-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a9e1-136">Recopilación de métricas de partición</span><span class="sxs-lookup"><span data-stu-id="1a9e1-136">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="1a9e1-137">Configuración de la memoria caché de partición</span><span class="sxs-lookup"><span data-stu-id="1a9e1-137">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="1a9e1-138">Administrar particiones locales</span><span class="sxs-lookup"><span data-stu-id="1a9e1-138">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="1a9e1-139">Administrar particiones en Active Directory</span><span class="sxs-lookup"><span data-stu-id="1a9e1-139">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> <dt>

[<span data-ttu-id="1a9e1-140">Establecer derechos administrativos para una partición</span><span class="sxs-lookup"><span data-stu-id="1a9e1-140">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 




