---
description: Para administrar registros, puede trabajar con información que se almacena en estructuras de registro del mismo nivel \_ .
ms.assetid: d38ea2d3-5cfb-4c4a-a63f-b274aa0dfe71
title: Administración de registros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c762689263e4a012bbdfad726b13e3ee8c79397e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667927"
---
# <a name="record-management"></a><span data-ttu-id="09817-103">Administración de registros</span><span class="sxs-lookup"><span data-stu-id="09817-103">Record Management</span></span>

<span data-ttu-id="09817-104">Para administrar registros, puede trabajar con información que se almacena en estructuras [**de \_ registro del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_record) .</span><span class="sxs-lookup"><span data-stu-id="09817-104">To manage records, you can work with information that is stored in [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) structures.</span></span> <span data-ttu-id="09817-105">Cuando se crean, actualizan o eliminan registros, los cambios realizados en un gráfico se replican en todos los nodos.</span><span class="sxs-lookup"><span data-stu-id="09817-105">When records are created, updated, or deleted, the changes made to a graph are replicated to all nodes.</span></span> <span data-ttu-id="09817-106">En la tabla siguiente se identifican las reglas para actualizar y actualizar automáticamente los registros.</span><span class="sxs-lookup"><span data-stu-id="09817-106">The following table identifies the rules for updating and automatically refreshing records.</span></span>



| <span data-ttu-id="09817-107">Tarea de administración</span><span class="sxs-lookup"><span data-stu-id="09817-107">Management Task</span></span>     | <span data-ttu-id="09817-108">Regla</span><span class="sxs-lookup"><span data-stu-id="09817-108">Rule</span></span>                                                                                                                                                                                                            |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09817-109">Actualizar un registro</span><span class="sxs-lookup"><span data-stu-id="09817-109">Updating a record</span></span>   | <span data-ttu-id="09817-110">Mantenga la hora de expiración igual o auméntelo.</span><span class="sxs-lookup"><span data-stu-id="09817-110">Keep the expiration time the same or increase it.</span></span> <span data-ttu-id="09817-111">No se puede reducir la hora de expiración.</span><span class="sxs-lookup"><span data-stu-id="09817-111">You cannot decrease the expiration time.</span></span>                                                                                                                      |
| <span data-ttu-id="09817-112">Actualizar un registro</span><span class="sxs-lookup"><span data-stu-id="09817-112">Refreshing a record</span></span> | <span data-ttu-id="09817-113">Use la marca de actualización automática de la [**\_ marca de registro \_ \_ del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_record) para actualizar un registro automáticamente.</span><span class="sxs-lookup"><span data-stu-id="09817-113">Use the [**PEER\_RECORD\_FLAG\_AUTOREFRESH**](/windows/desktop/api/P2P/ns-p2p-peer_record) flag to automatically refresh a record.</span></span> <span data-ttu-id="09817-114">Use esta marca solo cuando el nodo que está publicando un registro está en línea.</span><span class="sxs-lookup"><span data-stu-id="09817-114">Only use this flag when the node that is publishing a record is online.</span></span> <span data-ttu-id="09817-115">De lo contrario, no utilice esta marca.</span><span class="sxs-lookup"><span data-stu-id="09817-115">Otherwise, do not use this flag.</span></span> |



 

 

 



