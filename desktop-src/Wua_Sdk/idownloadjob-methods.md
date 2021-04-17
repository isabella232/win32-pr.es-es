---
description: La interfaz IDownloadJob define los siguientes métodos.
ms.assetid: b9a6b722-2e32-4177-bcef-514412e132ec
title: Métodos IDownloadJob
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f68acd6d7fef37c4ce9309c559a1de1b4d516dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542294"
---
# <a name="idownloadjob-methods"></a><span data-ttu-id="52cbf-103">Métodos IDownloadJob</span><span class="sxs-lookup"><span data-stu-id="52cbf-103">IDownloadJob Methods</span></span>

<span data-ttu-id="52cbf-104">La interfaz [**IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) define los siguientes métodos.</span><span class="sxs-lookup"><span data-stu-id="52cbf-104">The [**IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) interface defines the following methods.</span></span>



| <span data-ttu-id="52cbf-105">Método</span><span class="sxs-lookup"><span data-stu-id="52cbf-105">Method</span></span>                                            | <span data-ttu-id="52cbf-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="52cbf-106">Description</span></span>                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="52cbf-107">**Reparación**</span><span class="sxs-lookup"><span data-stu-id="52cbf-107">**CleanUp**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-cleanup)           | <span data-ttu-id="52cbf-108">Espera a que se complete una operación asincrónica y libera todas las devoluciones de llamada.</span><span class="sxs-lookup"><span data-stu-id="52cbf-108">Waits for an asynchronous operation to be completed and releases all callbacks.</span></span>                                        |
| [<span data-ttu-id="52cbf-109">**GetProgress**</span><span class="sxs-lookup"><span data-stu-id="52cbf-109">**GetProgress**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-getprogress)   | <span data-ttu-id="52cbf-110">Devuelve una interfaz [**IDownloadProgress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) que describe el progreso actual de una descarga.</span><span class="sxs-lookup"><span data-stu-id="52cbf-110">Returns an [**IDownloadProgress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) interface that describes the current progress of a download.</span></span> |
| [<span data-ttu-id="52cbf-111">**RequestAbort**</span><span class="sxs-lookup"><span data-stu-id="52cbf-111">**RequestAbort**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-requestabort) | <span data-ttu-id="52cbf-112">Realiza una solicitud para finalizar una descarga asincrónica.</span><span class="sxs-lookup"><span data-stu-id="52cbf-112">Makes a request to end an asynchronous download.</span></span>                                                                       |



 

 

 



