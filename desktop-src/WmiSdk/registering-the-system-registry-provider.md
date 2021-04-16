---
description: El proveedor del registro del sistema se registra como parte del proceso de instalación de WMI en Windows.
ms.assetid: ce5d0785-6e1b-411c-91df-f25767310530
ms.tgt_platform: multiple
title: Registrar el proveedor del registro del sistema
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d600872c4efab5560f4fd794cac63beb4365841c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706097"
---
# <a name="registering-the-system-registry-provider"></a><span data-ttu-id="59aed-103">Registrar el proveedor del registro del sistema</span><span class="sxs-lookup"><span data-stu-id="59aed-103">Registering the System Registry Provider</span></span>

<span data-ttu-id="59aed-104">El proveedor del registro del sistema se registra como parte del proceso de instalación de WMI en Windows.</span><span class="sxs-lookup"><span data-stu-id="59aed-104">The System Registry provider is registered as part of the WMI installation process on Windows.</span></span> <span data-ttu-id="59aed-105">Si usa otra plataforma y desea utilizar el proveedor del registro del sistema, primero debe registrar el proveedor siguiendo los pasos que se describen a continuación.</span><span class="sxs-lookup"><span data-stu-id="59aed-105">If you are using another platform and want to use the System Registry provider, you must first register the provider yourself following the steps described below.</span></span>

<span data-ttu-id="59aed-106">En el procedimiento siguiente se describe cómo registrar el proveedor del registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="59aed-106">The following procedure describes how to register the System Registry provider.</span></span>

<span data-ttu-id="59aed-107">**Para registrar el proveedor del registro del sistema**</span><span class="sxs-lookup"><span data-stu-id="59aed-107">**To register the System Registry provider**</span></span>

