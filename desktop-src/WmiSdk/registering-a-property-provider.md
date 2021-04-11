---
description: Para crear un proveedor de propiedades WMI, debe registrar la \_ \_ instancia de Win32Provider que representa el proveedor mediante una instancia de \_ \_ PropertyProviderRegistration.
ms.assetid: e7e30acc-ea41-41e2-9bb3-cd931e8d799e
ms.tgt_platform: multiple
title: Registrar un proveedor de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d56d91e3c2a45b0ad0fe83cf6b2bc32ab4353a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276147"
---
# <a name="registering-a-property-provider"></a><span data-ttu-id="03ac9-103">Registrar un proveedor de propiedades</span><span class="sxs-lookup"><span data-stu-id="03ac9-103">Registering a Property Provider</span></span>

<span data-ttu-id="03ac9-104">Para crear un [*proveedor de propiedades*](gloss-p.md) WMI, debe registrar la instancia de [**\_ \_ Win32Provider**](--win32provider.md) que representa el proveedor mediante una instancia de [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="03ac9-104">To create a WMI [*property provider*](gloss-p.md) you must register the [**\_\_Win32Provider**](--win32provider.md) instance that represents your provider using an instance of [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md).</span></span> <span data-ttu-id="03ac9-105">Como objeto COM, el proveedor debe registrarse en el sistema operativo y en WMI.</span><span class="sxs-lookup"><span data-stu-id="03ac9-105">As a COM object, your provider must register with the operating system and WMI.</span></span> <span data-ttu-id="03ac9-106">En el procedimiento siguiente se supone que ya ha implementado el proceso de registro como se describe en [registrar un proveedor](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="03ac9-106">The following procedure assumes that you have already implemented the registration process as described in [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="03ac9-107">En el procedimiento siguiente se describe cómo registrar un proveedor de propiedades.</span><span class="sxs-lookup"><span data-stu-id="03ac9-107">The following procedure describes how to register a property provider.</span></span>

<span data-ttu-id="03ac9-108">**Para registrar un proveedor de propiedades**</span><span class="sxs-lookup"><span data-stu-id="03ac9-108">**To register a property provider**</span></span>

1.  <span data-ttu-id="03ac9-109">Cree una instancia de la clase [**\_ \_ Win32Provider**](--win32provider.md) que describa el proveedor de propiedades.</span><span class="sxs-lookup"><span data-stu-id="03ac9-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class that describes the property provider.</span></span>

    <span data-ttu-id="03ac9-110">La clase [**\_ \_ Win32Provider**](--win32provider.md) acepta los valores predeterminados para otras propiedades, como el valor **true** para la propiedad **Pure** .</span><span class="sxs-lookup"><span data-stu-id="03ac9-110">The [**\_\_Win32Provider**](--win32provider.md) class accepts the default values for other properties, such as the **TRUE** value for the **Pure** property.</span></span> <span data-ttu-id="03ac9-111">Para obtener más información, vea [**\_ \_ Win32Provider**](--win32provider.md).</span><span class="sxs-lookup"><span data-stu-id="03ac9-111">For more information, see [**\_\_Win32Provider**](--win32provider.md).</span></span>

2.  <span data-ttu-id="03ac9-112">Cree una instancia de la clase [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md) que describa el conjunto de características del proveedor.</span><span class="sxs-lookup"><span data-stu-id="03ac9-112">Create an instance of the [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md) class that describes the feature set of the provider.</span></span>

    <span data-ttu-id="03ac9-113">La clase [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md) hereda muchas propiedades de la clase primaria [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) , que proporciona valores booleanos que indican la compatibilidad con características concretas y una matriz de cadenas para indicar la compatibilidad con consultas.</span><span class="sxs-lookup"><span data-stu-id="03ac9-113">The [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md) class inherits many properties from the [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md) parent class, which provides Boolean values that indicate support for particular features and an array of strings to indicate query support.</span></span>

    <span data-ttu-id="03ac9-114">Asegúrese de etiquetar la clase con los calificadores de [**proveedor**](/windows/desktop/api/Provider/nl-provider-provider) y [**dinámicos**](dynamic-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="03ac9-114">Be sure to tag the class with both the [**Dynamic**](dynamic-qualifier.md) and [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifiers.</span></span> <span data-ttu-id="03ac9-115">El calificador **dinámico** indica que WMI debe utilizar un proveedor dinámico para recuperar las instancias de clase que contienen las propiedades admitidas.</span><span class="sxs-lookup"><span data-stu-id="03ac9-115">The **Dynamic** qualifier signals that WMI should use a dynamic provider to retrieve the class instances that contain the supported properties.</span></span> <span data-ttu-id="03ac9-116">El calificador de **proveedor** especifica el nombre del proveedor que debe usar WMI.</span><span class="sxs-lookup"><span data-stu-id="03ac9-116">The **Provider** qualifier specifies the name of the provider that WMI should use.</span></span>

<span data-ttu-id="03ac9-117">WMI llama a NewQuery en un proveedor de eventos cuando un consumidor de cliente registra una consulta de filtro de eventos que contiene referencias a eventos admitidos por ese proveedor de eventos.</span><span class="sxs-lookup"><span data-stu-id="03ac9-117">WMI calls NewQuery on an event provider when a client consumer registers an event filter query that contains references to events supported by that event provider.</span></span> <span data-ttu-id="03ac9-118">Por lo tanto, el proveedor de eventos responsable de los eventos de modificación de instancias de la clase EmailClass puede configurarse para generar notificaciones solo para el remitente.</span><span class="sxs-lookup"><span data-stu-id="03ac9-118">So the event provider responsible for instance modification events for the EmailClass class can be set up to generate notifications only for sender.</span></span> <span data-ttu-id="03ac9-119">Cuando el proveedor recibe una consulta que solicita la notificación de los cambios en la propiedad de asunto, el proveedor puede empezar a generar esas notificaciones.</span><span class="sxs-lookup"><span data-stu-id="03ac9-119">When the provider receives a query requesting notification of changes to the subject property, the provider can start generating those notifications.</span></span> <span data-ttu-id="03ac9-120">En este escenario, no se requiere WMI para descartar las notificaciones que solo notifican los cambios de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="03ac9-120">In this scenario, WMI is not required to discard the notifications that report recipient changes only.</span></span>

<span data-ttu-id="03ac9-121">En el siguiente ejemplo de código MOF se describen las instancias de que se pueden utilizar para registrar un proveedor de propiedades.</span><span class="sxs-lookup"><span data-stu-id="03ac9-121">The following MOF code example describes instances that can be used to register a property provider.</span></span>

``` syntax
  instance of __Win32Provider as $P
  {
    Name    = "PropProvider" ;
    ClsId   = "{E30EC6A0-23CF-11d1-8FDE-0000F804AA5C}" ;
  };    

  instance of __PropertyProviderRegistration
  {
    Provider = $P;
    SupportsGet = TRUE;
    SupportsPut = FALSE;
  };
```

> [!Note]  
> <span data-ttu-id="03ac9-122">Solo los administradores pueden registrar o eliminar un proveedor de propiedades mediante la creación de una instancia de [**\_ \_ Win32Provider**](--win32provider.md) y [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="03ac9-122">Only administrators can register or delete a property provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md).</span></span>

 

 

 



