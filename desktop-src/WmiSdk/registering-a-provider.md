---
description: Antes de implementar el proveedor, primero debe registrar el proveedor con WMI. Al registrar el proveedor se define el tipo del proveedor y las clases que admite el proveedor. WMI solo puede tener acceso a proveedores registrados.
ms.assetid: b0a1a11c-a8e8-4bc1-b286-fb9243667976
ms.tgt_platform: multiple
title: Registrar un proveedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53592ecb452de1b6071cbb8f59cfaaef42b57f1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706654"
---
# <a name="registering-a-provider"></a><span data-ttu-id="7cd10-105">Registrar un proveedor</span><span class="sxs-lookup"><span data-stu-id="7cd10-105">Registering a Provider</span></span>

<span data-ttu-id="7cd10-106">Antes de implementar el proveedor, primero debe registrar el proveedor con WMI.</span><span class="sxs-lookup"><span data-stu-id="7cd10-106">Before implementing your provider, you should first register your provider with WMI.</span></span> <span data-ttu-id="7cd10-107">Al registrar el proveedor se define el tipo del proveedor y las clases que admite el proveedor.</span><span class="sxs-lookup"><span data-stu-id="7cd10-107">Registering the provider defines the type of the provider and the classes that the provider supports.</span></span> <span data-ttu-id="7cd10-108">WMI solo puede tener acceso a proveedores registrados.</span><span class="sxs-lookup"><span data-stu-id="7cd10-108">WMI can only access registered providers.</span></span>

> [!Note]  
> <span data-ttu-id="7cd10-109">Para obtener más información sobre cómo registrar un proveedor de MI, consulte [Cómo: registrar un proveedor de mi](/previous-versions/windows/desktop/wmi_v2/how-to-register-an-mi-provider).</span><span class="sxs-lookup"><span data-stu-id="7cd10-109">For more information on registering an MI provider, see [How to: Register an MI Provider](/previous-versions/windows/desktop/wmi_v2/how-to-register-an-mi-provider).</span></span>

 

<span data-ttu-id="7cd10-110">Puede escribir el código del proveedor antes de registrar el proveedor.</span><span class="sxs-lookup"><span data-stu-id="7cd10-110">You can write your provider code before you register the provider.</span></span> <span data-ttu-id="7cd10-111">Sin embargo, es muy difícil depurar un proveedor que no está registrado con WMI.</span><span class="sxs-lookup"><span data-stu-id="7cd10-111">However, it is very difficult to debug a provider that is not registered with WMI.</span></span> <span data-ttu-id="7cd10-112">La determinación de las interfaces del proveedor también ayuda a describir el propósito y la estructura de un proveedor.</span><span class="sxs-lookup"><span data-stu-id="7cd10-112">Determining the interfaces for your provider also helps to outline the purpose and structure of a provider.</span></span> <span data-ttu-id="7cd10-113">Por lo tanto, el registro del proveedor le ayudará a diseñar el proveedor.</span><span class="sxs-lookup"><span data-stu-id="7cd10-113">Therefore, registering your provider helps you design your provider.</span></span>

<span data-ttu-id="7cd10-114">Solo los administradores pueden registrar o eliminar un proveedor.</span><span class="sxs-lookup"><span data-stu-id="7cd10-114">Only administrators can register or delete a provider.</span></span>

<span data-ttu-id="7cd10-115">Un proveedor debe estar registrado para todos los distintos tipos de funciones de proveedor que realiza.</span><span class="sxs-lookup"><span data-stu-id="7cd10-115">A provider must be registered for all the different types of provider functions that it performs.</span></span> <span data-ttu-id="7cd10-116">Casi todos los proveedores proporcionan instancias de las clases que definen, pero también pueden proporcionar datos de propiedades, métodos, eventos o clases.</span><span class="sxs-lookup"><span data-stu-id="7cd10-116">Nearly all providers supply instances of classes they define, but they may also provide property data, methods, events, or classes.</span></span> <span data-ttu-id="7cd10-117">El proveedor también puede registrarse como proveedor de consumidor de eventos o como proveedor de contadores de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="7cd10-117">The provider may also be registered as an event consumer provider or a performance counter provider.</span></span> <span data-ttu-id="7cd10-118">Se recomienda combinar toda la funcionalidad del proveedor en un proveedor, en lugar de tener muchos proveedores independientes para cada tipo.</span><span class="sxs-lookup"><span data-stu-id="7cd10-118">It is recommended that you combine all provider functionality in one provider rather than having many separate providers for each type.</span></span> <span data-ttu-id="7cd10-119">Un ejemplo es el [proveedor del registro del sistema](/previous-versions/windows/desktop/regprov/system-registry-provider), que proporciona métodos e instancias, y el [proveedor de cuota de disco](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider), que proporciona instancias, métodos y eventos.</span><span class="sxs-lookup"><span data-stu-id="7cd10-119">An example is the [System Registry provider](/previous-versions/windows/desktop/regprov/system-registry-provider), which provides methods and instances, and the [Disk Quota provider](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider), which supplies instances, methods, and events.</span></span>

