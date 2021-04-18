---
description: Un proveedor de propiedades usa los métodos IWbemPropertyProvider como interfaz principal para WMI. Con IWbemPropertyProvider, puede implementar el código para recuperar y modificar las propiedades de la clase y de la instancia.
ms.assetid: d08c2ca4-9f8a-4a27-80fc-688d7c56f5eb
ms.tgt_platform: multiple
title: Implementar la interfaz principal para un proveedor de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 942117547380000e0da7d22a5e933cba4b3ffced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716556"
---
# <a name="implementing-the-primary-interface-for-a-property-provider"></a><span data-ttu-id="e20cb-104">Implementar la interfaz principal para un proveedor de propiedades</span><span class="sxs-lookup"><span data-stu-id="e20cb-104">Implementing the Primary Interface for a Property Provider</span></span>

<span data-ttu-id="e20cb-105">Un proveedor de propiedades usa los métodos [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) como interfaz principal para WMI.</span><span class="sxs-lookup"><span data-stu-id="e20cb-105">A property provider uses the [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) methods as the primary interface to WMI.</span></span> <span data-ttu-id="e20cb-106">Con **IWbemPropertyProvider**, puede implementar el código para recuperar y modificar las propiedades de la clase y de la instancia.</span><span class="sxs-lookup"><span data-stu-id="e20cb-106">With **IWbemPropertyProvider**, you can implement the code to retrieve and modify class and instance properties.</span></span>

<span data-ttu-id="e20cb-107">En la tabla siguiente se enumeran los métodos de [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) que se pueden implementar para un proveedor de propiedades.</span><span class="sxs-lookup"><span data-stu-id="e20cb-107">The following table lists the [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) methods that you can implement for a property provider.</span></span>



| <span data-ttu-id="e20cb-108">Método</span><span class="sxs-lookup"><span data-stu-id="e20cb-108">Method</span></span>                                                   | <span data-ttu-id="e20cb-109">Característica</span><span class="sxs-lookup"><span data-stu-id="e20cb-109">Feature</span></span>      |
|----------------------------------------------------------|--------------|
| [<span data-ttu-id="e20cb-110">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="e20cb-110">**GetProperty**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) | <span data-ttu-id="e20cb-111">Recuperación</span><span class="sxs-lookup"><span data-stu-id="e20cb-111">Retrieval</span></span>    |
| [<span data-ttu-id="e20cb-112">**PutProperty**</span><span class="sxs-lookup"><span data-stu-id="e20cb-112">**PutProperty**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty) | <span data-ttu-id="e20cb-113">Modificación</span><span class="sxs-lookup"><span data-stu-id="e20cb-113">Modification</span></span> |



 

> [!Note]  
> <span data-ttu-id="e20cb-114">Debe implementar un proveedor de propiedades como un proveedor en proceso.</span><span class="sxs-lookup"><span data-stu-id="e20cb-114">You must implement a property provider as an in-process provider.</span></span> <span data-ttu-id="e20cb-115">WMI inicializará los proveedores de propiedades escritos como servicios o archivos ejecutables, pero nunca llamará a sus métodos [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) y [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty) .</span><span class="sxs-lookup"><span data-stu-id="e20cb-115">WMI will initialize property providers written as services or executable files but will never call their [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) and [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty) methods.</span></span>

 

<span data-ttu-id="e20cb-116">Si decide no admitir uno de estos métodos, el proveedor puede proporcionar una implementación de código auxiliar que devuelva el **proveedor de WBEM \_ E \_ \_ no \_ compatible**.</span><span class="sxs-lookup"><span data-stu-id="e20cb-116">If you choose not to support one of these methods, your provider can supply a stub implementation that returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE**.</span></span>

<span data-ttu-id="e20cb-117">Un proveedor de propiedades identifica una clase o instancia administrada mediante un conjunto de tres calificadores: **PropertyContext**, **InstanceContext** y **ClassContext**.</span><span class="sxs-lookup"><span data-stu-id="e20cb-117">A property provider identifies a managed class or instance by a set of three qualifiers: **PropertyContext**, **InstanceContext**, and **ClassContext**.</span></span> <span data-ttu-id="e20cb-118">WMI pasará las constantes de cadena que describen estos tres calificadores al proveedor de propiedades.</span><span class="sxs-lookup"><span data-stu-id="e20cb-118">WMI will pass in string constants describing these three qualifiers to your property provider.</span></span>

