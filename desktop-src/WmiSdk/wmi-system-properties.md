---
description: Instrumental de administración de Windows (WMI) define un conjunto de propiedades del sistema que se asocian a todas las clases e instancias de clases.
ms.assetid: e812c0cb-3e08-4cac-8d05-2cd7abc922d1
ms.tgt_platform: multiple
title: Propiedades del sistema WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3ee541d9de0d37c9aa1eae4ded07d3cb70ff1bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276247"
---
# <a name="wmi-system-properties"></a><span data-ttu-id="aaf90-103">Propiedades del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="aaf90-103">WMI System Properties</span></span>

<span data-ttu-id="aaf90-104">Instrumental de administración de Windows (WMI) define un conjunto de propiedades del sistema que se asocian a todas las clases e instancias de clases.</span><span class="sxs-lookup"><span data-stu-id="aaf90-104">Windows Management Instrumentation (WMI) defines a set of system properties that are associated with all classes and instances of classes.</span></span> <span data-ttu-id="aaf90-105">Al igual que con las clases del sistema, los nombres de propiedad del sistema comienzan con un carácter de subrayado doble, para distinguirlos de las propiedades creadas por aplicaciones o proveedores que no deben comenzar por un carácter de subrayado simple o doble.</span><span class="sxs-lookup"><span data-stu-id="aaf90-105">As with system classes, system property names begin with a double underscore, distinguishing them from properties created by applications or providers that must not start with a single or double underscore.</span></span> <span data-ttu-id="aaf90-106">Otra manera de identificar una propiedad del sistema es usar el método [**IWbemClassObject:: get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) .</span><span class="sxs-lookup"><span data-stu-id="aaf90-106">Another way to identify a system property is to use the [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) method.</span></span>

<span data-ttu-id="aaf90-107">Las propiedades del sistema están disponibles en cualquier momento, pero los valores pueden ser **null**.</span><span class="sxs-lookup"><span data-stu-id="aaf90-107">System properties are available at any time, but values might be **NULL**.</span></span> <span data-ttu-id="aaf90-108">**Null** indica que una propiedad no se aplica a un objeto concreto.</span><span class="sxs-lookup"><span data-stu-id="aaf90-108">**NULL** indicates a property does not apply to a specific object.</span></span> <span data-ttu-id="aaf90-109">Sin embargo, es posible que las propiedades del sistema no estén disponibles en todo momento para todas las clases o instancias.</span><span class="sxs-lookup"><span data-stu-id="aaf90-109">However, system properties might not be available all the time for all classes or instances.</span></span>

## <a name="system-properties"></a><span data-ttu-id="aaf90-110">Propiedades del sistema</span><span class="sxs-lookup"><span data-stu-id="aaf90-110">System Properties</span></span>

<span data-ttu-id="aaf90-111">En la lista siguiente se describen las propiedades del sistema WMI.</span><span class="sxs-lookup"><span data-stu-id="aaf90-111">The following list describes the WMI system properties.</span></span> <span data-ttu-id="aaf90-112">Los ejemplos proporcionados se toman de las propiedades del sistema de la clase [**\_ OptionalFeature de Win32**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) , que se describe en la parte inferior de este tema.</span><span class="sxs-lookup"><span data-stu-id="aaf90-112">The examples given are taken from the system properties of the [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) class, which is described at the bottom of this topic.</span></span>

<dl> <dt>

<span data-ttu-id="aaf90-113"><span id="__Class"></span><span id="__class"></span><span id="__CLASS"></span>**\_\_Las**</span><span class="sxs-lookup"><span data-stu-id="aaf90-113"><span id="__Class"></span><span id="__class"></span><span id="__CLASS"></span>**\_\_Class**</span></span>
</dt> <dd>

<span data-ttu-id="aaf90-114">Tipo de datos **: \_ cadena CIM**</span><span class="sxs-lookup"><span data-stu-id="aaf90-114">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="aaf90-115">Tipo de acceso: solo lectura para instancias; lectura/escritura para clases</span><span class="sxs-lookup"><span data-stu-id="aaf90-115">Access type: Read-only for instances; read/write for classes</span></span>

<span data-ttu-id="aaf90-116">Nombre de la clase.</span><span class="sxs-lookup"><span data-stu-id="aaf90-116">The name of the class.</span></span>

