---
title: Implementación opcional
description: Las siguientes características son opcionales, pero se recomienda
ms.assetid: 6123bdda-06cf-4b8b-b2a8-89882b6341b4
ms.tgt_platform: multiple
keywords:
- ADSI de implementación opcional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 043b07f3a9bcfaef4bde8e95458d64828d4e46be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104531840"
---
# <a name="optional-implementation"></a><span data-ttu-id="a4ee9-104">Implementación opcional</span><span class="sxs-lookup"><span data-stu-id="a4ee9-104">Optional Implementation</span></span>

<span data-ttu-id="a4ee9-105">Las siguientes características son opcionales, pero se recomienda:</span><span class="sxs-lookup"><span data-stu-id="a4ee9-105">The following features are optional, but recommended:</span></span>

-   <span data-ttu-id="a4ee9-106">La interfaz [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) para clientes que no son de automatización.</span><span class="sxs-lookup"><span data-stu-id="a4ee9-106">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface for non-Automation clients.</span></span> <span data-ttu-id="a4ee9-107">Dado que el proveedor de OLE DB ADSI usa **IDirectorySearch** para presentar las consultas y recopilar los resultados del servicio de directorio subyacente, los proveedores que implementan esta interfaz proporcionan automáticamente acceso a las bases de datos de estilo OLE DB sin tener que implementar ninguna interfaz adicional.</span><span class="sxs-lookup"><span data-stu-id="a4ee9-107">Because the ADSI OLE DB provider uses **IDirectorySearch** to present queries and collect results from the underlying directory service, providers that implement this interface automatically provide access to OLE DB style databases without having to implement any additional interfaces.</span></span>
-   <span data-ttu-id="a4ee9-108">Las interfaces [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)y [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) .</span><span class="sxs-lookup"><span data-stu-id="a4ee9-108">The [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist), and [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) interfaces.</span></span> <span data-ttu-id="a4ee9-109">Se recomienda que los proveedores de servicios de directorio que admiten la seguridad de objetos basada en ACL implementen estas características adicionales.</span><span class="sxs-lookup"><span data-stu-id="a4ee9-109">Providers for directory services that support ACL-based object security are encouraged to implement these additional features.</span></span>

 

 




