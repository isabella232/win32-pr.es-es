---
description: La API de distribución del mismo nivel define los siguientes tipos de datos.
ms.assetid: 5a378965-696c-4205-b9de-bdf93f00018f
title: Tipos de datos de la API de distribución del mismo nivel (Peerdist. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a7bff6fe75c8f4632248c92af37aea6e00c3052
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667412"
---
# <a name="peer-distribution-api-data-types"></a><span data-ttu-id="c5c78-103">Tipos de datos de la API de distribución del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="c5c78-103">Peer Distribution API Data Types</span></span>

<span data-ttu-id="c5c78-104">La API de distribución del mismo nivel define los siguientes tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="c5c78-104">The Peer Distribution API defines the following data types.</span></span>


```C++
typedef HANDLE PEERDIST_INSTANCE_HANDLE;
typedef HANDLE PEERDIST_CONTENT_HANDLE;
typedef HANDLE PEERDIST_CONTENTINFO_HANDLE;
typedef HANDLE PEERDIST_STREAM_HANDLE;
```





| <span data-ttu-id="c5c78-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c5c78-105">Data type</span></span>                                                                                                                     | <span data-ttu-id="c5c78-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5c78-106">Description</span></span>                                                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5c78-107"><span id="PEERDIST_INSTANCE_HANDLE"></span><span id="peerdist_instance_handle"></span>**\_identificador de instancia de PEERDIST \_**</span><span class="sxs-lookup"><span data-stu-id="c5c78-107"><span id="PEERDIST_INSTANCE_HANDLE"></span><span id="peerdist_instance_handle"></span>**PEERDIST\_INSTANCE\_HANDLE**</span></span>          | <span data-ttu-id="c5c78-108">Identificador asociado a la instancia de distribución del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="c5c78-108">A handle associated with the Peer Distribution instance.</span></span> <span data-ttu-id="c5c78-109">[**PeerDistStartup**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup)crea este identificador y se usa en la mayoría de las operaciones de distribución del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="c5c78-109">This handle is created by [**PeerDistStartup**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup), and used in most Peer Distribution operations.</span></span><br/>                                          |
| <span data-ttu-id="c5c78-110"><span id="PEERDIST_CONTENT_HANDLE"></span><span id="peerdist_content_handle"></span>**\_identificador de contenido de PEERDIST \_**</span><span class="sxs-lookup"><span data-stu-id="c5c78-110"><span id="PEERDIST_CONTENT_HANDLE"></span><span id="peerdist_content_handle"></span>**PEERDIST\_CONTENT\_HANDLE**</span></span>             | <span data-ttu-id="c5c78-111">Identificador asociado con el contenido.</span><span class="sxs-lookup"><span data-stu-id="c5c78-111">A handle associated with content.</span></span> <span data-ttu-id="c5c78-112">Este identificador se crea mediante [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent) y se hace referencia a él al abrir, cerrar, agregar o publicar contenido.</span><span class="sxs-lookup"><span data-stu-id="c5c78-112">This handle is created by [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent) and is referenced when opening, closing, adding, or publishing content.</span></span><br/>                     |
| <span data-ttu-id="c5c78-113"><span id="PEERDIST_CONTENTINFO_HANDLE"></span><span id="peerdist_contentinfo_handle"></span>**\_identificador de CONTENTINFO de PEERDIST \_**</span><span class="sxs-lookup"><span data-stu-id="c5c78-113"><span id="PEERDIST_CONTENTINFO_HANDLE"></span><span id="peerdist_contentinfo_handle"></span>**PEERDIST\_CONTENTINFO\_HANDLE**</span></span> | <span data-ttu-id="c5c78-114">Identificador asociado a la información de contenido.</span><span class="sxs-lookup"><span data-stu-id="c5c78-114">A handle associated with content information.</span></span> <span data-ttu-id="c5c78-115">[**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)crea este identificador y se utiliza al recuperar la información de contenido codificado.</span><span class="sxs-lookup"><span data-stu-id="c5c78-115">This handle is created by [**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation), and is used when retrieving encoded content information.</span></span><br/> |
| <span data-ttu-id="c5c78-116"><span id="PEERDIST_STREAM_HANDLE"></span><span id="peerdist_stream_handle"></span>**\_identificador de flujo de PEERDIST \_**</span><span class="sxs-lookup"><span data-stu-id="c5c78-116"><span id="PEERDIST_STREAM_HANDLE"></span><span id="peerdist_stream_handle"></span>**PEERDIST\_STREAM\_HANDLE**</span></span>                | <span data-ttu-id="c5c78-117">Identificador asociado a un flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="c5c78-117">A handle associated with a data stream.</span></span> <span data-ttu-id="c5c78-118">Este identificador se crea mediante [**PeerDistServerPublishStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream) y se hace referencia a él al publicar, cerrar o agregar a contenido transmitido.</span><span class="sxs-lookup"><span data-stu-id="c5c78-118">This handle is created by [**PeerDistServerPublishStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream) and is referenced when publishing, closing, or adding to streamed content.</span></span><br/>        |



## <a name="requirements"></a><span data-ttu-id="c5c78-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5c78-119">Requirements</span></span>



| <span data-ttu-id="c5c78-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5c78-120">Requirement</span></span> | <span data-ttu-id="c5c78-121">Value</span><span class="sxs-lookup"><span data-stu-id="c5c78-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c5c78-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5c78-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c5c78-123">Solo aplicaciones de escritorio de Windows 7 Professional \[\]</span><span class="sxs-lookup"><span data-stu-id="c5c78-123">Windows 7 Professional \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c5c78-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5c78-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c5c78-125">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c5c78-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c5c78-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c5c78-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5c78-127"><dt>Peerdist. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5c78-127"><dt>Peerdist.h</dt></span></span> </dl> |



 

 