<span data-ttu-id="aaf90-117">Ejemplo: Win32 \_ OptionalFeature</span><span class="sxs-lookup"><span data-stu-id="aaf90-117">Example: Win32\_OptionalFeature</span></span>

</dd> <dt>

<span data-ttu-id="aaf90-118"><span id="__Derivation"></span><span id="__derivation"></span><span id="__DERIVATION"></span>**\_\_Deriva**</span><span class="sxs-lookup"><span data-stu-id="aaf90-118"><span id="__Derivation"></span><span id="__derivation"></span><span id="__DERIVATION"></span>**\_\_Derivation**</span></span>
</dt> <dd>

<span data-ttu-id="aaf90-119">Tipo de datos: matriz de **\_ cadenas CIM**</span><span class="sxs-lookup"><span data-stu-id="aaf90-119">Data type: **CIM\_STRING** array</span></span>

<span data-ttu-id="aaf90-120">Tipo de acceso: solo lectura para instancias y clases</span><span class="sxs-lookup"><span data-stu-id="aaf90-120">Access type: Read-only for both instances and classes</span></span>

<span data-ttu-id="aaf90-121">Jerarquía de clases de la clase o instancia actual.</span><span class="sxs-lookup"><span data-stu-id="aaf90-121">Class hierarchy of the current class or instance.</span></span> <span data-ttu-id="aaf90-122">El primer elemento es la clase primaria inmediata, el siguiente es su elemento primario, y así sucesivamente; el último elemento es la clase base.</span><span class="sxs-lookup"><span data-stu-id="aaf90-122">The first element is the immediate parent class, the next is its parent, and so on; the last element is the base class.</span></span>

<span data-ttu-id="aaf90-123">Ejemplo: {CIM \_ LogicalElement, CIM \_ ManagedSystemElement}</span><span class="sxs-lookup"><span data-stu-id="aaf90-123">Example: {CIM\_LogicalElement, CIM\_ManagedSystemElement}</span></span>

</dd> <dt>

<span data-ttu-id="aaf90-124"><span id="__Dynasty"></span><span id="__dynasty"></span><span id="__DYNASTY"></span>**\_\_Dynasty**</span><span class="sxs-lookup"><span data-stu-id="aaf90-124"><span id="__Dynasty"></span><span id="__dynasty"></span><span id="__DYNASTY"></span>**\_\_Dynasty**</span></span>
</dt> <dd>

<span data-ttu-id="aaf90-125">Tipo de datos **: \_ cadena CIM**</span><span class="sxs-lookup"><span data-stu-id="aaf90-125">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="aaf90-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aaf90-126">Access type: Read-only</span></span>

<span data-ttu-id="aaf90-127">Nombre de la clase de nivel superior de la que se deriva la clase o la instancia.</span><span class="sxs-lookup"><span data-stu-id="aaf90-127">Name of the top-level class from which the class or instance is derived.</span></span> <span data-ttu-id="aaf90-128">Cuando esta clase o instancia es la clase de nivel superior, los valores de **\_ \_ Dynasty** y **\_ \_ Class** son los mismos.</span><span class="sxs-lookup"><span data-stu-id="aaf90-128">When this class or instance is the top-level class, the values of **\_\_Dynasty** and **\_\_Class** are the same.</span></span>

<span data-ttu-id="aaf90-129">Ejemplo: el \_ ManagedSystemElement de CIM</span><span class="sxs-lookup"><span data-stu-id="aaf90-129">Example: CIM\_ManagedSystemElement</span></span>

</dd> <dt>

<span data-ttu-id="aaf90-130"><span id="__Genus"></span><span id="__genus"></span><span id="__GENUS"></span>**\_\_Género**</span><span class="sxs-lookup"><span data-stu-id="aaf90-130"><span id="__Genus"></span><span id="__genus"></span><span id="__GENUS"></span>**\_\_Genus**</span></span>
</dt> <dd>

<span data-ttu-id="aaf90-131">Tipo de datos: **CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="aaf90-131">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="aaf90-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aaf90-132">Access type: Read-only</span></span>

