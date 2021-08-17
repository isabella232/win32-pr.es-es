---
description: 'La clase Del proveedor del Registro del sistema StdRegProv para WMI tiene métodos que hacen lo siguiente:'
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
ms.openlocfilehash: 32258fb64e075889a6e423e2b6a3fa2e7b0fdeb0ee5a80e2f45436674ba79c4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118556950"
---
# <a name="changing-registry-data"></a>Cambio de los datos del Registro

La [clase Del proveedor del Registro](/previous-versions/windows/desktop/regprov/system-registry-provider) del sistema [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) para WMI tiene métodos que hacen lo siguiente:

-   Crear o eliminar claves del Registro.

    Use [**CreateKey**](/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov) o [**DeleteKey.**](/previous-versions/windows/desktop/regprov/deletekey-method-in-class-stdregprov)

-   Cree o elimine valores con nombre, que se denominan entradas cuando están bajo claves.

    Use el nombre de un nuevo valor y [**SetBinaryValue,**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov) [**SetDWORDValue,**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov) [**SetExpandedStringValue,**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov) [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov)o [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) para crear un valor con nombre. Use [**DeleteValue**](/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov) para eliminar un valor con nombre.

-   Cambie los valores con nombre.

    Use el nombre de un valor y los métodos Set (identificados en el elemento con viñetas anterior) para cambiar los valores con nombre existentes bajo una clave. Debe conocer el nombre de un valor para cambiarlo. Si no conoce los nombres de valor de una clave, use el [**método EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) para obtener los nombres.

En este tema se de abordan las secciones siguientes:

-   [Crear una clave del Registro mediante VBScript](#creating-a-registry-key-using-vbscript)
-   [Crear un valor del Registro con nombre mediante PowerShell y VBScript](#creating-a-named-registry-value-using-powershell-and-vbscript)

## <a name="creating-a-registry-key-using-vbscript"></a>Crear una clave del Registro mediante VBScript

Dado que el Registro es la base de datos de configuración central para el sistema operativo, las aplicaciones y los servicios, tenga cuidado al escribir cambios en los valores del Registro o eliminar claves.

> [!Note]  
> No se puede supervisar la subclave **RAÍZ HKEY \_ CLASSES \_** de **HKEY CURRENT \_ \_ USER(HKCU).** No **se recomienda supervisar usuarios \_ de HKEY** porque las subclaves aparecen y desaparecen a medida que se cargan los subárboles.

 

En los ejemplos de código siguientes se muestra cómo crear una nueva clave del Registro y una subclave.


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





## <a name="creating-a-named-registry-value-using-powershell-and-vbscript"></a>Crear un valor del Registro con nombre mediante PowerShell y VBScript

En el ejemplo de código siguiente se muestra cómo crear un valor con nombre denominado **MultiStringValue** bajo la clave **\_ \_** \\  \\ **MyKey** \\ **MySubKey** de HKEY LOCAL MACHINE SOFTWARE que crea el script anterior. El script llama [**a StdRegProv.SetMultiStringValue para**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov) escribir valores de cadena en un nuevo valor con nombre.


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

Con WMI, no se puede establecer la seguridad de acceso en una clave del Registro. Sin embargo, el método [**StdRegProv.CheckAccess**](/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov) compara la configuración de seguridad del usuario actual con el descriptor de seguridad de una clave del Registro para determinar si el usuario tiene un permiso específico, como **KEY SET \_ \_ VALUE**.
