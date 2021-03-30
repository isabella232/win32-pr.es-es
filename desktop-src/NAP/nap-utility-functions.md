---
title: Funciones de la utilidad NAP
description: Las siguientes funciones de utilidad admiten la API de NAP.
ms.assetid: 0819067c-cca5-4140-8b4d-f3b996826152
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260c423909011c81f52ea89ce8d3137b35c55167
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775336"
---
# <a name="nap-utility-functions"></a><span data-ttu-id="d4b14-103">Funciones de la utilidad NAP</span><span class="sxs-lookup"><span data-stu-id="d4b14-103">NAP Utility Functions</span></span>

> [!Note]  
> <span data-ttu-id="d4b14-104">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="d4b14-104">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="d4b14-105">Las siguientes funciones de utilidad admiten la API de NAP.</span><span class="sxs-lookup"><span data-stu-id="d4b14-105">The following utility functions support the NAP API.</span></span>

<span data-ttu-id="d4b14-106">Todas las interfaces COM que admite el sistema NAP usan reglas estándar de administración de memoria COM y el asignador de memoria COM (CoTaskMemAlloc y CoTaskMemFree).</span><span class="sxs-lookup"><span data-stu-id="d4b14-106">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocator (CoTaskMemAlloc and CoTaskMemFree).</span></span>

-   <span data-ttu-id="d4b14-107">IN Parameters: se asigna y libera por el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="d4b14-107">IN parameters — allocated and freed by caller.</span></span>
-   <span data-ttu-id="d4b14-108">Parámetros OUT (asignados por el destinatario) liberados por el llamador mediante CoTaskMem \* ()</span><span class="sxs-lookup"><span data-stu-id="d4b14-108">OUT parameters — allocated by callee, freed by caller using CoTaskMem\*()</span></span>
-   <span data-ttu-id="d4b14-109">Parámetros IN/OUT: asignados por el autor de la llamada, liberados y reasignados por el destinatario, que en última instancia ha liberado el llamador, mediante CoTaskMem \* ()</span><span class="sxs-lookup"><span data-stu-id="d4b14-109">IN/OUT parameters — allocated by caller, freed and reallocated by callee, ultimately freed by caller, using CoTaskMem\*()</span></span>

<span data-ttu-id="d4b14-110">En las funciones FreeXxx (), también se liberarán todos los punteros incrustados.</span><span class="sxs-lookup"><span data-stu-id="d4b14-110">In the FreeXxx() functions, all embedded pointers will also be freed.</span></span>

-   [<span data-ttu-id="d4b14-111">**AllocConnections**</span><span class="sxs-lookup"><span data-stu-id="d4b14-111">**AllocConnections**</span></span>](allocconnections-func.md)
-   [<span data-ttu-id="d4b14-112">**AllocCountedString**</span><span class="sxs-lookup"><span data-stu-id="d4b14-112">**AllocCountedString**</span></span>](alloccountedstring-func.md)
-   [<span data-ttu-id="d4b14-113">**AllocFixupInfo**</span><span class="sxs-lookup"><span data-stu-id="d4b14-113">**AllocFixupInfo**</span></span>](allocfixupinfo-func.md)
-   [<span data-ttu-id="d4b14-114">**FreeConnections**</span><span class="sxs-lookup"><span data-stu-id="d4b14-114">**FreeConnections**</span></span>](freeconnections-func.md)
-   [<span data-ttu-id="d4b14-115">**FreeCountedString**</span><span class="sxs-lookup"><span data-stu-id="d4b14-115">**FreeCountedString**</span></span>](freecountedstring-func.md)
-   [<span data-ttu-id="d4b14-116">**FreeFixupInfo**</span><span class="sxs-lookup"><span data-stu-id="d4b14-116">**FreeFixupInfo**</span></span>](freefixupinfo-func.md)
-   [<span data-ttu-id="d4b14-117">**FreeIsolationInfo**</span><span class="sxs-lookup"><span data-stu-id="d4b14-117">**FreeIsolationInfo**</span></span>](freeisolationinfo-func.md)
-   [<span data-ttu-id="d4b14-118">**FreeIsolationInfoEx**</span><span class="sxs-lookup"><span data-stu-id="d4b14-118">**FreeIsolationInfoEx**</span></span>](freeisolationinfoex.md)
-   [<span data-ttu-id="d4b14-119">**FreeNapComponentRegistrationInfoArray**</span><span class="sxs-lookup"><span data-stu-id="d4b14-119">**FreeNapComponentRegistrationInfoArray**</span></span>](freenapcomponentregistrationinfoarray-func.md)
-   [<span data-ttu-id="d4b14-120">**FreeNetworkSoH**</span><span class="sxs-lookup"><span data-stu-id="d4b14-120">**FreeNetworkSoH**</span></span>](freenetworksoh-func.md)
-   [<span data-ttu-id="d4b14-121">**FreePrivateData**</span><span class="sxs-lookup"><span data-stu-id="d4b14-121">**FreePrivateData**</span></span>](freeprivatedata-func.md)
-   [<span data-ttu-id="d4b14-122">**FreeSoH**</span><span class="sxs-lookup"><span data-stu-id="d4b14-122">**FreeSoH**</span></span>](freesoh-func.md)
-   [<span data-ttu-id="d4b14-123">**FreeSoHAttributeValue**</span><span class="sxs-lookup"><span data-stu-id="d4b14-123">**FreeSoHAttributeValue**</span></span>](freesohattributevalue-func.md)
-   [<span data-ttu-id="d4b14-124">**FreeSystemHealthAgentState**</span><span class="sxs-lookup"><span data-stu-id="d4b14-124">**FreeSystemHealthAgentState**</span></span>](freesystemhealthagentstate-func.md)
-   [<span data-ttu-id="d4b14-125">**InitializeNapAgentNotifier**</span><span class="sxs-lookup"><span data-stu-id="d4b14-125">**InitializeNapAgentNotifier**</span></span>](initializenapagentnotifier.md)
-   [<span data-ttu-id="d4b14-126">**UninitializeNapAgentNotifier**</span><span class="sxs-lookup"><span data-stu-id="d4b14-126">**UninitializeNapAgentNotifier**</span></span>](uninitializenapagentnotifier.md)

 

 




