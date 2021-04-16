---
description: En ocasiones, puede que desee actualizar solo parte de una instancia.
ms.assetid: c92bf8f9-9cac-4cf0-a45d-f60aee5a9ec2
ms.tgt_platform: multiple
title: Actualizar parte de una instancia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eaf58bfc151358a2b4f282815769d1b19c068f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706028"
---
# <a name="updating-part-of-an-instance"></a><span data-ttu-id="c0eff-103">Actualizar parte de una instancia</span><span class="sxs-lookup"><span data-stu-id="c0eff-103">Updating Part of an Instance</span></span>

<span data-ttu-id="c0eff-104">En ocasiones, puede que desee actualizar solo parte de una instancia.</span><span class="sxs-lookup"><span data-stu-id="c0eff-104">Occasionally, you may want to update only part of an instance.</span></span> <span data-ttu-id="c0eff-105">Por ejemplo, algunas instancias tienen un gran número de propiedades.</span><span class="sxs-lookup"><span data-stu-id="c0eff-105">For example, some instances have a large number of properties.</span></span> <span data-ttu-id="c0eff-106">Si tuviera que actualizar un gran número de estas instancias, puede reducir el rendimiento del sistema.</span><span class="sxs-lookup"><span data-stu-id="c0eff-106">If you had to update a large number of these instances, you may reduce system performance.</span></span> <span data-ttu-id="c0eff-107">Por lo tanto, puede optar por actualizar solo parte de la instancia y, por tanto, reducir la cantidad de información que debe enviar y recuperar en WMI.</span><span class="sxs-lookup"><span data-stu-id="c0eff-107">Therefore, you can choose to update only part of the instance, and thus reduce the amount of information you must send and retrieve to and from WMI.</span></span> <span data-ttu-id="c0eff-108">Sin embargo, WMI no admite directamente las operaciones de instancia parcial ni la mayoría de los proveedores.</span><span class="sxs-lookup"><span data-stu-id="c0eff-108">However, WMI does not directly support partial-instance operations, nor do most providers.</span></span> <span data-ttu-id="c0eff-109">Por lo tanto, si escribe una aplicación que utiliza operaciones de instancia parcial, debe estar preparado para que las llamadas produzcan un error con el **proveedor de WBEM \_ e \_ \_ \_** no compatible o el código de error **WBEM \_ e \_ no \_ admitido** en C++.</span><span class="sxs-lookup"><span data-stu-id="c0eff-109">Therefore, if you write an application that uses partial-instance operations, be prepared for your calls to fail with either the **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** or **WBEM\_E\_NOT\_SUPPORTED** error code in C++.</span></span> <span data-ttu-id="c0eff-110">En los lenguajes de scripting, los códigos de error son **wbemErrProviderNotCapable** o **wbemErrNotSupported**.</span><span class="sxs-lookup"><span data-stu-id="c0eff-110">In scripting languages the error codes are either **wbemErrProviderNotCapable** or **wbemErrNotSupported**.</span></span>

<span data-ttu-id="c0eff-111">En el scripting, esta operación solo es necesaria para ayudar al rendimiento al actualizar una o dos propiedades que se deben escribir en un gran número de objetos en una empresa.</span><span class="sxs-lookup"><span data-stu-id="c0eff-111">In scripting, this operation is only necessary to aid performance when updating one or two writeable properties in a very large number of objects over an enterprise.</span></span> <span data-ttu-id="c0eff-112">De lo contrario, las llamadas normales de VBScript a [**SWbemObject. put \_**](swbemobject-put-.md) o [**SWbemObject. PutAsync \_**](swbemobject-putasync-.md), mientras que parece que escriben todo el objeto, en realidad solo están actualizando las propiedades en las que el proveedor tiene habilitada la escritura.</span><span class="sxs-lookup"><span data-stu-id="c0eff-112">Otherwise, the normal VBScript calls to [**SWbemObject.Put\_**](swbemobject-put-.md) or [**SWbemObject.PutAsync\_**](swbemobject-putasync-.md), while seeming to write the entire object, are actually only updating the properties which the provider has write-enabled.</span></span>

<span data-ttu-id="c0eff-113">En el procedimiento siguiente se describe cómo solicitar una actualización de instancia parcial mediante PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c0eff-113">The following procedure describes how to request a partial-instance update using PowerShell.</span></span>

<span data-ttu-id="c0eff-114">**Para solicitar una actualización de instancia parcial mediante PowerShell**</span><span class="sxs-lookup"><span data-stu-id="c0eff-114">**To request a partial-instance update using PowerShell**</span></span>

