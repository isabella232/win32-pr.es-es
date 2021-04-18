---
description: La tunelización automática con direcciones compatibles con IPv4 y 6to4 funcionan a través de una ruta para un prefijo que está en el vínculo a la interfaz \# 2. Los bits 32 que siguen al prefijo se extraen y se usan como una dirección de destino IPv4 para el paquete encapsulado.
ms.assetid: 92261a1b-2b7f-4a76-b98a-2631dc303618
title: Tunelización automática IPv6 y 6to4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ede1179902a7ec3276058e078d56e069603e54a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715141"
---
# <a name="ipv6-automatic-tunneling-and-6to4"></a><span data-ttu-id="4cd28-104">Tunelización automática IPv6 y 6to4</span><span class="sxs-lookup"><span data-stu-id="4cd28-104">IPv6 Automatic Tunneling and 6to4</span></span>

<span data-ttu-id="4cd28-105">La tunelización automática con direcciones compatibles con IPv4 y 6to4 funcionan a través de una ruta para un prefijo que está en el vínculo a la interfaz \# 2.</span><span class="sxs-lookup"><span data-stu-id="4cd28-105">Automatic tunneling with IPv4-compatible addresses and 6to4 both work through a route for a prefix that is on-link to interface \#2.</span></span> <span data-ttu-id="4cd28-106">Los bits 32 que siguen al prefijo se extraen y se usan como una dirección de destino IPv4 para el paquete encapsulado.</span><span class="sxs-lookup"><span data-stu-id="4cd28-106">The 32 bits following the prefix are extracted and used as an IPv4 destination address for the encapsulated packet.</span></span>

<span data-ttu-id="4cd28-107">La tunelización automática usa el prefijo::/96, que está habilitado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="4cd28-107">Automatic tunneling uses the ::/96 prefix, which is enabled by default.</span></span> <span data-ttu-id="4cd28-108">Puede deshabilitarse quitando la ruta de::/96.</span><span class="sxs-lookup"><span data-stu-id="4cd28-108">It can be disabled by removing the route for ::/96.</span></span>

<span data-ttu-id="4cd28-109">6to4 usa el prefijo 2002::/16, que no está habilitado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="4cd28-109">6to4 uses the 2002::/16 prefix, which is not enabled by default.</span></span>

 

 



