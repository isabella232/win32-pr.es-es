---
description: WMI registra automáticamente el archivo DLL del proveedor de vistas durante el proceso de instalación de WMI. Sin embargo, todavía es necesario registrar el proveedor de vistas con WMI para cada espacio de nombres que contendrá clases de vista.
ms.assetid: 62db8cdc-0bbf-4784-bfc4-6fd5cb53368a
ms.tgt_platform: multiple
title: Registrar el proveedor de vistas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 530a701d3ffc39523b1b3432dd2d94a3da256605
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707274"
---
# <a name="registering-the-view-provider"></a><span data-ttu-id="49c43-104">Registrar el proveedor de vistas</span><span class="sxs-lookup"><span data-stu-id="49c43-104">Registering the View Provider</span></span>

<span data-ttu-id="49c43-105">WMI registra automáticamente el archivo DLL del proveedor de vistas durante el proceso de instalación de WMI.</span><span class="sxs-lookup"><span data-stu-id="49c43-105">WMI automatically registers the View Provider DLL during the WMI installation process.</span></span> <span data-ttu-id="49c43-106">Sin embargo, todavía es necesario registrar el proveedor de vistas con WMI para cada espacio de nombres que contendrá clases de vista.</span><span class="sxs-lookup"><span data-stu-id="49c43-106">However, you still need to register the View Provider with WMI for each namespace that will contain view classes.</span></span>

<span data-ttu-id="49c43-107">En el procedimiento siguiente se describe cómo registrar el proveedor de vistas.</span><span class="sxs-lookup"><span data-stu-id="49c43-107">The following procedure describes how to register the View Provider.</span></span>

<span data-ttu-id="49c43-108">**Para registrar el proveedor de vistas**</span><span class="sxs-lookup"><span data-stu-id="49c43-108">**To register the View Provider**</span></span>

1.  <span data-ttu-id="49c43-109">Cree una instancia de la clase [**\_ \_ Win32Provider**](--win32provider.md) para describir la implementación del proveedor de vistas.</span><span class="sxs-lookup"><span data-stu-id="49c43-109">Create an instance of the [**\_\_Win32Provider**](--win32provider.md) class to describe the implementation of the View Provider.</span></span>

    <span data-ttu-id="49c43-110">La instancia de [**\_ \_ Win32Provider**](--win32provider.md) describe el nombre del proveedor y su identificador de clase (CLSID), así como la configuración de seguridad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="49c43-110">The [**\_\_Win32Provider**](--win32provider.md) instance describes the name of the provider and its class identifier (CLSID), as well as the default security settings.</span></span>

    <span data-ttu-id="49c43-111">En el ejemplo de código siguiente se describe una implementación de [**\_ \_ Win32Provider**](--win32provider.md).</span><span class="sxs-lookup"><span data-stu-id="49c43-111">The following code example describes an implementation of [**\_\_Win32Provider**](--win32provider.md).</span></span>

    ``` syntax
    instance of __Win32Provider as $DataProv
    {
        Name = "MS_VIEW_INSTANCE_PROVIDER";
        ClsId = "{AA70DDF4-E11C-11D1-ABB0-00C04FD9159E}";
        ImpersonationLevel = 1;
        PerUserInitialization = "True";
        
    };
    ```

2.  <span data-ttu-id="49c43-112">Cree una instancia de la clase [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="49c43-112">Create an instance of the [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md) class.</span></span>

    <span data-ttu-id="49c43-113">En el ejemplo de código siguiente se muestra cómo crear una instancia de la clase **\_ \_ InstanceProviderRegistration** .</span><span class="sxs-lookup"><span data-stu-id="49c43-113">The following code example shows how to create an instance of the **\_\_InstanceProviderRegistration** class.</span></span>

    ``` syntax
    instance of __InstanceProviderRegistration
    {
        Provider = $DataProv;
        SupportsPut = True;
        SupportsGet = True;
        SupportsDelete = True;
        SupportsEnumeration = True;
        QuerySupportLevels = {"WQL:UnarySelect"};
    };
    ```

3.  <span data-ttu-id="49c43-114">Cree una instancia de la clase [**\_ \_ MethodProviderRegistration**](--methodproviderregistration.md) si desea tener los métodos de compatibilidad de la clase de vista Union.</span><span class="sxs-lookup"><span data-stu-id="49c43-114">Create an instance of the [**\_\_MethodProviderRegistration**](--methodproviderregistration.md) class if you want to have your union view class support methods.</span></span>

    <span data-ttu-id="49c43-115">En el ejemplo de código siguiente se muestra cómo crear una instancia de la clase **\_ \_ MethodProviderRegistration** .</span><span class="sxs-lookup"><span data-stu-id="49c43-115">The following code example shows how to create an instance of the **\_\_MethodProviderRegistration** class.</span></span>

    ``` syntax
    instance of __MethodProviderRegistration
    {
        Provider = $DataProv;
    };
    ```

4.  <span data-ttu-id="49c43-116">Compile el código MOF mediante el compilador MOF ([MOFCOMP](mofcomp.md)) o la interfaz [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .</span><span class="sxs-lookup"><span data-stu-id="49c43-116">Compile your MOF code using the MOF compiler ([mofcomp](mofcomp.md)) or the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface.</span></span>

    <span data-ttu-id="49c43-117">Si guarda el ejemplo de código MOF enumerado anteriormente en un archivo denominado Viewtest. mof, use el comando MOFCOMP para cargar el código MOF en el espacio de nombres de destino.</span><span class="sxs-lookup"><span data-stu-id="49c43-117">If you save the previously listed MOF code example into a file named Viewtest.mof, use the Mofcomp command to load the MOF code into the target namespace.</span></span> <span data-ttu-id="49c43-118">*NamespacePath* es el espacio de nombres en el que desea crear la instancia de la clase de vista.</span><span class="sxs-lookup"><span data-stu-id="49c43-118">*NamespacePath* is the namespace in which you wish to create the view class instance.</span></span>

    <span data-ttu-id="49c43-119">Escriba el siguiente comando en un símbolo del sistema para cargar el código MOF en el espacio de nombres de destino.</span><span class="sxs-lookup"><span data-stu-id="49c43-119">Type the following command at a command prompt to load the MOF code into the target namespace.</span></span>

    ``` syntax
    Mofcomp /N:<NamespacePath> Viewtest.mof
    ```

    <span data-ttu-id="49c43-120">Para obtener más información, vea [compilar archivos MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="49c43-120">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="49c43-121">Para obtener más información, vea [registrar un proveedor](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="49c43-121">For more information, see [Registering a Provider](registering-a-provider.md).</span></span>

 

 



