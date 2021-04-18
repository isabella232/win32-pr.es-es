---
description: 'La clase de proveedor del registro del sistema StdRegProv para WMI tiene métodos que hacen lo siguiente:'
ms.assetid: d42248b3-2f96-4771-aee9-a0db139b149e
ms.tgt_platform: multiple
title: Cambio de los datos del Registro
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7b51f3f18eb718dab7c79f31a4b2188dd7afa529
ms.sourcegitcommit: 3d9eb6638763fee8b87c378657458f814182e36c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105717337"
---
# <a name="changing-registry-data"></a><span data-ttu-id="3e367-103">Cambio de los datos del Registro</span><span class="sxs-lookup"><span data-stu-id="3e367-103">Changing Registry Data</span></span>

<span data-ttu-id="3e367-104">La clase de [proveedor del registro del sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) para WMI tiene métodos que hacen lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="3e367-104">The [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider) class [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) for WMI has methods that do the following:</span></span>

-   <span data-ttu-id="3e367-105">Cree o elimine las claves del registro.</span><span class="sxs-lookup"><span data-stu-id="3e367-105">Create or delete registry keys.</span></span>

    <span data-ttu-id="3e367-106">Use [**CreateKey**](/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov) o [**DeleteKey**](/previous-versions/windows/desktop/regprov/deletekey-method-in-class-stdregprov).</span><span class="sxs-lookup"><span data-stu-id="3e367-106">Use [**CreateKey**](/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov) or [**DeleteKey**](/previous-versions/windows/desktop/regprov/deletekey-method-in-class-stdregprov).</span></span>

-   <span data-ttu-id="3e367-107">Cree o elimine valores con nombre, que se denominan entradas cuando están bajo claves.</span><span class="sxs-lookup"><span data-stu-id="3e367-107">Create or delete named values, which are called entries when they are under keys.</span></span>

    <span data-ttu-id="3e367-108">Use el nombre de un nuevo valor y [**SetBinaryValue**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov), [**SetDWORDValue**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov), [**SetExpandedStringValue**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov), [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov)o [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) para crear un valor con nombre.</span><span class="sxs-lookup"><span data-stu-id="3e367-108">Use the name of a new value and [**SetBinaryValue**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov), [**SetDWORDValue**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov), [**SetExpandedStringValue**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov), [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov), or [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) to create a named value.</span></span> <span data-ttu-id="3e367-109">Use [**DeleteValue**](/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov) para eliminar un valor con nombre.</span><span class="sxs-lookup"><span data-stu-id="3e367-109">Use [**DeleteValue**](/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov) to delete a named value.</span></span>

-   <span data-ttu-id="3e367-110">Cambiar los valores con nombre.</span><span class="sxs-lookup"><span data-stu-id="3e367-110">Change named values.</span></span>

    <span data-ttu-id="3e367-111">Use el nombre de un valor y los métodos set (identificados en el elemento con viñeta anterior) para cambiar los valores con nombre existentes en una clave.</span><span class="sxs-lookup"><span data-stu-id="3e367-111">Use the name of a value and the Set methods (identified in the previous bulleted item) to change existing named values under a key.</span></span> <span data-ttu-id="3e367-112">Debe conocer el nombre de un valor para cambiarlo.</span><span class="sxs-lookup"><span data-stu-id="3e367-112">You must know the name of a value to change it.</span></span> <span data-ttu-id="3e367-113">Si no conoce los nombres de valor bajo una clave, utilice el método [**EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) para obtener los nombres.</span><span class="sxs-lookup"><span data-stu-id="3e367-113">If you do not know the value names under a key, use the [**EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) method to obtain the names.</span></span>

