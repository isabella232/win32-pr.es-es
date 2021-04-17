---
description: Los terminales conectables permiten a una aplicación crear terminales durante el tiempo de ejecución.
ms.assetid: 34ba4f3c-0a14-4705-9490-817c70700746
title: Terminales conectables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52802d98d7eb6985dbb7de9ca3facab90a5550e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688146"
---
# <a name="pluggable-terminals"></a><span data-ttu-id="b1136-103">Terminales conectables</span><span class="sxs-lookup"><span data-stu-id="b1136-103">Pluggable Terminals</span></span>

<span data-ttu-id="b1136-104">Los terminales conectables permiten a una aplicación crear terminales durante el tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="b1136-104">Pluggable terminals allow an application to create terminals during run time.</span></span> <span data-ttu-id="b1136-105">Normalmente, los terminales se crean y controlan mediante un par proveedor de servicios de telefonía/proveedor de servicios multimedia (TSP/MSP), y esto sigue siendo el medio más versátil y estable de manipular los terminales.</span><span class="sxs-lookup"><span data-stu-id="b1136-105">Terminals are normally created and controlled by a telephony service provider/media service provider (TSP/MSP) pair, and this remains the most versatile and stable means of manipulating terminals.</span></span> <span data-ttu-id="b1136-106">Sin embargo, algunas aplicaciones deben usar terminales simples en situaciones en las que no haya disponible un par de TSP/MSP adecuado.</span><span class="sxs-lookup"><span data-stu-id="b1136-106">However, some applications need to use simple terminals in situations where an appropriate TSP/MSP pair is not available.</span></span> <span data-ttu-id="b1136-107">Solo los escritores de aplicaciones que estén familiarizados con las operaciones de TSP y MSP deben usar terminales conectables.</span><span class="sxs-lookup"><span data-stu-id="b1136-107">Only application writers who are thoroughly familiar with TSP/MSP operations should use pluggable terminals.</span></span>

<span data-ttu-id="b1136-108">En la versión 3,1 de TAPI, los terminales conectables se agregan al modelo de TAPI.</span><span class="sxs-lookup"><span data-stu-id="b1136-108">In TAPI version 3.1, pluggable terminals are added to the TAPI model.</span></span> <span data-ttu-id="b1136-109">Los terminales conectables permiten a un tercero agregar un nuevo objeto de terminal que puede usar cualquier MSP.</span><span class="sxs-lookup"><span data-stu-id="b1136-109">Pluggable terminals allow a third party to add a new terminal object that any MSP can use.</span></span>

<span data-ttu-id="b1136-110">Consulte [registro de terminales conectables](pluggable-terminal-registration.md) y [escritura de un terminal acoplable](writing-a-pluggable-terminal.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="b1136-110">See [Pluggable Terminal Registration](pluggable-terminal-registration.md) and [Writing a Pluggable Terminal](writing-a-pluggable-terminal.md) for more information.</span></span>

 

 



