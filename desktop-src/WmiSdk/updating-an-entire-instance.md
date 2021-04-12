---
description: La forma más común de actualizar una instancia de clase WMI es actualizar toda la instancia a la vez.
ms.assetid: fca5f102-0823-4900-b147-9b29ca036607
ms.tgt_platform: multiple
title: Actualizar una instancia completa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae81b334d1d89a7e936e2c9d80aebfbeecb430bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277921"
---
# <a name="updating-an-entire-instance"></a><span data-ttu-id="07a6c-103">Actualizar una instancia completa</span><span class="sxs-lookup"><span data-stu-id="07a6c-103">Updating an Entire Instance</span></span>

<span data-ttu-id="07a6c-104">La forma más común de actualizar una instancia de clase WMI es actualizar toda la instancia a la vez.</span><span class="sxs-lookup"><span data-stu-id="07a6c-104">The most common means of updating a WMI class instance is to update the entire instance at once.</span></span> <span data-ttu-id="07a6c-105">Al actualizar una instancia completa, WMI no tiene que analizar la instancia en propiedades individuales y enviarlas a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="07a6c-105">By updating an entire instance, WMI does not have to parse the instance into individual properties and send them to your application.</span></span> <span data-ttu-id="07a6c-106">En su lugar, WMI simplemente le puede enviar toda la instancia.</span><span class="sxs-lookup"><span data-stu-id="07a6c-106">Instead, WMI can simply send you the entire instance.</span></span> <span data-ttu-id="07a6c-107">Cuando termine, WMI podrá copiar toda la instancia modificada en la instancia original.</span><span class="sxs-lookup"><span data-stu-id="07a6c-107">When you finish, WMI can then copy your entire changed instance over the original instance.</span></span>

<span data-ttu-id="07a6c-108">En el procedimiento siguiente se describe cómo modificar o actualizar una instancia de mediante PowerShell.</span><span class="sxs-lookup"><span data-stu-id="07a6c-108">The following procedure describes how to modify or update an instance using PowerShell.</span></span>

<span data-ttu-id="07a6c-109">**Para modificar o actualizar una instancia mediante PowerShell**</span><span class="sxs-lookup"><span data-stu-id="07a6c-109">**To modify or update an instance using PowerShell**</span></span>

1.  <span data-ttu-id="07a6c-110">Recupere una copia local del objeto con una llamada a get-WmiObject.</span><span class="sxs-lookup"><span data-stu-id="07a6c-110">Retrieve a local copy of the object with a call to Get-WmiObject.</span></span>

    ```PowerShell
    $mySettings = get-WMIObject Win32_WmiSetting
    ```

    

2.  <span data-ttu-id="07a6c-111">Si es necesario, vea las propiedades del objeto con una llamada a la colección Properties.</span><span class="sxs-lookup"><span data-stu-id="07a6c-111">If necessary, view the properties of the object with a call to the Properties collection.</span></span>

    <span data-ttu-id="07a6c-112">Aunque no es necesario, es posible que desee conocer el valor de la propiedad antes de cambiarla.</span><span class="sxs-lookup"><span data-stu-id="07a6c-112">Although not required, you may wish to know the value of the property before you change it.</span></span>

    ```PowerShell
    $mySettings.Properties
    ```

    

3.  <span data-ttu-id="07a6c-113">Realice los cambios en las propiedades del objeto local.</span><span class="sxs-lookup"><span data-stu-id="07a6c-113">Make any changes to the local object properties.</span></span>

    <span data-ttu-id="07a6c-114">Si lo hace, solo cambiará la copia local.</span><span class="sxs-lookup"><span data-stu-id="07a6c-114">Doing so changes only the local copy.</span></span> <span data-ttu-id="07a6c-115">Para guardar los cambios en WMI, debe volver a colocar la copia completa en el repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="07a6c-115">To save your changes to WMI, you must place the entire copy back into the WMI repository.</span></span>

    ```PowerShell
    $mySettings.LoggingLevel = 1
    ```

    

