---
title: Proveedores de servicios ADSI
description: En este tema se proporciona información general sobre los proveedores de servicios ADSI que se proporcionan en el servidor.
ms.assetid: 419d7953-a879-4d6c-be74-173d76c3f932
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, proveedores de servicios
- ADSI de proveedores de servicios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e44ba4ebc63338bfb38d2b9d5da1f46e51b31aa8
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105656394"
---
# <a name="adsi-service-providers"></a><span data-ttu-id="96af7-105">Proveedores de servicios ADSI</span><span class="sxs-lookup"><span data-stu-id="96af7-105">ADSI Service Providers</span></span>

<span data-ttu-id="96af7-106">ADSI incluye los proveedores de servicios que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="96af7-106">ADSI includes the service providers listed in the following table.</span></span>



| <span data-ttu-id="96af7-107">Proveedor de servicios</span><span class="sxs-lookup"><span data-stu-id="96af7-107">Service provider</span></span> | <span data-ttu-id="96af7-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="96af7-108">Description</span></span>                                                                                | <span data-ttu-id="96af7-109">Para obtener más información</span><span class="sxs-lookup"><span data-stu-id="96af7-109">For more information</span></span>                                      |
|------------------|--------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="96af7-110">LDAP</span><span class="sxs-lookup"><span data-stu-id="96af7-110">LDAP</span></span><br/>  | <span data-ttu-id="96af7-111">Implementación de espacio de nombres compatible con el Protocolo ligero de acceso a directorios.</span><span class="sxs-lookup"><span data-stu-id="96af7-111">Namespace implementation compatible with Lightweight Directory Access Protocol.</span></span><br/> | [<span data-ttu-id="96af7-112">Proveedor LDAP de ADSI</span><span class="sxs-lookup"><span data-stu-id="96af7-112">ADSI LDAP Provider</span></span>](adsi-ldap-provider.md)<br/>   |
| <span data-ttu-id="96af7-113">WinNT</span><span class="sxs-lookup"><span data-stu-id="96af7-113">WinNT</span></span><br/> | <span data-ttu-id="96af7-114">Implementación de espacio de nombres compatible con Windows.</span><span class="sxs-lookup"><span data-stu-id="96af7-114">Namespace implementation compatible with Windows.</span></span><br/>                               | [<span data-ttu-id="96af7-115">Proveedor WinNT de ADSI</span><span class="sxs-lookup"><span data-stu-id="96af7-115">ADSI WinNT Provider</span></span>](adsi-winnt-provider.md)<br/> |



 

<span data-ttu-id="96af7-116">Otros proveedores de servicios se incluyen como parte de productos distintos de ADSI.</span><span class="sxs-lookup"><span data-stu-id="96af7-116">Other service providers are included as part of products other than ADSI.</span></span> <span data-ttu-id="96af7-117">A continuación se indican los proveedores de servicios ADSI implementados por Microsoft.</span><span class="sxs-lookup"><span data-stu-id="96af7-117">The following are the ADSI service providers implemented by Microsoft.</span></span>



