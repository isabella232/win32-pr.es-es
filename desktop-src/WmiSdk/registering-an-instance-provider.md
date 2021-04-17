---
description: Para crear un proveedor de instancias WMI, debe registrar la \_ \_ instancia de Win32Provider que representa el proveedor mediante una instancia de \_ \_ InstanceProviderRegistration.
ms.assetid: 5ac8e964-606f-4010-84a8-7c0ae6ca2133
ms.tgt_platform: multiple
title: Registrar un proveedor de instancias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bde8189559b04f2e45ac8357ab47cc17bd253fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544694"
---
# <a name="registering-an-instance-provider"></a><span data-ttu-id="b79c7-103">Registrar un proveedor de instancias</span><span class="sxs-lookup"><span data-stu-id="b79c7-103">Registering an Instance Provider</span></span>

<span data-ttu-id="b79c7-104">Para crear un [*proveedor de instancias*](gloss-i.md) WMI, debe registrar la instancia de [**\_ \_ Win32Provider**](--win32provider.md) que representa el proveedor mediante una instancia de [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="b79c7-104">To create a WMI [*instance provider*](gloss-i.md) you must register the [**\_\_Win32Provider**](--win32provider.md) instance that represents your provider using an instance of [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md).</span></span> <span data-ttu-id="b79c7-105">Como objeto COM, el proveedor debe registrarse en el sistema operativo y en WMI.</span><span class="sxs-lookup"><span data-stu-id="b79c7-105">As a COM object, your provider must register with the operating system and WMI.</span></span> <span data-ttu-id="b79c7-106">En el procedimiento siguiente se supone que ya ha implementado el proceso de registro como se describe en [registrar un proveedor](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b79c7-106">The following procedure assumes that you have already implemented the registration process as described in [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="b79c7-107">En el procedimiento siguiente se describe cómo registrar un proveedor de instancias.</span><span class="sxs-lookup"><span data-stu-id="b79c7-107">The following procedure describes how to register an instance provider.</span></span>

<span data-ttu-id="b79c7-108">**Para registrar un proveedor de instancias**</span><span class="sxs-lookup"><span data-stu-id="b79c7-108">**To register an instance provider**</span></span>

1.  <span data-ttu-id="b79c7-109">Cree una instancia de la clase [**\_ \_ Win32Provider**](--win32provider.md) que describa el proveedor.</span><span class="sxs-lookup"><span data-stu-id="b79c7-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class that describes the provider.</span></span>
2.  <span data-ttu-id="b79c7-110">Cree una instancia de la clase [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) que describa el conjunto de características del proveedor.</span><span class="sxs-lookup"><span data-stu-id="b79c7-110">Create an instance of the [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="b79c7-111">La clase [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) hereda muchas propiedades de la clase primaria [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) , que proporciona valores booleanos que indican la compatibilidad con características concretas y una matriz de cadenas para indicar la compatibilidad con consultas.</span><span class="sxs-lookup"><span data-stu-id="b79c7-111">The [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) class inherits many properties from the [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md) parent class, which provides Boolean values that indicate support for particular features and an array of strings to indicate query support.</span></span>

    <span data-ttu-id="b79c7-112">Asegúrese de etiquetar la clase con los calificadores de [**proveedor**](/windows/desktop/api/Provider/nl-provider-provider) y [**dinámicos**](standard-wmi-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="b79c7-112">Be sure to tag the class with both the [**Dynamic**](standard-wmi-qualifiers.md) and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifiers.</span></span> <span data-ttu-id="b79c7-113">El calificador indica que WMI debe utilizar un proveedor **dinámico** para recuperar las instancias de clase.</span><span class="sxs-lookup"><span data-stu-id="b79c7-113">The qualifier signals that WMI should use a **Dynamic** provider to retrieve the class instances.</span></span> <span data-ttu-id="b79c7-114">El calificador de **proveedor** especifica el nombre del proveedor que debe usar WMI.</span><span class="sxs-lookup"><span data-stu-id="b79c7-114">The **Provider** qualifier specifies the name of the provider that WMI should use.</span></span>

<span data-ttu-id="b79c7-115">En el ejemplo de código siguiente se describe cómo registrar una instancia de [**\_ \_ Win32Provider**](--win32provider.md) y [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="b79c7-115">The following code example describes how to register a [**\_\_Win32Provider**](--win32provider.md) and [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) instance.</span></span>

``` syntax
instance of __Win32Provider as $P
{
    Name="TestProv";
    CLSID="{A41602A4-C038-11d1-AEB6-00C04FB68820}";
};

instance of __InstanceProviderRegistration
{
    Provider = $P;
    SupportsGet = TRUE;
    SupportsEnumeration = TRUE;
    QuerySupportLevels = { "WQL:UnarySelect" };
};
```

 

 



