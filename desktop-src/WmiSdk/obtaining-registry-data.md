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
# <a name="obtaining-registry-data"></a>Obtener datos del registro

Puede obtener o modificar los datos del registro mediante la clase [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) de WMI y sus métodos. Aunque use la utilidad regedit para ver y cambiar los valores del registro en el equipo local, **StdRegProv** le permite usar un script o una aplicación para automatizar dichas actividades en el equipo local y en los equipos remotos.

[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) contiene métodos para hacer lo siguiente:

-   Comprobar los permisos de acceso de un usuario
-   Crear, enumerar y eliminar claves del registro
-   Crear, enumerar y eliminar subclaves o valores con nombre
-   Leer, escribir y eliminar valores de datos

Los datos del registro se organizan por subárboles, claves y subclaves anidadas bajo una clave de nivel superior. Los valores de datos reales se denominan entradas o valores con nombre.

Entre los subárboles se incluyen los siguientes:

-   **HKEY \_ CLASSes \_ root** (abreviado como **HKCR**)
-   **HKEY \_ \_usuario actual** (**HKCU**)
-   **HKEY \_ \_máquina local** (**HKLM**)
-   **\_usuarios HKEY**
-   **HKEY \_ \_ configuración actual**

Por ejemplo, en la entrada del **registro HKEY** \\ **software** \\ **Microsoft** \\ **DirectX** \\ **InstalledVersion**, el subárbol HKEY **es software**; las subclaves son **Microsoft** y **DirectX**, y la entrada de valor con nombre es **InstalledVersion**.

Un [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) se produce cuando se produce un cambio en una clave específica, pero la entrada no identifica el modo en que cambian los valores ni los cambios por debajo de la clave especificada. Para identificar los cambios en cualquier parte de una estructura jerárquica de claves, use [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent), que no devuelve valores específicos o cambios clave que se producen. Para obtener un cambio de valor de entrada específico, use [**RegistryValueChangeEvent**](/previous-versions/windows/desktop/regprov/registryvaluechangeevent)y, a continuación, lea la entrada para obtener un valor de línea base.

[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) solo tiene métodos a los que se puede llamar desde C++ o script, que es diferente de la estructura de clase Win32.

En el ejemplo de código siguiente se muestra cómo usar el método [**StdRegProv. enumKey**](/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov) para enumerar todas las subclaves de software de Microsoft en la clave del registro.

**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft**


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





[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) tiene distintos métodos para leer los distintos tipos de datos del valor de entrada del registro. Si la entrada tiene valores desconocidos, puede llamar a [**StdRegProv. EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) para enumerarlos. En la tabla siguiente se muestra la correspondencia entre los métodos **StdRegProv** y los tipos de datos de.



| Método                                                                                  | Tipo de datos           |
|-----------------------------------------------------------------------------------------|---------------------|
| [**GetBinaryValue**](/previous-versions/windows/desktop/regprov/getbinaryvalue-method-in-class-stdregprov)                 | **\_binario de reg**     |
| [**GetDWORDValue**](/previous-versions/windows/desktop/regprov/getdwordvalue-method-in-class-stdregprov)                   | **\_valor DWORD reg**      |
| [**GetExpandedStringValue**](/previous-versions/windows/desktop/regprov/getexpandedstringvalue-method-in-class-stdregprov) | **REG \_ expandir \_ SZ** |
| [**GetMultiStringValue**](/previous-versions/windows/desktop/regprov/getmultistringvalue-method-in-class-stdregprov)       | **REG \_ multi \_ SZ**  |
| [**GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov)                 | **Registro \_ SZ**         |



 

En la tabla siguiente se enumeran los métodos correspondientes para crear nuevas claves o valores, o cambiar los existentes.



| Método                                                                                  | Tipo de datos           |
|-----------------------------------------------------------------------------------------|---------------------|
| [**SetBinaryValue**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov)                 | **\_binario de reg**     |
| [**SetDWORDValue**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov)                   | **\_valor DWORD reg**      |
| [**SetExpandedStringValue**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov) | **REG \_ expandir \_ SZ** |
| [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov)       | **REG \_ multi \_ SZ**  |
| [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov)                 | **Registro \_ SZ**         |



 

En el ejemplo siguiente se muestra cómo leer la lista de orígenes del registro de eventos del sistema desde la clave del registro.

**HKEY \_ \_** \\ **Sistema del** equipo local \\ **control actual** del sistema de registro de \\  \\ **eventos** \\  de servicios

Tenga en cuenta que los elementos del valor de cadena multistring se tratan como una colección o una matriz.


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



El proveedor del registro se hospeda en LocalService, no en LocalSystem. Por lo tanto, no es posible obtener información de forma remota desde el subárbol **HKEY \_ Current \_ User** . Sin embargo, los scripts que se ejecutan en el equipo local todavía pueden tener acceso a **HKEY \_ Current \_ User**. Puede establecer el modelo de hospedaje en LocalSystem en un equipo remoto, pero esto es un riesgo para la seguridad porque el registro del equipo remoto es vulnerable al acceso hostil. Para obtener más información, vea [hospedaje y seguridad de proveedores](provider-hosting-and-security.md).

## <a name="examples"></a>Ejemplos

En el ejemplo de código de VBScript [leer un valor de registro binario](https://Gallery.TechNet.Microsoft.Com/b0724cb2-36ed-4d0d-8b8f-428d0e3d0b82) en la galería de TechNet se usa WMI para leer un valor del registro binario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas WMI: registro](wmi-tasks--registry.md)
</dt> </dl>

 

 