4.  <span data-ttu-id="07a6c-116">Vuelva a colocar el objeto en el repositorio WMI mediante una llamada al método put.</span><span class="sxs-lookup"><span data-stu-id="07a6c-116">Place the object back into the WMI repository using a call to the Put method.</span></span>

    ```PowerShell
    $mySettings.Put()
    ```

    

<span data-ttu-id="07a6c-117">En el procedimiento siguiente se describe cómo modificar o actualizar una instancia de mediante C#.</span><span class="sxs-lookup"><span data-stu-id="07a6c-117">The following procedure describes how to modify or update an instance using C#.</span></span>

<span data-ttu-id="07a6c-118">**Para modificar o actualizar una instancia mediante C# (Microsoft. Management. Infrastructure)**</span><span class="sxs-lookup"><span data-stu-id="07a6c-118">**To modify or update an instance using C# (Microsoft.Management.Infrastructure)**</span></span>

1.  <span data-ttu-id="07a6c-119">Recupere una copia local del objeto con una llamada a [CimSession. getInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)), tal y como se describe en [recuperar una instancia de WMI](retrieving-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="07a6c-119">Retrieve a local copy of the object with a call to [CimSession.GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)), as described in [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "win32_logicalDisk";

    CimInstance diskDrive = new CimInstance(className, Namespace);
    diskDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));

    CimSession session = CimSession.Create("localhost");
    CimInstance myDisk = session.GetInstance(Namespace, diskDrive);
    ```

    

2.  <span data-ttu-id="07a6c-120">Si es necesario, vea las propiedades del objeto con una llamada a la colección Properties.</span><span class="sxs-lookup"><span data-stu-id="07a6c-120">If necessary, view the properties of the object with a call to the Properties collection.</span></span>

    <span data-ttu-id="07a6c-121">Aunque no es necesario, es posible que desee conocer el valor de la propiedad antes de cambiarla.</span><span class="sxs-lookup"><span data-stu-id="07a6c-121">Although not required, you may wish to know the value of the property before you change it.</span></span>

    ```CSharp
    foreach (CimProperty property in myDisk.CimInstanceProperties)
    {
       Console.WriteLine(property.ToString());
    }

    Console.ReadLine();
    ```

    

3.  <span data-ttu-id="07a6c-122">Realice los cambios en las propiedades del objeto local.</span><span class="sxs-lookup"><span data-stu-id="07a6c-122">Make any changes to the local object properties.</span></span>

    <span data-ttu-id="07a6c-123">Si lo hace, solo cambiará la copia local.</span><span class="sxs-lookup"><span data-stu-id="07a6c-123">Doing so changes only the local copy.</span></span> <span data-ttu-id="07a6c-124">Para guardar los cambios en WMI, debe volver a colocar la copia completa en el repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="07a6c-124">To save your changes to WMI, you must place the entire copy back into the WMI repository.</span></span>

    ```CSharp
    myDisk.CimInstanceProperties["VolumeName"].Value = "NewName";
    ```

    

4.  <span data-ttu-id="07a6c-125">Vuelva a colocar el objeto en el repositorio WMI mediante una llamada a [CimSession. ModifyInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832593(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="07a6c-125">Place the object back into the WMI repository using a call to [CimSession.ModifyInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832593(v=vs.85)).</span></span>

    ```CSharp
    session.ModifyInstance(Namespace,myDisk);
    ```

    

<span data-ttu-id="07a6c-126">En el procedimiento siguiente se describe cómo modificar o actualizar una instancia de mediante PowerShell.</span><span class="sxs-lookup"><span data-stu-id="07a6c-126">The following procedure describes how to modify or update an instance using PowerShell.</span></span>

> [!Note]  
> <span data-ttu-id="07a6c-127">**System. Management** era el espacio de nombres .net original utilizado para tener acceso a WMI. sin embargo, las API de este espacio de nombres suelen ser más lentas y no se escalan con respecto a sus homólogos de **Microsoft. Management. Infrastructure** más modernos.</span><span class="sxs-lookup"><span data-stu-id="07a6c-127">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="07a6c-128">**Para modificar o actualizar una instancia de mediante C# (Microsoft. Management)**</span><span class="sxs-lookup"><span data-stu-id="07a6c-128">**To modify or update an instance using C# (Microsoft.Management)**</span></span>

1.  <span data-ttu-id="07a6c-129">Recupere una copia local del objeto con una llamada a [ManagementObject. Get](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get).</span><span class="sxs-lookup"><span data-stu-id="07a6c-129">Retrieve a local copy of the object with a call to [ManagementObject.Get](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get).</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    myDisk.Get();
    ```

    