<span data-ttu-id="7cd10-120">Un proveedor debe estar registrado para todos los distintos tipos de funciones de proveedor que realiza.</span><span class="sxs-lookup"><span data-stu-id="7cd10-120">A provider must be registered for all the different types of provider functions that it performs.</span></span> <span data-ttu-id="7cd10-121">Casi todos los proveedores proporcionan instancias de las clases que definen, pero también pueden proporcionar datos de propiedades, métodos, eventos o clases.</span><span class="sxs-lookup"><span data-stu-id="7cd10-121">Nearly all providers supply instances of classes they define, but they may also provide property data, methods, events, or classes.</span></span> <span data-ttu-id="7cd10-122">El proveedor también puede registrarse como proveedor de consumidor de eventos o como proveedor de contadores de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="7cd10-122">The provider may also be registered as an event consumer provider or a performance counter provider.</span></span>

<span data-ttu-id="7cd10-123">Se usa la misma instancia de [**\_ \_ Win32Provider**](--win32provider.md) para cada tipo de registro:</span><span class="sxs-lookup"><span data-stu-id="7cd10-123">The same instance of [**\_\_Win32Provider**](--win32provider.md) is used for each type of registration:</span></span>

-   [<span data-ttu-id="7cd10-124">Registrar un proveedor de instancias</span><span class="sxs-lookup"><span data-stu-id="7cd10-124">Registering an Instance Provider</span></span>](registering-an-instance-provider.md)
-   [<span data-ttu-id="7cd10-125">Registrar un proveedor de clases</span><span class="sxs-lookup"><span data-stu-id="7cd10-125">Registering a Class Provider</span></span>](registering-a-class-provider.md)
-   [<span data-ttu-id="7cd10-126">Registrar un proveedor de métodos</span><span class="sxs-lookup"><span data-stu-id="7cd10-126">Registering a Method Provider</span></span>](registering-a-method-provider.md)
-   [<span data-ttu-id="7cd10-127">Registrar un proveedor de eventos</span><span class="sxs-lookup"><span data-stu-id="7cd10-127">Registering an Event Provider</span></span>](registering-an-event-provider.md)
-   [<span data-ttu-id="7cd10-128">Registrar un proveedor de consumidor de eventos</span><span class="sxs-lookup"><span data-stu-id="7cd10-128">Registering an Event Consumer Provider</span></span>](registering-an-event-consumer-provider.md)
-   [<span data-ttu-id="7cd10-129">Crear un proveedor de instancias en un proveedor de High-Performance</span><span class="sxs-lookup"><span data-stu-id="7cd10-129">Making an Instance Provider into a High-Performance Provider</span></span>](making-an-instance-provider-into-a-high-performance-provider.md)

## <a name="example-creating-and-registering-an-instance-of-a-provider"></a><span data-ttu-id="7cd10-130">Ejemplo: crear y registrar una instancia de un proveedor</span><span class="sxs-lookup"><span data-stu-id="7cd10-130">Example: Creating and Registering an Instance of a Provider</span></span>

<span data-ttu-id="7cd10-131">En el ejemplo siguiente se muestra un archivo MOF que crea y registra una instancia del [proveedor del registro del sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) en el \\ espacio de nombres root cimv2.</span><span class="sxs-lookup"><span data-stu-id="7cd10-131">The following example shows a MOF file that creates and registers an instance of the [System Registry provider](/previous-versions/windows/desktop/regprov/system-registry-provider) in the root\\cimv2 namespace.</span></span> <span data-ttu-id="7cd10-132">Asigna el alias $Reg al proveedor para evitar la ruta de la longitud necesaria en los registros de instancias y métodos.</span><span class="sxs-lookup"><span data-stu-id="7cd10-132">It assigns the alias $Reg to the provider to avoid the long pathname required in the instance and method registrations.</span></span> <span data-ttu-id="7cd10-133">Para obtener más información, vea [crear un alias](creating-an-alias.md).</span><span class="sxs-lookup"><span data-stu-id="7cd10-133">For more information, see [Creating an Alias](creating-an-alias.md).</span></span>

