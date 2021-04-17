---
description: Un proveedor de clases administra una clase o serie de clases para WMI.
ms.assetid: 755f1fde-a0bf-43f6-a01d-2da7d4e6c10d
ms.tgt_platform: multiple
title: Escribir un proveedor de clases
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff1e20115c4f833ad828e8d181ca97782d233130
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716188"
---
# <a name="writing-a-class-provider"></a><span data-ttu-id="afe58-103">Escribir un proveedor de clases</span><span class="sxs-lookup"><span data-stu-id="afe58-103">Writing a Class Provider</span></span>

<span data-ttu-id="afe58-104">Un proveedor de clases administra una clase o serie de clases para WMI.</span><span class="sxs-lookup"><span data-stu-id="afe58-104">A class provider manages a class or series of classes for WMI.</span></span> <span data-ttu-id="afe58-105">Un proveedor de clases puede ser de inserción o de extracción; es decir, puede almacenar sus propios datos o permitir a WMI almacenar datos para ellos en el servicio de administración de Windows.</span><span class="sxs-lookup"><span data-stu-id="afe58-105">A class provider can either be push or pull; that is, it can either store its own data or allow WMI to store data for it in the Windows Management Service.</span></span> <span data-ttu-id="afe58-106">Aunque un proveedor de clases se instala en un equipo específico, puede cambiar las definiciones de clase en toda la empresa.</span><span class="sxs-lookup"><span data-stu-id="afe58-106">Although a class provider is installed on a specific machine, it can change the class definitions across an entire enterprise.</span></span> <span data-ttu-id="afe58-107">Por lo tanto, la mayoría de los desarrolladores no suelen crear proveedores de clases.</span><span class="sxs-lookup"><span data-stu-id="afe58-107">Therefore, most developers do not often create class providers.</span></span>

<span data-ttu-id="afe58-108">Antes de construir un proveedor de clases, compruebe que las clases admitidas realmente se deben generar dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="afe58-108">Before constructing a class provider, verify that the supported classes truly must be generated dynamically.</span></span> <span data-ttu-id="afe58-109">En la mayoría de los casos, la lista de clases es de cambio lento y finita.</span><span class="sxs-lookup"><span data-stu-id="afe58-109">In most cases, the list of classes is slow-changing and finite.</span></span> <span data-ttu-id="afe58-110">Si es así, no debería tener que crear un proveedor de clases.</span><span class="sxs-lookup"><span data-stu-id="afe58-110">If this is the case, you should not have to create a class provider.</span></span> <span data-ttu-id="afe58-111">En su lugar, puede colocar las definiciones de clase en el repositorio WMI mediante la API de WMI o un archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="afe58-111">Instead, you can place your class definitions in the WMI repository using the WMI API or a MOF file.</span></span>

<span data-ttu-id="afe58-112">En el procedimiento siguiente se describe cómo implementar un proveedor de clases.</span><span class="sxs-lookup"><span data-stu-id="afe58-112">The following procedure describes how to implement a class provider.</span></span>

<span data-ttu-id="afe58-113">**Para implementar un proveedor de clases**</span><span class="sxs-lookup"><span data-stu-id="afe58-113">**To implement a class provider**</span></span>

1.  <span data-ttu-id="afe58-114">Determine si el proveedor es un proveedor de inserción o de extracción.</span><span class="sxs-lookup"><span data-stu-id="afe58-114">Determine if your provider is a push or pull provider.</span></span>

    <span data-ttu-id="afe58-115">Un proveedor de extracción proporciona datos dinámicamente en respuesta a una solicitud de aplicación, mientras que los proveedores de inserción almacenan sus datos una vez en el repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="afe58-115">A pull provider supplies data dynamically in response to an application request, whereas push providers store their data once in the WMI repository.</span></span> <span data-ttu-id="afe58-116">Para obtener más información, vea [determinar el estado de inserción o extracción](determining-push-or-pull-status.md).</span><span class="sxs-lookup"><span data-stu-id="afe58-116">For more information, see [Determining Push or Pull Status](determining-push-or-pull-status.md).</span></span>

