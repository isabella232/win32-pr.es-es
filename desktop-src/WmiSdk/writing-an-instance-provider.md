---
description: Un proveedor de instancias proporciona instancias de una o varias clases determinadas.
ms.assetid: d53c3399-cba8-4b5d-8da0-b5a23f94c0ae
ms.tgt_platform: multiple
title: Escribir un proveedor de instancias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bddfaa867624bd84cc975d32a8e7b747064d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706558"
---
# <a name="writing-an-instance-provider"></a><span data-ttu-id="ce904-103">Escribir un proveedor de instancias</span><span class="sxs-lookup"><span data-stu-id="ce904-103">Writing an Instance Provider</span></span>

<span data-ttu-id="ce904-104">Un proveedor de instancias proporciona instancias de una o varias clases determinadas.</span><span class="sxs-lookup"><span data-stu-id="ce904-104">An instance provider supplies instances of one or more given classes.</span></span> <span data-ttu-id="ce904-105">Por ejemplo, un proveedor de instancias puede proporcionar información relacionada con una CPU u otro tipo de hardware.</span><span class="sxs-lookup"><span data-stu-id="ce904-105">For example, an instance provider can supply information regarding a CPU or other type of hardware.</span></span> <span data-ttu-id="ce904-106">Dado que los objetos administrados por un proveedor de instancias tienden a cambiar periódicamente, todos los proveedores de instancias se consideran proveedores de extracción; es decir, un proveedor que recupera dinámicamente información relacionada con un objeto administrado siempre que WMI realiza una solicitud de la información.</span><span class="sxs-lookup"><span data-stu-id="ce904-106">Because the objects managed by an instance provider tend to change on a regular basis, all instance providers are considered pull providers; that is, a provider that dynamically retrieves information regarding a managed object whenever WMI makes a request for the information.</span></span> <span data-ttu-id="ce904-107">El nombre proviene de la idea de que WMI "extrae" la información del proveedor en nombre de una solicitud de cliente.</span><span class="sxs-lookup"><span data-stu-id="ce904-107">The name comes from the idea that WMI "pulls" the information from the provider on behalf of a client request.</span></span> <span data-ttu-id="ce904-108">Con la tecnología de extracción, un proveedor de instancias puede admitir la recuperación, enumeración, modificación, eliminación y procesamiento de consultas de una instancia específica.</span><span class="sxs-lookup"><span data-stu-id="ce904-108">Using pull technology, an instance provider can support retrieval, enumeration, modification, deletion, and query processing of a specific instance.</span></span>

