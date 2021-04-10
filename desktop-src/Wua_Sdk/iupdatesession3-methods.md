---
description: La interfaz IUpdateSession3 define los siguientes métodos.
ms.assetid: 8015443a-e232-44ab-b53a-e8cc4acd4dd3
title: Métodos IUpdateSession3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd4126d8bae9e1ba768e574fd9520bdb6cf3d45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153825"
---
# <a name="iupdatesession3-methods"></a><span data-ttu-id="3c751-103">Métodos IUpdateSession3</span><span class="sxs-lookup"><span data-stu-id="3c751-103">IUpdateSession3 Methods</span></span>

<span data-ttu-id="3c751-104">La interfaz [**IUpdateSession3**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession3) define los siguientes métodos.</span><span class="sxs-lookup"><span data-stu-id="3c751-104">The [**IUpdateSession3**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession3) interface defines the following methods.</span></span>



| <span data-ttu-id="3c751-105">Método</span><span class="sxs-lookup"><span data-stu-id="3c751-105">Method</span></span>                                                                           | <span data-ttu-id="3c751-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="3c751-106">Description</span></span>                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c751-107">**CreateUpdateServiceManager**</span><span class="sxs-lookup"><span data-stu-id="3c751-107">**CreateUpdateServiceManager**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-createupdateservicemanager) | <span data-ttu-id="3c751-108">Devuelve un puntero a una interfaz [**IUpdateServiceManager2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager2) para la sesión.</span><span class="sxs-lookup"><span data-stu-id="3c751-108">Returns a pointer to an [**IUpdateServiceManager2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager2) interface for the session.</span></span>                                                                                                                                                                                                                |
| [<span data-ttu-id="3c751-109">**QueryHistory**</span><span class="sxs-lookup"><span data-stu-id="3c751-109">**QueryHistory**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory)                             | <span data-ttu-id="3c751-110">Devuelve un puntero a una interfaz [**IUpdateHistoryEntryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection) .</span><span class="sxs-lookup"><span data-stu-id="3c751-110">Returns a pointer to an [**IUpdateHistoryEntryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection) interface.</span></span> <span data-ttu-id="3c751-111">La interfaz contiene registros de eventos coincidentes en el equipo.</span><span class="sxs-lookup"><span data-stu-id="3c751-111">The interface contains matching event records on the computer.</span></span> <span data-ttu-id="3c751-112">Esto hace que el método [**QueryHistory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory) consulte de forma sincrónica el equipo para consultar el historial de eventos de actualización.</span><span class="sxs-lookup"><span data-stu-id="3c751-112">This causes the [**QueryHistory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession3-queryhistory) method to synchronously query the computer for the history of update events.</span></span> |



 

<span data-ttu-id="3c751-113">Para obtener información sobre los miembros heredados por esta interfaz, vea las siguientes interfaces:</span><span class="sxs-lookup"><span data-stu-id="3c751-113">For information about the members inherited by this interface, see the following interfaces:</span></span>

-   [<span data-ttu-id="3c751-114">**IUpdateSession2**</span><span class="sxs-lookup"><span data-stu-id="3c751-114">**IUpdateSession2**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)
-   [<span data-ttu-id="3c751-115">**IUpdateSession**</span><span class="sxs-lookup"><span data-stu-id="3c751-115">**IUpdateSession**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)

 

 



