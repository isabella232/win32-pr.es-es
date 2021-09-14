---
description: Para cada producto enumerado por el paquete de revisión como apto para recibir la revisión, el método ApplyPatch del objeto Installer invoca una instalación y establece la propiedad PATCH en la ruta de acceso del paquete de revisión.
ms.assetid: eee93b6d-f45b-40ae-8e17-cfe6f46b66f4
title: Installer.ApplyPatch (método)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171738"
---
# <a name="installerapplypatch-method"></a>Installer.ApplyPatch (método)

Para cada producto enumerado por el paquete de revisión como apto para recibir la revisión, el método **ApplyPatch** del objeto [**Installer**](installer-object.md) invoca una instalación y establece la propiedad [**PATCH**](patch.md) en la ruta de acceso del paquete de revisión.

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

Si *InstallType* se establece en msiInstallTypeNetworkImage, *InstallPackage* especifica la ruta de acceso al producto al que se va a aplicar la revisión. Si *InstallType está* establecido en msiInstallTypeDefault e *InstallPackage* está establecido en 0, el instalador aplica la revisión a todos los productos aptos enumerados en el paquete de revisión.

Si *InstallType* es msiInstallTypeSingleInstance, el instalador aplica la revisión al producto especificado por *InstallPackage*. En este caso, se omiten otros productos aptos enumerados en el paquete de revisión y el parámetro *InstallPackage* contiene la cadena terminada en NULL que representa el código de producto de la instancia de que se va a aplicar la revisión. Este tipo de instalación requiere la versión de Windows Installer que se incluye con Windows Server 2003 o posterior o Windows Installer XP SP1 o posterior.

</dd> <dt>

*InstallType* 
</dt> <dd>

Este parámetro especifica el tipo de instalación que se va a aplicar a la revisión. El *parámetro InstallType* se omite si *se omite InstallPackage.*



| Value                                                                                                                                                                                                                                            | Significado                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallTypeNetworkImage"></span><span id="msiinstalltypenetworkimage"></span><span id="MSIINSTALLTYPENETWORKIMAGE"></span><dl> <dt>**msiInstallTypeNetworkImage**</dt> </dl> | Indica una instalación administrativa. En este caso, *InstallPackage debe* establecerse en una ruta de acceso del paquete. Un valor de 1 para msiInstallTypeNetworkImage especifica una instalación administrativa.<br/>                                                                                                                                                                                                                    |
| <span id="msiInstallTypeDefault"></span><span id="msiinstalltypedefault"></span><span id="MSIINSTALLTYPEDEFAULT"></span><dl> <dt>**msiInstallTypeDefault**</dt> </dl>                     | Busca productos para aplicar revisiones al sistema. En este caso, *InstallPackage* debe ser una cadena vacía.<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiInstallSingleInstance"></span><span id="msiinstallsingleinstance"></span><span id="MSIINSTALLSINGLEINSTANCE"></span><dl> <dt>**msiInstallSingleInstance**</dt> </dl>         | Aplicar una revisión al producto especificado por *InstallPackage.* *InstallPackage* es el código de producto de la instancia de que se va a aplicar la revisión. Este tipo de instalación requiere la versión de Windows Installer que se incluye con Windows Server 2003 o posterior o Windows Installer XP SP1 o posterior. Para obtener más información, [vea Instalación de varias instancias de productos y revisiones.](installing-multiple-instances-of-products-and-patches.md)<br/> |



 

</dd> <dt>

*CommandLine* 
</dt> <dd>

Especifica la configuración de propiedades que se establece en la línea de comandos. vea la sección Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Dado que el delimitador de lista para transformaciones, orígenes y revisiones es un punto y coma, este carácter no debe usarse para los nombres de archivo ni las rutas de acceso.

La [**propiedad REINSTALL**](reinstall.md) es necesaria al aplicar una actualización [pequeña](small-updates.md) o una [revisión de actualización](minor-upgrades.md) secundaria. Sin esta propiedad, la revisión se registra en el sistema, pero no se pueden actualizar los archivos.

**Windows Installer 2.0:** Debe establecer la propiedad [**REINSTALL en**](reinstall.md) la línea de comandos al aplicar una actualización [pequeña](small-updates.md) o una [revisión de actualización](minor-upgrades.md) secundaria. En el caso de las revisiones que no usan un tipo de acción [personalizada 51](custom-action-type-51.md) para establecer automáticamente las propiedades **REINSTALL** y [**REINSTALLMODE,**](reinstallmode.md) la propiedad **REINSTALL** debe establecerse explícitamente con el *parámetro CommandLine.* Establezca la **propiedad REINSTALL** para enumerar las características afectadas por la revisión o use una configuración predeterminada práctica de "REINSTALL=ALL". El valor predeterminado de la **propiedad REINSTALLMODE** es "omus".

**Windows Installer 3.0 y versiones posteriores:** A partir Windows Installer versión 3.0, el instalador configura la propiedad [**REINSTALL**](reinstall.md) y no es necesario establecerla en la línea de comandos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 3.0 o posterior en Windows Server 2003 o Windows XP.<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IInstaller de IID se define como \_ 000C1090-0000-0000-C000-00000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
</dt> <dt>

[Acerca de las propiedades](about-properties.md)
</dt> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