1.  <span data-ttu-id="c0eff-115">Recupere la ruta de acceso del objeto que desea actualizar.</span><span class="sxs-lookup"><span data-stu-id="c0eff-115">Retrieve the path of the object you wish to update.</span></span>

    <span data-ttu-id="c0eff-116">Puede describir la ruta de acceso manualmente, o bien consultar el objeto y, a continuación, recuperar la propiedad **\_ \_ path** .</span><span class="sxs-lookup"><span data-stu-id="c0eff-116">You can describe the path either manually, or else query the object and then retrieve the **\_\_Path** property.</span></span>

    ```PowerShell
    $myWMIDrivePath = (get-wmiObject Win32_LogicalDisk -filter "Name = 'C:'").__Path
    #or
    $myWmiDrivePath = \\myComputer\root\cimv2:Win32_LogicalDisk.DeviceID="C:"
    ```

    

2.  <span data-ttu-id="c0eff-117">Configure una tabla hash que Enumere los nombres de las propiedades que se van a actualizar y use esta tabla hash en una llamada a [set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="c0eff-117">Set up a hash table listing the names of the properties to be updated, and use this hash table in a call to [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true).</span></span>

    ```PowerShell
    $newDriveName = @{VolumeName = "OSDisk"}
    Set-WmiInstance -Path $myWMIDrivePath -Arguments $newDriveName
    ```

    

<span data-ttu-id="c0eff-118">En el procedimiento siguiente se describe cómo solicitar una actualización de instancia parcial mediante C#.</span><span class="sxs-lookup"><span data-stu-id="c0eff-118">The following procedure describes how to request a partial-instance update using C#.</span></span>

> [!Note]  
> <span data-ttu-id="c0eff-119">**System. Management** era el espacio de nombres .net original utilizado para tener acceso a WMI. sin embargo, las API de este espacio de nombres suelen ser más lentas y no se escalan con respecto a sus homólogos de **Microsoft. Management. Infrastructure** más modernos.</span><span class="sxs-lookup"><span data-stu-id="c0eff-119">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="c0eff-120">**Para solicitar una actualización de instancia parcial mediante C #**</span><span class="sxs-lookup"><span data-stu-id="c0eff-120">**To request a partial-instance update using C#**</span></span>

1.  <span data-ttu-id="c0eff-121">Cree un nuevo objeto [ManagementObject](/dotnet/api/system.management.managementobject) que represente la instancia específica que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="c0eff-121">Create a new [ManagementObject](/dotnet/api/system.management.managementobject) object that represents the specific instance to update.</span></span>

    ```PowerShell
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    ```

    

2.  <span data-ttu-id="c0eff-122">Establezca el valor de propiedad con una llamada a [ManagementObject. SetPropertyValue](/dotnet/api/system.management.managementbaseobject.setpropertyvalue#System_Management_ManagementBaseObject_SetPropertyValue_System_String_System_Object_).</span><span class="sxs-lookup"><span data-stu-id="c0eff-122">Set the property value with a call to [ManagementObject.SetPropertyValue](/dotnet/api/system.management.managementbaseobject.setpropertyvalue#System_Management_ManagementBaseObject_SetPropertyValue_System_String_System_Object_).</span></span>

    ```CSharp
    myDisk.SetPropertyValue("VolumeName", "OSDisk");
    ```

    

<span data-ttu-id="c0eff-123">En el procedimiento siguiente se describe cómo solicitar una actualización de instancia parcial mediante VBScript.</span><span class="sxs-lookup"><span data-stu-id="c0eff-123">The following procedure describes how to request a partial-instance update using VBScript.</span></span>

<span data-ttu-id="c0eff-124">**Para solicitar una actualización de instancia parcial mediante VBScript**</span><span class="sxs-lookup"><span data-stu-id="c0eff-124">**To request a partial-instance update using VBScript**</span></span>

1.  <span data-ttu-id="c0eff-125">Cree un objeto de contexto [**SWbemNamedValueSet**](swbemnamedvalueset.md) .</span><span class="sxs-lookup"><span data-stu-id="c0eff-125">Create an [**SWbemNamedValueSet**](swbemnamedvalueset.md) context object.</span></span>

    ```VB
    Set objwbemNamedValueSet = CreateObject ("WbemScripting.SWbemNamedValueSet")
    ```

    

2.  <span data-ttu-id="c0eff-126">Agregue los valores de la extensión put " \_ \_ Put \_ Extensions" y " \_ \_ Put \_ ext \_ Client \_ Request" al objeto de contexto mediante el método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) .</span><span class="sxs-lookup"><span data-stu-id="c0eff-126">Add the Put extension values "\_\_PUT\_EXTENSIONS" and "\_\_PUT\_EXT\_CLIENT\_REQUEST" to the context object using the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method.</span></span>

    ```VB
    objwbemNamedValueSet.Add "__PUT_EXTENSIONS", True
    objwbemNamedValueSet.Add "__PUT_EXT_CLIENT_REQUEST", True
    ```

    

3.  <span data-ttu-id="c0eff-127">Configure una matriz que Enumere los nombres de las propiedades que se van a actualizar y agregue esta matriz al objeto de contexto [**SWbemNamedValueSet**](swbemnamedvalueset.md) con el valor de la extensión put " \_ \_ Put \_ ext \_ Properties".</span><span class="sxs-lookup"><span data-stu-id="c0eff-127">Set up an array listing the names of the properties to be updated and add this array to the [**SWbemNamedValueSet**](swbemnamedvalueset.md) context object with the Put extension value "\_\_PUT\_EXT\_PROPERTIES".</span></span>

    ```VB
    arProperties = Array("propertyname1", "propertyname2") 
    objwbemNamedValueSet.Add "__PUT_EXT_PROPERTIES", arProperties
    ```

    

4.  <span data-ttu-id="c0eff-128">Establezca el parámetro *iFlags* de la llamada a [**SWbemObject \_ . put**](swbemobject-put-.md) en **wbemChangeFlagUpdateOnly**.</span><span class="sxs-lookup"><span data-stu-id="c0eff-128">Set the *iFlags* parameter of the [**SWbemObject.Put\_**](swbemobject-put-.md) call to **wbemChangeFlagUpdateOnly**.</span></span> <span data-ttu-id="c0eff-129">Sin este marcador, se producirá un error en la llamada con un contexto no válido.</span><span class="sxs-lookup"><span data-stu-id="c0eff-129">Without this flag the call will fail with an invalid context.</span></span>

5.  <span data-ttu-id="c0eff-130">Pase la marca y el objeto de contexto al proveedor en el parámetro *objwbemNamedValueSet* de [**SWbemObject. put \_**](swbemobject-put-.md) o [**SWbemObject. PutAsync \_**](swbemobject-putasync-.md).</span><span class="sxs-lookup"><span data-stu-id="c0eff-130">Pass your flag and context object to the provider in the *objwbemNamedValueSet* parameter of either [**SWbemObject.Put\_**](swbemobject-put-.md) or [**SWbemObject.PutAsync\_**](swbemobject-putasync-.md).</span></span>

    ```VB
    call objSystem.put_( wbemChangeFlagUpdateOnly, objwbemNamedValueSet)
    ```

    

<span data-ttu-id="c0eff-131">En el procedimiento siguiente se describe cómo solicitar una actualización de instancia parcial mediante C++.</span><span class="sxs-lookup"><span data-stu-id="c0eff-131">The following procedure describes how to request a partial-instance update using C++.</span></span>

<span data-ttu-id="c0eff-132">**Para solicitar una actualización de instancia parcial mediante C++**</span><span class="sxs-lookup"><span data-stu-id="c0eff-132">**To request a partial-instance update using C++**</span></span>

1.  <span data-ttu-id="c0eff-133">Cree un objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) con una llamada a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="c0eff-133">Create an [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object with a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="c0eff-134">Un objeto de contexto es un objeto que WMI utiliza para pasar más información a un proveedor WMI.</span><span class="sxs-lookup"><span data-stu-id="c0eff-134">A context object is an object that WMI uses to pass in more information to a WMI provider.</span></span> <span data-ttu-id="c0eff-135">En este caso, se usa el objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) para indicar al proveedor que acepte actualizaciones parciales de la instancia.</span><span class="sxs-lookup"><span data-stu-id="c0eff-135">In this case, you are using the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object to instruct the provider to accept partial-instance updates.</span></span>

