---
description: Un proveedor de propiedades recupera y modifica los valores de propiedad individuales para las instancias de una clase determinada que se almacena en el repositorio WMI.
ms.assetid: fe150157-cf9d-47da-8f94-b18eb0502bd8
ms.tgt_platform: multiple
title: Escribir un proveedor de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06bf22d927435b5c46f0ec8d8d2cf42ab872a0c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716187"
---
# <a name="writing-a-property-provider"></a><span data-ttu-id="644e4-103">Escribir un proveedor de propiedades</span><span class="sxs-lookup"><span data-stu-id="644e4-103">Writing a Property Provider</span></span>

<span data-ttu-id="644e4-104">Un proveedor de propiedades recupera y modifica los valores de propiedad individuales para las instancias de una clase determinada que se almacena en el repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="644e4-104">A property provider retrieves and modifies individual property values for instances of a given class that is stored in the WMI repository.</span></span>

<span data-ttu-id="644e4-105">En el procedimiento siguiente se describe cómo crear un proveedor de propiedades.</span><span class="sxs-lookup"><span data-stu-id="644e4-105">The following procedure describes how to create a property provider.</span></span>

<span data-ttu-id="644e4-106">**Para crear un proveedor de propiedades**</span><span class="sxs-lookup"><span data-stu-id="644e4-106">**To create a property provider**</span></span>

1.  <span data-ttu-id="644e4-107">Diseñe y registre el proveedor con WMI.</span><span class="sxs-lookup"><span data-stu-id="644e4-107">Design and register your provider with WMI.</span></span>

    <span data-ttu-id="644e4-108">Los proveedores de instancias se registran en WMI mediante la creación de una instancia de [**\_ \_ Win32Provider**](--win32provider.md) y una clase [**\_ \_ PropertyProviderRegistration**](--propertyproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="644e4-108">Instance providers register with WMI by creating a [**\_\_Win32Provider**](--win32provider.md) instance and a [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md) class.</span></span> <span data-ttu-id="644e4-109">Para obtener más información, vea [registrar un proveedor de propiedades](registering-a-property-provider.md).</span><span class="sxs-lookup"><span data-stu-id="644e4-109">For more information, see [Registering a Property Provider](registering-a-property-provider.md).</span></span>

2.  <span data-ttu-id="644e4-110">Implemente la interfaz [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="644e4-110">Implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface for your provider.</span></span>

    <span data-ttu-id="644e4-111">WMI usa [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para cargar e inicializar un proveedor.</span><span class="sxs-lookup"><span data-stu-id="644e4-111">WMI uses [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) to load and initialize a provider.</span></span> <span data-ttu-id="644e4-112">Se trata de una tarea común a todos los proveedores.</span><span class="sxs-lookup"><span data-stu-id="644e4-112">This is a task common to all providers.</span></span> <span data-ttu-id="644e4-113">Para obtener más información, vea [inicializar un proveedor](initializing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="644e4-113">For more information, see [Initializing a Provider](initializing-a-provider.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="644e4-114">Se recomienda encarecidamente a los proveedores de propiedades que utilicen el modelo de multithreading "both".</span><span class="sxs-lookup"><span data-stu-id="644e4-114">Property providers are strongly encouraged to use the multithreading model "Both".</span></span>

     

3.  <span data-ttu-id="644e4-115">Implemente la interfaz [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="644e4-115">Implement the [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) interface for your provider.</span></span>

    <span data-ttu-id="644e4-116">La interfaz [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) es la interfaz principal para un proveedor de propiedades.</span><span class="sxs-lookup"><span data-stu-id="644e4-116">The [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) interface is the primary interface for a property provider.</span></span> <span data-ttu-id="644e4-117">Los dos métodos principales son [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) y [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty).</span><span class="sxs-lookup"><span data-stu-id="644e4-117">The two main methods are [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) and [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty).</span></span> <span data-ttu-id="644e4-118">Para obtener más información, vea [implementar la interfaz principal para un proveedor de propiedades](implementing-the-primary-interface-for-a-property-provider.md).</span><span class="sxs-lookup"><span data-stu-id="644e4-118">For more information, see [Implementing the Primary Interface for a Property Provider](implementing-the-primary-interface-for-a-property-provider.md).</span></span>

4.  <span data-ttu-id="644e4-119">Agregue el código adicional necesario para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="644e4-119">Add any additional code necessary for your provider.</span></span>

    <span data-ttu-id="644e4-120">Al diseñar el proveedor, lo más probable es que necesite llamar a interfaces de WMI.</span><span class="sxs-lookup"><span data-stu-id="644e4-120">When designing your provider, you will most likely need to call WMI interfaces.</span></span> <span data-ttu-id="644e4-121">Para obtener más información, consulte [llamar a un método](calling-a-method.md) y [mantener los niveles de seguridad en un proveedor](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="644e4-121">For more information, see [Calling a Method](calling-a-method.md) and [Maintaining Security Levels in a Provider](impersonating-a-client.md).</span></span>

    <span data-ttu-id="644e4-122">Al recuperar información de un cliente, es posible que necesite tener acceso a los niveles de seguridad de ese cliente.</span><span class="sxs-lookup"><span data-stu-id="644e4-122">When retrieving information for a client, you may need to access the security levels for that client.</span></span> <span data-ttu-id="644e4-123">Para obtener más información, vea [Suplantar a un cliente](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="644e4-123">For more information, see [Impersonating a Client](impersonating-a-client.md).</span></span>

5.  <span data-ttu-id="644e4-124">Reemplace el proveedor preexistente con el código nuevo.</span><span class="sxs-lookup"><span data-stu-id="644e4-124">Replace the preexisting provider with your new code.</span></span>

    <span data-ttu-id="644e4-125">No es necesario que realice este paso si no tiene un proveedor preexistente en el que realizar la copia.</span><span class="sxs-lookup"><span data-stu-id="644e4-125">You do not need to perform this step if you do not have a preexisting provider to copy over.</span></span> <span data-ttu-id="644e4-126">Para obtener más información, consulte [actualización de un proveedor](updating-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="644e4-126">For more information, see [Updating a Provider](updating-a-provider.md).</span></span>

 

 