| <span data-ttu-id="96af7-118">Proveedor de servicios</span><span class="sxs-lookup"><span data-stu-id="96af7-118">Service provider</span></span> | <span data-ttu-id="96af7-119">Para obtener más información</span><span class="sxs-lookup"><span data-stu-id="96af7-119">For more information</span></span>                                                                        |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="96af7-120">IIS</span><span class="sxs-lookup"><span data-stu-id="96af7-120">IIS</span></span><br/>   | <span data-ttu-id="96af7-121">[Arquitectura del proveedor ADSI de IIS](/previous-versions/iis/6.0-sdk/ms525929(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="96af7-121">[IIS ADSI Provider Architecture](/previous-versions/iis/6.0-sdk/ms525929(v=vs.90))</span></span><br/> |



 

<span data-ttu-id="96af7-122">Todos los proveedores de servicios no admiten los métodos y métodos de propiedad expuestos por las interfaces ADSI.</span><span class="sxs-lookup"><span data-stu-id="96af7-122">The methods and property methods exposed by ADSI interfaces are not supported by every service provider.</span></span> <span data-ttu-id="96af7-123">Dado que los distintos servicios de directorio varían en los tipos de objetos y propiedades almacenados, usan protocolos y autenticación diferentes, ADSI está diseñado para funcionar sin problemas con proveedores de servicios compatibles.</span><span class="sxs-lookup"><span data-stu-id="96af7-123">Because different directory services vary in the types of objects and properties stored, use different protocols, and authentication, ADSI is designed to work seamlessly with supported service providers.</span></span> <span data-ttu-id="96af7-124">Por lo tanto, hay interfaces, métodos y métodos de propiedad que funcionan con un proveedor de servicios, como LDAP, que puede que no funcionen en otro, como Winnt.</span><span class="sxs-lookup"><span data-stu-id="96af7-124">Thus, there are interfaces, methods, and property methods that work with one service provider, such as LDAP, that may not work on another, such as WinNT.</span></span>

<span data-ttu-id="96af7-125">Esta sección contiene información específica del proveedor, como el formato de ADsPath, una lista de objetos ADSI utilizados para ese proveedor de servicios e información sobre el tipo de datos y la sintaxis de los proveedores de servicios incluidos con ADSI.</span><span class="sxs-lookup"><span data-stu-id="96af7-125">This section contains provider-specific information, such as the ADsPath format, a listing of ADSI objects used for that service provider, and data type and syntax information for the service providers included with ADSI.</span></span> <span data-ttu-id="96af7-126">También hay una descripción breve de las interfaces ADSI que admite cada proveedor incluido con ADSI.</span><span class="sxs-lookup"><span data-stu-id="96af7-126">There is also a summary description of ADSI interfaces supported by each provider included with ADSI.</span></span>

<span data-ttu-id="96af7-127">En ADSI, los distintos proveedores están asociados a distintos archivos dll.</span><span class="sxs-lookup"><span data-stu-id="96af7-127">In ADSI, different providers are associated with different DLLs.</span></span> <span data-ttu-id="96af7-128">El proveedor LDAP está asociado a Adsldp.dll, Adsldpc.dll y Adsmsext.dll.</span><span class="sxs-lookup"><span data-stu-id="96af7-128">The LDAP provider is associated with Adsldp.dll, Adsldpc.dll, and Adsmsext.dll.</span></span> <span data-ttu-id="96af7-129">El proveedor de WinNT está asociado a Adsnt.dll.</span><span class="sxs-lookup"><span data-stu-id="96af7-129">The WinNT provider is associated with Adsnt.dll.</span></span> <span data-ttu-id="96af7-130">El proveedor del enrutador está asociado a Activeds.dll.</span><span class="sxs-lookup"><span data-stu-id="96af7-130">The ROUTER provider is associated with Activeds.dll.</span></span>

> [!Note]  
> <span data-ttu-id="96af7-131">No asuma que los proveedores ADSI predeterminados son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="96af7-131">Do not assume that default ADSI providers are thread-safe.</span></span> <span data-ttu-id="96af7-132">Los desarrolladores de aplicaciones multiproceso deben coordinar el acceso entre subprocesos mediante el uso correcto de objetos de sincronización como semáforos, exclusiones mutuas, secciones críticas, etc.</span><span class="sxs-lookup"><span data-stu-id="96af7-132">Multithreaded application developers should coordinate access between threads through the proper use of synchronization objects such as semaphores, mutexes, critical sections, and so on.</span></span>

 

<span data-ttu-id="96af7-133">Para obtener más información acerca de los proveedores de servicios ADSI, consulte compatibilidad con el [enrutador ADSI](adsi-router.md) y el [proveedor de interfaces ADSI](provider-support-of-adsi-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="96af7-133">For more information about ADSI service providers, see [ADSI Router](adsi-router.md) and [Provider Support of ADSI interfaces](provider-support-of-adsi-interfaces.md).</span></span>

 