1.  <span data-ttu-id="59aed-108">Registre el proveedor como un servidor COM.</span><span class="sxs-lookup"><span data-stu-id="59aed-108">Register the provider as a COM server.</span></span>

    <span data-ttu-id="59aed-109">Si es necesario, puede que tenga que crear entradas del registro.</span><span class="sxs-lookup"><span data-stu-id="59aed-109">If necessary, you may need to create registry entries.</span></span> <span data-ttu-id="59aed-110">Este proceso se aplica a todos los servidores COM y no está relacionado con WMI.</span><span class="sxs-lookup"><span data-stu-id="59aed-110">This process applies to all COM servers and is unrelated to WMI.</span></span> <span data-ttu-id="59aed-111">Para obtener más información, vea la documentación de [com](https://msdn.microsoft.com/library/aa139695.aspx) en el kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="59aed-111">For more information, see the [COM](https://msdn.microsoft.com/library/aa139695.aspx) documentation in the Microsoft Windows Software Development Kit (SDK).</span></span>

2.  <span data-ttu-id="59aed-112">Cree una instancia de la clase [**\_ \_ Win32Provider**](--win32provider.md) para describir la implementación del proveedor del registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="59aed-112">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class to describe the implementation of the System Registry provider.</span></span>

    <span data-ttu-id="59aed-113">La instancia de [**\_ \_ Win32Provider**](--win32provider.md) describe el nombre del proveedor y su identificador de clase (**CLSID**).</span><span class="sxs-lookup"><span data-stu-id="59aed-113">The [**\_\_Win32Provider**](--win32provider.md) instance describes the name of the provider and its class identifier (**CLSID**).</span></span>

    <span data-ttu-id="59aed-114">En el ejemplo siguiente se describe cómo registrar [**\_ \_ Win32Provider**](--win32provider.md) como una propiedad de instancia, un evento o un proveedor de métodos.</span><span class="sxs-lookup"><span data-stu-id="59aed-114">The following example describes how to register [**\_\_Win32Provider**](--win32provider.md) as an instance property, event, or method provider.</span></span>

    ``` syntax
    // Instance provider
    instance of __Win32Provider as $InstProv
    {
        Name    = "RegProv" ;
        ClsId   = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}" ;
    };    
    // Property provider 
    instance of __Win32Provider as $PropProv 
    {
        Name = "RegPropProv"; 
        Clsid = "{72967901-68EC-11d0-B729-00AA0062CBB7}"; 
    }; 
    // Event provider
    instance of __Win32Provider as $RegEvent
    {
        Name = "RegistryEventProvider";
        Clsid = "{fa77a74e-e109-11d0-ad6e-00c04fd8fdff}";
    };
    instance of __Win32Provider as $RegMethod
    {
        Name = "RegistryMethodProvider";
        Clsid = "{44DE513E-60C2-11d3-AF33-00C04F79FEB1}";
    };
    ```

3.  <span data-ttu-id="59aed-115">Cree una o más instancias de clases derivadas de la clase [**\_ \_ ProviderRegistration**](--providerregistration.md) para describir la implementación lógica del proveedor del registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="59aed-115">Create one or more instances of classes derived from the [**\_\_ProviderRegistration**](--providerregistration.md) class to describe the logical implementation of the System Registry provider.</span></span>

    <span data-ttu-id="59aed-116">Dependiendo del propósito para el que registre el proveedor del registro del sistema, puede crear una o varias de las siguientes clases.</span><span class="sxs-lookup"><span data-stu-id="59aed-116">Depending on the purpose for which you are registering the System Registry provider, you can create one or more of the following classes.</span></span>

    [<span data-ttu-id="59aed-117">**\_\_InstanceProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="59aed-117">**\_\_InstanceProviderRegistration**</span></span>](--instanceproviderregistration.md)

    [<span data-ttu-id="59aed-118">**\_\_PropertyProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="59aed-118">**\_\_PropertyProviderRegistration**</span></span>](--propertyproviderregistration.md)

    [<span data-ttu-id="59aed-119">**\_\_EventProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="59aed-119">**\_\_EventProviderRegistration**</span></span>](--eventproviderregistration.md)

    [<span data-ttu-id="59aed-120">**\_\_MethodProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="59aed-120">**\_\_MethodProviderRegistration**</span></span>](--methodproviderregistration.md)

    <span data-ttu-id="59aed-121">En el siguiente ejemplo de código MOF se describe cómo se puede registrar el proveedor del registro del sistema como una instancia, una propiedad, un evento o un proveedor de métodos.</span><span class="sxs-lookup"><span data-stu-id="59aed-121">The following MOF code example describes how you can register the System Registry provider as an instance, property, event, or method provider.</span></span>

    ``` syntax
    instance of __InstanceProviderRegistration
    {
        Provider = $InstProv;
        SupportsPut = TRUE;
        SupportsGet = TRUE;
        SupportsDelete = FALSE;
        SupportsEnumeration = TRUE;
    };
    instance of __PropertyProviderRegistration
    {
        Provider = $PropProv;
        SupportsPut = TRUE;
        SupportsGet = TRUE;
    }; 
    instance of __EventProviderRegistration
    {
        Provider = $RegEvent;
        EventQueryList = {
                "select * from RegistryKeyChangeEvent",
                "select * from RegistryValueChangeEvent",
                "select * from RegistryTreeChangeEvent"};
    };
    // Method provider
    instance of __MethodProviderRegistration
    {
        Provider = $RegMethod;
    };
    ```

4.  <span data-ttu-id="59aed-122">Compile el archivo MOF mediante el compilador MOF o la interfaz [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .</span><span class="sxs-lookup"><span data-stu-id="59aed-122">Compile the MOF file using the MOF compiler or the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface.</span></span>

<span data-ttu-id="59aed-123">El archivo RegEvent. mof proporcionado en la sección WMI del Windows SDK contiene las instancias [**\_ \_ Win32Provider**](--win32provider.md) y [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) necesarias para registrar el proveedor del registro del sistema como un proveedor de eventos.</span><span class="sxs-lookup"><span data-stu-id="59aed-123">The RegEvent.mof file provided in the WMI section of the Windows SDK contains the [**\_\_Win32Provider**](--win32provider.md) and [**\_\_EventProviderRegistration**](--eventproviderregistration.md) instances necessary to register the System Registry provider as an event provider.</span></span> <span data-ttu-id="59aed-124">Para obtener más información acerca del registro de un proveedor, vea [registrar un proveedor](registering-a-provider.md) y [recibir un evento WMI](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="59aed-124">For more information about registering a provider, see [Registering a Provider](registering-a-provider.md) and [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

 

 



