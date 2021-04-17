---
description: Dado que WMI carga un proveedor de alto rendimiento en el proceso en WMI o en una aplicación cliente, debe diseñar el proveedor de alto rendimiento como un servidor en proceso.
ms.assetid: c37e3652-8c76-4125-ba62-ae860858797e
ms.tgt_platform: multiple
title: Implementar la interfaz High-Performance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea6e7f75e1031caacbb7379fba025baceb7b1a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697422"
---
# <a name="implementing-the-high-performance-interface"></a><span data-ttu-id="d4866-103">Implementar la interfaz High-Performance</span><span class="sxs-lookup"><span data-stu-id="d4866-103">Implementing the High-Performance Interface</span></span>

<span data-ttu-id="d4866-104">Dado que WMI carga un proveedor de alto rendimiento en el proceso en WMI o en una aplicación cliente, debe diseñar el proveedor de alto rendimiento como un servidor en proceso.</span><span class="sxs-lookup"><span data-stu-id="d4866-104">Because WMI loads a high-performance provider in-process to either WMI or a client application, you must design your high-performance provider as an in-process server.</span></span> <span data-ttu-id="d4866-105">Además, debe implementar los métodos de proveedor de alto rendimiento en las interfaces [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) e [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) .</span><span class="sxs-lookup"><span data-stu-id="d4866-105">In addition, you must implement the high-performance provider methods in the [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) and [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) interfaces.</span></span>

