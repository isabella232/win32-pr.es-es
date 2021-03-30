---
description: 'Hay dos maneras de implementar un proveedor de clases: implementar la interfaz como un proveedor de inserción o como un proveedor de extracción.'
ms.assetid: 2c6d3f73-e219-409b-9347-492035c1eb9f
ms.tgt_platform: multiple
title: Implementar la interfaz principal para un proveedor de clases
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f760dba053cadf56d37445c997fc52a99b242a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360944"
---
# <a name="implementing-the-primary-interface-for-a-class-provider"></a><span data-ttu-id="d5aeb-103">Implementar la interfaz principal para un proveedor de clases</span><span class="sxs-lookup"><span data-stu-id="d5aeb-103">Implementing the Primary Interface for a Class Provider</span></span>

<span data-ttu-id="d5aeb-104">Hay dos maneras de implementar un proveedor de clases: implementar la interfaz como un proveedor de inserción o como un proveedor de extracción.</span><span class="sxs-lookup"><span data-stu-id="d5aeb-104">There are two ways to implement a class provider: implement the interface as a push provider, or as a pull provider.</span></span>

<span data-ttu-id="d5aeb-105">En este tema se describen las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="d5aeb-105">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="d5aeb-106">Implementar la interfaz principal para un proveedor de clase de inserciones</span><span class="sxs-lookup"><span data-stu-id="d5aeb-106">Implementing the Primary Interface for a Push Class Provider</span></span>](#implementing-the-primary-interface-for-a-push-class-provider)
-   [<span data-ttu-id="d5aeb-107">Implementar la interfaz principal para un proveedor de clase de extracción</span><span class="sxs-lookup"><span data-stu-id="d5aeb-107">Implementing the Primary Interface for a Pull Class Provider</span></span>](#implementing-the-primary-interface-for-a-pull-class-provider)

## <a name="implementing-the-primary-interface-for-a-push-class-provider"></a><span data-ttu-id="d5aeb-108">Implementar la interfaz principal para un proveedor de clase de inserciones</span><span class="sxs-lookup"><span data-stu-id="d5aeb-108">Implementing the Primary Interface for a Push Class Provider</span></span>

<span data-ttu-id="d5aeb-109">Mientras que todos los proveedores implementan [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para la inicialización y al menos otra interfaz como su interfaz principal, un proveedor de inserciones solo implementa **IWbemProviderInit**.</span><span class="sxs-lookup"><span data-stu-id="d5aeb-109">Whereas all providers implement [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) for initialization and at least one other interface as their primary interface, a push provider implements only **IWbemProviderInit**.</span></span>

<span data-ttu-id="d5aeb-110">Asegúrese de que la implementación realiza las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="d5aeb-110">Ensure that your implementation performs the following tasks:</span></span>

-   <span data-ttu-id="d5aeb-111">Recupera los datos de clase adecuados.</span><span class="sxs-lookup"><span data-stu-id="d5aeb-111">Retrieves the appropriate class data.</span></span>
-   <span data-ttu-id="d5aeb-112">Coloca los datos en el repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="d5aeb-112">Places the data in the WMI repository.</span></span>
-   <span data-ttu-id="d5aeb-113">Elimina los datos obsoletos.</span><span class="sxs-lookup"><span data-stu-id="d5aeb-113">Deletes obsolete data.</span></span>

<span data-ttu-id="d5aeb-114">Después de completar el proceso de inicialización, WMI controla todas las solicitudes de aplicación para las clases que pertenecen al proveedor de inserciones sin más interacción con el proveedor.</span><span class="sxs-lookup"><span data-stu-id="d5aeb-114">After completing the initialization process, WMI handles all application requests for classes belonging to the push provider without any further provider interaction.</span></span> <span data-ttu-id="d5aeb-115">Después, el proveedor de inserciones actúa eficazmente como un cliente de WMI en lugar de un proveedor.</span><span class="sxs-lookup"><span data-stu-id="d5aeb-115">Afterward, the push provider effectively acts as a client of WMI rather than a provider.</span></span> <span data-ttu-id="d5aeb-116">Para obtener más información sobre la implementación de [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit), vea [inicializar un proveedor](initializing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d5aeb-116">For more information about implementing [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit), see [Initializing a Provider](initializing-a-provider.md).</span></span>

> [!Note]  
> <span data-ttu-id="d5aeb-117">Al llamar a WMI para crear, actualizar o quitar datos en un proveedor de inserciones, establezca el parámetro *lFlags* para incluir la marca de actualización del propietario de la **\_ marca \_ \_ WBEM** en todas las llamadas a métodos [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="d5aeb-117">When calling WMI to create, update, or remove data in a push provider, set the *lFlags* parameter to include the **WBEM\_FLAG\_OWNER\_UPDATE** flag in all calls to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) methods.</span></span>

 

## <a name="implementing-the-primary-interface-for-a-pull-class-provider"></a><span data-ttu-id="d5aeb-118">Implementar la interfaz principal para un proveedor de clase de extracción</span><span class="sxs-lookup"><span data-stu-id="d5aeb-118">Implementing the Primary Interface for a Pull Class Provider</span></span>

<span data-ttu-id="d5aeb-119">Un proveedor de extracción de clases debe implementar [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) como la interfaz principal.</span><span class="sxs-lookup"><span data-stu-id="d5aeb-119">A class pull provider should implement [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) as the primary interface.</span></span> <span data-ttu-id="d5aeb-120">La interfaz **IWbemServices** admite la recuperación de datos, la actualización de datos, la eliminación de datos, la enumeración y el procesamiento de consultas.</span><span class="sxs-lookup"><span data-stu-id="d5aeb-120">The **IWbemServices** interface supports data retrieval, data update, data removal, enumeration, and query processing.</span></span> <span data-ttu-id="d5aeb-121">Sin embargo, dado que las aplicaciones y los proveedores también usan **IWbemServices** para solicitar servicios de WMI, **IWbemServices** contiene muchos métodos que son irrelevantes para un proveedor de clases.</span><span class="sxs-lookup"><span data-stu-id="d5aeb-121">However, because **IWbemServices** is also used by applications and providers to request services of WMI, **IWbemServices** contains many methods that are irrelevant to a class provider.</span></span> <span data-ttu-id="d5aeb-122">La implementación de debe admitir la recuperación y enumeración de clases, a través de los métodos [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) y [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d5aeb-122">Your implementation must support class retrieval and enumeration, through the [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) and [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) methods respectively.</span></span> <span data-ttu-id="d5aeb-123">En la tabla siguiente se enumeran los métodos **IWbemServices** asincrónicos adicionales que se pueden implementar para un proveedor de clases.</span><span class="sxs-lookup"><span data-stu-id="d5aeb-123">The following table lists the additional asynchronous **IWbemServices** methods that you can implement for a class provider.</span></span>



| <span data-ttu-id="d5aeb-124">Método</span><span class="sxs-lookup"><span data-stu-id="d5aeb-124">Method</span></span>                                                     | <span data-ttu-id="d5aeb-125">Característica</span><span class="sxs-lookup"><span data-stu-id="d5aeb-125">Feature</span></span>      |
|------------------------------------------------------------|--------------|
| [<span data-ttu-id="d5aeb-126">**PutInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="d5aeb-126">**PutInstanceAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) | <span data-ttu-id="d5aeb-127">Modificación</span><span class="sxs-lookup"><span data-stu-id="d5aeb-127">Modification</span></span> |
| [<span data-ttu-id="d5aeb-128">**DeleteClassAsync**</span><span class="sxs-lookup"><span data-stu-id="d5aeb-128">**DeleteClassAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) | <span data-ttu-id="d5aeb-129">Eliminación</span><span class="sxs-lookup"><span data-stu-id="d5aeb-129">Deletion</span></span>     |



 

> [!Note]  
> <span data-ttu-id="d5aeb-130">Dado que la devolución de llamada al receptor podría no devolverse en el mismo nivel de autenticación que requiere el cliente, se recomienda usar semisincrónico en lugar de la comunicación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="d5aeb-130">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="d5aeb-131">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="d5aeb-131">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="d5aeb-132">El proveedor de clases debe proporcionar una implementación de código auxiliar que devuelva el **\_ proveedor WBEM E \_ no sea \_ \_ compatible** con todos los demás métodos [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) que no admitan su conjunto de características.</span><span class="sxs-lookup"><span data-stu-id="d5aeb-132">Your class provider should supply a stub implementation that returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** for all of other [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) methods that do not support your feature set.</span></span> <span data-ttu-id="d5aeb-133">En concreto, WMI no admite el procesamiento de consultas para los proveedores de clases.</span><span class="sxs-lookup"><span data-stu-id="d5aeb-133">Specifically, WMI does not support query processing for class providers.</span></span> <span data-ttu-id="d5aeb-134">Como tal, un proveedor de clases debe devolver el **proveedor de WBEM \_ E \_ \_ no \_ compatible** desde su implementación de [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync), establezca su propiedad de registro **QuerySupportLevels** en **null** o en ambas.</span><span class="sxs-lookup"><span data-stu-id="d5aeb-134">As such, a class provider must return **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from their implementation of [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync), set their **QuerySupportLevels** registration property to **NULL**, or both.</span></span>

<span data-ttu-id="d5aeb-135">Las interfaces que implementa un proveedor de clases son muy similares a las interfaces de un proveedor de instancias y un proveedor de métodos.</span><span class="sxs-lookup"><span data-stu-id="d5aeb-135">The interfaces that a class provider implements are very similar to the interfaces for an instance provider and a method provider.</span></span> <span data-ttu-id="d5aeb-136">De hecho, un solo proveedor puede actuar como los tres tipos de proveedor implementando todos los métodos y registrando correctamente.</span><span class="sxs-lookup"><span data-stu-id="d5aeb-136">In fact, a single provider can act as all three types of provider by implementing all the methods and registering properly.</span></span>

 

 



