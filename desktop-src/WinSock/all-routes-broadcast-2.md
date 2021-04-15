---
description: Una difusión general a través de Internet se logra estableciendo los \_ campos SA netnum y SA \_ nodenum en binarios (1).
ms.assetid: a56f3059-d6e5-42eb-8ba2-16071fffafa5
title: Difundir todas las rutas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15830ad4f82a3cc5d93e84762c8c17ed0cfd85bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497476"
---
# <a name="all-routes-broadcast"></a><span data-ttu-id="80afd-103">Difundir todas las rutas</span><span class="sxs-lookup"><span data-stu-id="80afd-103">All Routes Broadcast</span></span>

<span data-ttu-id="80afd-104">Una difusión general a través de Internet se logra estableciendo los campos **SA \_ netnum** y **SA \_ nodenum** en binarios (1).</span><span class="sxs-lookup"><span data-stu-id="80afd-104">A general broadcast through the Internet is achieved by setting the **sa\_netnum** and **sa\_nodenum** fields to binary ones (1).</span></span> <span data-ttu-id="80afd-105">El proveedor de servicios traduce esta solicitud a un paquete de tipo 20, que los enrutadores IPX reconocen y reenvían.</span><span class="sxs-lookup"><span data-stu-id="80afd-105">The service provider translates this request to a type-20 packet, which IPX routers recognize and forward.</span></span> <span data-ttu-id="80afd-106">El paquete visita todas las subredes y puede duplicarse varias veces.</span><span class="sxs-lookup"><span data-stu-id="80afd-106">The packet visits all subnets and may be duplicated several times.</span></span> <span data-ttu-id="80afd-107">Los receptores deben controlar varias copias duplicadas del datagrama.</span><span class="sxs-lookup"><span data-stu-id="80afd-107">Receivers must handle several duplicate copies of the datagram.</span></span>

<span data-ttu-id="80afd-108">El uso de este tipo de difusión no es popular entre los administradores de red, por lo que su uso debe ser extremadamente limitado.</span><span class="sxs-lookup"><span data-stu-id="80afd-108">Use of this broadcast type is unpopular among network administrators, so its use should be extremely limited.</span></span> <span data-ttu-id="80afd-109">Muchos enrutadores deshabilitan este tipo de difusión y dejan las partes de la subred invisibles para el paquete.</span><span class="sxs-lookup"><span data-stu-id="80afd-109">Many routers disable this type of broadcast, leaving parts of the subnet invisible to the packet.</span></span>

 

 



