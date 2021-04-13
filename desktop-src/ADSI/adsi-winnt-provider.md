---
title: Proveedor WinNT de ADSI
description: El proveedor ADSI de Microsoft implementa un conjunto de objetos ADSI para admitir varias interfaces ADSI.
ms.assetid: 6341be08-2e53-4708-a403-09c86fcc31a8
ms.tgt_platform: multiple
keywords:
- ADSI del proveedor WinNT ADSI
- ADSI del proveedor de servicios de Winnt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9748e17185417eb382281774c31554cb983742
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418359"
---
# <a name="adsi-winnt-provider"></a><span data-ttu-id="8ea69-105">Proveedor WinNT de ADSI</span><span class="sxs-lookup"><span data-stu-id="8ea69-105">ADSI WinNT Provider</span></span>

<span data-ttu-id="8ea69-106">El proveedor ADSI de Microsoft implementa un conjunto de objetos ADSI para admitir varias interfaces ADSI.</span><span class="sxs-lookup"><span data-stu-id="8ea69-106">The Microsoft ADSI provider implements a set of ADSI objects to support various ADSI interfaces.</span></span> <span data-ttu-id="8ea69-107">El nombre del espacio de nombres para el proveedor de Windows es "WinNT" y este proveedor se conoce comúnmente como proveedor de Winnt.</span><span class="sxs-lookup"><span data-stu-id="8ea69-107">The namespace name for the Windows provider is "WinNT" and this provider is commonly referred to as the WinNT provider.</span></span> <span data-ttu-id="8ea69-108">Para tener acceso al proveedor de WinNT, enlace a cualquiera de los [objetos ADSI de WinNT](adsi-objects-of-winnt.md)mediante el [AdsPath de WinNT](winnt-adspath.md).</span><span class="sxs-lookup"><span data-stu-id="8ea69-108">To access the WinNT provider, bind to any of the [ADSI objects of WinNT](adsi-objects-of-winnt.md), using the [WinNT AdsPath](winnt-adspath.md).</span></span>

<span data-ttu-id="8ea69-109">El proveedor de WinNT se incluye en el componente del sistema ADSI para Windows y Windows Server.</span><span class="sxs-lookup"><span data-stu-id="8ea69-109">The WinNT provider is included in the ADSI system component for Windows and Windows Server.</span></span>

> [!Note]  
> <span data-ttu-id="8ea69-110">No se puede suponer que el proveedor de WinNT predeterminado sea totalmente seguro para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="8ea69-110">The default WinNT provider cannot be assumed to be completely thread-safe.</span></span> <span data-ttu-id="8ea69-111">Los escritores de aplicaciones multiproceso deben controlar el multithreading para coordinar correctamente el acceso entre subprocesos mediante el uso correcto de objetos de sincronización como semáforos, exclusiones mutuas, secciones críticas, etc.</span><span class="sxs-lookup"><span data-stu-id="8ea69-111">Writers of multithreaded applications should handle multithreading to properly coordinate any access between threads through the proper use of synchronization objects such as semaphores, mutexes, critical sections, and so on.</span></span>

 

 

 




