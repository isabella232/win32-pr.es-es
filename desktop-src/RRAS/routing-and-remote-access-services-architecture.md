---
title: Arquitectura de servicios de enrutamiento y acceso remoto
description: En la ilustración siguiente se muestra una vista arquitectónica general del enrutador 2000 de Windows.
ms.assetid: 599435e2-e2f3-4632-8a79-441172aacf13
keywords:
- RRAS del servicio de enrutamiento y acceso remoto RRAS, arquitectura de servicios de enrutamiento y acceso remoto RRAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a3e72f7c61bc9cb558b020c3470718a7f419c04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486919"
---
# <a name="routing-and-remote-access-services-architecture"></a><span data-ttu-id="c2d1f-104">Arquitectura de servicios de enrutamiento y acceso remoto</span><span class="sxs-lookup"><span data-stu-id="c2d1f-104">Routing and Remote Access Services Architecture</span></span>

<span data-ttu-id="c2d1f-105">En la ilustración siguiente se muestra una vista arquitectónica general del enrutador 2000 de Windows.</span><span class="sxs-lookup"><span data-stu-id="c2d1f-105">The following illustration presents a general architectural view of the Windows 2000 router.</span></span>

<span data-ttu-id="c2d1f-106">Los componentes que son específicos de la familia del protocolo IP se muestran en gris claro.</span><span class="sxs-lookup"><span data-stu-id="c2d1f-106">Components that are specific to the IP protocol family are shown in light gray.</span></span> <span data-ttu-id="c2d1f-107">Los componentes que son específicos de la familia de protocolos IPX se muestran en gris oscuro.</span><span class="sxs-lookup"><span data-stu-id="c2d1f-107">Components that are specific to the IPX protocol family are shown in dark gray.</span></span> <span data-ttu-id="c2d1f-108">Los componentes que son generales para todas las familias de protocolos no están sombreados.</span><span class="sxs-lookup"><span data-stu-id="c2d1f-108">Components that are general to all protocol families are unshaded.</span></span>

<span data-ttu-id="c2d1f-109">El servicio de enrutamiento y acceso remoto proporciona las API para administrar y configurar el servicio.</span><span class="sxs-lookup"><span data-stu-id="c2d1f-109">The Routing and Remote Access Service provides APIs for administering and configuring the service.</span></span> <span data-ttu-id="c2d1f-110">Estas API incluyen agentes SNMP para IP e IPX.</span><span class="sxs-lookup"><span data-stu-id="c2d1f-110">These APIs include SNMP agents for both IP and IPX.</span></span>

<span data-ttu-id="c2d1f-111">RRAS incluye protocolos de enrutamiento para IP e IPX.</span><span class="sxs-lookup"><span data-stu-id="c2d1f-111">RRAS includes routing protocols for both IP and IPX.</span></span> <span data-ttu-id="c2d1f-112">Para IP, RRAS proporciona los protocolos de enrutamiento protocolo de información de enrutamiento (RIP) y ruta de acceso más corta (OSPF).</span><span class="sxs-lookup"><span data-stu-id="c2d1f-112">For IP, RRAS provides the Routing Information Protocol (RIP) and Open Shortest Path First (OSPF) routing protocols.</span></span> <span data-ttu-id="c2d1f-113">Para IPX, RRAS proporciona IPX RIP y el protocolo de anuncio de servicio (SAP).</span><span class="sxs-lookup"><span data-stu-id="c2d1f-113">For IPX, RRAS provides IPX RIP and Service Advertising Protocol (SAP).</span></span>

<span data-ttu-id="c2d1f-114">RRAS usa un administrador de tabla de enrutamiento (RTM) para IP e IPX.</span><span class="sxs-lookup"><span data-stu-id="c2d1f-114">RRAS uses one Routing Table Manager (RTM) for both IP and IPX.</span></span> <span data-ttu-id="c2d1f-115">Sin embargo, cada familia de protocolos tiene su propio administrador de enrutadores.</span><span class="sxs-lookup"><span data-stu-id="c2d1f-115">However, each protocol family has its own Router Manager.</span></span> <span data-ttu-id="c2d1f-116">RRAS también tiene un componente independiente para administrar grupos de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="c2d1f-116">RRAS also has separate component for managing Multicast Groups.</span></span>

<span data-ttu-id="c2d1f-117">Las interfaces de Dynamic interface Manager (DIM) con servicios PPP y TAPI para administrar las interfaces PPP utilizadas por algunas rutas.</span><span class="sxs-lookup"><span data-stu-id="c2d1f-117">The Dynamic Interface Manager (DIM) interfaces with PPP and TAPI services in order to manage PPP interfaces used by some routes.</span></span>

![vista arquitectónica general del enrutador de Windows 2000](images/rtarch.png)

 

 




