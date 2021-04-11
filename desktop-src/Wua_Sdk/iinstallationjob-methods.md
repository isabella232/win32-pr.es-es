---
description: La interfaz IInstallationJob define los siguientes métodos.
ms.assetid: 4990ef7c-b6cd-46fc-9e7d-8d1d78edc9f2
title: Métodos IInstallationJob
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa0c1a5850f3d71ad1a6a51046fe890ea9bc7426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154513"
---
# <a name="iinstallationjob-methods"></a><span data-ttu-id="49046-103">Métodos IInstallationJob</span><span class="sxs-lookup"><span data-stu-id="49046-103">IInstallationJob Methods</span></span>

<span data-ttu-id="49046-104">La interfaz [**IInstallationJob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) define los siguientes métodos.</span><span class="sxs-lookup"><span data-stu-id="49046-104">The [**IInstallationJob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) interface defines the following methods.</span></span>



| <span data-ttu-id="49046-105">Método</span><span class="sxs-lookup"><span data-stu-id="49046-105">Method</span></span>                                                | <span data-ttu-id="49046-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="49046-106">Description</span></span>                                                                                                                                           |
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="49046-107">**Reparación**</span><span class="sxs-lookup"><span data-stu-id="49046-107">**CleanUp**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-cleanup)           | <span data-ttu-id="49046-108">Espera a que se complete una operación asincrónica y, a continuación, libera todas las devoluciones de llamada.</span><span class="sxs-lookup"><span data-stu-id="49046-108">Waits for an asynchronous operation to be completed and then releases all the callbacks.</span></span>                                                              |
| [<span data-ttu-id="49046-109">**GetProgress**</span><span class="sxs-lookup"><span data-stu-id="49046-109">**GetProgress**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-getprogress)   | <span data-ttu-id="49046-110">Devuelve una interfaz [**IInstallationProgress**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationprogress) que describe el progreso actual de una instalación o desinstalación.</span><span class="sxs-lookup"><span data-stu-id="49046-110">Returns an [**IInstallationProgress**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationprogress) interface that describes the current progress of an installation or uninstallation.</span></span> |
| [<span data-ttu-id="49046-111">**RequestAbort**</span><span class="sxs-lookup"><span data-stu-id="49046-111">**RequestAbort**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-requestabort) | <span data-ttu-id="49046-112">Realiza una solicitud para cancelar la instalación o desinstalación.</span><span class="sxs-lookup"><span data-stu-id="49046-112">Makes a request to cancel the installation or uninstallation.</span></span>                                                                                         |



 

 

 



