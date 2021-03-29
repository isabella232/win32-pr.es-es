---
title: Proveedor LDAP de ADSI
description: El proveedor LDAP de ADSI implementa un conjunto de objetos ADSI que admiten diversas interfaces ADSI. Para tener acceso al proveedor LDAP, enlace con cualquiera de los objetos LDAP de ADSI mediante la ADsPath de LDAP.
ms.assetid: 3c13ea2f-fe40-4fd4-8540-422f277e07c1
ms.tgt_platform: multiple
keywords:
- Proveedor LDAP de ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8edbca53708a46c2f788c328a78bd2488973486
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903082"
---
# <a name="adsi-ldap-provider"></a><span data-ttu-id="afaac-105">Proveedor LDAP de ADSI</span><span class="sxs-lookup"><span data-stu-id="afaac-105">ADSI LDAP Provider</span></span>

<span data-ttu-id="afaac-106">El proveedor LDAP de ADSI implementa un conjunto de objetos ADSI que admiten diversas interfaces ADSI.</span><span class="sxs-lookup"><span data-stu-id="afaac-106">The ADSI LDAP Provider implements a set of ADSI objects that support various ADSI interfaces.</span></span> <span data-ttu-id="afaac-107">Para tener acceso al proveedor LDAP, enlace con cualquiera de los objetos LDAP de ADSI mediante la ADsPath de LDAP.</span><span class="sxs-lookup"><span data-stu-id="afaac-107">To access the LDAP provider, bind to any of the ADSI LDAP objects, using the LDAP ADsPath.</span></span>

<span data-ttu-id="afaac-108">Debe tener Adsldp.dll, Adsldpc.dll, Adsmsext.dll y Activeds.dll instalados en el equipo cliente para que funcionen con el proveedor.</span><span class="sxs-lookup"><span data-stu-id="afaac-108">You must have Adsldp.dll, Adsldpc.dll, Adsmsext.dll, and Activeds.dll installed on your client computer to work with the provider.</span></span>

> [!Note]  
> <span data-ttu-id="afaac-109">No se puede suponer que el proveedor LDAP de ADSI predeterminado sea totalmente seguro para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="afaac-109">The default ADSI LDAP provider cannot be assumed to be completely thread-safe.</span></span> <span data-ttu-id="afaac-110">Los escritores de aplicaciones multiproceso deben coordinar correctamente el acceso entre subprocesos mediante el uso correcto de objetos de sincronización como semáforos, exclusiones mutuas, secciones críticas, etc.</span><span class="sxs-lookup"><span data-stu-id="afaac-110">Writers of multithreaded applications should properly coordinate access between threads through the proper use of synchronization objects such as semaphores, mutexes, critical sections, and so on.</span></span>

 

 

 




