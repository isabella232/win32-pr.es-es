---
description: Conceptualmente similar a un localizador uniforme de recursos (URL), una ruta de acceso de objeto WMI es una cadena que identifica de forma única el espacio de nombres en un servidor, una clase dentro de un espacio de nombres o instancias de una clase.
ms.assetid: 7a390541-609d-4b97-b91c-1a41d21ec17d
ms.tgt_platform: multiple
title: Describir la ubicación de un objeto WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b58b58a6b668955d6eba1e4c51f6f8dccdac890
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715832"
---
# <a name="describing-the-location-of-a-wmi-object"></a><span data-ttu-id="18c0f-103">Describir la ubicación de un objeto WMI</span><span class="sxs-lookup"><span data-stu-id="18c0f-103">Describing the Location of a WMI Object</span></span>

<span data-ttu-id="18c0f-104">Conceptualmente similar a un localizador uniforme de recursos (URL), una ruta de acceso de objeto WMI es una cadena que identifica de forma única el espacio de nombres en un servidor, una clase dentro de un espacio de nombres o instancias de una clase.</span><span class="sxs-lookup"><span data-stu-id="18c0f-104">Conceptually similar to a Uniform Resource Locator (URL), a WMI object path is a string that uniquely identifies the namespace on a server, a class within a namespace, or instances of a class.</span></span> <span data-ttu-id="18c0f-105">Una ruta de acceso de objeto es jerárquica y contiene varios elementos que describen la ubicación del objeto en cuestión.</span><span class="sxs-lookup"><span data-stu-id="18c0f-105">An object path is hierarchical, and contains several elements that describe the location of the object in question.</span></span> <span data-ttu-id="18c0f-106">Al igual que las rutas de acceso de archivo, las rutas de objeto WMI se pueden describir en su totalidad o se especifican como una ruta de acceso relativa.</span><span class="sxs-lookup"><span data-stu-id="18c0f-106">Like file paths, WMI object paths can be described in full or specified as a relative path.</span></span>

<span data-ttu-id="18c0f-107">El espacio de nombres de un objeto WMI se muestra en la página de referencia WMI.</span><span class="sxs-lookup"><span data-stu-id="18c0f-107">The namespace of a WMI object is listed on the WMI reference page.</span></span> <span data-ttu-id="18c0f-108">Por ejemplo, la ubicación de la mayoría de las clases admitidas por los [proveedores WMI de CIMWin32](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers) se encuentra en el \\ espacio de \\ nombres root cimv2.</span><span class="sxs-lookup"><span data-stu-id="18c0f-108">For example, the location of most of the classes supported by the [CIMWin32 WMI Providers](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers) are located in the \\root\\cimv2 namespace.</span></span> <span data-ttu-id="18c0f-109">El siguiente código de PowerShell describe una llamada para recuperar el objeto [**\_ ComputerSystem de Win32**](/windows/desktop/CIMWin32Prov/win32-computersystem) en el equipo local:</span><span class="sxs-lookup"><span data-stu-id="18c0f-109">The following PowerShell code describes a call to retrieve the [**Win32\_ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) object on your local machine:</span></span>

`Get-WmiObject -Class Win32_ComputerSystem -Namespace "root\cimv2" -ComputerName "."`

<span data-ttu-id="18c0f-110">Como alternativa, una instancia específica de [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) puede tener la siguiente ruta de acceso de la propiedad [**SWbemObject. Path \_**](swbemobject-path-.md) .</span><span class="sxs-lookup"><span data-stu-id="18c0f-110">Alternately, a specific instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) may have the following path from the [**SWbemObject.Path\_**](swbemobject-path-.md) property.</span></span>

`\\Machine1\root\cimv2:Win32_LogicalDisk.DeviceID="C:"`

<span data-ttu-id="18c0f-111">En el ejemplo siguiente se muestra la ruta de acceso relativa a esta instancia, tal como se muestra al mostrar la propiedad [**Relpath**](swbemobjectpath-relpath.md) del objeto [**SWbemObjectPath**](swbemobjectpath.md) devuelto por la llamada a [**SWbemObject. \_ path**](swbemobject-path-.md).</span><span class="sxs-lookup"><span data-stu-id="18c0f-111">The following example shows the relative path to this instance, as seen by displaying the [**Relpath**](swbemobjectpath-relpath.md) property of the [**SWbemObjectPath**](swbemobjectpath.md) object returned by the call to [**SWbemObject.Path\_**](swbemobject-path-.md).</span></span>

`Win32_LogicalDisk.DeviceID="A:"`

