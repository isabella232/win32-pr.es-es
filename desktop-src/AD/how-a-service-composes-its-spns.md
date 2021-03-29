---
title: Cómo un servicio crea sus SPN
description: Un servicio puede usar dos funciones para componer sus SPN DsGetSpn es una función de uso general para la creación de SPN y DsServerRegisterSpn es una función especializada para crear y registrar SPN simples para un servicio basado en host.
ms.assetid: 8710409a-67b1-45e5-9cd7-5125443ab921
ms.tgt_platform: multiple
keywords:
- nombre de entidad de seguridad de servicio AD, cómo se compone un servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5611527cc3c240eebc195058ce39daab71aeef23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903116"
---
# <a name="how-a-service-composes-its-spns"></a><span data-ttu-id="24864-104">Cómo un servicio crea sus SPN</span><span class="sxs-lookup"><span data-stu-id="24864-104">How a Service Composes its SPNs</span></span>

<span data-ttu-id="24864-105">Un servicio puede usar dos funciones para crear sus SPN: [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) es una función de uso general para la creación de SPN y [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) es una función especializada para crear y registrar SPN simples para un servicio basado en host.</span><span class="sxs-lookup"><span data-stu-id="24864-105">A service can use two functions to compose its SPNs: [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) is a general-purpose function for composing SPNs and [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) is a specialized function for composing and registering simple SPNs for a host-based service.</span></span>

<span data-ttu-id="24864-106">Un instalador de servicio suele usar la función [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) para crear SPN, que después se registra en la cuenta de inicio de sesión del servicio mediante la función [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) .</span><span class="sxs-lookup"><span data-stu-id="24864-106">A service installer typically uses the [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) function to compose SPNs, which it then registers on the service's logon account using the [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) function.</span></span> <span data-ttu-id="24864-107">El **DsGetSpn** puede realizar las siguientes funciones.</span><span class="sxs-lookup"><span data-stu-id="24864-107">The **DsGetSpn** can perform the following functions.</span></span>

-   <span data-ttu-id="24864-108">Cree un SPN simple con el <service class> / <host> formato "" para un servicio basado en host.</span><span class="sxs-lookup"><span data-stu-id="24864-108">Create a simple SPN with the "<service class>/<host>" format for a host-based service.</span></span>
-   <span data-ttu-id="24864-109">Cree un SPN complejo que incluya el &lt; componente de "nombre de servicio &gt; " que usan los servicios replicables o el &lt; componente "Port &gt; " que distingue varias instancias de un servicio en un solo host.</span><span class="sxs-lookup"><span data-stu-id="24864-109">Create a complex SPN that includes the "&lt;service name&gt;" component used by replicable services or the "&lt;port&gt;" component that distinguishes multiple instances of a service on a single host.</span></span>
-   <span data-ttu-id="24864-110">Cree un único SPN con el &lt; componente "host &gt; " establecido en el nombre de un host especificado o en el nombre del equipo local de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="24864-110">Create a single SPN with the "&lt;host&gt;" component set to either the name of a specified host or the name of the local computer by default.</span></span>
-   <span data-ttu-id="24864-111">Cree una matriz de SPN para varias instancias de servicio que se ejecutarán en varios hosts de todo el bosque.</span><span class="sxs-lookup"><span data-stu-id="24864-111">Create an array of SPNs for multiple service instances that will run on multiple hosts throughout the forest.</span></span> <span data-ttu-id="24864-112">Cada SPN especifica el nombre del host para una instancia de servicio.</span><span class="sxs-lookup"><span data-stu-id="24864-112">Each SPN specifies the name of the host for a service instance.</span></span>
-   <span data-ttu-id="24864-113">Cree una matriz de SPN para varias instancias de servicio que se ejecutarán en el mismo host.</span><span class="sxs-lookup"><span data-stu-id="24864-113">Create an array of SPNs for multiple service instances that will run on the same host.</span></span> <span data-ttu-id="24864-114">Cada SPN especifica el nombre del host y un número de puerto para una instancia de servicio.</span><span class="sxs-lookup"><span data-stu-id="24864-114">Each SPN specifies the name of the host and a port number for a service instance.</span></span>

<span data-ttu-id="24864-115">La matriz de nombres devuelta por [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) debe liberarse llamando a la función [**DsFreeSpnArray**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreespnarraya) .</span><span class="sxs-lookup"><span data-stu-id="24864-115">The array of names returned by [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) must be freed by calling the [**DsFreeSpnArray**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreespnarraya) function.</span></span>

<span data-ttu-id="24864-116">Tenga en cuenta que las funciones [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna), [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna)y [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) no comprueban que los SPN son únicos.</span><span class="sxs-lookup"><span data-stu-id="24864-116">Be aware that the [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna), [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna), and [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) functions do not verify that SPNs are unique.</span></span> <span data-ttu-id="24864-117">Dado que se produce un error en la autenticación mutua si un cliente presenta un SPN que no es único, Compruebe la unicidad antes de registrar un SPN.</span><span class="sxs-lookup"><span data-stu-id="24864-117">Because mutual authentication fails if a client presents an SPN that is not unique, verify uniqueness before registering an SPN.</span></span> <span data-ttu-id="24864-118">Para ello, busque en el catálogo global (GC) los atributos **ServicePrincipalName** que coinciden con su SPN.</span><span class="sxs-lookup"><span data-stu-id="24864-118">To do this, search the global catalog (GC) for **servicePrincipalName** attributes that match your SPN.</span></span> <span data-ttu-id="24864-119">Para obtener más información acerca de la búsqueda en el [catálogo global, vea Buscar en el catálogo global](searching-global-catalog-contents.md).</span><span class="sxs-lookup"><span data-stu-id="24864-119">For more information about searching the GC, see [Searching the Global Catalog](searching-global-catalog-contents.md).</span></span>

 

 




