---
description: El proveedor de espacios de nombres del Protocolo de resolución de nombres de mismo nivel (PNRP) es una tecnología de resolución de nombres sin servidor que permite a los nodos detectarse entre sí.
ms.assetid: e11d0f07-f3a0-4c0f-94ce-1d4944a34230
title: Acerca de PNRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec402548423ef6baeb15e64a859455fe52332cc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156548"
---
# <a name="about-pnrp"></a><span data-ttu-id="4e116-103">Acerca de PNRP</span><span class="sxs-lookup"><span data-stu-id="4e116-103">About PNRP</span></span>

<span data-ttu-id="4e116-104">El proveedor de espacios de nombres del Protocolo de resolución de nombres de mismo nivel (PNRP) es una tecnología de resolución de nombres sin servidor que permite a los nodos detectarse entre sí.</span><span class="sxs-lookup"><span data-stu-id="4e116-104">The Peer Name Resolution Protocol (PNRP) Namespace Provider (NSP) is a serverless name resolution technology that allows nodes to discover each other.</span></span> <span data-ttu-id="4e116-105">PNRP usa la API del proveedor de espacios de nombres Winsock 2.</span><span class="sxs-lookup"><span data-stu-id="4e116-105">PNRP uses the Winsock 2 Namespace Provider API.</span></span>

<span data-ttu-id="4e116-106">PNRP requiere compatibilidad con IPv6 y es el único protocolo de Internet nativo para la API.</span><span class="sxs-lookup"><span data-stu-id="4e116-106">IPv6 support is required by PNRP and is the only Internet Protocol native to the API.</span></span> <span data-ttu-id="4e116-107">Sin embargo, PNRP puede resolver direcciones IPv4 a través de las tecnologías de transición 6to4 o [Teredo](/windows/desktop/Teredo/portal) .</span><span class="sxs-lookup"><span data-stu-id="4e116-107">However, PNRP can resolve IPv4 addresses via the 6to4 or [Teredo](/windows/desktop/Teredo/portal) transition technologies.</span></span> <span data-ttu-id="4e116-108">Los usuarios de Windows XP con Service Pack 1 (SP1) deben descargar el [paquete de redes avanzadas](https://www.microsoft.com/downloads/details.aspx?FamilyID=e88cc382-8ce6-4739-97c0-1a52a6f005e4) para habilitar la compatibilidad con IPv6 que requiere PNRP.</span><span class="sxs-lookup"><span data-stu-id="4e116-108">Windows XP with Service Pack 1 (SP1) users must download the [Advanced Networking Pack](https://www.microsoft.com/downloads/details.aspx?FamilyID=e88cc382-8ce6-4739-97c0-1a52a6f005e4) to enable the IPv6 support required by PNRP.</span></span>

> [!Note]  
> <span data-ttu-id="4e116-109">Las aplicaciones que usan PNRP en un entorno con un firewall requieren grupos de excepciones que cubran el puerto específico de la aplicación, así como el puerto ' 3540-UDP ' para PNRP.</span><span class="sxs-lookup"><span data-stu-id="4e116-109">Applications using PNRP in an environment with a firewall require exception groups that cover the port specific to the application, as well as port '3540-UDP' for PNRP.</span></span> <span data-ttu-id="4e116-110">Estos grupos de excepciones se deben habilitar cada vez que se ejecute la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4e116-110">These exception groups should be enabled whenever the application is running.</span></span>

 

<span data-ttu-id="4e116-111">Aunque PNRP 2,0 es nativo para las plataformas Windows Vista y Windows Server 2008, los usuarios de Windows XP deben descargar Windows Update [KB920342](https://www.microsoft.com/downloads/details.aspx?familyid=55219164-EC71-4A32-A648-4ED2582EBC7C) para actualizar a PNRP 2,0.</span><span class="sxs-lookup"><span data-stu-id="4e116-111">While PNRP 2.0 is native to the Windows Vista and Windows Server 2008 platforms, Windows XP users must download Windows Update [KB920342](https://www.microsoft.com/downloads/details.aspx?familyid=55219164-EC71-4A32-A648-4ED2582EBC7C) to upgrade to PNRP 2.0.</span></span>

 

 