``` syntax
// Place the Registry provider in the root\cimv2 namespace
#pragma namespace("\\\\.\\ROOT\\cimv2")

// Create an instance of __Win32Provider
instance of __Win32Provider as $Reg
{
Name = "RegProv";        
CLSID = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}";
HostingModel = "NetworkServiceHost:LocalServiceHost";
};

// Register as an instance provider by
// creating an instance
// of __InstanceProviderRegistration
instance of __InstanceProviderRegistration
{
 provider = $Reg;
 SupportsDelete = FALSE;
 SupportsEnumeration = TRUE;
 SupportsGet = TRUE;
 SupportsPut = TRUE;
};

// Register as a method provider by
// creating an instance
// of __MethodProviderRegistration
instance of __MethodProviderRegistration
{
 provider = $Reg;
};

// Define the StdRegProv class
[dynamic: ToInstance, provider("RegProv")]
class StdRegProv
{
[implemented, static] uint32 CreateKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName);
[implemented, static] uint32 DeleteKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName);
[implemented, static] uint32 EnumKey(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [OUT] string sNames[]);
[implemented, static] uint32 EnumValues(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [OUT] string sNames[], 
 [OUT] sint32 Types[]);
[implemented, static] uint32 DeleteValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName);
 [implemented, static] uint32 SetDWORDValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] uint32 uValue = 3);
[implemented, static] uint32 GetDWORDValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] uint32 uValue);
[implemented, static] uint32 SetStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue = "hello");
[implemented, static] uint32 GetStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [in] string sValueName, 
 [OUT] string sValue);
[implemented, static] uint32 SetMultiStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue[] = {"hello", "there"});
[implemented, static] uint32 GetMultiStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] string sValue[]);
[implemented, static] uint32 SetExpandedStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [IN] string sValue = "%path%");
[implemented, static] uint32 GetExpandedStringValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] string sValue);
[implemented, static] uint32 SetBinaryValue(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [in] string sValueName, 
 [in] uint8 uValue[] = {1, 2});
[implemented, static] uint32 GetBinaryValue(
 {IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] string sValueName, 
 [OUT] uint8 uValue[]);
[implemented, static] uint32 CheckAccess(
 [IN] uint32 hDefKey = 2147483650, 
 [IN] string sSubKeyName, 
 [IN] uint32 uRequired = 3, 
 [OUT] boolean bGranted);
};
```

## <a name="example-registering-a-provider"></a><span data-ttu-id="7cd10-134">Ejemplo: registrar un proveedor</span><span class="sxs-lookup"><span data-stu-id="7cd10-134">Example: Registering a Provider</span></span>

<span data-ttu-id="7cd10-135">En el procedimiento siguiente se describe cómo registrar un proveedor.</span><span class="sxs-lookup"><span data-stu-id="7cd10-135">The following procedure describes how to register a provider.</span></span>

<span data-ttu-id="7cd10-136">**Para registrar un proveedor**</span><span class="sxs-lookup"><span data-stu-id="7cd10-136">**To register a provider**</span></span>

1.  <span data-ttu-id="7cd10-137">Registre el proveedor como un servidor COM.</span><span class="sxs-lookup"><span data-stu-id="7cd10-137">Register the provider as a COM server.</span></span>

    <span data-ttu-id="7cd10-138">Si es necesario, puede que tenga que crear entradas del registro.</span><span class="sxs-lookup"><span data-stu-id="7cd10-138">If necessary, you may need to create registry entries.</span></span> <span data-ttu-id="7cd10-139">Este proceso se aplica a todos los servidores COM y no está relacionado con WMI.</span><span class="sxs-lookup"><span data-stu-id="7cd10-139">This process applies to all COM servers and is unrelated to WMI.</span></span> <span data-ttu-id="7cd10-140">Para obtener más información, vea la sección COM en la documentación del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="7cd10-140">For more information, see the COM section in the Microsoft Windows Software Development Kit (SDK) documentation.</span></span>

