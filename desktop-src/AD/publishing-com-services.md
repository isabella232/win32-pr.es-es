---
title: Publicar servicios COM+
description: Los servicios basados en COM proporcionan un proxy de aplicación en forma de paquete de Windows Installer (MSI).
ms.assetid: 38200a22-bea5-4967-a51a-e777b34f299d
ms.tgt_platform: multiple
keywords:
- Publicar servicios COM+
- Active Directory, usar, publicar un servicio, servicios COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9044b72b4a604a4d863315963cd097be67f6afce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075108"
---
# <a name="publishing-com-services"></a><span data-ttu-id="7dec7-105">Publicar servicios COM+</span><span class="sxs-lookup"><span data-stu-id="7dec7-105">Publishing COM+ Services</span></span>

<span data-ttu-id="7dec7-106">Los servicios basados en COM proporcionan un proxy de aplicación en forma de paquete de Windows Installer (MSI).</span><span class="sxs-lookup"><span data-stu-id="7dec7-106">COM-based services provide an application-proxy in the form of a Windows installer (MSI) package.</span></span> <span data-ttu-id="7dec7-107">Este archivo. msi contiene el nombre del servidor que se va a usar y otros elementos necesarios, como el proxy o los códigos auxiliares y las bibliotecas de tipos necesarios para la serialización.</span><span class="sxs-lookup"><span data-stu-id="7dec7-107">This .msi file contains the server name to be used and other required elements, such as proxy/stubs and type libraries required for marshalling.</span></span> <span data-ttu-id="7dec7-108">El complemento Servicios de componentes genera automáticamente estos proxies de aplicación para las aplicaciones de servidor COM+.</span><span class="sxs-lookup"><span data-stu-id="7dec7-108">The Component Services snap-in auto-generate these application proxies for COM+ Server applications.</span></span>

<span data-ttu-id="7dec7-109">Los proxies de aplicación se publican en objetos de directiva en Active Directory mediante el editor de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="7dec7-109">The application proxies are published into policy objects in Active Directory using the Group Policy Editor.</span></span> <span data-ttu-id="7dec7-110">No se requiere ninguna intervención especial en la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="7dec7-110">No special intervention is required in the client application.</span></span> <span data-ttu-id="7dec7-111">La cuenta de equipo o de usuario en el equipo cliente debe estar en una unidad organizativa configurada para usar el objeto de directiva en el que se publican los proxies de aplicación.</span><span class="sxs-lookup"><span data-stu-id="7dec7-111">The computer/user account on the client computer must be in an OU configured to use the policy object in which the application proxies are published.</span></span> <span data-ttu-id="7dec7-112">El enlazador COM busca automáticamente el servidor por medio del directorio cuando el cliente establece una instancia de los objetos afectados.</span><span class="sxs-lookup"><span data-stu-id="7dec7-112">The COM binder automatically locates the server by means of the directory when the client establishes an instance of the objects concerned.</span></span>

 

 




