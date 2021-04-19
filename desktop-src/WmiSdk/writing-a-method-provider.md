---
description: Un proveedor de métodos permite el acceso de WMI a los métodos de una clase. Por ejemplo, una clase que representa una aplicación puede tener un método que finaliza la aplicación.
ms.assetid: bce87e65-5cba-4eef-91da-a3e13c80b8a6
ms.tgt_platform: multiple
title: Escribir un proveedor de métodos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8626e2e16fe5424a0b05df81e2444a72ecb8841f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715816"
---
# <a name="writing-a-method-provider"></a><span data-ttu-id="1a16a-104">Escribir un proveedor de métodos</span><span class="sxs-lookup"><span data-stu-id="1a16a-104">Writing a Method Provider</span></span>

<span data-ttu-id="1a16a-105">Un proveedor de métodos permite el acceso de WMI a los métodos de una clase.</span><span class="sxs-lookup"><span data-stu-id="1a16a-105">A method provider allows WMI access to the methods of a class.</span></span> <span data-ttu-id="1a16a-106">Por ejemplo, una clase que representa una aplicación puede tener un método que finaliza la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1a16a-106">For example, a class that represents an application may have a method that terminates the application.</span></span>

<span data-ttu-id="1a16a-107">Si se cambia el orden de los parámetros de entrada y salida del método al actualizar un proveedor de métodos existente, puede producirse un error en las aplicaciones que llaman al método.</span><span class="sxs-lookup"><span data-stu-id="1a16a-107">Changing the order of method input and output parameters when updating an existing method provider can cause failure for applications that call the method.</span></span> <span data-ttu-id="1a16a-108">El orden de los parámetros de entrada o salida lo establece el valor del calificador de [**ID**](standard-wmi-qualifiers.md) . en cada parámetro.</span><span class="sxs-lookup"><span data-stu-id="1a16a-108">The order of the input or output parameters is established by the value of the [**ID**](standard-wmi-qualifiers.md) qualifier on each parameter.</span></span> <span data-ttu-id="1a16a-109">El primer parámetro tiene un valor de **identificador** de cero.</span><span class="sxs-lookup"><span data-stu-id="1a16a-109">The first parameter has an **ID** value of zero.</span></span> <span data-ttu-id="1a16a-110">Agregue nuevos parámetros de entrada al final de los parámetros existentes en lugar de insertarlos en la secuencia ya establecida.</span><span class="sxs-lookup"><span data-stu-id="1a16a-110">Add new input parameters at the end of the existing parameters rather than inserting them in the already established sequence.</span></span>

<span data-ttu-id="1a16a-111">En el procedimiento siguiente se describe cómo implementar un proveedor de métodos.</span><span class="sxs-lookup"><span data-stu-id="1a16a-111">The following procedure describes how to implement a method provider.</span></span>

<span data-ttu-id="1a16a-112">**Para implementar un proveedor de métodos**</span><span class="sxs-lookup"><span data-stu-id="1a16a-112">**To implement a method provider**</span></span>

1.  <span data-ttu-id="1a16a-113">Diseñe y registre el proveedor de clases con WMI.</span><span class="sxs-lookup"><span data-stu-id="1a16a-113">Design and register your class provider with WMI.</span></span>

    <span data-ttu-id="1a16a-114">Los proveedores de clases se registran en WMI mediante la creación de una instancia de [**\_ \_ Win32Provider**](--win32provider.md) y una clase [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="1a16a-114">Class providers register with WMI by creating a [**\_\_Win32Provider**](--win32provider.md) instance and a [**\_\_MethodProviderRegistration**](--methodproviderregistration.md) class.</span></span> <span data-ttu-id="1a16a-115">Para obtener más información, vea [registrar un proveedor de métodos](registering-a-method-provider.md).</span><span class="sxs-lookup"><span data-stu-id="1a16a-115">For more information, see [Registering a Method Provider](registering-a-method-provider.md).</span></span>

2.  <span data-ttu-id="1a16a-116">Implemente la interfaz [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="1a16a-116">Implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface for your provider.</span></span>

    > [!Note]  
    > <span data-ttu-id="1a16a-117">Se recomienda encarecidamente a los proveedores de métodos que utilicen el modelo de multithreading "both".</span><span class="sxs-lookup"><span data-stu-id="1a16a-117">Method providers are strongly encouraged to use the multithreading model "Both".</span></span>

     

3.  <span data-ttu-id="1a16a-118">Implemente el método [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="1a16a-118">Implement the [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) method for your provider.</span></span>

    <span data-ttu-id="1a16a-119">La interfaz [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) es la interfaz principal para un proveedor de métodos.</span><span class="sxs-lookup"><span data-stu-id="1a16a-119">The [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface is the primary interface for a method provider.</span></span> <span data-ttu-id="1a16a-120">Para obtener más información, vea [implementar la interfaz principal para un proveedor de métodos](implementing-the-primary-interface-for-a-method-provider.md).</span><span class="sxs-lookup"><span data-stu-id="1a16a-120">For more information, see [Implementing the Primary Interface for a Method Provider](implementing-the-primary-interface-for-a-method-provider.md).</span></span>

4.  <span data-ttu-id="1a16a-121">Agregue el código adicional necesario para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="1a16a-121">Add any additional code necessary for your provider.</span></span>

    <span data-ttu-id="1a16a-122">Al diseñar el proveedor, lo más probable es que necesite llamar a interfaces de WMI.</span><span class="sxs-lookup"><span data-stu-id="1a16a-122">When designing your provider, you will most likely need to call WMI interfaces.</span></span> <span data-ttu-id="1a16a-123">Para obtener más información, consulte [llamar a un método](calling-a-method.md) y [mantener los niveles de seguridad en un proveedor](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="1a16a-123">For more information, see [Calling a Method](calling-a-method.md) and [Maintaining Security Levels in a Provider](impersonating-a-client.md).</span></span>

    <span data-ttu-id="1a16a-124">Al recuperar información de un cliente, es posible que necesite tener acceso a los niveles de seguridad de ese cliente.</span><span class="sxs-lookup"><span data-stu-id="1a16a-124">When retrieving information for a client, you may need to access the security levels for that client.</span></span> <span data-ttu-id="1a16a-125">Para obtener más información, vea [Suplantar a un cliente](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="1a16a-125">For more information, see [Impersonating a Client](impersonating-a-client.md).</span></span>

5.  <span data-ttu-id="1a16a-126">Reemplace el proveedor preexistente con el código nuevo.</span><span class="sxs-lookup"><span data-stu-id="1a16a-126">Replace the preexisting provider with your new code.</span></span>

    <span data-ttu-id="1a16a-127">No es necesario que realice este paso si no tiene un proveedor preexistente en el que realizar la copia.</span><span class="sxs-lookup"><span data-stu-id="1a16a-127">You do not need to perform this step if you do not have a preexisting provider to copy over.</span></span> <span data-ttu-id="1a16a-128">Para obtener más información, consulte [actualización de un proveedor](updating-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="1a16a-128">For more information, see [Updating a Provider](updating-a-provider.md).</span></span>

 

 