<span data-ttu-id="aaf90-133">Valor que se usa para distinguir entre clases e instancias.</span><span class="sxs-lookup"><span data-stu-id="aaf90-133">Value that is used to distinguish between classes and instances.</span></span> <span data-ttu-id="aaf90-134">Este valor es **la \_ \_ clase de género de WBEM** (1) para las clases y la **\_ \_ instancia de género de WBEM** (2) para instancias y eventos.</span><span class="sxs-lookup"><span data-stu-id="aaf90-134">This value is **WBEM\_GENUS\_CLASS** (1) for classes, and **WBEM\_GENUS\_INSTANCE** (2) for instances and events.</span></span>

<span data-ttu-id="aaf90-135">Ejemplo: 2</span><span class="sxs-lookup"><span data-stu-id="aaf90-135">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="aaf90-136"><span id="__Namespace"></span><span id="__namespace"></span><span id="__NAMESPACE"></span>[**\_\_System.IO**](--namespace.md)</span><span class="sxs-lookup"><span data-stu-id="aaf90-136"><span id="__Namespace"></span><span id="__namespace"></span><span id="__NAMESPACE"></span>[**\_\_Namespace**](--namespace.md)</span></span>
</dt> <dd>

<span data-ttu-id="aaf90-137">Tipo de datos **: \_ cadena CIM**</span><span class="sxs-lookup"><span data-stu-id="aaf90-137">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="aaf90-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aaf90-138">Access type: Read-only</span></span>

<span data-ttu-id="aaf90-139">Nombre del [*espacio de nombres*](gloss-n.md) de la clase o la instancia.</span><span class="sxs-lookup"><span data-stu-id="aaf90-139">Name of the [*namespace*](gloss-n.md) of the class or instance.</span></span>

<span data-ttu-id="aaf90-140">Ejemplo: raíz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="aaf90-140">Example: root\\cimv2</span></span>

</dd> <dt>

<span data-ttu-id="aaf90-141"><span id="__Path"></span><span id="__path"></span><span id="__PATH"></span>**\_\_Camino**</span><span class="sxs-lookup"><span data-stu-id="aaf90-141"><span id="__Path"></span><span id="__path"></span><span id="__PATH"></span>**\_\_Path**</span></span>
</dt> <dd>

<span data-ttu-id="aaf90-142">Tipo de datos **: \_ cadena CIM**</span><span class="sxs-lookup"><span data-stu-id="aaf90-142">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="aaf90-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aaf90-143">Access type: Read-only</span></span>

<span data-ttu-id="aaf90-144">Ruta de acceso completa a la clase o instancia, incluido el servidor y el espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="aaf90-144">Full path to the class or instance—including server and namespace.</span></span>

<span data-ttu-id="aaf90-145">Ejemplo: \\ \\ servidor \\ raíz \\ cimv2: Win32 \_ OptionalFeature. Name = "TelnetClient"</span><span class="sxs-lookup"><span data-stu-id="aaf90-145">Example: \\\\MyServer\\root\\cimv2:Win32\_OptionalFeature.Name="TelnetClient"</span></span>

</dd> <dt>

<span data-ttu-id="aaf90-146"><span id="__Property_Count"></span><span id="__property_count"></span><span id="__PROPERTY_COUNT"></span>**\_\_Recuento de propiedades \_**</span><span class="sxs-lookup"><span data-stu-id="aaf90-146"><span id="__Property_Count"></span><span id="__property_count"></span><span id="__PROPERTY_COUNT"></span>**\_\_Property\_Count**</span></span>
</dt> <dd>

<span data-ttu-id="aaf90-147">Tipo de datos: **CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="aaf90-147">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="aaf90-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aaf90-148">Access type: Read-only</span></span>

<span data-ttu-id="aaf90-149">Número de propiedades no del sistema definidas para la clase o la instancia.</span><span class="sxs-lookup"><span data-stu-id="aaf90-149">Number of nonsystem properties defined for the class or instance.</span></span>

<span data-ttu-id="aaf90-150">Ejemplo: 6</span><span class="sxs-lookup"><span data-stu-id="aaf90-150">Example: 6</span></span>

</dd> <dt>

<span data-ttu-id="aaf90-151"><span id="__Relpath"></span><span id="__relpath"></span><span id="__RELPATH"></span>**\_\_Relpath**</span><span class="sxs-lookup"><span data-stu-id="aaf90-151"><span id="__Relpath"></span><span id="__relpath"></span><span id="__RELPATH"></span>**\_\_Relpath**</span></span>
</dt> <dd>

