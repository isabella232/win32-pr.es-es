---
description: Puede obtener o modificar los datos del registro mediante la clase StdRegProv de WMI y sus métodos.
ms.assetid: 7cba9dcb-741b-4118-9769-8830c6dc0752
ms.tgt_platform: multiple
title: Obtener datos del registro
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f5468a577acedeccf4396607147428d9160b4d38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705437"
---
# <a name="obtaining-registry-data"></a><span data-ttu-id="a3d40-103">Obtener datos del registro</span><span class="sxs-lookup"><span data-stu-id="a3d40-103">Obtaining Registry Data</span></span>

<span data-ttu-id="a3d40-104">Puede obtener o modificar los datos del registro mediante la clase [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) de WMI y sus métodos.</span><span class="sxs-lookup"><span data-stu-id="a3d40-104">You can obtain or modify registry data by using the WMI [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) class and its methods.</span></span> <span data-ttu-id="a3d40-105">Aunque use la utilidad regedit para ver y cambiar los valores del registro en el equipo local, **StdRegProv** le permite usar un script o una aplicación para automatizar dichas actividades en el equipo local y en los equipos remotos.</span><span class="sxs-lookup"><span data-stu-id="a3d40-105">While use the Regedit utility to view and change registry values on the local computer, **StdRegProv** allows you to use a script or application to automate such activities on the local computer and remote computers.</span></span>

<span data-ttu-id="a3d40-106">[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) contiene métodos para hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a3d40-106">[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) contains methods to do the following:</span></span>

-   <span data-ttu-id="a3d40-107">Comprobar los permisos de acceso de un usuario</span><span class="sxs-lookup"><span data-stu-id="a3d40-107">Verify the access permissions for a user</span></span>
-   <span data-ttu-id="a3d40-108">Crear, enumerar y eliminar claves del registro</span><span class="sxs-lookup"><span data-stu-id="a3d40-108">Create, enumerate, and delete registry keys</span></span>
-   <span data-ttu-id="a3d40-109">Crear, enumerar y eliminar subclaves o valores con nombre</span><span class="sxs-lookup"><span data-stu-id="a3d40-109">Create, enumerate, and delete subkeys or named values</span></span>
-   <span data-ttu-id="a3d40-110">Leer, escribir y eliminar valores de datos</span><span class="sxs-lookup"><span data-stu-id="a3d40-110">Read, write, and delete data values</span></span>

<span data-ttu-id="a3d40-111">Los datos del registro se organizan por subárboles, claves y subclaves anidadas bajo una clave de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="a3d40-111">Registry data is organized by subtrees, keys, and subkeys nested under a top level key.</span></span> <span data-ttu-id="a3d40-112">Los valores de datos reales se denominan entradas o valores con nombre.</span><span class="sxs-lookup"><span data-stu-id="a3d40-112">The actual data values are called entries or named values.</span></span>

<span data-ttu-id="a3d40-113">Entre los subárboles se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="a3d40-113">The subtrees include the following:</span></span>

-   <span data-ttu-id="a3d40-114">**HKEY \_ CLASSes \_ root** (abreviado como **HKCR**)</span><span class="sxs-lookup"><span data-stu-id="a3d40-114">**HKEY\_CLASSES\_ROOT** (abbreviated as **HKCR**)</span></span>
-   <span data-ttu-id="a3d40-115">**HKEY \_ \_usuario actual** (**HKCU**)</span><span class="sxs-lookup"><span data-stu-id="a3d40-115">**HKEY\_CURRENT\_USER** (**HKCU**)</span></span>
-   <span data-ttu-id="a3d40-116">**HKEY \_ \_máquina local** (**HKLM**)</span><span class="sxs-lookup"><span data-stu-id="a3d40-116">**HKEY\_LOCAL\_MACHINE** (**HKLM**)</span></span>
-   <span data-ttu-id="a3d40-117">**\_usuarios HKEY**</span><span class="sxs-lookup"><span data-stu-id="a3d40-117">**HKEY\_USERS**</span></span>
-   <span data-ttu-id="a3d40-118">**HKEY \_ \_ configuración actual**</span><span class="sxs-lookup"><span data-stu-id="a3d40-118">**HKEY\_CURRENT\_CONFIG**</span></span>