<span data-ttu-id="3e367-114">En este tema se describen las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="3e367-114">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="3e367-115">Crear una clave del registro mediante VBScript</span><span class="sxs-lookup"><span data-stu-id="3e367-115">Creating a Registry Key Using VBScript</span></span>](#creating-a-registry-key-using-vbscript)
-   [<span data-ttu-id="3e367-116">Crear un valor del registro con nombre mediante PowerShell y VBScript</span><span class="sxs-lookup"><span data-stu-id="3e367-116">Creating a Named Registry Value Using PowerShell and VBScript</span></span>](#creating-a-named-registry-value-using-powershell-and-vbscript)

## <a name="creating-a-registry-key-using-vbscript"></a><span data-ttu-id="3e367-117">Crear una clave del registro mediante VBScript</span><span class="sxs-lookup"><span data-stu-id="3e367-117">Creating a Registry Key Using VBScript</span></span>

<span data-ttu-id="3e367-118">Dado que el registro es la base de datos de configuración central para el sistema operativo, las aplicaciones y los servicios, tenga cuidado al escribir cambios en los valores del registro o eliminar claves.</span><span class="sxs-lookup"><span data-stu-id="3e367-118">Because the registry is the central configuration database for the operating system, applications, and services, use caution when you write changes to registry values or delete keys.</span></span>

> [!Note]  
> <span data-ttu-id="3e367-119">No se puede supervisar la subclave **\_ \_ raíz de las clases HKEY** de **HKEY \_ Current \_ User (HKCU)**.</span><span class="sxs-lookup"><span data-stu-id="3e367-119">You cannot monitor the **HKEY\_CLASSES\_ROOT** subkey of **HKEY\_CURRENT\_USER(HKCU)**.</span></span> <span data-ttu-id="3e367-120">No se recomienda supervisar **\_ los usuarios de HKEY** porque las subclaves aparecen y desaparecen cuando se cargan los subárboles.</span><span class="sxs-lookup"><span data-stu-id="3e367-120">Monitoring **HKEY\_USERS** is not recommended because the subkeys appear and disappear as hives are loaded.</span></span>

 

<span data-ttu-id="3e367-121">En los siguientes ejemplos de código se muestra cómo crear una nueva clave del registro y una subclave.</span><span class="sxs-lookup"><span data-stu-id="3e367-121">The following code examples show how to create a new registry key and a subkey.</span></span>


```VB
HKEY_LOCAL_MACHINE = &H80000002
strComputer = "."

Set ObjRegistry = GetObject("winmgmts:{impersonationLevel = impersonate}!\\" & strComputer & "\root\default:StdRegProv")

strPath = "SOFTWARE\MyKey\MySubKey"

Return = objRegistry.CreateKey(HKEY_LOCAL_MACHINE, strPath)

If Return <> 0 Then
    WScript.Echo "The operation failed." & Err.Number
    WScript.Quit
Else
    wScript.Echo "New registry key created" & VBCRLF & "HKLM\SOFTWARE\MYKey\"

End If
```


```PowerShell

$HKEY_LOCAL_MACHINE = 2147483650 
$strComputer = "."
$strPath = "SOFTWARE\MyKey\MySubKey"

$reg = [wmiclass]"\\$strComputer\root\default:StdRegprov"

[void]$reg.CreateKey($HKEY_LOCAL_MACHINE, $strPath)
```





## <a name="creating-a-named-registry-value-using-powershell-and-vbscript"></a><span data-ttu-id="3e367-122">Crear un valor del registro con nombre mediante PowerShell y VBScript</span><span class="sxs-lookup"><span data-stu-id="3e367-122">Creating a Named Registry Value Using PowerShell and VBScript</span></span>

<span data-ttu-id="3e367-123">En el ejemplo de código siguiente se muestra cómo crear un valor con nombre denominado **MultiStringValue** en la clave HKEY **\_ \_** \\  \\  \\ **subsubkey** software de la máquina local.</span><span class="sxs-lookup"><span data-stu-id="3e367-123">The following code example shows how to create a named value called **MultiStringValue** under the **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**MyKey**\\**MySubKey** key that the previous script creates.</span></span> <span data-ttu-id="3e367-124">El script llama a [**StdRegProv. SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov) para escribir valores de cadena en un nuevo valor con nombre.</span><span class="sxs-lookup"><span data-stu-id="3e367-124">The script calls [**StdRegProv.SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov) to write string values to a new named value.</span></span>


```VB
const HKEY_LOCAL_MACHINE = &H80000002 
strComputer = "."

Set objRegistry = _
    GetObject("winmgmts:{impersonationLevel=impersonate}!\\" _ 
    & strComputer & "\root\default:StdRegProv")

strKeyPath = "SOFTWARE\MyKey\MySubKey"
strValueName = "MultiStringValue"
arrStringValues = Array("one", "two","three", "four")

objRegistry.SetMultiStringValue HKEY_LOCAL_MACHINE, strKeyPath,_
    strValueName, arrStringValues

' Read the values that were just written
objRegistry.GetMultiStringValue HKEY_LOCAL_MACHINE, strKeyPath,_
    strValueName, arrStringValues   

For Each strValue in arrStringValues
    WScript.Echo strValue 
Next
```


```PowerShell

$HKEY_LOCAL_MACHINE = 2147483650 
$strComputer = "."
$strPath = "SOFTWARE\MyKey\MySubKey"

$strValueName = "MultiStringValue"
$arrStringValues = @("one", "two","three", "four")

$reg = [wmiclass]"\\$strComputer\root\default:StdRegprov"

[void]$reg.SetMultiStringValue($HKEY_LOCAL_MACHINE, $strKeyPath, $strValueName, $arrStringValues)

$multiValues = $reg.GetMultiStringValue($HKEY_LOCAL_MACHINE, $strKeyPath, $strValueName)
$multiValues.sValue
```

<span data-ttu-id="3e367-125">Con WMI, no se puede establecer la seguridad de acceso en una clave del registro.</span><span class="sxs-lookup"><span data-stu-id="3e367-125">Using WMI, you cannot set access security on a registry key.</span></span> <span data-ttu-id="3e367-126">Sin embargo, el método [**StdRegProv. checkAccess**](/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov) compara la configuración de seguridad del usuario actual con el descriptor de seguridad de una clave del registro para determinar si el usuario tiene un permiso específico, como el **\_ \_ valor del conjunto de claves**.</span><span class="sxs-lookup"><span data-stu-id="3e367-126">However, the [**StdRegProv.CheckAccess**](/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov) method compares the security settings of the current user to the security descriptor on a registry key to determine if the user has a specific permission, such as **KEY\_SET\_VALUE**.</span></span>