<span data-ttu-id="aaf90-152">Tipo de datos **: \_ cadena CIM**</span><span class="sxs-lookup"><span data-stu-id="aaf90-152">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="aaf90-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aaf90-153">Access type: Read-only</span></span>

<span data-ttu-id="aaf90-154">Ruta de acceso relativa a la clase o instancia.</span><span class="sxs-lookup"><span data-stu-id="aaf90-154">Relative path to the class or instance.</span></span>

<span data-ttu-id="aaf90-155">Ejemplo: Win32 \_ OptionalFeature. Name = "TelnetClient"</span><span class="sxs-lookup"><span data-stu-id="aaf90-155">Example: Win32\_OptionalFeature.Name="TelnetClient"</span></span>

</dd> <dt>

<span data-ttu-id="aaf90-156"><span id="__Server"></span><span id="__server"></span><span id="__SERVER"></span>**\_\_Servidor**</span><span class="sxs-lookup"><span data-stu-id="aaf90-156"><span id="__Server"></span><span id="__server"></span><span id="__SERVER"></span>**\_\_Server**</span></span>
</dt> <dd>

<span data-ttu-id="aaf90-157">Tipo de datos **: \_ cadena CIM**</span><span class="sxs-lookup"><span data-stu-id="aaf90-157">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="aaf90-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aaf90-158">Access type: Read-only</span></span>

<span data-ttu-id="aaf90-159">Nombre del servidor que proporciona la clase o la instancia.</span><span class="sxs-lookup"><span data-stu-id="aaf90-159">Name of the server supplying the class or instance.</span></span>

<span data-ttu-id="aaf90-160">Ejemplo: mi Server</span><span class="sxs-lookup"><span data-stu-id="aaf90-160">Example: MyServer</span></span>

</dd> <dt>

<span data-ttu-id="aaf90-161"><span id="__Superclass"></span><span id="__superclass"></span><span id="__SUPERCLASS"></span>**\_\_Dados**</span><span class="sxs-lookup"><span data-stu-id="aaf90-161"><span id="__Superclass"></span><span id="__superclass"></span><span id="__SUPERCLASS"></span>**\_\_Superclass**</span></span>
</dt> <dd>

<span data-ttu-id="aaf90-162">Tipo de datos **: \_ cadena CIM**</span><span class="sxs-lookup"><span data-stu-id="aaf90-162">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="aaf90-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aaf90-163">Access type: Read-only</span></span>

<span data-ttu-id="aaf90-164">Nombre de la clase primaria inmediata de la clase o instancia.</span><span class="sxs-lookup"><span data-stu-id="aaf90-164">Name of the immediate parent class of the class or instance.</span></span>

<span data-ttu-id="aaf90-165">Ejemplo: CIM \_ LogicalElement</span><span class="sxs-lookup"><span data-stu-id="aaf90-165">Example: CIM\_LogicalElement</span></span>

</dd> </dl>

<span data-ttu-id="aaf90-166">El siguiente código de PowerShell recupera las propiedades de la [**clase \_ OptionalFeature de Win32**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) , que incluye las propiedades del sistema.</span><span class="sxs-lookup"><span data-stu-id="aaf90-166">The following PowerShell code retrieves the properties of the [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) class, which includes the system properties.</span></span>


```PowerShell
Get-WmiObject win32_OptionalFeature | Where-Object {$_.name -eq "TelnetClient"}
```



<span data-ttu-id="aaf90-167">El ejemplo de código anterior devuelve lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="aaf90-167">The previous code sample returns the following:</span></span>


```PowerShell
__GENUS          : 2
__CLASS          : Win32_OptionalFeature
__SUPERCLASS     : CIM_LogicalElement
__DYNASTY        : CIM_ManagedSystemElement
__RELPATH        : Win32_OptionalFeature.Name="TelnetClient"
__PROPERTY_COUNT : 6
__DERIVATION     : {CIM_LogicalElement, CIM_ManagedSystemElement}
__SERVER         : myServer
__NAMESPACE      : root\cimv2
__PATH           : \\myServer\root\cimv2:Win32_OptionalFeature.Name="TelnetClient"
Caption          : Telnet Client
Description      : 
InstallDate      : 
InstallState     : 2
Name             : TelnetClient
Status           : 
PSComputerName   : myServer
```



 

 
