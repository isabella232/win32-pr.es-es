---
title: Problemas con varios subprocesos
description: Problemas con varios subprocesos
ms.assetid: 17e74d2a-af4f-4188-89fa-b4f50abc424f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0910e1602d00d3429bb9e4c7a1667bf8113cd659
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419214"
---
# <a name="multi-threaded-issues"></a><span data-ttu-id="d853d-103">Problemas con varios subprocesos</span><span class="sxs-lookup"><span data-stu-id="d853d-103">Multi-Threaded Issues</span></span>

<span data-ttu-id="d853d-104">OLE proporciona compatibilidad con aplicaciones multiproceso, lo que permite a las aplicaciones realizar llamadas OLE desde varios subprocesos.</span><span class="sxs-lookup"><span data-stu-id="d853d-104">OLE provides support for multithreaded applications, allowing applications to make OLE calls from multiple threads.</span></span> <span data-ttu-id="d853d-105">Esta compatibilidad con multiproceso se conoce como el modelo de apartamento, es importante que todos los componentes OLE que usan varios subprocesos sigan este modelo.</span><span class="sxs-lookup"><span data-stu-id="d853d-105">This multithreaded support is called the apartment model, it is important that all OLE components using multiple threads follow this model.</span></span> <span data-ttu-id="d853d-106">El modelo de Apartamento requiere que se calculen las referencias de los punteros de interfaz (mediante [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface)y [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)) cuando se pasan entre subprocesos.</span><span class="sxs-lookup"><span data-stu-id="d853d-106">The apartment model requires that interface pointers are marshaled (using [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface), and [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)) when passed between threads.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d853d-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d853d-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d853d-108">Procesos, subprocesos y apartamentos</span><span class="sxs-lookup"><span data-stu-id="d853d-108">Processes, Threads, and Apartments</span></span>](processes--threads--and-apartments.md)
</dt> </dl>

 

 