<span data-ttu-id="ce904-109">Los proveedores de alto rendimiento pueden aumentar la eficacia de un proveedor de instancias o tener acceso mediante programación a los datos que aparecen en el monitor de sistema.</span><span class="sxs-lookup"><span data-stu-id="ce904-109">High-performance providers can increase the efficiency of an instance provider or programmatically access the data that appears in System Monitor.</span></span> <span data-ttu-id="ce904-110">Para obtener más información, vea [crear un proveedor de instancias en un proveedor de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ce904-110">For more information, see [Making an Instance Provider into a High-Performance Provider](making-an-instance-provider-into-a-high-performance-provider.md).</span></span>

<span data-ttu-id="ce904-111">En el procedimiento siguiente se describe cómo escribir un proveedor de instancias.</span><span class="sxs-lookup"><span data-stu-id="ce904-111">The following procedure describes how to write an instance provider.</span></span>

<span data-ttu-id="ce904-112">**Para escribir un proveedor de instancias**</span><span class="sxs-lookup"><span data-stu-id="ce904-112">**To write an instance provider**</span></span>

1.  <span data-ttu-id="ce904-113">[Registre el proveedor con WMI](registering-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ce904-113">[Register your provider with WMI](registering-an-instance-provider.md).</span></span>

    <span data-ttu-id="ce904-114">Los proveedores de instancias se registran en WMI mediante la creación de una instancia de [**\_ \_ Win32Provider**](--win32provider.md) y una clase [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="ce904-114">Instance providers register with WMI by creating a [**\_\_Win32Provider**](--win32provider.md) instance and an [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) class.</span></span>

2.  <span data-ttu-id="ce904-115">[Inicialice el proveedor](initializing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ce904-115">[Initialize your provider](initializing-a-provider.md).</span></span>

    <span data-ttu-id="ce904-116">WMI usa [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para cargar e inicializar un proveedor.</span><span class="sxs-lookup"><span data-stu-id="ce904-116">WMI uses [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) to load and initialize a provider.</span></span> <span data-ttu-id="ce904-117">Se trata de una tarea común a todos los proveedores.</span><span class="sxs-lookup"><span data-stu-id="ce904-117">This is a task common to all providers.</span></span>

    > [!Note]  
    > <span data-ttu-id="ce904-118">Se recomienda encarecidamente a los proveedores de instancias que utilicen el modelo de multithreading "both".</span><span class="sxs-lookup"><span data-stu-id="ce904-118">Instance providers are strongly encouraged to use the multithreading model "Both".</span></span>

     

3.  <span data-ttu-id="ce904-119">[Implemente la interfaz IWbemServices para su proveedor](implementing-the-primary-interface-for-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ce904-119">[Implement the IWbemServices interface for your provider](implementing-the-primary-interface-for-an-instance-provider.md).</span></span>

    <span data-ttu-id="ce904-120">La interfaz [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) es la interfaz principal para un proveedor de instancias.</span><span class="sxs-lookup"><span data-stu-id="ce904-120">The [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface is the primary interface for an instance provider.</span></span>

4.  <span data-ttu-id="ce904-121">Agregue el código adicional necesario para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="ce904-121">Add any additional code necessary for your provider.</span></span>

    <span data-ttu-id="ce904-122">Al diseñar el proveedor, lo más probable es que necesite llamar a interfaces de WMI.</span><span class="sxs-lookup"><span data-stu-id="ce904-122">When designing your provider, you will most likely need to call WMI interfaces.</span></span> <span data-ttu-id="ce904-123">Para obtener más información, consulte [realizar llamadas a WMI](making-calls-to-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="ce904-123">For more information, see [Making Calls to WMI](making-calls-to-wmi.md).</span></span>

    <span data-ttu-id="ce904-124">Al recuperar información de un cliente, es posible que necesite tener acceso a los niveles de seguridad de ese cliente.</span><span class="sxs-lookup"><span data-stu-id="ce904-124">When retrieving information for a client, you may need to access the security levels for that client.</span></span> <span data-ttu-id="ce904-125">Para obtener más información, vea [Suplantar a un cliente](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="ce904-125">For more information, see [Impersonating a Client](impersonating-a-client.md).</span></span>

5.  <span data-ttu-id="ce904-126">Si es necesario, [implemente la interfaz de alto rendimiento](improving-the-efficiency-of-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ce904-126">If necessary, [implement the high-performance interface](improving-the-efficiency-of-an-instance-provider.md).</span></span>

    <span data-ttu-id="ce904-127">La interfaz de alto rendimiento aumenta la velocidad a la que el proveedor puede reaccionar ante las solicitudes de WMI.</span><span class="sxs-lookup"><span data-stu-id="ce904-127">The high-performance interface increases the speed at which the provider can react to requests from WMI.</span></span>

6.  <span data-ttu-id="ce904-128">Si es necesario, [implemente la compatibilidad con las actualizaciones de instancias parciales](supporting-partial-instance-operations.md).</span><span class="sxs-lookup"><span data-stu-id="ce904-128">If necessary, [implement support for partial-instance updates](supporting-partial-instance-operations.md).</span></span>

    <span data-ttu-id="ce904-129">Como su nombre implica, una actualización de instancia parcial es una técnica que se usa para actualizar solo parte de una instancia.</span><span class="sxs-lookup"><span data-stu-id="ce904-129">As the name implies, a partial-instance update is a technique use to update only part of an instance.</span></span> <span data-ttu-id="ce904-130">Para obtener más información sobre cómo llamar a una instancia parcial desde un cliente, vea [Actualizar parte de una instancia](updating-part-of-an-instance.md) y [recuperar parte de una instancia de WMI](retrieving-part-of-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="ce904-130">For more information about calling a partial instance from a client, see [Updating Part of an Instance](updating-part-of-an-instance.md) and [Retrieving Part of a WMI Instance](retrieving-part-of-an-instance.md).</span></span>

7.  <span data-ttu-id="ce904-131">Reemplace el proveedor preexistente con el código nuevo.</span><span class="sxs-lookup"><span data-stu-id="ce904-131">Replace the preexisting provider with your new code.</span></span>

    <span data-ttu-id="ce904-132">No es necesario que realice este paso si no tiene un proveedor preexistente en el que realizar la copia.</span><span class="sxs-lookup"><span data-stu-id="ce904-132">You do not need to perform this step if you do not have a preexisting provider to copy over.</span></span> <span data-ttu-id="ce904-133">Para obtener más información, consulte [actualización de un proveedor](updating-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ce904-133">For more information, see [Updating a Provider](updating-a-provider.md).</span></span>

 

 



