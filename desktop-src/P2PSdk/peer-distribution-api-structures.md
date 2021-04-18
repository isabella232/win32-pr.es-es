---
description: El servicio de distribución del mismo nivel de Microsoft es compatible con las siguientes estructuras.
ms.assetid: 26badfe6-3a5a-4c2e-9ef1-534c2e8573d0
title: Estructuras de API de distribución del mismo nivel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc9fbf86c242406aa86b7dd30497ba4c5085488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667409"
---
# <a name="peer-distribution-api-structures"></a><span data-ttu-id="97606-103">Estructuras de API de distribución del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="97606-103">Peer Distribution API Structures</span></span>

<span data-ttu-id="97606-104">El servicio de distribución del mismo nivel de Microsoft es compatible con las siguientes estructuras.</span><span class="sxs-lookup"><span data-stu-id="97606-104">The Microsoft Peer Distribution service supports the following structures.</span></span>



| <span data-ttu-id="97606-105">Estructura</span><span class="sxs-lookup"><span data-stu-id="97606-105">Structure</span></span>                                                              | <span data-ttu-id="97606-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="97606-106">Description</span></span>                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="97606-107">**\_ \_ información básica del cliente de PEERDIST \_**</span><span class="sxs-lookup"><span data-stu-id="97606-107">**PEERDIST\_CLIENT\_BASIC\_INFO**</span></span>](/windows/desktop/api/peerdist/ns-peerdist-peerdist_client_basic_info)    | <span data-ttu-id="97606-108">Indica si hay muchos clientes que descargan simultáneamente el mismo contenido.</span><span class="sxs-lookup"><span data-stu-id="97606-108">Indicates whether or not there are many clients simultaneously downloading the same content.</span></span>                                                                                                                                                                                             |
| [<span data-ttu-id="97606-109">**\_etiqueta de contenido de PEERDIST \_**</span><span class="sxs-lookup"><span data-stu-id="97606-109">**PEERDIST\_CONTENT\_TAG**</span></span>](/windows/win32/api/peerdist/ns-peerdist-peerdist_content_tag)                 | <span data-ttu-id="97606-110">Contiene una etiqueta suministrada por el cliente que es un valor de entrada para [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent).</span><span class="sxs-lookup"><span data-stu-id="97606-110">Contains a client supplied tag which is an input value for [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent).</span></span> <span data-ttu-id="97606-111">La etiqueta está asociada con el segmento de contenido y se usa en las API de administración de contenido, como [**PeerDistClientFlushContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientflushcontent).</span><span class="sxs-lookup"><span data-stu-id="97606-111">The tag is associated with the content segment and is used in content management APIs, like [**PeerDistClientFlushContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientflushcontent).</span></span> |
| [<span data-ttu-id="97606-112">**\_Opciones de publicación de PEERDIST \_**</span><span class="sxs-lookup"><span data-stu-id="97606-112">**PEERDIST\_PUBLICATION\_OPTIONS**</span></span>](/windows/desktop/api/peerdist/ns-peerdist-peerdist_publication_options) | <span data-ttu-id="97606-113">Contiene opciones de publicación, incluida la información de versión de la API y posibles marcas de opciones.</span><span class="sxs-lookup"><span data-stu-id="97606-113">Contains publication options, including the API version information and possible option flags.</span></span>                                                                                                                                                                                           |
| [<span data-ttu-id="97606-114">**\_Opciones de recuperación del mismo nivel \_**</span><span class="sxs-lookup"><span data-stu-id="97606-114">**PEER\_RETRIEVAL\_OPTIONS**</span></span>](/windows/desktop/api/peerdist/ns-peerdist-peerdist_retrieval_options)         | <span data-ttu-id="97606-115">Contiene la versión de la información de contenido que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="97606-115">Contains version of the content information to retrieve.</span></span>                                                                                                                                                                                                                                 |
| [<span data-ttu-id="97606-116">**\_información de estado de PEERDIST \_**</span><span class="sxs-lookup"><span data-stu-id="97606-116">**PEERDIST\_STATUS\_INFO**</span></span>](/windows/desktop/api/peerdist/ns-peerdist-peerdist_status_info)                 | <span data-ttu-id="97606-117">Contiene información sobre el estado actual y las capacidades del servicio BranchCache en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="97606-117">Contains information about the current status and capabilities of the BranchCache service on the local computer.</span></span>                                                                                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="97606-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="97606-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97606-119">Referencia de la API de distribución del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="97606-119">Peer Distribution API Reference</span></span>](peer-distribution-api-reference.md)
</dt> </dl>

 

 