2.  <span data-ttu-id="07a6c-130">Si es necesario, vea las propiedades del objeto con una llamada a la colección Properties.</span><span class="sxs-lookup"><span data-stu-id="07a6c-130">If necessary, view the properties of the object with a call to the Properties collection.</span></span>

    <span data-ttu-id="07a6c-131">Aunque no es necesario, es posible que desee conocer el valor de la propiedad antes de cambiarla.</span><span class="sxs-lookup"><span data-stu-id="07a6c-131">Although not required, you may wish to know the value of the property before you change it.</span></span>

    ```CSharp
    foreach (PropertyData property in myDisk.Properties)
    {
       Console.WriteLine(property.Name + " " + property.Value);
    }

    Console.ReadLine();
    ```

    

3.  <span data-ttu-id="07a6c-132">Realice los cambios en las propiedades del objeto local.</span><span class="sxs-lookup"><span data-stu-id="07a6c-132">Make any changes to the local object properties.</span></span>

    <span data-ttu-id="07a6c-133">Si lo hace, solo cambiará la copia local.</span><span class="sxs-lookup"><span data-stu-id="07a6c-133">Doing so changes only the local copy.</span></span> <span data-ttu-id="07a6c-134">Para guardar los cambios en WMI, debe volver a colocar la copia completa en el repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="07a6c-134">To save your changes to WMI, you must place the entire copy back into the WMI repository.</span></span>

    ```CSharp
    myDisk["VolumeName"] = "newName";
    ```

    