<span data-ttu-id="a3d40-119">Por ejemplo, en la entrada del **registro HKEY** \\ **software** \\ **Microsoft** \\ **DirectX** \\ **InstalledVersion**, el subárbol HKEY **es software**; las subclaves son **Microsoft** y **DirectX**, y la entrada de valor con nombre es **InstalledVersion**.</span><span class="sxs-lookup"><span data-stu-id="a3d40-119">For example, in the registry entry **HKEY**\\**SOFTWARE**\\**Microsoft**\\**DirectX**\\**InstalledVersion**, the HKEY subtree is **SOFTWARE**; the subkeys are **Microsoft** and **DirectX**; and the named value entry is **InstalledVersion**.</span></span>

<span data-ttu-id="a3d40-120">Un [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) se produce cuando se produce un cambio en una clave específica, pero la entrada no identifica el modo en que cambian los valores ni los cambios por debajo de la clave especificada.</span><span class="sxs-lookup"><span data-stu-id="a3d40-120">A [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) occurs when a change to a specific key occurs, but the entry does not identify how the values change nor will this event be triggered by changes below the specified key.</span></span> <span data-ttu-id="a3d40-121">Para identificar los cambios en cualquier parte de una estructura jerárquica de claves, use [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent), que no devuelve valores específicos o cambios clave que se producen.</span><span class="sxs-lookup"><span data-stu-id="a3d40-121">To identify changes anywhere in a hierarchical key structure, use the [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent), which does not return specific values or key changes that occur.</span></span> <span data-ttu-id="a3d40-122">Para obtener un cambio de valor de entrada específico, use [**RegistryValueChangeEvent**](/previous-versions/windows/desktop/regprov/registryvaluechangeevent)y, a continuación, lea la entrada para obtener un valor de línea base.</span><span class="sxs-lookup"><span data-stu-id="a3d40-122">To obtain a specific entry value change, use the [**RegistryValueChangeEvent**](/previous-versions/windows/desktop/regprov/registryvaluechangeevent), and then read the entry to obtain a baseline value.</span></span>

<span data-ttu-id="a3d40-123">[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) solo tiene métodos a los que se puede llamar desde C++ o script, que es diferente de la estructura de clase Win32.</span><span class="sxs-lookup"><span data-stu-id="a3d40-123">[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) only has methods that can be called from C++ or script, which is different from the Win32 class structure.</span></span>

<span data-ttu-id="a3d40-124">En el ejemplo de código siguiente se muestra cómo usar el método [**StdRegProv. enumKey**](/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov) para enumerar todas las subclaves de software de Microsoft en la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="a3d40-124">The following code example shows how to use the [**StdRegProv.EnumKey**](/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov) method to list all of the Microsoft software subkeys under the registry key.</span></span>

<span data-ttu-id="a3d40-125">**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft**</span><span class="sxs-lookup"><span data-stu-id="a3d40-125">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**</span></span>


```VB
const HKEY_LOCAL_MACHINE = &H80000002
strComputer = "."

Set objReg=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\default:StdRegProv")

strKeyPath = "SOFTWARE\Microsoft"
objReg.EnumKey HKEY_LOCAL_MACHINE, strKeyPath, arrSubKeys

For Each subkey In arrSubKeys
Wscript.Echo subkey
    
Next
```


```PowerShell

$HKEY_LOCAL_MACHINE = 2147483650
$strKeyPath = &quot;SOFTWARE\Microsoft&quot;

$objReg = [WMIClass]&quot;root\default:StdRegProv&quot;

$arrSubKeys = $objReg.EnumKey($HKEY_LOCAL_MACHINE, $strKeyPath)
foreach ($subKey in ($arrSubKeys.sNames))
{
    $subKey
}
```





<span data-ttu-id="a3d40-126">[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) tiene distintos métodos para leer los distintos tipos de datos del valor de entrada del registro.</span><span class="sxs-lookup"><span data-stu-id="a3d40-126">[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) has different methods for reading the various registry entry value data types.</span></span> <span data-ttu-id="a3d40-127">Si la entrada tiene valores desconocidos, puede llamar a [**StdRegProv. EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) para enumerarlos.</span><span class="sxs-lookup"><span data-stu-id="a3d40-127">If the entry has unknown values, then you can call [**StdRegProv.EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) to list them.</span></span> <span data-ttu-id="a3d40-128">En la tabla siguiente se muestra la correspondencia entre los métodos **StdRegProv** y los tipos de datos de.</span><span class="sxs-lookup"><span data-stu-id="a3d40-128">The following table lists the correspondence between **StdRegProv** methods and the data types.</span></span>