2.  <span data-ttu-id="afe58-117">Diseñe y registre el proveedor de clases con WMI.</span><span class="sxs-lookup"><span data-stu-id="afe58-117">Design and register your class provider with WMI.</span></span>

    <span data-ttu-id="afe58-118">Los proveedores de clases se registran en WMI mediante la creación de una instancia de [**\_ \_ Win32Provider**](--win32provider.md) y una instancia de [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="afe58-118">Class providers register with WMI by creating a [**\_\_Win32Provider**](--win32provider.md) instance and a [**\_\_ClassProviderRegistration**](--classproviderregistration.md) instance.</span></span> <span data-ttu-id="afe58-119">Para obtener más información, vea [registrar un proveedor de clases](registering-a-class-provider.md).</span><span class="sxs-lookup"><span data-stu-id="afe58-119">For more information, see [Registering a Class Provider](registering-a-class-provider.md).</span></span>

3.  <span data-ttu-id="afe58-120">Implemente la interfaz [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="afe58-120">Implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface for your provider.</span></span>

    <span data-ttu-id="afe58-121">WMI usa [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para cargar e inicializar un proveedor.</span><span class="sxs-lookup"><span data-stu-id="afe58-121">WMI uses [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) to load and initialize a provider.</span></span> <span data-ttu-id="afe58-122">Si está diseñando un proveedor de inserciones, **IWbemProviderInit** es la única interfaz que va a implementar.</span><span class="sxs-lookup"><span data-stu-id="afe58-122">If you are designing a push provider, **IWbemProviderInit** is the only interface you will implement.</span></span> <span data-ttu-id="afe58-123">Para obtener más información, vea [inicializar un proveedor](initializing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="afe58-123">For more information, see [Initializing a Provider](initializing-a-provider.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="afe58-124">Se recomienda encarecidamente a los proveedores de clases que utilicen el modelo de multithreading "both".</span><span class="sxs-lookup"><span data-stu-id="afe58-124">Class providers are strongly encouraged to use the multithreading model "Both".</span></span>

     

4.  <span data-ttu-id="afe58-125">Agregue el código adicional necesario para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="afe58-125">Add any additional code necessary for your provider.</span></span>

    <span data-ttu-id="afe58-126">Al diseñar el proveedor, lo más probable es que necesite llamar a interfaces de WMI.</span><span class="sxs-lookup"><span data-stu-id="afe58-126">When designing your provider, you will most likely need to call WMI interfaces.</span></span> <span data-ttu-id="afe58-127">Para obtener más información, consulte [llamar a un método](calling-a-method.md) y [mantener los niveles de seguridad en un proveedor](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="afe58-127">For more information, see [Calling a Method](calling-a-method.md) and [Maintaining Security Levels in a Provider](impersonating-a-client.md).</span></span>

    <span data-ttu-id="afe58-128">Al recuperar información de un cliente, es posible que necesite tener acceso a los niveles de seguridad de ese cliente.</span><span class="sxs-lookup"><span data-stu-id="afe58-128">When retrieving information for a client, you may need to access the security levels for that client.</span></span> <span data-ttu-id="afe58-129">Para obtener más información, vea [Suplantar a un cliente](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="afe58-129">For more information, see [Impersonating a Client](impersonating-a-client.md).</span></span>

5.  <span data-ttu-id="afe58-130">Implemente la interfaz [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) para su proveedor.</span><span class="sxs-lookup"><span data-stu-id="afe58-130">Implement the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface for your provider.</span></span>

    <span data-ttu-id="afe58-131">La interfaz [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) es la interfaz principal para un proveedor de clase de extracción.</span><span class="sxs-lookup"><span data-stu-id="afe58-131">The [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface is the primary interface for a pull class provider.</span></span> <span data-ttu-id="afe58-132">Para obtener más información, vea [implementar la interfaz principal para un proveedor de clases](implementing-the-primary-interface-for-a-class-provider.md).</span><span class="sxs-lookup"><span data-stu-id="afe58-132">For more information, see [Implementing the Primary Interface for a Class Provider](implementing-the-primary-interface-for-a-class-provider.md).</span></span>

6.  <span data-ttu-id="afe58-133">Reemplace el proveedor preexistente con el código nuevo.</span><span class="sxs-lookup"><span data-stu-id="afe58-133">Replace the preexisting provider with your new code.</span></span>

    <span data-ttu-id="afe58-134">No es necesario que realice este paso si no tiene un proveedor preexistente en el que realizar la copia.</span><span class="sxs-lookup"><span data-stu-id="afe58-134">You do not need to perform this step if you do not have a preexisting provider to copy over.</span></span> <span data-ttu-id="afe58-135">Para obtener más información, consulte [actualización de un proveedor](updating-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="afe58-135">For more information, see [Updating a Provider](updating-a-provider.md).</span></span>

 

 



