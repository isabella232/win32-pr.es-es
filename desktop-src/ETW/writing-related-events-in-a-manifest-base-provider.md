---
description: Utilice la función EventWriteTransfer cuando varios componentes deseen relacionar sus eventos en un escenario de seguimiento de un extremo a otro.
ms.assetid: 715e3161-d85a-45c0-84df-c6c360b266a1
title: Escribir eventos relacionados en un proveedor basado en manifiestos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb9508996503f53c738d62fac32905919a8c73ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543067"
---
# <a name="writing-related-events-in-a-manifest-based-provider"></a><span data-ttu-id="650ba-103">Escribir eventos relacionados en un proveedor basado en manifiestos</span><span class="sxs-lookup"><span data-stu-id="650ba-103">Writing Related Events in a Manifest-based Provider</span></span>

<span data-ttu-id="650ba-104">Utilice la función [**EventWriteTransfer**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritetransfer) cuando varios componentes deseen relacionar sus eventos en un escenario de seguimiento de un extremo a otro.</span><span class="sxs-lookup"><span data-stu-id="650ba-104">Use the [**EventWriteTransfer**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritetransfer) function when several components want to relate their events in an end-to-end tracing scenario.</span></span> <span data-ttu-id="650ba-105">Por ejemplo, los componentes A, B y C realizan trabajo en una actividad relacionada y desean vincular todos los eventos relacionados con esa actividad.</span><span class="sxs-lookup"><span data-stu-id="650ba-105">For example, components A, B and C perform work on a related activity and want to link all the events related to that activity.</span></span>

<span data-ttu-id="650ba-106">ETW usa el almacenamiento local de subprocesos para que el identificador de actividad del componente anterior esté disponible para el componente siguiente.</span><span class="sxs-lookup"><span data-stu-id="650ba-106">ETW uses thread local storage to make the previous component's activity identifier available to the next component.</span></span> <span data-ttu-id="650ba-107">El componente recupera el identificador del componente anterior del almacenamiento local y establece el identificador de actividad relacionado en él.</span><span class="sxs-lookup"><span data-stu-id="650ba-107">The component retrieves the previous component's identifier from the local storage and sets the related activity identifier to it.</span></span> <span data-ttu-id="650ba-108">A continuación, el consumidor puede utilizar el identificador de actividad relacionado para recorrer la cadena de eventos de un componente al siguiente.</span><span class="sxs-lookup"><span data-stu-id="650ba-108">The consumer can then use the related activity identifier to walk the chain of the events from one component to the next.</span></span>

 

 