2.  <span data-ttu-id="c0eff-136">Agregue los \_ \_ valores "Put \_ Extensions" y " \_ \_ Put \_ ext \_ Client \_ Request" con nombre al objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) con una llamada a [**IWbemContext:: SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue).</span><span class="sxs-lookup"><span data-stu-id="c0eff-136">Add the "\_\_PUT\_EXTENSIONS" and "\_\_PUT\_EXT\_CLIENT\_REQUEST" named values to the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object with a call to [**IWbemContext::SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue).</span></span>

    <span data-ttu-id="c0eff-137">En la tabla siguiente se muestra el significado de " \_ \_ Put \_ Extensions" y " \_ \_ Put \_ ext \_ Client \_ Request".</span><span class="sxs-lookup"><span data-stu-id="c0eff-137">The following table lists the meaning of "\_\_PUT\_EXTENSIONS" and "\_\_PUT\_EXT\_CLIENT\_REQUEST".</span></span>

    

    | <span data-ttu-id="c0eff-138">Valor con nombre</span><span class="sxs-lookup"><span data-stu-id="c0eff-138">Named value</span></span>                     | <span data-ttu-id="c0eff-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0eff-139">Description</span></span>                                                                                                                                                                                                                                             |
    |---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="c0eff-140">" \_ \_ Put \_ Extensions"</span><span class="sxs-lookup"><span data-stu-id="c0eff-140">"\_\_PUT\_EXTENSIONS"</span></span>           | <span data-ttu-id="c0eff-141">**VT \_ BOOL** se establece en **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="c0eff-141">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="c0eff-142">Valor que indica que se han especificado uno o varios de los demás valores de contexto.</span><span class="sxs-lookup"><span data-stu-id="c0eff-142">A value indicating that one or more of the other context values has been specified.</span></span> <span data-ttu-id="c0eff-143">Esto permite realizar una comprobación rápida del objeto de contexto dentro del proveedor para determinar si se están usando actualizaciones parciales de instancia.</span><span class="sxs-lookup"><span data-stu-id="c0eff-143">This allows a quick check of the context object inside the provider to determine if partial-instance updates are being used.</span></span> |
    | <span data-ttu-id="c0eff-144">" \_ \_ Put \_ ext \_ Client \_ Request"</span><span class="sxs-lookup"><span data-stu-id="c0eff-144">"\_\_PUT\_EXT\_CLIENT\_REQUEST"</span></span> | <span data-ttu-id="c0eff-145">**VT \_ BOOL** se establece en **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="c0eff-145">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="c0eff-146">Establecido por el cliente durante la solicitud inicial.</span><span class="sxs-lookup"><span data-stu-id="c0eff-146">Set by the client during the initial request.</span></span> <span data-ttu-id="c0eff-147">Este valor se usa para evitar errores de reentrada.</span><span class="sxs-lookup"><span data-stu-id="c0eff-147">This value is used to prevent reentrancy errors.</span></span>                                                                                                                   |

    

     

