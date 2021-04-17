---
title: Implementar una interfaz principal de proveedor de instancias
description: Un proveedor de instancias utiliza los métodos asincrónicos de IWbemServices como la interfaz principal para WMI.
ms.assetid: 80425fa8-2746-4eba-8e7d-4a61e222852a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 443b095cfbb134cf031ae8e1403565bc1fa31aea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716555"
---
# <a name="implementing-an-instance-provider-primary-interface"></a><span data-ttu-id="42e1e-103">Implementar una interfaz principal de proveedor de instancias</span><span class="sxs-lookup"><span data-stu-id="42e1e-103">Implementing an instance provider primary interface</span></span>

<span data-ttu-id="42e1e-104">Un proveedor de instancias utiliza los métodos asincrónicos de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) como la interfaz principal para WMI.</span><span class="sxs-lookup"><span data-stu-id="42e1e-104">An instance provider uses the asynchronous methods of [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) as the primary interface to WMI.</span></span> <span data-ttu-id="42e1e-105">Al implementar solo los métodos que satisfacen las necesidades de su proveedor de instancias, puede reducir la cantidad de recursos que emplea para codificar.</span><span class="sxs-lookup"><span data-stu-id="42e1e-105">By implementing only the methods that fulfill the needs of your instance provider, you can reduce the amount of resources you spend coding.</span></span> <span data-ttu-id="42e1e-106">Sin embargo, mediante la implementación de métodos reservados para otros tipos de proveedores, puede reducir el número de proveedores que escribe.</span><span class="sxs-lookup"><span data-stu-id="42e1e-106">However, by implementing methods reserved for other types of providers, you can reduce the number of providers you write.</span></span>

<span data-ttu-id="42e1e-107">Dado que las aplicaciones y los proveedores también lo utilizan para solicitar servicios de WMI, [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) contiene muchos métodos que son irrelevantes para un proveedor de instancias.</span><span class="sxs-lookup"><span data-stu-id="42e1e-107">Because it is also used by applications and providers to request services of WMI, [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) contains many methods that are irrelevant to an instance provider.</span></span> <span data-ttu-id="42e1e-108">En la tabla siguiente se enumeran los métodos **IWbemServices** que se pueden implementar para un proveedor de instancias.</span><span class="sxs-lookup"><span data-stu-id="42e1e-108">The following table lists the **IWbemServices** methods that you can implement for an instance provider.</span></span>



| <span data-ttu-id="42e1e-109">Método</span><span class="sxs-lookup"><span data-stu-id="42e1e-109">Method</span></span>                                                                   | <span data-ttu-id="42e1e-110">Característica</span><span class="sxs-lookup"><span data-stu-id="42e1e-110">Feature</span></span>          |
|--------------------------------------------------------------------------|------------------|
| [<span data-ttu-id="42e1e-111">**GetObjectAsync**</span><span class="sxs-lookup"><span data-stu-id="42e1e-111">**GetObjectAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)                   | <span data-ttu-id="42e1e-112">Recuperación</span><span class="sxs-lookup"><span data-stu-id="42e1e-112">Retrieval</span></span>        |
| [<span data-ttu-id="42e1e-113">**PutInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="42e1e-113">**PutInstanceAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)               | <span data-ttu-id="42e1e-114">Modificación</span><span class="sxs-lookup"><span data-stu-id="42e1e-114">Modification</span></span>     |
| [<span data-ttu-id="42e1e-115">**DeleteInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="42e1e-115">**DeleteInstanceAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)         | <span data-ttu-id="42e1e-116">Eliminación</span><span class="sxs-lookup"><span data-stu-id="42e1e-116">Deletion</span></span>         |
| [<span data-ttu-id="42e1e-117">**CreateInstanceEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="42e1e-117">**CreateInstanceEnumAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) | <span data-ttu-id="42e1e-118">Enumeración</span><span class="sxs-lookup"><span data-stu-id="42e1e-118">Enumeration</span></span>      |
| [<span data-ttu-id="42e1e-119">**ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="42e1e-119">**ExecQueryAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)                   | <span data-ttu-id="42e1e-120">Procesamiento de consultas</span><span class="sxs-lookup"><span data-stu-id="42e1e-120">Query processing</span></span> |



 

<span data-ttu-id="42e1e-121">En el caso de los métodos que no use, el proveedor puede proporcionar una implementación de código auxiliar que devuelva el **proveedor de WBEM \_ E \_ \_ no \_ compatible**.</span><span class="sxs-lookup"><span data-stu-id="42e1e-121">For methods that you do not use, your provider can supply a stub implementation that returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE**.</span></span> <span data-ttu-id="42e1e-122">Esto incluye todos los métodos [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) que no aparecen en la tabla anterior.</span><span class="sxs-lookup"><span data-stu-id="42e1e-122">This includes all [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) methods not listed in the above table.</span></span>

<span data-ttu-id="42e1e-123">Un único proveedor puede actuar simultáneamente como una clase, una instancia y un proveedor de métodos mediante el registro y la implementación correctos de todos los métodos pertinentes.</span><span class="sxs-lookup"><span data-stu-id="42e1e-123">A single provider can act simultaneously as a class, instance, and method provider by proper registration and implementation of all relevant methods.</span></span> <span data-ttu-id="42e1e-124">Para obtener más información, vea [escribir un proveedor de clases](writing-a-class-provider.md) y [escribir un proveedor de métodos](writing-a-method-provider.md).</span><span class="sxs-lookup"><span data-stu-id="42e1e-124">For more information, see [Writing a Class Provider](writing-a-class-provider.md) and [Writing a Method Provider](writing-a-method-provider.md).</span></span>

 

 