<span data-ttu-id="18c0f-112">Tenga en cuenta que **DeviceID** es la propiedad clave de la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="18c0f-112">Note that **DeviceID** is the key property of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>

## <a name="c"></a><span data-ttu-id="18c0f-113">C++</span><span class="sxs-lookup"><span data-stu-id="18c0f-113">C++</span></span>

<span data-ttu-id="18c0f-114">En la tabla siguiente se enumeran los tipos de ruta de acceso de objeto y los métodos asociados que requieren rutas de objeto.</span><span class="sxs-lookup"><span data-stu-id="18c0f-114">The following table lists object path types and the associated methods that require object paths.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="18c0f-115">Tipo de ruta de objeto</span><span class="sxs-lookup"><span data-stu-id="18c0f-115">Object path type</span></span></th>
<th><span data-ttu-id="18c0f-116">Método</span><span class="sxs-lookup"><span data-stu-id="18c0f-116">Method</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="18c0f-117"><a href="describing-a-wmi-namespace-object-path.md">Espacio de nombres</a></span><span class="sxs-lookup"><span data-stu-id="18c0f-117"><a href="describing-a-wmi-namespace-object-path.md">Namespace</a></span></span></td>
<td><dl><span data-ttu-id="18c0f-118"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-opennamespace"><strong>IWbemServices:: Opennamespace (</strong></a></span><span class="sxs-lookup"><span data-stu-id="18c0f-118"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-opennamespace"><strong>IWbemServices::OpenNamespace</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="18c0f-119"><a href="describing-a-class-object-path.md">Clase</a></span><span class="sxs-lookup"><span data-stu-id="18c0f-119"><a href="describing-a-class-object-path.md">Class</a></span></span></td>
<td><dl><span data-ttu-id="18c0f-120"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod"><strong>IWbemServices:: ExecMethod</strong></a></span><span class="sxs-lookup"><span data-stu-id="18c0f-120"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod"><strong>IWbemServices::ExecMethod</strong></a></span></span><br />
<span data-ttu-id="18c0f-121">[<strong>IWbemServices:: ExecMethodAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)</span><span class="sxs-lookup"><span data-stu-id="18c0f-121">[<strong>IWbemServices::ExecMethodAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="18c0f-122"><a href="describing-a-class-object-path.md">Clase</a> o <a href="describing-an-instance-object-path.md">instancia</a></span><span class="sxs-lookup"><span data-stu-id="18c0f-122"><a href="describing-a-class-object-path.md">Class</a> or <a href="describing-an-instance-object-path.md">Instance</a></span></span></td>
<td><dl><span data-ttu-id="18c0f-123"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject"><strong>IWbemServices:: GetObject</strong></a></span><span class="sxs-lookup"><span data-stu-id="18c0f-123"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject"><strong>IWbemServices::GetObject</strong></a></span></span><br />
<span data-ttu-id="18c0f-124">[<strong>IWbemServices:: GetObjectAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)</span><span class="sxs-lookup"><span data-stu-id="18c0f-124">[<strong>IWbemServices::GetObjectAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="18c0f-125"><a href="describing-an-instance-object-path.md">Instancia</a></span><span class="sxs-lookup"><span data-stu-id="18c0f-125"><a href="describing-an-instance-object-path.md">Instance</a></span></span></td>
<td><dl><span data-ttu-id="18c0f-126"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance"><strong>IWbemServices::D eleteInstance</strong></a></span><span class="sxs-lookup"><span data-stu-id="18c0f-126"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance"><strong>IWbemServices::DeleteInstance</strong></a></span></span><br />
<span data-ttu-id="18c0f-127">[<strong>IWbemServices::D eleteinstanceasync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)</span><span class="sxs-lookup"><span data-stu-id="18c0f-127">[<strong>IWbemServices::DeleteInstanceAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="script"></a><span data-ttu-id="18c0f-128">Script</span><span class="sxs-lookup"><span data-stu-id="18c0f-128">Script</span></span>

<span data-ttu-id="18c0f-129">Las rutas de acceso a objetos se pueden construir de varias maneras:</span><span class="sxs-lookup"><span data-stu-id="18c0f-129">Object paths can be constructed in several ways:</span></span>

-   <span data-ttu-id="18c0f-130">Recupere la propiedad de un método que devuelve un objeto [**SWbemObjectPath**](swbemobjectpath.md) .</span><span class="sxs-lookup"><span data-stu-id="18c0f-130">Retrieve the property of a method that returns an [**SWbemObjectPath**](swbemobjectpath.md) object.</span></span>
-   <span data-ttu-id="18c0f-131">Recupere la propiedad [**SWbemObject \_ . Path**](swbemobject-path-.md) .</span><span class="sxs-lookup"><span data-stu-id="18c0f-131">Retrieve the [**SWbemObject.Path\_**](swbemobject-path-.md) property.</span></span>
-   <span data-ttu-id="18c0f-132">Cree una variable de cadena que contenga la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="18c0f-132">Create a string variable that contains the object path.</span></span>

<span data-ttu-id="18c0f-133">En la tabla siguiente se enumeran los objetos de scripting que requieren rutas de objeto.</span><span class="sxs-lookup"><span data-stu-id="18c0f-133">The following table lists the scripting objects that require object paths.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="18c0f-134">Scripting (objeto)</span><span class="sxs-lookup"><span data-stu-id="18c0f-134">Scripting object</span></span></th>
<th><span data-ttu-id="18c0f-135">Método</span><span class="sxs-lookup"><span data-stu-id="18c0f-135">Method</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="18c0f-136"><a href="swbemservices.md"><strong>SWbemServices</strong></a></span><span class="sxs-lookup"><span data-stu-id="18c0f-136"><a href="swbemservices.md"><strong>SWbemServices</strong></a></span></span></td>
<td><dl><span data-ttu-id="18c0f-137"><a href="swbemservices-associatorsof.md"><strong>AssociatorsOf</strong></a></span><span class="sxs-lookup"><span data-stu-id="18c0f-137"><a href="swbemservices-associatorsof.md"><strong>AssociatorsOf</strong></a></span></span><br />
<span data-ttu-id="18c0f-138">[<strong>AssociatorsOfAsync</strong>] (swbemservices-associatorsofasync.md)</span><span class="sxs-lookup"><span data-stu-id="18c0f-138">[<strong>AssociatorsOfAsync</strong>](swbemservices-associatorsofasync.md)</span></span><br />
<span data-ttu-id="18c0f-139">[<strong>Eliminar</strong>] (swbemservices-delete.md)</span><span class="sxs-lookup"><span data-stu-id="18c0f-139">[<strong>Delete</strong>](swbemservices-delete.md)</span></span><br />
<span data-ttu-id="18c0f-140">[<strong>DeleteAsync</strong>] (swbemservices-deleteasync.md)</span><span class="sxs-lookup"><span data-stu-id="18c0f-140">[<strong>DeleteAsync</strong>](swbemservices-deleteasync.md)</span></span><br />
<span data-ttu-id="18c0f-141">[<strong>ExecMethod</strong>] (swbemservices-execmethod.md)</span><span class="sxs-lookup"><span data-stu-id="18c0f-141">[<strong>ExecMethod</strong>](swbemservices-execmethod.md)</span></span><br />
<span data-ttu-id="18c0f-142">[<strong>ExecMethodAsync</strong>] (swbemservices-execmethodasync.md)</span><span class="sxs-lookup"><span data-stu-id="18c0f-142">[<strong>ExecMethodAsync</strong>](swbemservices-execmethodasync.md)</span></span><br />
<span data-ttu-id="18c0f-143">[<strong>Obtener</strong>] (swbemservices-get.md)</span><span class="sxs-lookup"><span data-stu-id="18c0f-143">[<strong>Get</strong>](swbemservices-get.md)</span></span><br />
<span data-ttu-id="18c0f-144">[<strong>GetAsync</strong>] (swbemservices-getasync.md)</span><span class="sxs-lookup"><span data-stu-id="18c0f-144">[<strong>GetAsync</strong>](swbemservices-getasync.md)</span></span><br />
<span data-ttu-id="18c0f-145">[<strong>Referencias a</strong>] (swbemservices-referencesto.md)</span><span class="sxs-lookup"><span data-stu-id="18c0f-145">[<strong>ReferencesTo</strong>](swbemservices-referencesto.md)</span></span><br />
<span data-ttu-id="18c0f-146">[<strong>ReferencesToAsync</strong>] (swbemservices-referencestoasync.md)</span><span class="sxs-lookup"><span data-stu-id="18c0f-146">[<strong>ReferencesToAsync</strong>](swbemservices-referencestoasync.md)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="18c0f-147"><a href="swbemobjectset.md"><strong>SWbemObjectSet</strong></a></span><span class="sxs-lookup"><span data-stu-id="18c0f-147"><a href="swbemobjectset.md"><strong>SWbemObjectSet</strong></a></span></span></td>
<td><dl><span data-ttu-id="18c0f-148"><a href="swbemobjectset-item.md"><strong>Elemento</strong></a></span><span class="sxs-lookup"><span data-stu-id="18c0f-148"><a href="swbemobjectset-item.md"><strong>Item</strong></a></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

 

 
