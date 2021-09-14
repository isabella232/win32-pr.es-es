---
description: El objeto Patch representa una instancia única de una revisión que se ha registrado o aplicado. Se puede crear una instancia del objeto con la propiedad Patch &\# 0034; WindowsInstaller.Installer.Patch(PatchCode, ProductCode, UserSid, Context)&\# 0034;.
ms.assetid: c1283179-f2c8-42b8-a713-1c82e456f97c
title: Objeto Patch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f6fa55d6ced2afdc53ef8050732f5dee5d6c1f3d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250887"
---
# <a name="patch-object"></a>Objeto Patch

El **objeto Patch** representa una instancia única de una revisión que se ha registrado o aplicado.

Se puede crear una instancia del objeto con la propiedad **Patch** como "WindowsInstaller.Installer.Patch(*PatchCode*, *ProductCode*, *UserSid*, *Context*)". Para un contexto de máquina, el *parámetro UserSid* debe ser una cadena vacía. *ProductCode se* puede establecer en una cadena vacía para las revisiones que se registran solo y que aún no se aplican a ningún producto. *ProductCode se* puede establecer en una cadena vacía cuando solo se lee o actualiza la información de la lista de origen de una revisión.

## <a name="members"></a>Members

El **objeto Patch** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto Patch** tiene estos métodos.



| Método                                                               | Descripción                                                                                                                             |
|:---------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**SourceListAddMediaDisk**](patch-sourcelistaddmediadisk.md)       | Agregue un disco al conjunto de discos registrados.<br/>                                                                                   |
| [**SourceListAddSource**](patch-sourcelistaddsource.md)             | Agregue un origen de red o dirección URL a la lista de origen. <br/>                                                                             |
| [**SourceListClearAll**](patch-sourcelistclearall.md)               | Borra la lista de origen completa del tipo de orígenes especificado.<br/>                                                            |
| [**SourceListClearMediaDisk**](patch-sourcelistclearmediadisk.md)   | Quite un disco del conjunto de discos registrados de la lista de origen. <br/>                                                        |
| [**SourceListClearSource**](patch-sourcelistclearsource.md)         | Quite un origen de red o dirección URL de la lista de origen.<br/>                                                                         |
| [**SourceListForceResolution**](patch-sourcelistforceresolution.md) | Borra el último origen usado de la lista de origen. Esto fuerza una resolución de lista de origen la próxima vez que se requiera el origen.<br/> |



 

### <a name="properties"></a>Propiedades

El **objeto Patch** tiene estas propiedades.



| Propiedad                                                  | Descripción                                                                                                |
|:----------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**Context**](patch-context.md)<br/>               | El contexto de esta instancia de revisión es un valor MSIINSTALLCONTEXT.<br/>                                   |
| [**MediaDisks**](patch-mediadisks.md)<br/>         | Enumera todos los discos multimedia de esta instancia de revisión.<br/>                                         |
| [**PatchCode**](patch-patchcode.md)<br/>           | Devuelve el código de revisión.<br/>                                                                         |
| [**PatchProperty**](patch-patchproperty.md)<br/>   | Obtiene información de propiedades sobre una revisión específica aplicada a una instancia específica del producto.<br/> |
| [**ProductCode**](patch-productcode.md)<br/>       | Devuelve el código del producto.<br/>                                                                       |
| [**SourceListInfo**](patch-sourcelistinfo.md)<br/> | Obtiene y establece las propiedades de información de origen. Se trata de una propiedad de lectura o escritura.<br/>              |
| [**Fuentes**](patch-sources.md)<br/>               | Enumera todos los orígenes de esta instancia de revisión.<br/>                                             |
| [**State**](patch-state.md)<br/>                   | Estado de instalación de la revisión.<br/>                                                                |
| [**UserSid**](patch-usersid.md)<br/>               | Devuelve el SID de usuario, en la cuenta esta instancia de revisión está disponible.<br/>                       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 3.0 o posterior en Windows Server 2003, Windows XP y Windows 2000<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IPatch se define como \_ 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Windows Ejemplos de scripting del instalador](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




