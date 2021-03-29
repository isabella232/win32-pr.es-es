---
description: Para crear un proveedor de métodos WMI, debe registrar la \_ \_ instancia de Win32Provider que representa el proveedor mediante una instancia de \_ \_ MethodProviderRegistration.
ms.assetid: 1cfb16ae-8dcf-437d-b779-db2f30bb0d34
ms.tgt_platform: multiple
title: Registrar un proveedor de métodos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a399f90c6fc6f97e9ada8051055505b43885da3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277697"
---
# <a name="registering-a-method-provider"></a><span data-ttu-id="5382f-103">Registrar un proveedor de métodos</span><span class="sxs-lookup"><span data-stu-id="5382f-103">Registering a Method Provider</span></span>

<span data-ttu-id="5382f-104">Para crear un [*proveedor de métodos*](gloss-m.md) WMI, debe registrar la instancia de [**\_ \_ Win32Provider**](--win32provider.md) que representa el proveedor mediante una instancia de [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="5382f-104">To create a WMI [*method provider*](gloss-m.md) you must register the [**\_\_Win32Provider**](--win32provider.md) instance that represents your provider using an instance of [**\_\_MethodProviderRegistration**](--methodproviderregistration.md).</span></span> <span data-ttu-id="5382f-105">Después de crear una instancia de [**\_ \_ Win32Provider**](--win32provider.md), debe registrar ese proveedor con WMI.</span><span class="sxs-lookup"><span data-stu-id="5382f-105">After creating an instance of [**\_\_Win32Provider**](--win32provider.md), you must register that provider with WMI.</span></span> <span data-ttu-id="5382f-106">Como objeto COM, el proveedor debe registrarse en el sistema operativo y en WMI.</span><span class="sxs-lookup"><span data-stu-id="5382f-106">As a COM object, your provider must register with the operating system and WMI.</span></span> <span data-ttu-id="5382f-107">En el procedimiento siguiente se supone que ya ha implementado el proceso de registro como se describe en [registrar un proveedor](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="5382f-107">The following procedure assumes that you have already implemented the registration process as described in [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="5382f-108">En el procedimiento siguiente se describe cómo registrar un proveedor de métodos.</span><span class="sxs-lookup"><span data-stu-id="5382f-108">The following procedure describes how to register a method provider.</span></span>

<span data-ttu-id="5382f-109">**Para registrar un proveedor de métodos**</span><span class="sxs-lookup"><span data-stu-id="5382f-109">**To register a method provider**</span></span>

1.  <span data-ttu-id="5382f-110">Cree una instancia de la clase [**\_ \_ Win32Provider**](--win32provider.md) que describa el proveedor.</span><span class="sxs-lookup"><span data-stu-id="5382f-110">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class that describes the provider.</span></span>

    <span data-ttu-id="5382f-111">La clase del sistema [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md) hereda muchas propiedades de la clase primaria [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) , sin embargo, la única propiedad pertinente para un proveedor de métodos es la ruta de acceso del objeto a la instancia de [**\_ \_ Win32Provider**](--win32provider.md) .</span><span class="sxs-lookup"><span data-stu-id="5382f-111">The [**\_\_MethodProviderRegistration**](--methodproviderregistration.md) system class inherits many properties from the [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md) parent class, However, the only property relevant for a method provider is the object path to the [**\_\_Win32Provider**](--win32provider.md) instance.</span></span>

2.  <span data-ttu-id="5382f-112">Cree una instancia de la clase [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md) que describa el conjunto de características del proveedor.</span><span class="sxs-lookup"><span data-stu-id="5382f-112">Create an instance of the [**\_\_MethodProviderRegistration**](--methodproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="5382f-113">Asegúrese de etiquetar la clase con los calificadores de [**proveedor**](/windows/desktop/api/Provider/nl-provider-provider) y [**dinámicos**](dynamic-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="5382f-113">Be sure to tag the class with both the [**Dynamic**](dynamic-qualifier.md) and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifiers.</span></span> <span data-ttu-id="5382f-114">El calificador **dinámico** indica que WMI debe utilizar un proveedor para recuperar las instancias de clase.</span><span class="sxs-lookup"><span data-stu-id="5382f-114">The **Dynamic** qualifier signals that WMI should use a provider to retrieve the class instances.</span></span> <span data-ttu-id="5382f-115">El calificador de **proveedor** especifica el nombre del proveedor que debe usar WMI.</span><span class="sxs-lookup"><span data-stu-id="5382f-115">The **Provider** qualifier specifies the name of the provider that WMI should use.</span></span>

<span data-ttu-id="5382f-116">En el ejemplo de código siguiente se describe cómo registrar un proveedor de métodos.</span><span class="sxs-lookup"><span data-stu-id="5382f-116">The following code example describes how to register a method provider.</span></span>

``` syntax
  instance of __Win32Provider as $P
  {
    Name    = "MethProvider" ;
    ClsId   = "{E30EC6A0-23CF-11d1-8FDE-0000F804AA5C}" ;
  };    

  instance of __MethodProviderRegistration
  {
    Provider = $P;
  };
```

 

 



