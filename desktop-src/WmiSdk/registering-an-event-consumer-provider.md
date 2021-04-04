---
description: Para crear un proveedor de consumidor de eventos WMI, debe registrar la \_ \_ instancia de Win32Provider que representa el proveedor mediante una instancia de \_ \_ EventConsumerProviderRegistration.
ms.assetid: d1aa035c-f9ee-46b5-9fa5-8af77156f904
ms.tgt_platform: multiple
title: Registrar un proveedor de consumidor de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df6bf47e11b1b9df072f9efbca0ba0f620e96d78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812434"
---
# <a name="registering-an-event-consumer-provider"></a><span data-ttu-id="787b3-103">Registrar un proveedor de consumidor de eventos</span><span class="sxs-lookup"><span data-stu-id="787b3-103">Registering an Event Consumer Provider</span></span>

<span data-ttu-id="787b3-104">Para crear un [*proveedor de consumidor de eventos*](gloss-e.md) WMI, debe registrar la instancia de [**\_ \_ Win32Provider**](--win32provider.md) que representa el proveedor mediante una instancia de [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="787b3-104">To create a WMI [*event consumer provider*](gloss-e.md) you must register the [**\_\_Win32Provider**](--win32provider.md) instance that represents your provider using an instance of [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md).</span></span> <span data-ttu-id="787b3-105">Como objeto COM, el proveedor debe registrarse en el sistema operativo y en WMI.</span><span class="sxs-lookup"><span data-stu-id="787b3-105">As a COM object, your provider must register with the operating system and WMI.</span></span> <span data-ttu-id="787b3-106">En el procedimiento siguiente se supone que ya ha implementado el proceso de registro como se describe en [registrar un proveedor](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="787b3-106">The following procedure assumes that you have already implemented the registration process as described in [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="787b3-107">En el procedimiento siguiente se describe cómo registrar un proveedor de consumidor de eventos.</span><span class="sxs-lookup"><span data-stu-id="787b3-107">The following procedure describes how to register an event consumer provider.</span></span>

<span data-ttu-id="787b3-108">**Para registrar un proveedor de consumidores de eventos**</span><span class="sxs-lookup"><span data-stu-id="787b3-108">**To register an event consumer provider**</span></span>

1.  <span data-ttu-id="787b3-109">Cree una instancia de la clase [**\_ \_ Win32Provider**](--win32provider.md) que describa el proveedor.</span><span class="sxs-lookup"><span data-stu-id="787b3-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class that describes the provider.</span></span>
2.  <span data-ttu-id="787b3-110">Cree una instancia de la clase [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) que describa el conjunto de características del proveedor.</span><span class="sxs-lookup"><span data-stu-id="787b3-110">Create an instance of the [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="787b3-111">Las propiedades definidas por [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) incluyen la ruta de acceso del objeto al proveedor y los nombres de las clases de consumidor lógicas que admite el proveedor del consumidor de eventos.</span><span class="sxs-lookup"><span data-stu-id="787b3-111">The properties that are defined by [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) include the object path to the provider and the names of the logical consumer classes that the event consumer provider supports.</span></span>

    <span data-ttu-id="787b3-112">Asegúrese de etiquetar la clase con los calificadores de [**proveedor**](/windows/desktop/api/Provider/nl-provider-provider) y **dinámicos** .</span><span class="sxs-lookup"><span data-stu-id="787b3-112">Be sure to tag the class with both the **Dynamic** and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifiers.</span></span> <span data-ttu-id="787b3-113">El calificador **dinámico** indica que WMI debe utilizar un proveedor para recuperar las instancias de clase.</span><span class="sxs-lookup"><span data-stu-id="787b3-113">The **Dynamic** qualifier signals that WMI should use a provider to retrieve the class instances.</span></span> <span data-ttu-id="787b3-114">El calificador de **proveedor** especifica el nombre del proveedor que debe usar WMI.</span><span class="sxs-lookup"><span data-stu-id="787b3-114">The **Provider** qualifier specifies the name of the provider that WMI should use.</span></span>

<span data-ttu-id="787b3-115">En el ejemplo de código siguiente se muestra cómo registrar un proveedor de consumidor de eventos.</span><span class="sxs-lookup"><span data-stu-id="787b3-115">The following code example shows how to register an event consumer provider.</span></span>

``` syntax
// Provider registration.
// ======================

instance of __Win32Provider as $P
{
    Name  = "MyEventConsumer";
    CLSID = "{4916157B-FBE7-11d1-AEC4-00C04FB68820}";

    DefaultMachineName = NULL;
    ClientLoadableCLSID = NULL;
    ImpersonationLevel = 0;

    PerUserInitialization = FALSE;
    Pure = TRUE;
    UnloadTimeout = NULL;
};


instance of __EventConsumerProviderRegistration
{
    Provider = $P;
    ConsumerClassNames = { "MyConsumer" };
};
```

 

 



