---
description: Las siguientes interfaces COM se utilizan para desarrollar monitores.
ms.assetid: 619991f5-1db1-400a-bf18-d4a6dd6999a8
title: Supervisión de interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66bb06e6153d18c7b0a4291df1c7520380a29844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666540"
---
# <a name="monitor-interfaces"></a><span data-ttu-id="b4aba-103">Supervisión de interfaces</span><span class="sxs-lookup"><span data-stu-id="b4aba-103">Monitor Interfaces</span></span>

<span data-ttu-id="b4aba-104">Las siguientes interfaces COM se utilizan para desarrollar monitores.</span><span class="sxs-lookup"><span data-stu-id="b4aba-104">The following COM interfaces are used to develop monitors.</span></span>



| <span data-ttu-id="b4aba-105">Interfaz</span><span class="sxs-lookup"><span data-stu-id="b4aba-105">Interface</span></span>                              | <span data-ttu-id="b4aba-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4aba-106">Description</span></span>                                                                                                                                             |
|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b4aba-107">IMonitor</span><span class="sxs-lookup"><span data-stu-id="b4aba-107">IMonitor</span></span>](imonitor.md)               | <span data-ttu-id="b4aba-108">Proporciona métodos que controlan la operación de supervisión.</span><span class="sxs-lookup"><span data-stu-id="b4aba-108">Provides methods that control monitor operation.</span></span> <span data-ttu-id="b4aba-109">El monitor debe implementar esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="b4aba-109">This interface must be implemented by the monitor.</span></span>                                                     |
| [<span data-ttu-id="b4aba-110">IMonitorEventer</span><span class="sxs-lookup"><span data-stu-id="b4aba-110">IMonitorEventer</span></span>](imonitoreventer.md) | <span data-ttu-id="b4aba-111">Proporciona métodos que se usan para enviar eventos.</span><span class="sxs-lookup"><span data-stu-id="b4aba-111">Provides methods used to send events.</span></span> <span data-ttu-id="b4aba-112">Esta interfaz la proporciona el [*servicio de control de supervisión*](m.md) (MCSVC).</span><span class="sxs-lookup"><span data-stu-id="b4aba-112">This interface is provided by the [*Monitor Control Service*](m.md) (MCSVC).</span></span> |



 

 

 



