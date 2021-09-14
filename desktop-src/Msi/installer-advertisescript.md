---
description: El método AdvertiseScript del objeto Installer anuncia un paquete de instalación.
ms.assetid: 45e5268f-7a5f-412f-b9f6-0abb75b79361
title: Installer::AdvertiseScript (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.AdvertiseScript
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7e4ec5afae8d870511c6f91502f8b5844ce135bd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171745"
---
# <a name="installeradvertisescript-method"></a>Installer::AdvertiseScript (método)

El **método AdvertiseScript** del [**objeto Installer**](installer-object.md) anuncia un paquete de instalación.

## <a name="syntax"></a>Sintaxis


```JScript
.AdvertiseScript(
  scriptPath,
  scriptFlags,
  removeItems
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*scriptPath* 
</dt> <dd>

Ruta de acceso completa al archivo de script generado por [**el método CreateAdvertiseScript.**](installer-createadvertisescript.md)

</dd> <dt>

*scriptFlags* 
</dt> <dd>

Marcas que controlan el anuncio. Este parámetro puede ser una combinación de los valores siguientes.



| Value                                                                                                                                                                                                                                                                                                                                                                           | Significado                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseScriptCacheInfo"></span><span id="msiadvertisescriptcacheinfo"></span><span id="MSIADVERTISESCRIPTCACHEINFO"></span><dl> <dt>**msiAdvertiseScriptCacheInfo**</dt> <dt>0x001</dt> </dl>                                                                 | Incluya esta marca si es necesario crear o quitar los iconos.<br/>                                                                                                                                                                                                                                                                                                            |
| <span id="msiAdvertiseScriptShortcuts"></span><span id="msiadvertisescriptshortcuts"></span><span id="MSIADVERTISESCRIPTSHORTCUTS"></span><dl> <dt>**msiAdvertiseScriptShortcuts**</dt> <dt>0x004</dt> </dl>                                                                 | Incluya esta marca si es necesario crear o quitar los accesos directos.<br/>                                                                                                                                                                                                                                                                                                        |
| <span id="msiAdvertiseScriptMachineAssign"></span><span id="msiadvertisescriptmachineassign"></span><span id="MSIADVERTISESCRIPTMACHINEASSIGN"></span><dl> <dt>**msiAdvertiseScriptMachineAssign**</dt> <dt>0x008</dt> </dl>                                                 | Incluya esta marca si el producto se va a asignar a un equipo.<br/>                                                                                                                                                                                                                                                                                                        |
| <span id="msiAdvertiseScriptConfigurationRegistration"></span><span id="msiadvertisescriptconfigurationregistration"></span><span id="MSIADVERTISESCRIPTCONFIGURATIONREGISTRATION"></span><dl> <dt>**msiAdvertiseScriptConfigurationRegistration**</dt> <dt>0x020</dt> </dl> | Incluya esta marca si es necesario escribir o quitar la información de configuración y administración en los datos del Registro.<br/>                                                                                                                                                                                                                                                   |
| <span id="msiAdvertiseScriptValidateTransformList"></span><span id="msiadvertisescriptvalidatetransformlist"></span><span id="MSIADVERTISESCRIPTVALIDATETRANSFORMLIST"></span><dl> <dt>**msiAdvertiseScriptValidateTransformList**</dt> <dt>0x040</dt> </dl>                 | Incluya esta marca para forzar la validación de las transformaciones enumeradas en el script en las transformaciones registradas previamente para este producto. Tenga en cuenta que los conflictos de transformación se detectan mediante una comparación de cadenas que no tiene en cuenta mayúsculas de minúsculas y se evalúan entre instalaciones por usuario y por máquina en todos los [contextos de instalación.](installation-context.md)<br/> |
| <span id="msiAdvertiseScriptClassInfoRegistration"></span><span id="msiadvertisescriptclassinforegistration"></span><span id="MSIADVERTISESCRIPTCLASSINFOREGISTRATION"></span><dl> <dt>**msiAdvertiseScriptClassInfoRegistration**</dt> <dt>0x080</dt> </dl>                 | Incluya esta marca si es necesario escribir o quitar información de anuncio en el Registro relacionada con las clases COM.<br/>                                                                                                                                                                                                                                                    |
| <span id="msiAdvertiseScriptExtensionInfoRegistration"></span><span id="msiadvertisescriptextensioninforegistration"></span><span id="MSIADVERTISESCRIPTEXTENSIONINFOREGISTRATION"></span><dl> <dt>**msiAdvertiseScriptExtensionInfoRegistration**</dt> <dt>0x100</dt> </dl> | Incluya esta marca si es necesario escribir o quitar información de anuncio en el Registro relacionada con una extensión.<br/>                                                                                                                                                                                                                                                   |
| <span id="msiAdvertiseScriptAppInfo"></span><span id="msiadvertisescriptappinfo"></span><span id="MSIADVERTISESCRIPTAPPINFO"></span><dl> <dt>**msiAdvertiseScriptAppInfo**</dt> <dt>0x180</dt> </dl>                                                                         | Incluya esta marca si es necesario escribir o quitar la información del anuncio en el Registro.<br/>                                                                                                                                                                                                                                                                       |
| <span id="msiAdvertiseScriptRegData"></span><span id="msiadvertisescriptregdata"></span><span id="MSIADVERTISESCRIPTREGDATA"></span><dl> <dt>**msiAdvertiseScriptRegData**</dt> <dt>0x1A0</dt> </dl>                                                                         | Incluya esta marca si es necesario escribir o quitar la información del anuncio en el Registro.<br/>                                                                                                                                                                                                                                                                       |



 

</dd> <dt>

*removeItems* 
</dt> <dd>

TRUE si los elementos especificados se van a quitar en lugar de crearse.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El **método AdvertiseScript** usa la [**función MsiAdvertiseScript.**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta) El uso del método **AdvertiseScript** requiere que el script se ejecute dentro de un proceso del sistema local.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso del **método AdvertiseScript.**


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' Advertise Simple package using an advertise script
'   created by CreateAdvertiseScript Method
'
'  Flags 424 indicate msiAdvertiseScriptMachineAssign, msiAdvertiseScriptRegData

Installer.AdvertiseScript "c:\scratch\simpletst\rtm\simple.aas", 424, false

' Verify Simple is installed
MsgBox Installer.ProductState("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}")

'
' Remove Simple using advertise script
'
Installer.AdvertiseScript "c:\scratch\simpletst\rtm\simple.aas", 424, true

' Verify simple is removed
MsgBox Installer.ProductState("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}")
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 4.5 en Windows Server 2003 y Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IInstaller de IID se define como \_ 000C1090-0000-0000-C000-00000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Instalador**](installer-object.md)
</dt> <dt>

[No se admite en Windows Installer 3.1 y versiones anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




