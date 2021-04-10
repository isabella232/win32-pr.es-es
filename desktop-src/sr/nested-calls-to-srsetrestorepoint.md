---
title: Llamadas anidadas a SRSetRestorePoint
description: En este tema se describe la compatibilidad con llamadas anidadas a SRSetRestorePoint a través de los \_ tipos de eventos Begin Nested \_ System Change \_ y end \_ Nested \_ System \_ Change.
ms.assetid: ee2dea47-f95d-4293-ac33-eff622b84db6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5654dc7bb6e42ae55cbad18fc2418df3bdd942d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268878"
---
# <a name="nested-calls-to-srsetrestorepoint"></a><span data-ttu-id="b03a3-103">Llamadas anidadas a SRSetRestorePoint</span><span class="sxs-lookup"><span data-stu-id="b03a3-103">Nested Calls to SRSetRestorePoint</span></span>

<span data-ttu-id="b03a3-104">En este tema se describe la compatibilidad con llamadas anidadas a [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) a través de los \_ tipos de eventos Begin Nested System Change \_ \_ y end \_ Nested \_ System \_ Change.</span><span class="sxs-lookup"><span data-stu-id="b03a3-104">This topic describes support for nested calls to [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) through the BEGIN\_NESTED\_SYSTEM\_CHANGE and END\_NESTED\_SYSTEM\_CHANGE event types.</span></span>

<span data-ttu-id="b03a3-105">Las aplicaciones pueden llamar a [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) con seguridad cuando se usan estos tipos de eventos.</span><span class="sxs-lookup"><span data-stu-id="b03a3-105">Applications can safely call [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) when using these event types.</span></span> <span data-ttu-id="b03a3-106">La primera llamada a la función crea un punto de restauración.</span><span class="sxs-lookup"><span data-stu-id="b03a3-106">The first call to the function creates a restore point.</span></span> <span data-ttu-id="b03a3-107">Las llamadas anidadas subsiguientes a la función no crean puntos de restauración.</span><span class="sxs-lookup"><span data-stu-id="b03a3-107">Subsequent nested calls to the function do not create restore points.</span></span> <span data-ttu-id="b03a3-108">Por ejemplo, supongamos que una aplicación realiza las siguientes llamadas a **SRSetRestorePoint**:</span><span class="sxs-lookup"><span data-stu-id="b03a3-108">For example, suppose an application makes the following calls to **SRSetRestorePoint**:</span></span><dl> <span data-ttu-id="b03a3-109">Para el punto de restauración A con dwEventType = iniciar \_ cambio de sistema anidado \_ \_</span><span class="sxs-lookup"><span data-stu-id="b03a3-109">For restore point A with dwEventType = BEGIN\_NESTED\_SYSTEM\_CHANGE</span></span>  
<span data-ttu-id="b03a3-110">Para el punto de restauración B con dwEventType = BEGIN \_ Nested \_ System \_ Change</span><span class="sxs-lookup"><span data-stu-id="b03a3-110">For restore point B with dwEventType = BEGIN\_NESTED\_SYSTEM\_CHANGE</span></span>  
<span data-ttu-id="b03a3-111">Para el punto de restauración B con dwEventType = fin de \_ cambiar el sistema anidado \_ \_</span><span class="sxs-lookup"><span data-stu-id="b03a3-111">For restore point B with dwEventType = END\_NESTED\_SYSTEM\_CHANGE</span></span>  
<span data-ttu-id="b03a3-112">Para el punto de restauración A con dwEventType = fin de \_ \_ cambio del sistema anidado \_</span><span class="sxs-lookup"><span data-stu-id="b03a3-112">For restore point A with dwEventType = END\_NESTED\_SYSTEM\_CHANGE</span></span>  
</dl>

<span data-ttu-id="b03a3-113">La segunda llamada no crea un nuevo punto de restauración porque la llamada está anidada.</span><span class="sxs-lookup"><span data-stu-id="b03a3-113">The second call does not create a new restore point because the call is nested.</span></span>

 

 