2.  <span data-ttu-id="7cd10-141">Cree un archivo MOF que contenga instancias de [**\_ \_ Win32Provider**](--win32provider.md) y una instancia de una clase derivada directa o indirectamente de [**\_ \_ ProviderRegistration**](--providerregistration.md), como [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="7cd10-141">Create a MOF file that contains instances of [**\_\_Win32Provider**](--win32provider.md) and an instance of a class derived either directly or indirectly from [**\_\_ProviderRegistration**](--providerregistration.md), such as [**\_\_InstanceProviderRegistration**](--instanceproviderregistration.md).</span></span> <span data-ttu-id="7cd10-142">Solo los administradores pueden registrar o eliminar un proveedor mediante la creación de instancias de clases derivadas de **\_ \_ Win32Provider** o [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="7cd10-142">Only administrators can register or delete a provider by creating instances of classes derived from **\_\_Win32Provider** or [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>
3.  <span data-ttu-id="7cd10-143">Establezca [**HostingModel**](--win32provider.md) en la instancia de **\_ \_ Win32Provider** según los valores de los [modelos de hospedaje](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="7cd10-143">Set the [**HostingModel**](--win32provider.md) in the instance of **\_\_Win32Provider** according to the values in [Hosting models](provider-hosting-and-security.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="7cd10-144">A menos que el proveedor requiera los privilegios elevados de la cuenta LocalSystem, la propiedad [**\_ \_ Win32Provider. HostingModel**](--win32provider.md) debe establecerse en "NetworkServiceHost".</span><span class="sxs-lookup"><span data-stu-id="7cd10-144">Unless the provider requires the high privileges of the LocalSystem account, the [**\_\_Win32Provider.HostingModel**](--win32provider.md) property should be set to "NetworkServiceHost".</span></span> <span data-ttu-id="7cd10-145">Para obtener más información, vea [hospedaje y seguridad de proveedores](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="7cd10-145">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

     

    <span data-ttu-id="7cd10-146">En el siguiente ejemplo de MOF del ejemplo completo se muestra el código que crea una instancia de [**\_ \_ Win32Provider**](--win32provider.md).</span><span class="sxs-lookup"><span data-stu-id="7cd10-146">The following MOF example from the full example shows the code that creates an instance of [**\_\_Win32Provider**](--win32provider.md).</span></span>

    ```mof
    instance of __Win32Provider as $Reg
    {
    Name = "RegProv";        
    CLSID = "{fe9af5c0-d3b6-11ce-a5b6-00aa00680c3f}";
    HostingModel = "NetworkServiceHost:LocalServiceHost";
    };
    ```

    

4.  <span data-ttu-id="7cd10-147">Instancia de una clase derivada directa o indirectamente de [**\_ \_ ProviderRegistration**](--providerregistration.md), para describir la implementación lógica del proveedor.</span><span class="sxs-lookup"><span data-stu-id="7cd10-147">An instance of a class derived either directly or indirectly from [**\_\_ProviderRegistration**](--providerregistration.md), to describe the logical implementation of the provider.</span></span> <span data-ttu-id="7cd10-148">Un proveedor se puede registrar para varios tipos diferentes de funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="7cd10-148">A provider can be registered for several different types of functionality.</span></span> <span data-ttu-id="7cd10-149">En el ejemplo anterior se registra RegProv como proveedor de instancias y métodos.</span><span class="sxs-lookup"><span data-stu-id="7cd10-149">The example above registers RegProv as an instance and method provider.</span></span> <span data-ttu-id="7cd10-150">Pero si RegProv admite la funcionalidad, también podría registrarse como proveedor de propiedades o eventos.</span><span class="sxs-lookup"><span data-stu-id="7cd10-150">But if RegProv supports the functionality, it could also be registered as a property or event provider.</span></span> <span data-ttu-id="7cd10-151">En la tabla siguiente se enumeran las clases que registran la funcionalidad del proveedor.</span><span class="sxs-lookup"><span data-stu-id="7cd10-151">The following table lists the classes that register provider functionality.</span></span>

    

    | <span data-ttu-id="7cd10-152">Clases de registro de proveedor</span><span class="sxs-lookup"><span data-stu-id="7cd10-152">Provider registration classes</span></span>                                                        | <span data-ttu-id="7cd10-153">Descripción</span><span class="sxs-lookup"><span data-stu-id="7cd10-153">Description</span></span>                                                                         |
    |--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
    | [<span data-ttu-id="7cd10-154">**\_\_InstanceProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="7cd10-154">**\_\_InstanceProviderRegistration**</span></span>](--instanceproviderregistration.md)           | <span data-ttu-id="7cd10-155">Registra un [proveedor de instancias](registering-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7cd10-155">Registers an [instance provider](registering-an-instance-provider.md).</span></span>             |
    | [<span data-ttu-id="7cd10-156">**\_\_EventProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="7cd10-156">**\_\_EventProviderRegistration**</span></span>](--eventproviderregistration.md)                 | <span data-ttu-id="7cd10-157">Registra un [proveedor de eventos](registering-an-event-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7cd10-157">Registers an [event provider](registering-an-event-provider.md).</span></span>                   |
    | [<span data-ttu-id="7cd10-158">**\_\_EventConsumerProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="7cd10-158">**\_\_EventConsumerProviderRegistration**</span></span>](--eventconsumerproviderregistration.md) | <span data-ttu-id="7cd10-159">Registra un [proveedor de consumidor de eventos](registering-an-event-consumer-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7cd10-159">Registers an [event consumer provider](registering-an-event-consumer-provider.md).</span></span> |
    | [<span data-ttu-id="7cd10-160">**\_\_MethodProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="7cd10-160">**\_\_MethodProviderRegistration**</span></span>](--methodproviderregistration.md)               | <span data-ttu-id="7cd10-161">Registra un [proveedor de métodos](registering-an-event-consumer-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7cd10-161">Registers a [method provider](registering-an-event-consumer-provider.md).</span></span>          |
    | [<span data-ttu-id="7cd10-162">**\_\_PropertyProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="7cd10-162">**\_\_PropertyProviderRegistration**</span></span>](--propertyproviderregistration.md)           | <span data-ttu-id="7cd10-163">Registra un [proveedor de propiedades](registering-a-property-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7cd10-163">Registers a [property provider](registering-a-property-provider.md).</span></span>               |

    

     

5.  <span data-ttu-id="7cd10-164">Coloque el archivo MOF en un directorio permanente.</span><span class="sxs-lookup"><span data-stu-id="7cd10-164">Place the MOF file into a permanent directory.</span></span>

    <span data-ttu-id="7cd10-165">Normalmente, debe colocar el archivo en el directorio de instalación del proveedor.</span><span class="sxs-lookup"><span data-stu-id="7cd10-165">Typically, you should place the file in the installation directory of the provider.</span></span>

6.  <span data-ttu-id="7cd10-166">Compile el archivo MOF mediante [MOFCOMP](mofcomp.md) o la interfaz [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .</span><span class="sxs-lookup"><span data-stu-id="7cd10-166">Compile the MOF file using [mofcomp](mofcomp.md) or the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface.</span></span>

    <span data-ttu-id="7cd10-167">Para obtener más información, vea [compilar archivos MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="7cd10-167">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

    <span data-ttu-id="7cd10-168">**Windows 8 y Windows Server 2012:** Al instalar proveedores, tanto [**MOFCOMP**](mofcomp.md) como la interfaz [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) tratan los \[ \] calificadores de clave y \[ estáticos \] como true si están presentes, independientemente de sus valores reales.</span><span class="sxs-lookup"><span data-stu-id="7cd10-168">**Windows 8 and Windows Server 2012:** When installing providers, both [**mofcomp**](mofcomp.md) and the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface treat the \[Key\] and \[Static\] qualifiers as true if they are present, regardless of their actual values.</span></span> <span data-ttu-id="7cd10-169">Otros calificadores se tratan como false si están presentes pero no se establecen explícitamente en true.</span><span class="sxs-lookup"><span data-stu-id="7cd10-169">Other qualifiers are treated as false if they are present but not explicitly set to true.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7cd10-170">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7cd10-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cd10-171">Desarrollar un proveedor WMI</span><span class="sxs-lookup"><span data-stu-id="7cd10-171">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="7cd10-172">Configuración de descriptores de seguridad de espacio</span><span class="sxs-lookup"><span data-stu-id="7cd10-172">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="7cd10-173">Protección del proveedor</span><span class="sxs-lookup"><span data-stu-id="7cd10-173">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> </dl>

 

 
