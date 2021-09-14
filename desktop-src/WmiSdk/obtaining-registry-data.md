---
description: Puede obtener o modificar datos del Registro mediante la clase Wmi StdRegProv y sus métodos.
ms.assetid: 7cba9dcb-741b-4118-9769-8830c6dc0752
ms.tgt_platform: multiple
title: Obtener datos del Registro
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f5468a577acedeccf4396607147428d9160b4d38
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973763"
---
# <a name="obtaining-registry-data"></a>Obtener datos del Registro

Puede obtener o modificar datos del Registro mediante la clase [**Wmi StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) y sus métodos. Aunque usa la utilidad Regedit para ver y cambiar los valores del Registro en el equipo local, **StdRegProv** permite usar un script o una aplicación para automatizar dichas actividades en el equipo local y en los equipos remotos.

[**StdRegProv contiene**](/previous-versions/windows/desktop/regprov/stdregprov) métodos para hacer lo siguiente:

-   Comprobación de los permisos de acceso de un usuario
-   Creación, enumeración y eliminación de claves del Registro
-   Crear, enumerar y eliminar subclaves o valores con nombre
-   Lectura, escritura y eliminación de valores de datos

Los datos del Registro se organizan por subárboles, claves y subclaves anidados bajo una clave de nivel superior. Los valores de datos reales se denominan entradas o valores con nombre.

Los subárboles incluyen lo siguiente:

-   **HKEY \_ CLASSES \_ ROOT** (abreviado como **HKCR)**
-   **HKEY \_ USUARIO \_ ACTUAL** (**HKCU**)
-   **HKEY \_ MÁQUINA \_ LOCAL** (**HKLM**)
-   **USUARIOS DE \_ HKEY**
-   **CONFIGURACIÓN ACTUAL DE HKEY \_ \_**

Por ejemplo, en la entrada del Registro **HKEY** \\ **SOFTWARE** \\ **Microsoft** \\ **DirectX** \\ **InstalledVersion**,  el subárbol HKEY es SOFTWARE ; las subclaves son Microsoft y **DirectX;** y la entrada de valor con nombre es **InstalledVersion**.

Se [**produce un evento RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) cuando se produce un cambio en una clave específica, pero la entrada no identifica cómo cambian los valores ni se desencadenará este evento mediante cambios por debajo de la clave especificada. Para identificar los cambios en cualquier parte de una estructura de clave jerárquica, use [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent), que no devuelve valores específicos ni cambios de clave que se produzcan. Para obtener un cambio de valor de entrada específico, use [**RegistryValueChangeEvent**](/previous-versions/windows/desktop/regprov/registryvaluechangeevent)y, a continuación, lea la entrada para obtener un valor de línea base.

[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) solo tiene métodos a los que se puede llamar desde C++ o script, que es diferente de la estructura de clase Win32.

En el ejemplo de código siguiente se muestra cómo usar el método [**StdRegProv.EnumKey**](/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov) para enumerar todas las subclaves de software de Microsoft bajo la clave del Registro.

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft**


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





[**StdRegProv tiene**](/previous-versions/windows/desktop/regprov/stdregprov) distintos métodos para leer los distintos tipos de datos de valor de entrada del Registro. Si la entrada tiene valores desconocidos, puede llamar a [**StdRegProv.EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) para enumerarlos. En la tabla siguiente se muestra la correspondencia **entre los métodos StdRegProv** y los tipos de datos.



| Método                                                                                  | Tipo de datos           |
|-----------------------------------------------------------------------------------------|---------------------|
| [**GetBinaryValue**](/previous-versions/windows/desktop/regprov/getbinaryvalue-method-in-class-stdregprov)                 | **REG \_ BINARY**     |
| [**GetDWORDValue**](/previous-versions/windows/desktop/regprov/getdwordvalue-method-in-class-stdregprov)                   | **REG \_ DWORD**      |
| [**GetExpandedStringValue**](/previous-versions/windows/desktop/regprov/getexpandedstringvalue-method-in-class-stdregprov) | **REG \_ EXPAND \_ SZ** |
| [**GetMultiStringValue**](/previous-versions/windows/desktop/regprov/getmultistringvalue-method-in-class-stdregprov)       | **REG \_ MULTI \_ SZ**  |
| [**GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov)                 | **REG \_ SZ**         |



 

En la tabla siguiente se enumeran los métodos correspondientes para crear nuevas claves o valores, o cambiar los existentes.



| Método                                                                                  | Tipo de datos           |
|-----------------------------------------------------------------------------------------|---------------------|
| [**SetBinaryValue**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov)                 | **REG \_ BINARY**     |
| [**SetDWORDValue**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov)                   | **REG \_ DWORD**      |
| [**SetExpandedStringValue**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov) | **REG \_ EXPAND \_ SZ** |
| [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov)       | **REG \_ MULTI \_ SZ**  |
| [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov)                 | **REG \_ SZ**         |



 

En el ejemplo siguiente se muestra cómo leer la lista de orígenes del registro de eventos del sistema desde la clave del Registro.

**HKEY \_ SISTEMA DE \_ MÁQUINA LOCAL** Sistema de registro de eventos \\  \\  \\ **de servicios del** conjunto de \\ **controles** \\ **actual**

Tenga en cuenta que los elementos del valor de varias cadenas se tratan como una colección o matriz.


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



El proveedor del Registro se hospeda en LocalService, no en LocalSystem. Por lo tanto, no es posible obtener información de forma remota desde el subárbol **HKEY \_ CURRENT \_ USER.** Sin embargo, los scripts que se ejecutan en el equipo local todavía pueden acceder **a HKEY \_ CURRENT \_ USER**. Puede establecer el modelo de hospedaje en LocalSystem en un equipo remoto, pero eso es un riesgo de seguridad porque el registro de la máquina remota es vulnerable a un acceso agresivo. Para obtener más información, vea [Provider Hosting and Security](provider-hosting-and-security.md).

## <a name="examples"></a>Ejemplos

El [ejemplo de código DE](https://Gallery.TechNet.Microsoft.Com/b0724cb2-36ed-4d0d-8b8f-428d0e3d0b82) VBScript Leer un valor de registro binario en la Galería de TechNet usa WMI para leer un valor del Registro binario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas wmi: Registro](wmi-tasks--registry.md)
</dt> </dl>

 

 