4.  <span data-ttu-id="07a6c-135">Vuelva a colocar el objeto en el repositorio WMI mediante una llamada al método [ManagementObject. put](/dotnet/api/system.management.managementobject.put#System_Management_ManagementObject_Put) o.</span><span class="sxs-lookup"><span data-stu-id="07a6c-135">Place the object back into the WMI repository using a call to the [ManagementObject.Put](/dotnet/api/system.management.managementobject.put#System_Management_ManagementObject_Put) or method.</span></span>

    ```CSharp
    myDisk.Put();
    ```

    

<span data-ttu-id="07a6c-136">En el procedimiento siguiente se describe cómo modificar o actualizar una instancia de mediante VBScript.</span><span class="sxs-lookup"><span data-stu-id="07a6c-136">The following procedure describes how to modify or update an instance using VBScript.</span></span>

<span data-ttu-id="07a6c-137">**Para modificar o actualizar una instancia de mediante VBScript**</span><span class="sxs-lookup"><span data-stu-id="07a6c-137">**To modify or update an instance using VBScript**</span></span>

1.  <span data-ttu-id="07a6c-138">Recupere una copia local del objeto con una llamada a **GetObject**.</span><span class="sxs-lookup"><span data-stu-id="07a6c-138">Retrieve a local copy of the object with a call to **GetObject**.</span></span>
2.  <span data-ttu-id="07a6c-139">Si es necesario, vea las propiedades del objeto con una llamada al método [**Properties \_**](swbemobject-properties-.md) .</span><span class="sxs-lookup"><span data-stu-id="07a6c-139">If necessary, view the properties of the object with a call to the [**Properties\_**](swbemobject-properties-.md) method.</span></span>

    <span data-ttu-id="07a6c-140">Aunque no es necesario, es posible que desee conocer el valor de la propiedad antes de cambiarla.</span><span class="sxs-lookup"><span data-stu-id="07a6c-140">Although not required, you may wish to know the value of the property before you change it.</span></span>

3.  <span data-ttu-id="07a6c-141">Realice cualquier cambio en las propiedades del objeto con una llamada al método [**SWbemProperty. Value**](swbemproperty-value.md) .</span><span class="sxs-lookup"><span data-stu-id="07a6c-141">Make any changes to the object properties with a call to the [**SWbemProperty.Value**](swbemproperty-value.md) method.</span></span>

    <span data-ttu-id="07a6c-142">El método **Value** solo cambia la copia local.</span><span class="sxs-lookup"><span data-stu-id="07a6c-142">The **Value** method changes only the local copy.</span></span> <span data-ttu-id="07a6c-143">Para guardar los cambios en WMI, debe volver a colocar la copia completa en el repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="07a6c-143">To save your changes to WMI, you must place the entire copy back into the WMI repository.</span></span>

4.  <span data-ttu-id="07a6c-144">Vuelva a colocar el objeto en el repositorio WMI con una llamada a los métodos [**SWbemObject. put \_**](swbemobject-put-.md) o [**SWbemObject. PutAsync \_**](swbemobject-putasync-.md) .</span><span class="sxs-lookup"><span data-stu-id="07a6c-144">Place the object back into the WMI repository with a call the [**SWbemObject.Put\_**](swbemobject-put-.md) or [**SWbemObject.PutAsync\_**](swbemobject-putasync-.md) methods.</span></span>

<span data-ttu-id="07a6c-145">Como los nombres implican [**, \_ ponga**](swbemobject-put-.md) las actualizaciones sincrónicamente mientras el [**PutAsync \_**](swbemobject-putasync-.md) se actualiza de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="07a6c-145">As the names imply, [**Put\_**](swbemobject-put-.md) updates synchronously while [**PutAsync\_**](swbemobject-putasync-.md) updates asynchronously.</span></span> <span data-ttu-id="07a6c-146">Cualquiera de los métodos copia la instancia original con la instancia modificada.</span><span class="sxs-lookup"><span data-stu-id="07a6c-146">Either method copies over the original instance with your modified instance.</span></span> <span data-ttu-id="07a6c-147">Sin embargo, para aprovechar el procesamiento asincrónico, debe crear un objeto [**SWbemSink**](swbemsink.md) .</span><span class="sxs-lookup"><span data-stu-id="07a6c-147">However, to take advantage of asynchronous processing, you must create an [**SWbemSink**](swbemsink.md) object.</span></span> <span data-ttu-id="07a6c-148">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="07a6c-148">For more information, see [Calling a method](calling-a-method.md).</span></span>

<span data-ttu-id="07a6c-149">En el procedimiento siguiente se describe cómo modificar o actualizar una instancia de mediante C++.</span><span class="sxs-lookup"><span data-stu-id="07a6c-149">The following procedure describes how to modify or update an instance using C++.</span></span>

<span data-ttu-id="07a6c-150">**Para modificar o actualizar una instancia de mediante C++**</span><span class="sxs-lookup"><span data-stu-id="07a6c-150">**To modify or update an instance using C++**</span></span>

1.  <span data-ttu-id="07a6c-151">Recupere una copia local de la instancia de con una llamada a [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="07a6c-151">Retrieve a local copy of the instance with a call to [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>
2.  <span data-ttu-id="07a6c-152">Si es necesario, vea las propiedades del objeto con una llamada a [**IWbemClassObject:: get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get).</span><span class="sxs-lookup"><span data-stu-id="07a6c-152">If necessary, view the properties of the object with a call to [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get).</span></span>

    <span data-ttu-id="07a6c-153">Aunque no es necesario, es posible que desee conocer el valor de la propiedad antes de cambiarla.</span><span class="sxs-lookup"><span data-stu-id="07a6c-153">Although not required, you may wish to know the value of the property before you change it.</span></span>

3.  <span data-ttu-id="07a6c-154">Realice los cambios necesarios en la copia con una llamada a [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span><span class="sxs-lookup"><span data-stu-id="07a6c-154">Make any necessary changes to the copy with a call to [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>

    <span data-ttu-id="07a6c-155">El método **Put** cambia solo la copia local.</span><span class="sxs-lookup"><span data-stu-id="07a6c-155">The **Put** method changes only the local copy.</span></span> <span data-ttu-id="07a6c-156">Para guardar los cambios en WMI, debe volver a colocar la copia completa en el repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="07a6c-156">To save your changes to WMI, you must place the entire copy back into the WMI repository.</span></span>

4.  <span data-ttu-id="07a6c-157">Vuelva a colocar la copia en el repositorio WMI con una llamada a los métodos [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) o [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) .</span><span class="sxs-lookup"><span data-stu-id="07a6c-157">Place your copy back into the WMI repository with a call the [**IWbemServices::PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) methods.</span></span>

    <span data-ttu-id="07a6c-158">Como los nombres implican, **PutInstance** se actualiza sincrónicamente mientras [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) actualiza de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="07a6c-158">As the names imply, **PutInstance** updates synchronously while [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) updates asynchronously.</span></span> <span data-ttu-id="07a6c-159">Cualquiera de los métodos copia la instancia original con la instancia modificada.</span><span class="sxs-lookup"><span data-stu-id="07a6c-159">Either method copies over the original instance with your modified instance.</span></span> <span data-ttu-id="07a6c-160">Sin embargo, para aprovechar el procesamiento asincrónico, debe implementar la interfaz [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="07a6c-160">However, to take advantage of asynchronous processing, you must implement the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

    <span data-ttu-id="07a6c-161">Debe tener en cuenta que una operación de actualización en una instancia que pertenece a una jerarquía de clases podría no realizarse correctamente debido a un error relacionado con otra clase de la jerarquía.</span><span class="sxs-lookup"><span data-stu-id="07a6c-161">You should be aware that an update operation on an instance belonging to a class hierarchy might not succeed due to an error involving another class in the hierarchy.</span></span> <span data-ttu-id="07a6c-162">WMI llama al método [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) de cada uno de los proveedores responsables de las clases de las que se deriva la clase propietaria de la instancia original.</span><span class="sxs-lookup"><span data-stu-id="07a6c-162">WMI calls the [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) method of each of the providers responsible for the classes from which the class owning the original instance derives.</span></span> <span data-ttu-id="07a6c-163">Si se produce un error en cualquiera de estos proveedores, se produce un error en la solicitud de actualización original.</span><span class="sxs-lookup"><span data-stu-id="07a6c-163">If any of these providers fail, the original update request fails.</span></span> <span data-ttu-id="07a6c-164">Para obtener más información, vea la sección Comentarios de [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="07a6c-164">For more information, see the Remarks section of [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span></span>

<span data-ttu-id="07a6c-165">Para obtener más información, consulte [llamar a un método de proveedor](calling-a-provider-method.md).</span><span class="sxs-lookup"><span data-stu-id="07a6c-165">For more information, see [Calling a Provider Method](calling-a-provider-method.md).</span></span>

> [!Note]  
> <span data-ttu-id="07a6c-166">Dado que la devolución de llamada al receptor podría no devolverse en el mismo nivel de autenticación que requiere el cliente, se recomienda usar semisincrónico en lugar de la comunicación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="07a6c-166">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="07a6c-167">Para obtener más información, consulte [llamar a un método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="07a6c-167">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

 

 
