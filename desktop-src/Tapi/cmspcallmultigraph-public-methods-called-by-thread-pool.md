---
description: La lista siguiente contiene los métodos públicos CMSPCallMultiGraph llamados por el grupo de subprocesos.
ms.assetid: f0a5f621-99c4-40f0-8a0e-0e43792e00a1
title: CMSPCallMultiGraph métodos públicos, llamado por el grupo de subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3878298024164a4c940b96dceb88e0ff005d59ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105677945"
---
# <a name="cmspcallmultigraph-public-methods-called-by-thread-pool"></a><span data-ttu-id="f3440-103">CMSPCallMultiGraph métodos públicos, llamado por el grupo de subprocesos</span><span class="sxs-lookup"><span data-stu-id="f3440-103">CMSPCallMultiGraph Public Methods, Called by Thread Pool</span></span>



| <span data-ttu-id="f3440-104">Métodos públicos de CMSPCallMultiGraph</span><span class="sxs-lookup"><span data-stu-id="f3440-104">CMSPCallMultiGraph public methods</span></span>                                   | <span data-ttu-id="f3440-105">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3440-105">Description</span></span>                                                                                                                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f3440-106">**DispatchGraphEvent**</span><span class="sxs-lookup"><span data-stu-id="f3440-106">**DispatchGraphEvent**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-dispatchgraphevent) | <span data-ttu-id="f3440-107">Se llama cuando el gráfico de filtro señala un evento.</span><span class="sxs-lookup"><span data-stu-id="f3440-107">Called when the filter graph signals an event.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="f3440-108">**HandleGraphEvent**</span><span class="sxs-lookup"><span data-stu-id="f3440-108">**HandleGraphEvent**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-handlegraphevent)     | <span data-ttu-id="f3440-109">Llamado por el método estático [**DispatchGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-dispatchgraphevent) .</span><span class="sxs-lookup"><span data-stu-id="f3440-109">Called by the [**DispatchGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-dispatchgraphevent) static method.</span></span> <span data-ttu-id="f3440-110">Pone en cola [**ProcessGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-processgraphevent) en el subproceso de trabajo MSP principal.</span><span class="sxs-lookup"><span data-stu-id="f3440-110">Queues [**ProcessGraphEvent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-processgraphevent) on the main MSP worker thread.</span></span> |
| [<span data-ttu-id="f3440-111">**ProcessGraphEvent**</span><span class="sxs-lookup"><span data-stu-id="f3440-111">**ProcessGraphEvent**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-processgraphevent)   | <span data-ttu-id="f3440-112">Permite que la instancia del objeto de llamada MSP controle el evento de gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="f3440-112">Allows the MSP call object instance to handle the filter graph event.</span></span>                                                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="f3440-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f3440-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3440-114">**CMSPCallMultiGraph**</span><span class="sxs-lookup"><span data-stu-id="f3440-114">**CMSPCallMultiGraph**</span></span>](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallmultigraph)
</dt> </dl>

 

 



