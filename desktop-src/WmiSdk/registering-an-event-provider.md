---
description: Para crear un proveedor de eventos WMI, debe registrar la \_ \_ instancia de Win32Provider que representa el proveedor mediante una instancia de \_ \_ EventProviderRegistration.
ms.assetid: 81f2ba3b-a1cb-42f5-b1a7-b1ca65963902
ms.tgt_platform: multiple
title: Registrar un proveedor de eventos
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2a4aa77c5c5936639435844179f259080085e02c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156764"
---
# <a name="registering-an-event-provider"></a><span data-ttu-id="1b115-103">Registrar un proveedor de eventos</span><span class="sxs-lookup"><span data-stu-id="1b115-103">Registering an Event Provider</span></span>

<span data-ttu-id="1b115-104">Para crear un [*proveedor de eventos*](gloss-e.md) WMI, debe registrar la instancia de [**\_ \_ Win32Provider**](--win32provider.md) que representa el proveedor mediante una instancia de [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="1b115-104">To create a WMI [*event provider*](gloss-e.md) you must register the [**\_\_Win32Provider**](--win32provider.md) instance that represents your provider using an instance of [**\_\_EventProviderRegistration**](--eventproviderregistration.md).</span></span> <span data-ttu-id="1b115-105">Como objeto COM, el proveedor debe registrarse en el sistema operativo y en WMI.</span><span class="sxs-lookup"><span data-stu-id="1b115-105">As a COM object, your provider must register with the operating system and WMI.</span></span> <span data-ttu-id="1b115-106">En el procedimiento siguiente se supone que ya ha implementado el proceso de registro como se describe en [registrar un proveedor](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="1b115-106">The following procedure assumes that you have already implemented the registration process as described in [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="1b115-107">En el procedimiento siguiente se describe cómo registrar un proveedor de eventos.</span><span class="sxs-lookup"><span data-stu-id="1b115-107">The following procedure describes how to register an event provider.</span></span>

<span data-ttu-id="1b115-108">**Para registrar un proveedor de eventos**</span><span class="sxs-lookup"><span data-stu-id="1b115-108">**To register an event provider**</span></span>

1.  <span data-ttu-id="1b115-109">Cree una instancia de la clase [**\_ \_ Win32Provider**](--win32provider.md) que describa el proveedor.</span><span class="sxs-lookup"><span data-stu-id="1b115-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class that describes the provider.</span></span>
2.  <span data-ttu-id="1b115-110">Cree una instancia de la clase [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) que describa el conjunto de características del proveedor.</span><span class="sxs-lookup"><span data-stu-id="1b115-110">Create an instance of the [**\_\_EventProviderRegistration**](--eventproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="1b115-111">La clase [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) hereda muchas propiedades de la clase primaria [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="1b115-111">The [**\_\_EventProviderRegistration**](--eventproviderregistration.md) class inherits many properties from the [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md) parent class.</span></span> <span data-ttu-id="1b115-112">Las propiedades locales de la clase **\_ \_ EventProviderRegistration** son la ruta de acceso del objeto al proveedor y una lista de consultas que describen los eventos que admite el proveedor.</span><span class="sxs-lookup"><span data-stu-id="1b115-112">The properties local to the **\_\_EventProviderRegistration** class are the object path to the provider and a list of queries that describe the events that the provider supports.</span></span> <span data-ttu-id="1b115-113">Para obtener más información, consulte [consultar WMI](querying-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="1b115-113">For more information, see [Querying WMI](querying-wmi.md).</span></span>

3.  <span data-ttu-id="1b115-114">Cargue la implementación de las clases [**\_ \_ Win32Provider**](--win32provider.md) y [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) en el repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="1b115-114">Load your implementation of the [**\_\_Win32Provider**](--win32provider.md) and [**\_\_EventProviderRegistration**](--eventproviderregistration.md) classes into the WMI repository.</span></span>

    <span data-ttu-id="1b115-115">WMI utiliza la definición de clase para registrar y tener acceso al proveedor de eventos.</span><span class="sxs-lookup"><span data-stu-id="1b115-115">WMI uses your class definition to register and access your event provider.</span></span> <span data-ttu-id="1b115-116">Para obtener más información, vea [registrar un proveedor](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="1b115-116">For more information, see [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="1b115-117">En el ejemplo de código siguiente se describe una implementación de una clase [**\_ \_ Win32Provider**](--win32provider.md) y una clase [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="1b115-117">The following code example describes an implementation of a [**\_\_Win32Provider**](--win32provider.md) class and a [**\_\_EventProviderRegistration**](--eventproviderregistration.md) class.</span></span>

``` syntax
instance of __Win32Provider as $P
{
    ClientLoadableCLSID = NULL;
    CLSID = "{AA7828C5-95F9-11d2-BB0D-00C042424242}";
    DefaultMachineName = NULL;
    ImpersonationLevel = 0;
    InitializationReentrancy = 0;
    InitializeAsAdminFirst = FALSE;
    Name = "FaxEventProvider";
    PerLocaleInitialization = FALSE;
    PerUserInitialization = FALSE;
    Pure = TRUE;
    UnloadTimeout = NULL;
};

instance of __EventProviderRegistration
{  
Provider = $P;
EventQueryList = {
         "SELECT * FROM FaxEvent",
         "SELECT * FROM __InstanceCreationEvent WHERE TargetInstance ISA \"Win32_LogicalDisk\""};
};
```

<span data-ttu-id="1b115-118">La primera consulta indica que el proveedor genera todas las notificaciones de eventos para la clase de evento extrínseco FaxEvent.</span><span class="sxs-lookup"><span data-stu-id="1b115-118">The first query indicates that the provider generates all event notifications for the extrinsic event class FaxEvent.</span></span> <span data-ttu-id="1b115-119">Dado que utiliza el operador ISA, la segunda consulta implica que el proveedor genera notificaciones para todos los eventos de creación de instancia para la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) y todas sus subclases.</span><span class="sxs-lookup"><span data-stu-id="1b115-119">Because it uses the ISA operator, the second query implies that the provider generates notifications for all instance creation events for the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class and all of its subclasses.</span></span>

<span data-ttu-id="1b115-120">Cuando un proveedor se registra para proporcionar un evento intrínseco, el evento se debe aplicar a todas las instancias de una clase.</span><span class="sxs-lookup"><span data-stu-id="1b115-120">When a provider registers to provide an intrinsic event, the event must apply to all instances of a class.</span></span> <span data-ttu-id="1b115-121">En otras palabras, no se puede escribir una consulta para proporcionar eventos de creación de instancias solo para algunas de las unidades de disco que pertenecen a la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="1b115-121">In other words, a query cannot be written to provide instance creation events for only some of the disk drives that belong to the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>

 

 
