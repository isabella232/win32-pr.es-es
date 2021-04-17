---
description: El objeto patch representa una instancia única de una revisión que se ha registrado o aplicado. Se puede crear una instancia del objeto con la propiedad patch como &\# 0034; WindowsInstaller. Installer. patch (PatchCode, ProductCode, UserSid, context) &\# 0034;.
ms.assetid: c1283179-f2c8-42b8-a713-1c82e456f97c
title: Patch (objeto)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653373"
---
# <a name="patch-object"></a>Patch (objeto)

El objeto **patch** representa una instancia única de una revisión que se ha registrado o aplicado.

Se puede crear una instancia del objeto con la propiedad **patch** como "WindowsInstaller. Installer. patch (*PatchCode*, *ProductCode*, *UserSid*, *Context*)". En el contexto de un equipo, el parámetro *UserSid* debe ser una cadena vacía. *ProductCode* se puede establecer en una cadena vacía para las revisiones que solo se registran y aún no se aplican a ningún producto. *ProductCode* se puede establecer en una cadena vacía cuando solo se lee o se actualiza la información de la lista de origen de una revisión.

## <a name="members"></a>Miembros

El objeto **patch** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **patch** tiene estos métodos.



| Método                                                               | Descripción                                                                                                                             |
|:---------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**SourceListAddMediaDisk**](patch-sourcelistaddmediadisk.md)       | Agregue un disco al conjunto de discos registrados.<br/>                                                                                   |
| [**SourceListAddSource**](patch-sourcelistaddsource.md)             | Agregue una red o un origen de URL a la lista de origen. <br/>                                                                             |
| [**SourceListClearAll**](patch-sourcelistclearall.md)               | Borra la lista de origen completa del tipo de orígenes especificado.<br/>                                                            |
| [**SourceListClearMediaDisk**](patch-sourcelistclearmediadisk.md)   | Quitar un disco del conjunto de discos registrados de la lista de origen. <br/>                                                        |
| [**SourceListClearSource**](patch-sourcelistclearsource.md)         | Quite una red o un origen de la dirección URL de la lista de origen.<br/>                                                                         |
| [**SourceListForceResolution**](patch-sourcelistforceresolution.md) | Borra el origen usado por última vez de la lista de origen. Esto fuerza la resolución de una lista de origen la próxima vez que se requiera el origen.<br/> |



 

### <a name="properties"></a>Propiedades

El objeto **patch** tiene estas propiedades.



| Propiedad                                                  | Descripción                                                                                                |
|:----------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**Context**](patch-context.md)<br/>               | El contexto de esta instancia de Patch es un valor de MSIINSTALLCONTEXT.<br/>                                   |
| [**MediaDisks**](patch-mediadisks.md)<br/>         | Enumera todos los discos multimedia para esta instancia de patch.<br/>                                         |
| [**PatchCode**](patch-patchcode.md)<br/>           | Devuelve el código de revisión.<br/>                                                                         |
| [**PatchProperty**](patch-patchproperty.md)<br/>   | Obtiene información de propiedades sobre una revisión específica aplicada a una instancia específica del producto.<br/> |
| [**ProductCode**](patch-productcode.md)<br/>       | Devuelve el código de producto.<br/>                                                                       |
| [**SourceListInfo**](patch-sourcelistinfo.md)<br/> | Obtiene y establece las propiedades de información de origen. Se trata de una propiedad de lectura o escritura.<br/>              |
| [**Orígenes**](patch-sources.md)<br/>               | Enumera todos los orígenes de esta instancia de patch.<br/>                                             |
| [**State**](patch-state.md)<br/>                   | Estado de instalación de la revisión.<br/>                                                                |
| [**UserSid**](patch-usersid.md)<br/>               | Devuelve el SID de usuario, en la cuenta que esta instancia de revisión está disponible.<br/>                       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer 3,0 o posterior en Windows Server 2003, Windows XP y Windows 2000<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IPatch se define como 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Ejemplos de scripting Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




