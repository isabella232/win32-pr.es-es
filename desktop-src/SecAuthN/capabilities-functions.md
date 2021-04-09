---
description: La API del proveedor de red especifica una función de funcionalidad única.
ms.assetid: fc74a043-da13-485f-9f54-a43064add927
title: Funciones de funcionalidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83cde32ba0d3116ce83e7ca6621666f5e9a86650
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082404"
---
# <a name="capabilities-functions"></a><span data-ttu-id="79d34-103">Funciones de funcionalidad</span><span class="sxs-lookup"><span data-stu-id="79d34-103">Capabilities Functions</span></span>

<span data-ttu-id="79d34-104">La API del proveedor de red especifica una función de funcionalidad única.</span><span class="sxs-lookup"><span data-stu-id="79d34-104">The Network Provider API specifies a single capabilities function.</span></span> <span data-ttu-id="79d34-105">Cuando el sistema operativo solicita información acerca de las capacidades de un proveedor de red, el [*enrutador de proveedor múltiple*](/windows/desktop/SecGloss/m-gly) (MPR) llama a la función [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) de cada proveedor de red cuya red está activa.</span><span class="sxs-lookup"><span data-stu-id="79d34-105">When the operating system requests information about a network provider's capabilities, the [*Multiple Provider Router*](/windows/desktop/SecGloss/m-gly) (MPR) calls the [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) function of each network provider whose network is active.</span></span>

<span data-ttu-id="79d34-106">La función [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) devuelve una máscara de máscara que indica qué funciones de la API de proveedor de red admite el proveedor de red.</span><span class="sxs-lookup"><span data-stu-id="79d34-106">The [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) function returns a bitmask indicating which functions of the Network Provider API the network provider supports.</span></span> <span data-ttu-id="79d34-107">La función **NPGetCaps** es la única función que un proveedor de red debe implementar.</span><span class="sxs-lookup"><span data-stu-id="79d34-107">The **NPGetCaps** function is the only function that a network provider must implement.</span></span> <span data-ttu-id="79d34-108">El sistema operativo llama a esta función para determinar qué otras funciones de la API del proveedor de red admite el proveedor.</span><span class="sxs-lookup"><span data-stu-id="79d34-108">The operating system calls this function to determine which other functions of the Network Provider API the provider supports.</span></span>

 

 