<span data-ttu-id="e20cb-119">El proveedor de propiedades debe estar preparado para controlar los siguientes tipos de calificadores de contexto:</span><span class="sxs-lookup"><span data-stu-id="e20cb-119">Your property provider must be prepared to handle the following types of context qualifiers:</span></span>

-   <span data-ttu-id="e20cb-120">El calificador **InstanceContext** se adjunta a una instancia de y contiene información que se aplica a todas las propiedades de la instancia.</span><span class="sxs-lookup"><span data-stu-id="e20cb-120">The **InstanceContext** qualifier is attached to an instance and contains information that applies to every property in the instance.</span></span>
-   <span data-ttu-id="e20cb-121">El calificador **ClassContext** se adjunta a una clase y contiene información que se aplica a todas las instancias de la clase.</span><span class="sxs-lookup"><span data-stu-id="e20cb-121">The **ClassContext** qualifier is attached to a class and contains information that applies to every instance in the class.</span></span> <span data-ttu-id="e20cb-122">Por ejemplo, en una clase que se usa para almacenar los datos suministrados por el proveedor del registro, **ClassContext** puede ser la ruta de acceso a la clave del registro que contiene las propiedades que se van a informar.</span><span class="sxs-lookup"><span data-stu-id="e20cb-122">For example, in a class used to store data supplied by the Registry provider, **ClassContext** can be the path to the registry key that contains the properties to be reported.</span></span>
-   <span data-ttu-id="e20cb-123">El calificador **PropertyContext** especifica la información específica del contexto que pertenece a la propiedad.</span><span class="sxs-lookup"><span data-stu-id="e20cb-123">The **PropertyContext** qualifier specifies context-specific information that pertains to the property.</span></span> <span data-ttu-id="e20cb-124">Por ejemplo, en una clase que se usa para almacenar los datos suministrados por el proveedor del registro, **PropertyContext** especifica el nombre del valor del registro que la propiedad va a almacenar.</span><span class="sxs-lookup"><span data-stu-id="e20cb-124">For example, in a class used to store data supplied by the Registry provider, **PropertyContext** specifies the name of the registry value to be stored by the property.</span></span>

<span data-ttu-id="e20cb-125">Estos calificadores pueden funcionar juntos.</span><span class="sxs-lookup"><span data-stu-id="e20cb-125">These qualifiers can work together.</span></span> <span data-ttu-id="e20cb-126">Puede designar un valor **InstanceContext** y **PropertyContext** para indicar al proveedor cómo tratar determinados tipos de instancias.</span><span class="sxs-lookup"><span data-stu-id="e20cb-126">You can designate both an **InstanceContext** and **PropertyContext** value to tell the provider how to treat particular types of instances.</span></span> <span data-ttu-id="e20cb-127">Por ejemplo, puede marcar las instancias que el proveedor reconocerá como legibles pero con una sola propiedad que se puede escribir.</span><span class="sxs-lookup"><span data-stu-id="e20cb-127">For example, you might want to mark instances the provider will recognize as readable but having only one writeable property.</span></span>

<span data-ttu-id="e20cb-128">El calificador más común que se usa es **PropertyContext**.</span><span class="sxs-lookup"><span data-stu-id="e20cb-128">The most common qualifier used is **PropertyContext**.</span></span> <span data-ttu-id="e20cb-129">Por lo tanto, WMI proporciona el calificador **DynProps** como un acceso directo.</span><span class="sxs-lookup"><span data-stu-id="e20cb-129">Therefore, WMI provides the **DynProps** qualifier as a shortcut.</span></span> <span data-ttu-id="e20cb-130">WMI considera que cada propiedad de una instancia marcada con **DynProps** también tiene los calificadores **Dynamic**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider)y **PropertyContext** .</span><span class="sxs-lookup"><span data-stu-id="e20cb-130">WMI considers each property in an instance marked with **DynProps** to also have the **Dynamic**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider), and **PropertyContext** qualifiers.</span></span>

 

 



