---
title: MDM_RemoteWipe (clase)
description: La \_ clase RemoteWipe de MDM permite el borrado remoto de un dispositivo.
ms.assetid: 8c7c8705-8694-4ce3-ba21-ca610fe1f547
keywords:
- MDM_RemoteWipe (clase)
- MDM_RemoteWipe clase, descrita
topic_type:
- apiref
api_name:
- MDM_RemoteWipe
- MDM_RemoteWipe.InstanceID
- MDM_RemoteWipe.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ece626fca573e34cf938105f5e59b61e0585fd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078905"
---
# <a name="mdm_remotewipe-class"></a><span data-ttu-id="3232b-105">\_Clase RemoteWipe de MDM</span><span class="sxs-lookup"><span data-stu-id="3232b-105">MDM\_RemoteWipe class</span></span>

<span data-ttu-id="3232b-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="3232b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3232b-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="3232b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3232b-108">La **clase \_ RemoteWipe de MDM** permite el borrado remoto de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3232b-108">The **MDM\_RemoteWipe** class allows a remote wipe of a device.</span></span>

<span data-ttu-id="3232b-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="3232b-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3232b-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3232b-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_RemoteWipe
{
  string InstanceID;
  string ParentID;
};
```

## <a name="members"></a><span data-ttu-id="3232b-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="3232b-111">Members</span></span>

<span data-ttu-id="3232b-112">La **clase \_ RemoteWipe de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3232b-112">The **MDM\_RemoteWipe** class has these types of members:</span></span>

-   [<span data-ttu-id="3232b-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="3232b-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="3232b-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3232b-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3232b-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="3232b-115">Methods</span></span>

<span data-ttu-id="3232b-116">La **clase \_ RemoteWipe de MDM** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="3232b-116">The **MDM\_RemoteWipe** class has these methods.</span></span>



| <span data-ttu-id="3232b-117">Método</span><span class="sxs-lookup"><span data-stu-id="3232b-117">Method</span></span>                                              | <span data-ttu-id="3232b-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="3232b-118">Description</span></span>                                              |
|:----------------------------------------------------|:---------------------------------------------------------|
| [<span data-ttu-id="3232b-119">**doWipeMethod**</span><span class="sxs-lookup"><span data-stu-id="3232b-119">**doWipeMethod**</span></span>](mdm-remotewipe-dowipemethod.md) | <span data-ttu-id="3232b-120">Desencadena el dispositivo para iniciar el borrado remoto.</span><span class="sxs-lookup"><span data-stu-id="3232b-120">Triggers the device to start the remote wipe.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3232b-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3232b-121">Properties</span></span>

<span data-ttu-id="3232b-122">La **clase \_ RemoteWipe de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3232b-122">The **MDM\_RemoteWipe** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3232b-123">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3232b-123">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3232b-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3232b-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3232b-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3232b-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3232b-126">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3232b-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3232b-127">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="3232b-127">Identifies the name of the parent node.</span></span> <span data-ttu-id="3232b-128">Para esta clase, la cadena es "RemoteWipe".</span><span class="sxs-lookup"><span data-stu-id="3232b-128">For this class, the string is "RemoteWipe".</span></span>

</dd> <dt>

<span data-ttu-id="3232b-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="3232b-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3232b-130">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3232b-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3232b-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3232b-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3232b-132">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3232b-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3232b-133">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="3232b-133">Describes the full path to the parent node.</span></span> <span data-ttu-id="3232b-134">Para esta clase, la cadena es "./Vendor/MSFT/".</span><span class="sxs-lookup"><span data-stu-id="3232b-134">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="3232b-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3232b-135">Example</span></span>

<span data-ttu-id="3232b-136">En el ejemplo siguiente se muestra cómo usar RemoteWipe e invocar doWipeMethod.</span><span class="sxs-lookup"><span data-stu-id="3232b-136">The following example demonstrates how to use the RemoteWipe and invoke the doWipeMethod.</span></span>

> [!Note]  
> <span data-ttu-id="3232b-137">Este ejemplo debe ejecutarse en el usuario del sistema local.</span><span class="sxs-lookup"><span data-stu-id="3232b-137">This example must be executed under local system user.</span></span> <span data-ttu-id="3232b-138">Para ello, descargue la herramienta de PsExec desde <https://technet.microsoft.com/sysinternals/bb897553.aspx> y ejecute `psexec.exe -i -s cmd.exe` desde un símbolo del sistema de administrador con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="3232b-138">To do that, download the psexec tool from <https://technet.microsoft.com/sysinternals/bb897553.aspx> and run `psexec.exe -i -s cmd.exe` from an elevated admin command prompt.</span></span>

 

``` syntax
$namespaceName = "root\cimv2\mdm\dmmap"
$className = "MDM_RemoteWipe"
$methodName = "doWipeMethod"

$session = New-CimSession

$params = New-Object Microsoft.Management.Infrastructure.CimMethodParametersCollection
$param = [Microsoft.Management.Infrastructure.CimMethodParameter]::Create("param", "", "String", "In")
$params.Add($param)

try
{
    $instance = Get-CimInstance -Namespace $namespaceName -ClassName $className -Filter "ParentID='./Vendor/MSFT' and InstanceID='RemoteWipe'"
    $session.InvokeMethod($namespaceName, $instance, $methodName, $params)
}
catch [Exception]
{
    write-host $_ | out-string
}
```

## <a name="requirements"></a><span data-ttu-id="3232b-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3232b-139">Requirements</span></span>



| <span data-ttu-id="3232b-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="3232b-140">Requirement</span></span> | <span data-ttu-id="3232b-141">Value</span><span class="sxs-lookup"><span data-stu-id="3232b-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3232b-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3232b-142">Minimum supported client</span></span><br/> | <span data-ttu-id="3232b-143">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="3232b-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3232b-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3232b-144">Minimum supported server</span></span><br/> | <span data-ttu-id="3232b-145">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3232b-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="3232b-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3232b-146">Namespace</span></span><br/>                | <span data-ttu-id="3232b-147">DMMap de MDM raíz de \\ CIMv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="3232b-147">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="3232b-148">MOF</span><span class="sxs-lookup"><span data-stu-id="3232b-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3232b-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3232b-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3232b-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3232b-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3232b-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3232b-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3232b-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="3232b-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3232b-153">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="3232b-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

