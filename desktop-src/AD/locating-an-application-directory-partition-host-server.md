---
title: Localizar un servidor host de partición de directorio de aplicaciones
description: En este tema se describe cómo localizar un servidor host de partición de directorio de aplicaciones.
ms.assetid: 636e8bc2-136c-42be-aa64-1b059dedf775
ms.tgt_platform: multiple
keywords:
- Localizar un servidor host de partición de directorio de aplicaciones AD
- Particiones de directorio de aplicaciones AD, localizar un servidor host
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5c9e8f80ccf4b1549af9a76e7b588685d38c297
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773141"
---
# <a name="locating-an-application-directory-partition-host-server"></a><span data-ttu-id="d3f18-105">Localizar un servidor host de partición de directorio de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="d3f18-105">Locating an Application Directory Partition Host Server</span></span>

<span data-ttu-id="d3f18-106">El servicio NetLogon registra la siguiente lista de registros SRV para una partición de directorio de aplicaciones:</span><span class="sxs-lookup"><span data-stu-id="d3f18-106">The NetLogon service registers the following list of SRV records for an application directory partition:</span></span>

-   <span data-ttu-id="d3f18-107">\_LDAP. \_ TCP.<partition name></span><span class="sxs-lookup"><span data-stu-id="d3f18-107">\_ldap.\_tcp.<partition name></span></span>
-   <span data-ttu-id="d3f18-108">\_LDAP. \_ TCP. <site name> . \_ sitios.<partition name></span><span class="sxs-lookup"><span data-stu-id="d3f18-108">\_ldap.\_tcp.<site name>.\_sites.<partition name></span></span>

<span data-ttu-id="d3f18-109">Para buscar un controlador de dominio que hospede una réplica de una partición de directorio de aplicación especificada, llame a la función [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea) con el parámetro *domainname* establecido en el nombre DNS de la partición de directorio de la aplicación y el indicador **\_ solo \_ LDAP \_ necesario** establecido en el parámetro *Flags* .</span><span class="sxs-lookup"><span data-stu-id="d3f18-109">To locate a domain controller that hosts a replica of a specified application directory partition, call the [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea) function with the *DomainName* parameter set to the DNS name of the application directory partition and the **DS\_ONLY\_LDAP\_NEEDED** flag set in the *Flags* parameter.</span></span> <span data-ttu-id="d3f18-110">Para obtener más información y un ejemplo de código que muestre, mediante la función **DsGetDcName** , cómo buscar un controlador de dominio que hospede una réplica de una partición de directorio de aplicaciones, vea el [código de ejemplo para buscar un servidor host de partición de directorio de aplicaciones](example-code-for-locating-an-application-directory-partition-host-server.md).</span><span class="sxs-lookup"><span data-stu-id="d3f18-110">For more information and a code example that shows, using the **DsGetDcName** function, how to locate a domain controller that hosts a replica of an application directory partition, see [Example Code for Locating an Application Directory Partition Host Server](example-code-for-locating-an-application-directory-partition-host-server.md).</span></span>

 

 