| <span data-ttu-id="a3d40-129">Método</span><span class="sxs-lookup"><span data-stu-id="a3d40-129">Method</span></span>                                                                                  | <span data-ttu-id="a3d40-130">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a3d40-130">Data Type</span></span>           |
|-----------------------------------------------------------------------------------------|---------------------|
| [<span data-ttu-id="a3d40-131">**GetBinaryValue**</span><span class="sxs-lookup"><span data-stu-id="a3d40-131">**GetBinaryValue**</span></span>](/previous-versions/windows/desktop/regprov/getbinaryvalue-method-in-class-stdregprov)                 | <span data-ttu-id="a3d40-132">**\_binario de reg**</span><span class="sxs-lookup"><span data-stu-id="a3d40-132">**REG\_BINARY**</span></span>     |
| [<span data-ttu-id="a3d40-133">**GetDWORDValue**</span><span class="sxs-lookup"><span data-stu-id="a3d40-133">**GetDWORDValue**</span></span>](/previous-versions/windows/desktop/regprov/getdwordvalue-method-in-class-stdregprov)                   | <span data-ttu-id="a3d40-134">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="a3d40-134">**REG\_DWORD**</span></span>      |
| [<span data-ttu-id="a3d40-135">**GetExpandedStringValue**</span><span class="sxs-lookup"><span data-stu-id="a3d40-135">**GetExpandedStringValue**</span></span>](/previous-versions/windows/desktop/regprov/getexpandedstringvalue-method-in-class-stdregprov) | <span data-ttu-id="a3d40-136">**REG \_ expandir \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="a3d40-136">**REG\_EXPAND\_SZ**</span></span> |
| [<span data-ttu-id="a3d40-137">**GetMultiStringValue**</span><span class="sxs-lookup"><span data-stu-id="a3d40-137">**GetMultiStringValue**</span></span>](/previous-versions/windows/desktop/regprov/getmultistringvalue-method-in-class-stdregprov)       | <span data-ttu-id="a3d40-138">**REG \_ multi \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="a3d40-138">**REG\_MULTI\_SZ**</span></span>  |
| [<span data-ttu-id="a3d40-139">**GetStringValue**</span><span class="sxs-lookup"><span data-stu-id="a3d40-139">**GetStringValue**</span></span>](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov)                 | <span data-ttu-id="a3d40-140">**Registro \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="a3d40-140">**REG\_SZ**</span></span>         |



 

<span data-ttu-id="a3d40-141">En la tabla siguiente se enumeran los métodos correspondientes para crear nuevas claves o valores, o cambiar los existentes.</span><span class="sxs-lookup"><span data-stu-id="a3d40-141">The following table lists the corresponding methods for creating new keys or values, or changing existing ones.</span></span>



| <span data-ttu-id="a3d40-142">Método</span><span class="sxs-lookup"><span data-stu-id="a3d40-142">Method</span></span>                                                                                  | <span data-ttu-id="a3d40-143">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a3d40-143">Data Type</span></span>           |
|-----------------------------------------------------------------------------------------|---------------------|
| [<span data-ttu-id="a3d40-144">**SetBinaryValue**</span><span class="sxs-lookup"><span data-stu-id="a3d40-144">**SetBinaryValue**</span></span>](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov)                 | <span data-ttu-id="a3d40-145">**\_binario de reg**</span><span class="sxs-lookup"><span data-stu-id="a3d40-145">**REG\_BINARY**</span></span>     |
| [<span data-ttu-id="a3d40-146">**SetDWORDValue**</span><span class="sxs-lookup"><span data-stu-id="a3d40-146">**SetDWORDValue**</span></span>](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov)                   | <span data-ttu-id="a3d40-147">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="a3d40-147">**REG\_DWORD**</span></span>      |
| [<span data-ttu-id="a3d40-148">**SetExpandedStringValue**</span><span class="sxs-lookup"><span data-stu-id="a3d40-148">**SetExpandedStringValue**</span></span>](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov) | <span data-ttu-id="a3d40-149">**REG \_ expandir \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="a3d40-149">**REG\_EXPAND\_SZ**</span></span> |
| [<span data-ttu-id="a3d40-150">**SetMultiStringValue**</span><span class="sxs-lookup"><span data-stu-id="a3d40-150">**SetMultiStringValue**</span></span>](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov)       | <span data-ttu-id="a3d40-151">**REG \_ multi \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="a3d40-151">**REG\_MULTI\_SZ**</span></span>  |
| [<span data-ttu-id="a3d40-152">**SetStringValue**</span><span class="sxs-lookup"><span data-stu-id="a3d40-152">**SetStringValue**</span></span>](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov)                 | <span data-ttu-id="a3d40-153">**Registro \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="a3d40-153">**REG\_SZ**</span></span>         |



 

