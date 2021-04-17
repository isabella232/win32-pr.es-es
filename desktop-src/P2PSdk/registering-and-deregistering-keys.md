---
description: Registrar y anular el registro de claves
ms.assetid: 90fd8df0-e2a8-4183-a50c-e6f8ea5041cc
title: Registrar y anular el registro de claves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 009ee41e85027ff8eba3f6869359a9ba304f4242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668060"
---
# <a name="registering-and-deregistering-keys"></a><span data-ttu-id="100db-103">Registrar y anular el registro de claves</span><span class="sxs-lookup"><span data-stu-id="100db-103">Registering and Deregistering Keys</span></span>

## <a name="registering-keys"></a><span data-ttu-id="100db-104">Registrar claves</span><span class="sxs-lookup"><span data-stu-id="100db-104">Registering Keys</span></span>

<span data-ttu-id="100db-105">Un nodo puede registrar claves con [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) en cualquier momento mientras se encuentra en el estado de DRT **\_ activo**, **DRT \_ solo** y DRT sin Estados de **\_ \_ red** .</span><span class="sxs-lookup"><span data-stu-id="100db-105">A node can register keys with [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) at anytime while in the **DRT\_ACTIVE**, **DRT\_ALONE**, and **DRT\_NO\_NETWORK** states.</span></span> <span data-ttu-id="100db-106">Claves registradas **solo \_ en DRT** y DRT no solo los Estados de **\_ \_ red** pueden ser reconocidos por otros DRTs después de que el nodo local haya pasado a **DRT \_ activo**.</span><span class="sxs-lookup"><span data-stu-id="100db-106">Keys registered in **DRT\_ALONE** and **DRT\_NO\_NETWORK** states can only be recognized by other DRTs after the local node has transitioned to **DRT\_ACTIVE**.</span></span>

<span data-ttu-id="100db-107">No se pueden registrar claves idénticas dentro de la misma instancia de DRT cuando se usa [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider).</span><span class="sxs-lookup"><span data-stu-id="100db-107">Identical keys cannot be registered within the same DRT instance when using [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider).</span></span> <span data-ttu-id="100db-108">Si se intenta registrar claves idénticas, se producirá un error en el registro de la segunda clave.</span><span class="sxs-lookup"><span data-stu-id="100db-108">If the registration of identical keys is attempted, the registration of the second key will fail.</span></span> <span data-ttu-id="100db-109">El uso de claves idénticas también debe evitarse entre diferentes instancias de DRT.</span><span class="sxs-lookup"><span data-stu-id="100db-109">The use of identical keys should also be avoided between different DRT instances.</span></span> <span data-ttu-id="100db-110">Busca en la designación de clave única estas claves compartidas idénticas podrían devolver cualquiera de las claves, independientemente de los datos que estén asociados a la clave.</span><span class="sxs-lookup"><span data-stu-id="100db-110">Searches against the unique key designation these identical keys share could return any one of the keys, regardless of what data is associated to the key.</span></span>

> [!Note]  
> <span data-ttu-id="100db-111">Si se requiere un comportamiento diferente para la implementación, se puede crear un proveedor de seguridad en lugar de [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) para acomodar.</span><span class="sxs-lookup"><span data-stu-id="100db-111">If different behavior is required for implementation, a security provider can be created in place of [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) to accommodate.</span></span>

 

## <a name="deregistering-keys"></a><span data-ttu-id="100db-112">Anular el registro de claves</span><span class="sxs-lookup"><span data-stu-id="100db-112">Deregistering Keys</span></span>

<span data-ttu-id="100db-113">Un nodo puede anular el registro de una clave en cualquier momento después de que se haya registrado.</span><span class="sxs-lookup"><span data-stu-id="100db-113">A node can deregister a key anytime after it has been registered.</span></span> <span data-ttu-id="100db-114">Sin embargo, solo la aplicación que registró la clave puede anular su registro.</span><span class="sxs-lookup"><span data-stu-id="100db-114">However, only the application that registered the key can deregister it.</span></span> <span data-ttu-id="100db-115">Una aplicación puede anular el registro de una clave del nodo local mediante la función [**DrtUnregisterKey**](/windows/desktop/api/drt/nf-drt-drtunregisterkey) .</span><span class="sxs-lookup"><span data-stu-id="100db-115">An application can deregister a key from the local node using the [**DrtUnregisterKey**](/windows/desktop/api/drt/nf-drt-drtunregisterkey) function.</span></span> <span data-ttu-id="100db-116">Una vez finalizada la función, desencadena un evento de **\_ \_ \_ \_ cambio de clave LEAFSET de evento de DRT** , que informa a la aplicación así como a otros nodos que participan en la malla de DRT.</span><span class="sxs-lookup"><span data-stu-id="100db-116">Upon completion the function triggers a **DRT\_EVENT\_LEAFSET\_KEY\_CHANGE** event; informing the application as well as other nodes participating in the DRT mesh.</span></span>

<span data-ttu-id="100db-117">En el estado **de \_ error de DRT** , la llamada necesaria de [**DrtClose**](/windows/desktop/api/drt/nf-drt-drtclose) producirá la eliminación del registro de todas las claves de la infraestructura de DRT.</span><span class="sxs-lookup"><span data-stu-id="100db-117">While in the **DRT\_FAULTED** state, the required call of [**DrtClose**](/windows/desktop/api/drt/nf-drt-drtclose) will result in the DRT infrastructure deregistering all keys.</span></span>

## <a name="related-topics"></a><span data-ttu-id="100db-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="100db-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="100db-119">Buscar una tabla de enrutamiento distribuida</span><span class="sxs-lookup"><span data-stu-id="100db-119">Searching a Distributed Routing Table</span></span>](searching-a-distributed-routing-table.md)
</dt> <dt>

[<span data-ttu-id="100db-120">Acerca de las tablas de enrutamiento distribuido</span><span class="sxs-lookup"><span data-stu-id="100db-120">About Distributed Routing Tables</span></span>](about-distributed-routing-tables.md)
</dt> <dt>

[<span data-ttu-id="100db-121">Referencia de Table API de enrutamiento distribuido</span><span class="sxs-lookup"><span data-stu-id="100db-121">Distributed Routing Table API Reference</span></span>](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