3.  <span data-ttu-id="c0eff-148">Agregue las \_ \_ \_ propiedades Put ext \_ Strict, Put ext o Put ext \_ \_ \_ \_ \_ \_ \_ \_ \_ Atomic en cualquier combinación según sea necesario para el objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) con otra llamada a [**IWbemContext:: SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue).</span><span class="sxs-lookup"><span data-stu-id="c0eff-148">Add the \_\_PUT\_EXT\_STRICT\_NULLS, \_\_PUT\_EXT\_PROPERTIES, or \_\_PUT\_EXT\_ATOMIC in any combination as needed to the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object with another call to [**IWbemContext::SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue).</span></span>

    <span data-ttu-id="c0eff-149">En la tabla siguiente se muestra el significado de los valores con nombre.</span><span class="sxs-lookup"><span data-stu-id="c0eff-149">The following table lists the meaning of the named values.</span></span>

    

    | <span data-ttu-id="c0eff-150">Valor con nombre</span><span class="sxs-lookup"><span data-stu-id="c0eff-150">Named value</span></span>                   | <span data-ttu-id="c0eff-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0eff-151">Description</span></span>                                                                                                                                                                                                                                   |
    |-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="c0eff-152">" \_ \_ Put \_ ext \_ STRICT \_ Nulls"</span><span class="sxs-lookup"><span data-stu-id="c0eff-152">"\_\_PUT\_EXT\_STRICT\_NULLS"</span></span> | <span data-ttu-id="c0eff-153">**VT \_ BOOL** se establece en **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="c0eff-153">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="c0eff-154">Indica que el cliente ha establecido intencionadamente las propiedades en **VT \_ null** y espera que la operación de escritura se realice correctamente.</span><span class="sxs-lookup"><span data-stu-id="c0eff-154">Indicates that the client has intentionally set properties to **VT\_NULL** and expects the write operation to succeed.</span></span> <span data-ttu-id="c0eff-155">Si el proveedor no puede establecer los valores en **null**, se debe informar de un error.</span><span class="sxs-lookup"><span data-stu-id="c0eff-155">If the provider cannot set the values to **NULL**, an error should be reported.</span></span> |
    | <span data-ttu-id="c0eff-156">" \_ \_ Put \_ ext \_ Properties"</span><span class="sxs-lookup"><span data-stu-id="c0eff-156">"\_\_PUT\_EXT\_PROPERTIES"</span></span>    | <span data-ttu-id="c0eff-157">[**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) de cadenas que contiene una lista de nombres de propiedad que se van a actualizar.</span><span class="sxs-lookup"><span data-stu-id="c0eff-157">[**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) of strings containing a list of property names to be updated.</span></span> <span data-ttu-id="c0eff-158">Se puede usar por sí solo o en combinación con " \_ \_ Put \_ ext \_ Properties".</span><span class="sxs-lookup"><span data-stu-id="c0eff-158">May be used alone or in combination with "\_\_PUT\_EXT\_PROPERTIES".</span></span> <span data-ttu-id="c0eff-159">Los valores se encuentran en la instancia que se está escribiendo.</span><span class="sxs-lookup"><span data-stu-id="c0eff-159">The values are in the instance being written.</span></span>                           |
    | <span data-ttu-id="c0eff-160">" \_ \_ Put \_ ext \_ Atomic"</span><span class="sxs-lookup"><span data-stu-id="c0eff-160">"\_\_PUT\_EXT\_ATOMIC"</span></span>        | <span data-ttu-id="c0eff-161">**VT \_ BOOL** se establece en **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="c0eff-161">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="c0eff-162">Indica que todas las actualizaciones deben realizarse de forma simultánea (semántica atómica) o el proveedor debe revertirse.</span><span class="sxs-lookup"><span data-stu-id="c0eff-162">Indicates that all updates must succeed simultaneously (atomic semantics) or the provider must revert back.</span></span> <span data-ttu-id="c0eff-163">No puede haber ningún éxito parcial.</span><span class="sxs-lookup"><span data-stu-id="c0eff-163">There can be no partial success.</span></span> <span data-ttu-id="c0eff-164">Se puede usar por sí solo o en combinación con otras marcas.</span><span class="sxs-lookup"><span data-stu-id="c0eff-164">May be used alone or in combination with other flags.</span></span>     |

    

     

