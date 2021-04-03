---
title: Propiedades de control de agente
description: Propiedades de control de agente
ms.assetid: e6a5b2db-9abf-4988-be41-fc7f4530507f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f5e80b10469e7e256b1b2bf3bcf55fb5a8a08b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075281"
---
# <a name="agent-control-properties"></a><span data-ttu-id="54106-103">Propiedades de control de agente</span><span class="sxs-lookup"><span data-stu-id="54106-103">Agent Control Properties</span></span>

<span data-ttu-id="54106-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="54106-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="54106-105">Se accede directamente a las siguientes propiedades desde el control del agente:</span><span class="sxs-lookup"><span data-stu-id="54106-105">The following properties are directly accessed from the Agent control:</span></span>

-   [<span data-ttu-id="54106-106">**Conectado**</span><span class="sxs-lookup"><span data-stu-id="54106-106">**Connected**</span></span>](connected-property.md)
-   [<span data-ttu-id="54106-107">**Name**</span><span class="sxs-lookup"><span data-stu-id="54106-107">**Name**</span></span>](name-property-a.md)
-   [<span data-ttu-id="54106-108">**RaiseRequestErrors**</span><span class="sxs-lookup"><span data-stu-id="54106-108">**RaiseRequestErrors**</span></span>](raiserequesterrors-property.md)

<span data-ttu-id="54106-109">Además, algunos entornos de programación pueden asignar propiedades adicionales en tiempo de diseño o en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="54106-109">In addition, some programming environments may assign additional design-time or run-time properties.</span></span> <span data-ttu-id="54106-110">Por ejemplo, Visual Basic agrega propiedades izquierda, índice, etiqueta y superior que definen la ubicación del control en un formulario aunque el control no aparezca en la página del formulario en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="54106-110">For example, Visual Basic adds Left, Index, Tag, and Top properties that define the location of the control on a form even though the control does not appear on the form's page at run time.</span></span>

<span data-ttu-id="54106-111">La propiedad Suspended todavía se admite por compatibilidad con versiones anteriores, pero siempre devuelve **false** porque el servidor ya no admite un estado suspendido.</span><span class="sxs-lookup"><span data-stu-id="54106-111">The Suspended property is still supported for backward compatibility, but always returns **False** because the server no longer supports a suspended state.</span></span>

 

 




