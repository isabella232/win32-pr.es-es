---
description: Para cada producto incluido en el paquete de revisión como válido para recibir la revisión, el método ApplyPatch del objeto de instalador invoca una instalación y establece la propiedad PATCH en la ruta de acceso del paquete patch.
ms.assetid: eee93b6d-f45b-40ae-8e17-cfe6f46b66f4
title: Instalador. ApplyPatch (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ApplyPatch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cc1b7509ddb4c61fa84a4547dcd47f2c7637b913
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653640"
---
# <a name="installerapplypatch-method"></a>Instalador. ApplyPatch (método)

Para cada producto incluido en el paquete de revisión como válido para recibir la revisión, el método **ApplyPatch** del objeto de [**instalador**](installer-object.md) invoca una instalación y establece la propiedad [**patch**](patch.md) en la ruta de acceso del paquete patch.

## <a name="syntax"></a>Sintaxis


```JScript
Installer.ApplyPatch(
  PatchPackage,
  InstallPackage,
  InstallType,
  CommandLine
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PatchPackage* 
</dt> <dd>

Especifica una ruta de acceso al paquete de revisión.

</dd> <dt>

*InstallPackage* 
</dt> <dd>

Si *InstallType* está establecido en MsiInstallTypeNetworkImage, *InstallPackage* especifica la ruta de acceso al producto que se va a revisar. Si *InstallType* se establece en MsiInstallTypeDefault y *InstallPackage* se establece en 0, el instalador aplica la revisión a todos los productos válidos que se enumeran en el paquete de revisión.

Si *InstallType* es msiInstallTypeSingleInstance, el instalador aplica la revisión al producto especificado por *InstallPackage*. En este caso, se omiten otros productos válidos enumerados en el paquete de revisión y el parámetro *InstallPackage* contiene la cadena terminada en null que representa el código de producto de la instancia que se va a revisar. Este tipo de instalación requiere la versión Windows Installer incluida con Windows Server 2003 o posterior, o Windows Installer XP SP1 o posterior.

</dd> <dt>

*InstallType* 
</dt> <dd>

Este parámetro especifica el tipo de instalación que se va a revisar. El parámetro *InstallType* se omite si se omite *InstallPackage* .



| Value                                                                                                                                                                                                                                            | Significado                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallTypeNetworkImage"></span><span id="msiinstalltypenetworkimage"></span><span id="MSIINSTALLTYPENETWORKIMAGE"></span><dl> <dt>**msiInstallTypeNetworkImage**</dt> </dl> | Indica una instalación administrativa. En este caso, *InstallPackage* se debe establecer en una ruta de acceso del paquete. Un valor de 1 para msiInstallTypeNetworkImage especifica una instalación administrativa.<br/>                                                                                                                                                                                                                    |
| <span id="msiInstallTypeDefault"></span><span id="msiinstalltypedefault"></span><span id="MSIINSTALLTYPEDEFAULT"></span><dl> <dt>**msiInstallTypeDefault**</dt> </dl>                     | Busca los productos en el sistema para aplicar revisiones. En este caso, *InstallPackage* debe ser una cadena vacía.<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiInstallSingleInstance"></span><span id="msiinstallsingleinstance"></span><span id="MSIINSTALLSINGLEINSTANCE"></span><dl> <dt>**msiInstallSingleInstance**</dt> </dl>         | Aplique una revisión al producto especificado por *InstallPackage*. *InstallPackage* es el código de producto de la instancia que se va a revisar. Este tipo de instalación requiere la versión Windows Installer incluida con Windows Server 2003 o posterior, o Windows Installer XP SP1 o posterior. Para obtener más información, vea [instalar varias instancias de productos y revisiones](installing-multiple-instances-of-products-and-patches.md).<br/> |



 

</dd> <dt>

*CommandLine* 
</dt> <dd>

Especifica la configuración de propiedades que se establece en la línea de comandos. vea la sección Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Dado que el delimitador de lista para las transformaciones, los orígenes y las revisiones es un punto y coma, este carácter no se debe utilizar para los nombres de archivo o las rutas de acceso.

La propiedad [**REINSTALL**](reinstall.md) es necesaria cuando se aplica una [pequeña actualización](small-updates.md) o una revisión de [actualización secundaria](minor-upgrades.md) . Sin esta propiedad, la revisión se registra en el sistema pero no se pueden actualizar los archivos.

**Windows Installer 2,0:** Debe establecer la propiedad [**REINSTALL**](reinstall.md) en la línea de comandos al aplicar una [pequeña actualización](small-updates.md) o una revisión de [actualización secundaria](minor-upgrades.md) . En el caso de las revisiones que no usan una [acción personalizada, escriba 51](custom-action-type-51.md) para establecer automáticamente las propiedades **REINSTALL** y [**REINSTALLMODE**](reinstallmode.md) , la propiedad **REINSTALL** debe establecerse explícitamente con el parámetro *commandLine* . Establezca la propiedad **REINSTALL (reinstalar** ) para enumerar las características afectadas por la revisión o use una configuración predeterminada práctica de "REINSTALL = ALL". El valor predeterminado de la propiedad **REINSTALLMODE** es "OMUs".

**Windows Installer 3,0 y versiones posteriores:** A partir de Windows Installer versión 3,0, el instalador configura la propiedad [**REINSTALL**](reinstall.md) y no es necesario establecerla en la línea de comandos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer 3,0 o posterior en Windows Server 2003 o Windows XP.<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
</dt> <dt>

[Acerca de las propiedades](about-properties.md)
</dt> <dt>

[No se admite en Windows Installer 2,0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