4.  <span data-ttu-id="c0eff-165">Establezca el parámetro *iFlags* en **WBEM \_ marcar \_ \_ solo actualizar**.</span><span class="sxs-lookup"><span data-stu-id="c0eff-165">Set the *iFlags* parameter to **WBEM\_FLAG\_UPDATE\_ONLY**.</span></span> <span data-ttu-id="c0eff-166">Sin este marcador, se producirá un error en la llamada con un contexto no válido.</span><span class="sxs-lookup"><span data-stu-id="c0eff-166">Without this flag the call will fail with an invalid context.</span></span>
5.  <span data-ttu-id="c0eff-167">Pase el objeto de contexto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) a las llamadas [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) o [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) en el parámetro *pCtx* .</span><span class="sxs-lookup"><span data-stu-id="c0eff-167">Pass the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) context object into any calls [**IWbemServices::PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) in the *pCtx* parameter.</span></span>

    <span data-ttu-id="c0eff-168">Al pasar el objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) se indica al proveedor que permita las actualizaciones parciales de la instancia.</span><span class="sxs-lookup"><span data-stu-id="c0eff-168">Passing the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object instructs the provider to allow partial-instance updates.</span></span> <span data-ttu-id="c0eff-169">En una actualización de instancia completa, establecería *pCtx* en **null**.</span><span class="sxs-lookup"><span data-stu-id="c0eff-169">In a full-instance update, you would set *pCtx* to **NULL**.</span></span>

    <span data-ttu-id="c0eff-170">El proveedor puede escribir las propiedades necesarias si el objeto de contexto presente en la llamada no contiene " \_ \_ Put \_ Extensions".</span><span class="sxs-lookup"><span data-stu-id="c0eff-170">The provider may write any necessary properties if the context object present in the call does not contain "\_\_PUT\_EXTENSIONS".</span></span> <span data-ttu-id="c0eff-171">Si " \_ \_ Put \_ Extensions" está presente en el objeto de contexto, WMI requiere que el proveedor cumpla la semántica de la operación exactamente o que se produzca un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="c0eff-171">If "\_\_PUT\_EXTENSIONS" is present in the context object, WMI requires the provider to either obey the semantics of the operation exactly or else fail the call.</span></span> <span data-ttu-id="c0eff-172">Para obtener más información, vea [controlar los mensajes de acceso denegado en un proveedor](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="c0eff-172">For more information, see [Handling Access Denied Messages in a Provider](impersonating-a-client.md).</span></span>

 

 
