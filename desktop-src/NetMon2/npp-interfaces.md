---
description: Los proveedores de paquetes de red (NPPs) proporcionan interfaces COM a las que llaman las aplicaciones NPP y Monitor de red.
ms.assetid: 101ce722-3101-4f50-b492-dad8b68a7aaf
title: Interfaces NPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3146d34798c57aea0bbd0f4bfec0037ed2ac879c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666671"
---
# <a name="npp-interfaces"></a><span data-ttu-id="b60ba-103">Interfaces NPP</span><span class="sxs-lookup"><span data-stu-id="b60ba-103">NPP Interfaces</span></span>

<span data-ttu-id="b60ba-104">Los proveedores de paquetes de red (NPPs) proporcionan interfaces COM a las que llaman las aplicaciones NPP y Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="b60ba-104">Network packet providers (NPPs) provide COM interfaces that are called by NPP applications, and Network Monitor.</span></span> <span data-ttu-id="b60ba-105">Cuando llame a [CreateNPPInterface](createnppinterface.md), recuerde que cada NPP se representa como un único objeto com en proceso.</span><span class="sxs-lookup"><span data-stu-id="b60ba-105">When you call [CreateNPPInterface](createnppinterface.md), remember that each NPP is represented as a single in-process COM object.</span></span> <span data-ttu-id="b60ba-106">Las aplicaciones pueden crear instancias de cualquier número de objetos NPP.</span><span class="sxs-lookup"><span data-stu-id="b60ba-106">Applications can instantiate any number of NPP objects.</span></span> <span data-ttu-id="b60ba-107">Sin embargo, cada objeto con instancias debe usar uno, y solo uno, de las cinco interfaces NPP.</span><span class="sxs-lookup"><span data-stu-id="b60ba-107">However, each instantiated object must use one—and only one—of the five NPP interfaces.</span></span>

<span data-ttu-id="b60ba-108">Tenga en cuenta también que diferentes interfaces NPP proporcionan datos de red en varios formatos.</span><span class="sxs-lookup"><span data-stu-id="b60ba-108">Note also that different NPP interfaces provide network data in various forms.</span></span> <span data-ttu-id="b60ba-109">Por ejemplo, Monitor de red usa la interfaz **IDelaydC** para capturar el tráfico de red y guardarlo en un archivo de captura; mientras los monitores usan la interfaz **IRTC** para capturar el tráfico de red en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="b60ba-109">For example, Network Monitor uses the **IDelaydC** interface to capture network traffic and save it to a capture file; while monitors use the **IRTC** interface to capture real time network traffic.</span></span> <span data-ttu-id="b60ba-110">En la tabla siguiente se describen Monitor de red interfaces NPP.</span><span class="sxs-lookup"><span data-stu-id="b60ba-110">The following table describes Network Monitor NPP interfaces.</span></span>



| <span data-ttu-id="b60ba-111">Interfaz</span><span class="sxs-lookup"><span data-stu-id="b60ba-111">Interface</span></span>                | <span data-ttu-id="b60ba-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="b60ba-112">Description</span></span>                                                                                                                                                         |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b60ba-113">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="b60ba-113">IDelaydC</span></span>](idelaydc.md) | <span data-ttu-id="b60ba-114">Captura el tráfico de red que se almacena en un archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="b60ba-114">Captures network traffic that is stored in a capture file.</span></span> <span data-ttu-id="b60ba-115">Esta interfaz la usan las aplicaciones Monitor de red y NPP.</span><span class="sxs-lookup"><span data-stu-id="b60ba-115">This interface is used by Network Monitor and NPP applications.</span></span>                                          |
| [<span data-ttu-id="b60ba-116">IESP</span><span class="sxs-lookup"><span data-stu-id="b60ba-116">IESP</span></span>](iesp.md)         | <span data-ttu-id="b60ba-117">Captura el tráfico de red que se almacena en un archivo de captura y proporciona estadísticas mejoradas en un formato de archivo ESP especial.</span><span class="sxs-lookup"><span data-stu-id="b60ba-117">Captures network traffic that is stored in a capture file and provides enhanced statistics in a special ESP file format.</span></span> <span data-ttu-id="b60ba-118">Esta interfaz la usan las aplicaciones NPP</span><span class="sxs-lookup"><span data-stu-id="b60ba-118">This interface is used by NPP applications</span></span> |
| [<span data-ttu-id="b60ba-119">IRTC</span><span class="sxs-lookup"><span data-stu-id="b60ba-119">IRTC</span></span>](irtc.md)         | <span data-ttu-id="b60ba-120">Captura el tráfico de red en tiempo real y desencadena eventos cuando se producen.</span><span class="sxs-lookup"><span data-stu-id="b60ba-120">Captures real time network traffic and triggers events when they occur.</span></span> <span data-ttu-id="b60ba-121">Esta interfaz la usan las aplicaciones de [*monitores*](m.md) y NPP.</span><span class="sxs-lookup"><span data-stu-id="b60ba-121">This interface is used by [*monitors*](m.md) and NPP applications.</span></span>     |
| [<span data-ttu-id="b60ba-122">IStas</span><span class="sxs-lookup"><span data-stu-id="b60ba-122">IStats</span></span>](istats.md)     | <span data-ttu-id="b60ba-123">Recupera estadísticas como datos sin procesar en lugar de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="b60ba-123">Retrieves statistics as raw data rather than frames.</span></span> <span data-ttu-id="b60ba-124">Las aplicaciones NPP, como [*Perfmon*](p.md), usan esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="b60ba-124">This interface is used by NPP applications such as [*Perfmon*](p.md).</span></span>                     |



 

 

 