<span data-ttu-id="a3d40-154">En el ejemplo siguiente se muestra cómo leer la lista de orígenes del registro de eventos del sistema desde la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="a3d40-154">The following example shows how to read the list of sources for the system event log from the registry key.</span></span>

<span data-ttu-id="a3d40-155">**HKEY \_ \_** \\ **Sistema del** equipo local \\ **control actual** del sistema de registro de \\  \\ **eventos** \\  de servicios</span><span class="sxs-lookup"><span data-stu-id="a3d40-155">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**Current Control Set**\\**Services**\\**Eventlog**\\**System**</span></span>

<span data-ttu-id="a3d40-156">Tenga en cuenta que los elementos del valor de cadena multistring se tratan como una colección o una matriz.</span><span class="sxs-lookup"><span data-stu-id="a3d40-156">Note that the items in the multistring value are treated as a collection or array.</span></span>


```VB
const HKEY_LOCAL_MACHINE = &H80000002
strComputer = "."

Set objReg=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" _ 
    & strComputer & "\root\default:StdRegProv")

strKeyPath = "SOFTWARE\Microsoft"
objReg.EnumKey HKEY_LOCAL_MACHINE, strKeyPath, arrSubKeys

For Each subkey In arrSubKeys
Wscript.Echo subkey
    
Next
```



<span data-ttu-id="a3d40-157">El proveedor del registro se hospeda en LocalService, no en LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="a3d40-157">The registry provider is hosted in LocalService—not the LocalSystem.</span></span> <span data-ttu-id="a3d40-158">Por lo tanto, no es posible obtener información de forma remota desde el subárbol **HKEY \_ Current \_ User** .</span><span class="sxs-lookup"><span data-stu-id="a3d40-158">Therefore, obtaining information remotely from the subtree **HKEY\_CURRENT\_USER** is not possible.</span></span> <span data-ttu-id="a3d40-159">Sin embargo, los scripts que se ejecutan en el equipo local todavía pueden tener acceso a **HKEY \_ Current \_ User**.</span><span class="sxs-lookup"><span data-stu-id="a3d40-159">However, scripts run on the local computer can still access **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="a3d40-160">Puede establecer el modelo de hospedaje en LocalSystem en un equipo remoto, pero esto es un riesgo para la seguridad porque el registro del equipo remoto es vulnerable al acceso hostil.</span><span class="sxs-lookup"><span data-stu-id="a3d40-160">You can set the hosting model to LocalSystem on a remote machine, but that is a security risk because the registry on the remote machine is vulnerable to hostile access.</span></span> <span data-ttu-id="a3d40-161">Para obtener más información, vea [hospedaje y seguridad de proveedores](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="a3d40-161">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a3d40-162">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a3d40-162">Examples</span></span>

<span data-ttu-id="a3d40-163">En el ejemplo de código de VBScript [leer un valor de registro binario](https://Gallery.TechNet.Microsoft.Com/b0724cb2-36ed-4d0d-8b8f-428d0e3d0b82) en la galería de TechNet se usa WMI para leer un valor del registro binario.</span><span class="sxs-lookup"><span data-stu-id="a3d40-163">The [Read a Binary Registry Value](https://Gallery.TechNet.Microsoft.Com/b0724cb2-36ed-4d0d-8b8f-428d0e3d0b82) VBScript code example on TechNet Gallery uses WMI to read a binary registry value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3d40-164">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a3d40-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3d40-165">Tareas WMI: registro</span><span class="sxs-lookup"><span data-stu-id="a3d40-165">WMI Tasks: Registry</span></span>](wmi-tasks--registry.md)
</dt> </dl>

 

 