<span data-ttu-id="d4866-106">Debe implementar un proveedor de alto rendimiento como un servidor en proceso.</span><span class="sxs-lookup"><span data-stu-id="d4866-106">You should implement a high-performance provider as an in-process server.</span></span> <span data-ttu-id="d4866-107">Una característica que debe tener en cuenta al implementar la seguridad de un servidor en proceso es cómo el proveedor identifica su propia ubicación.</span><span class="sxs-lookup"><span data-stu-id="d4866-107">One feature you should be aware of when implementing the security of an in-process server is how the provider identifies its own location.</span></span> <span data-ttu-id="d4866-108">Cuando se carga en proceso en WMI, WMI crea instancias del proveedor mediante un CLSID.</span><span class="sxs-lookup"><span data-stu-id="d4866-108">When loaded in-process to WMI, WMI instantiates the provider using a CLSID.</span></span> <span data-ttu-id="d4866-109">Cuando se carga en proceso en una aplicación cliente, la aplicación cliente crea una instancia del proveedor con la propiedad **ClientLoadableCLSID** .</span><span class="sxs-lookup"><span data-stu-id="d4866-109">When loaded in process to a client application, the client application instantiates the provider with the **ClientLoadableCLSID** property.</span></span> <span data-ttu-id="d4866-110">Al asignar valores diferentes a un CLSID y a un **ClientLoadableCLSID**, se permite al proveedor determinar si se carga en proceso en WMI o en una aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="d4866-110">By giving different values to a CLSID and **ClientLoadableCLSID**, you allow the provider to determine if it is loaded in-process to WMI or to a client application.</span></span> <span data-ttu-id="d4866-111">Si se encuentra en un proceso WMI, el proveedor debe realizar cualquier suplantación de cliente necesaria mediante **ClientLoadableCLSID**.</span><span class="sxs-lookup"><span data-stu-id="d4866-111">If located in a WMI process, the provider should do any necessary client impersonation by using **ClientLoadableCLSID**.</span></span> <span data-ttu-id="d4866-112">Si se encuentra en un proceso de cliente, el proveedor hereda el token de acceso del subproceso en el que se llama.</span><span class="sxs-lookup"><span data-stu-id="d4866-112">If located in a client process, the provider inherits the access token of the thread it is called on.</span></span> <span data-ttu-id="d4866-113">Para obtener más información sobre cómo implementar un servidor en proceso, vea la [sección com](https://msdn.microsoft.com/library/aa139695.aspx) de MSDN.</span><span class="sxs-lookup"><span data-stu-id="d4866-113">For more information about implementing an in-process server, see the [COM section](https://msdn.microsoft.com/library/aa139695.aspx) of MSDN.</span></span>

<span data-ttu-id="d4866-114">Como servidor en proceso, un proveedor de alto rendimiento usa un objeto actualizador para mantener los datos actualizados para el cliente remoto.</span><span class="sxs-lookup"><span data-stu-id="d4866-114">As an in-process server, a high-performance provider uses a refresher object to keep data current for the remote client.</span></span> <span data-ttu-id="d4866-115">En la tabla siguiente se enumeran los métodos que debe implementar para un proveedor de alto rendimiento.</span><span class="sxs-lookup"><span data-stu-id="d4866-115">The following table lists methods that you must implement for a high-performance provider.</span></span>



| <span data-ttu-id="d4866-116">Método</span><span class="sxs-lookup"><span data-stu-id="d4866-116">Method</span></span>                                                                                              | <span data-ttu-id="d4866-117">Característica</span><span class="sxs-lookup"><span data-stu-id="d4866-117">Feature</span></span>                                           |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="d4866-118">**IWbemHiPerfProvider:: QueryInstances**</span><span class="sxs-lookup"><span data-stu-id="d4866-118">**IWbemHiPerfProvider::QueryInstances**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)                   | <span data-ttu-id="d4866-119">Consultas</span><span class="sxs-lookup"><span data-stu-id="d4866-119">Queries</span></span>                                           |
| [<span data-ttu-id="d4866-120">**IWbemHiPerfProvider:: GetObjects**</span><span class="sxs-lookup"><span data-stu-id="d4866-120">**IWbemHiPerfProvider::GetObjects**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)                           | <span data-ttu-id="d4866-121">Recuperación de objetos</span><span class="sxs-lookup"><span data-stu-id="d4866-121">Object retrieval</span></span>                                  |
| [<span data-ttu-id="d4866-122">**IWbemHiPerfProvider:: CreateRefresher**</span><span class="sxs-lookup"><span data-stu-id="d4866-122">**IWbemHiPerfProvider::CreateRefresher**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)                 | <span data-ttu-id="d4866-123">Crea un actualizador</span><span class="sxs-lookup"><span data-stu-id="d4866-123">Creates a refresher</span></span>                               |
| [<span data-ttu-id="d4866-124">**IWbemHiPerfProvider:: CreateRefreshableObject**</span><span class="sxs-lookup"><span data-stu-id="d4866-124">**IWbemHiPerfProvider::CreateRefreshableObject**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject) | <span data-ttu-id="d4866-125">Crea un objeto de instancia actualizable.</span><span class="sxs-lookup"><span data-stu-id="d4866-125">Creates a refreshable instance object</span></span>             |
| [<span data-ttu-id="d4866-126">**IWbemHiPerfProvider:: CreateRefreshableEnum**</span><span class="sxs-lookup"><span data-stu-id="d4866-126">**IWbemHiPerfProvider::CreateRefreshableEnum**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)     | <span data-ttu-id="d4866-127">Crea un enumerador actualizable</span><span class="sxs-lookup"><span data-stu-id="d4866-127">Creates a refreshable enumerator</span></span>                  |
| [<span data-ttu-id="d4866-128">**IWbemHiPerfProvider:: StopRefreshing**</span><span class="sxs-lookup"><span data-stu-id="d4866-128">**IWbemHiPerfProvider::StopRefreshing**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)                   | <span data-ttu-id="d4866-129">Detiene la actualización de un enumerador o un objeto de instancia</span><span class="sxs-lookup"><span data-stu-id="d4866-129">Stops refreshing an enumerator or instance object</span></span> |
| [<span data-ttu-id="d4866-130">**IWbemRefresher:: Refresh**</span><span class="sxs-lookup"><span data-stu-id="d4866-130">**IWbemRefresher::Refresh**</span></span>](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh)                                           | <span data-ttu-id="d4866-131">Crea un actualizador</span><span class="sxs-lookup"><span data-stu-id="d4866-131">Creates a refresher</span></span>                               |



 

## <a name="related-topics"></a><span data-ttu-id="d4866-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d4866-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4866-133">Crear un proveedor de instancias en un proveedor de High-Performance</span><span class="sxs-lookup"><span data-stu-id="d4866-133">Making an Instance Provider into a High-Performance Provider</span></span>](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 



