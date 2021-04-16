---
description: Normalmente, un proveedor de servicios multimedia (MSP) implementa la creación de terminal.
ms.assetid: 203fccc0-aa5a-4ec3-97d3-546c36018d52
title: Escritura de un terminal conectable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6cbfe2da0c121fcee820d47fd57216840d23c59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542438"
---
# <a name="writing-a-pluggable-terminal"></a><span data-ttu-id="81264-103">Escritura de un terminal conectable</span><span class="sxs-lookup"><span data-stu-id="81264-103">Writing a Pluggable Terminal</span></span>

<span data-ttu-id="81264-104">Normalmente, un proveedor de servicios multimedia (MSP) implementa la creación de terminal.</span><span class="sxs-lookup"><span data-stu-id="81264-104">Normally, a media service provider (MSP) implements terminal creation.</span></span> <span data-ttu-id="81264-105">A partir de Windows 2000 SP1, TAPI 3 incluye terminales conectables para permitir que una aplicación implemente la creación de terminal.</span><span class="sxs-lookup"><span data-stu-id="81264-105">Starting with Windows 2000 SP1, TAPI 3 includes pluggable terminals to allow an application to implement terminal creation.</span></span> <span data-ttu-id="81264-106">Consulte la información general sobre la [implementación de terminales conectables](implementing-pluggable-terminals.md) para obtener información adicional sobre el uso de estos terminales.</span><span class="sxs-lookup"><span data-stu-id="81264-106">Please see the overview on [implementing pluggable terminals](implementing-pluggable-terminals.md) for additional information on using these terminals.</span></span>

<span data-ttu-id="81264-107">No debe usar los terminales conectables de forma rutinaria porque las capacidades completas de un terminal solo estarán disponibles cuando un MSP sea totalmente consciente de ello.</span><span class="sxs-lookup"><span data-stu-id="81264-107">You should not use pluggable terminals routinely because the full capabilities of a terminal will only be available when an MSP is fully aware of it.</span></span> <span data-ttu-id="81264-108">Además, no debe intentar implementar terminales conectables a menos que ya esté familiarizado con la escritura de proveedores de servicios multimedia.</span><span class="sxs-lookup"><span data-stu-id="81264-108">Further, you should not attempt to implement pluggable terminals unless you are already familiar with writing media service providers.</span></span> <span data-ttu-id="81264-109">Las técnicas y los posibles problemas que conlleva son bastante similares.</span><span class="sxs-lookup"><span data-stu-id="81264-109">The techniques and potential problems involved are quite similar.</span></span>

<span data-ttu-id="81264-110">El aprovisionamiento de un caso especial de terminal acoplable existe actualmente para la situación de un servidor de conferencia que necesita agregar clientes que no son de Windows 2000 SP1 o que no son de multidifusión H. 323 a conferencias de multidifusión a SDP/IP en TAPI 3</span><span class="sxs-lookup"><span data-stu-id="81264-110">Provision for a special case of pluggable terminal currently exists for the situation of a conferencing server that needs to add non-Windows 2000 SP1 or nonmulticast H.323 clients to TAPI 3 multiparty SDP/IP multicast conferences.</span></span>

 

 



