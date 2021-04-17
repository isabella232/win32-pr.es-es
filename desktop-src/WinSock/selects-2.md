---
description: En la interfaz de socket original de distribución de software (BSD), la función Select era el estándar (y solo), para obtener indicaciones de eventos de red.
ms.assetid: f7f42b03-1f89-4801-abf0-396ff8b61cae
title: Selecciona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e50339f298c18c75ad6451590f191fc1bd8afba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706105"
---
# <a name="selects"></a><span data-ttu-id="7d2a3-103">Selecciona</span><span class="sxs-lookup"><span data-stu-id="7d2a3-103">Selects</span></span>

<span data-ttu-id="7d2a3-104">En la interfaz de socket original de distribución de software (BSD), la función [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) era el estándar (y solo), para obtener indicaciones de eventos de red.</span><span class="sxs-lookup"><span data-stu-id="7d2a3-104">In the original Berkeley Software Distribution (BSD) socket interface the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) function was the standard (and only) means to obtain network event indications.</span></span> <span data-ttu-id="7d2a3-105">Para cada socket, la información sobre el estado de lectura, escritura o error se puede sondear o esperar.</span><span class="sxs-lookup"><span data-stu-id="7d2a3-105">For each socket, information on read, write, or error status can be polled or waited on.</span></span> <span data-ttu-id="7d2a3-106">Vea [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="7d2a3-106">See [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) for more information.</span></span> <span data-ttu-id="7d2a3-107">Tenga en cuenta que \_ este enfoque no puede obtener el QoS del evento FD de red.</span><span class="sxs-lookup"><span data-stu-id="7d2a3-107">Note that network event FD\_QOS cannot be obtained by this approach.</span></span>

 

 
