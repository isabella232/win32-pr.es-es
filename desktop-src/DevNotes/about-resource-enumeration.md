---
description: La enumeración de recursos proporciona una vista cercana y precisa de la actividad de instrumentación que tiene lugar cuando se ejecuta una aplicación.
ms.assetid: 4a421006-32ff-4555-a3c8-69fffdb46845
title: Acerca de la enumeración de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 601e65550dacbd07d493f35a6c35fece98657b6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659303"
---
# <a name="about-resource-enumeration"></a><span data-ttu-id="2bf8d-103">Acerca de la enumeración de recursos</span><span class="sxs-lookup"><span data-stu-id="2bf8d-103">About Resource Enumeration</span></span>

<span data-ttu-id="2bf8d-104">La enumeración de recursos proporciona una vista cercana y precisa de la actividad de instrumentación que tiene lugar cuando se ejecuta una aplicación.</span><span class="sxs-lookup"><span data-stu-id="2bf8d-104">Resource enumeration provides a close and precise view of instrumentation activity that takes place when an application is running.</span></span> <span data-ttu-id="2bf8d-105">La información de instrumentación se puede abstraer y clasificar como un conjunto de elementos específicos del proceso como parte del proceso de depuración.</span><span class="sxs-lookup"><span data-stu-id="2bf8d-105">The instrumentation information can be abstracted and categorized as a set of process-specific items as part of the debugging process.</span></span>

<span data-ttu-id="2bf8d-106">Las herramientas, como los depuradores, suelen requerir el acceso a la información de instrumentación, pero pueden encontrar que no está disponible.</span><span class="sxs-lookup"><span data-stu-id="2bf8d-106">Tools, such as debuggers, often require access to instrumentation information but may find it is unavailable.</span></span> <span data-ttu-id="2bf8d-107">Para solucionar este problema, la función [**VerifierEnumerateResource**](/windows/desktop/api/Avrfsdk/nf-avrfsdk-verifierenumerateresource) extrae este tipo de información de las aplicaciones para proporcionar una mejor información de contexto para el problema que se está depurando.</span><span class="sxs-lookup"><span data-stu-id="2bf8d-107">To solve this problem, the [**VerifierEnumerateResource**](/windows/desktop/api/Avrfsdk/nf-avrfsdk-verifierenumerateresource) function extracts this type of information from applications to provide better context information for the problem being debugged.</span></span>

 

 



