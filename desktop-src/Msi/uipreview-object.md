---
description: El objeto UIPreview se usa para ver los cuadros de diálogo y las cartelera de la interfaz de usuario durante la creación. Este objeto se crea mediante el método EnableUIPreview del objeto de base de datos.
ms.assetid: 5df2a4f3-6352-4575-b822-1811150a86be
title: Objeto UIPreview
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6650dc9bcc66a24d0e8a9d7f0d971884a2379f60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679556"
---
# <a name="uipreview-object"></a>Objeto UIPreview

El objeto **UIPreview** se usa para ver los cuadros de diálogo y las cartelera de la interfaz de usuario durante la creación. Este objeto se crea mediante el método [**EnableUIPreview**](database-enableuipreview.md) del objeto de [**base de datos**](database-object.md) .

## <a name="members"></a>Miembros

El objeto **UIPreview** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **UIPreview** tiene estos métodos.



| Método                                           | Descripción                                                                                             |
|:-------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**ViewBillboard**](uipreview-viewbillboard.md) | Muestra una cartelera creada mediante el control host del cuadro de diálogo que se muestra actualmente.<br/> |
| [**ViewDialog**](uipreview-viewdialog.md)       | Muestra un cuadro de diálogo de interfaz de usuario creado almacenado en la base de datos actual.<br/>                           |



 

### <a name="properties"></a>Propiedades

El objeto **UIPreview** tiene estas propiedades.



| Propiedad                                          | Tipo de acceso           | Descripción                                                                                                                                                                       |
|:--------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Propiedad**](uipreview-property.md)<br/> | Lectura/escritura<br/> | Representa el valor de cadena de una propiedad de instalador con nombre o, si tiene como prefijo un signo de porcentaje (%), el valor de una variable de entorno del sistema para el proceso actual.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IUIPreview se define como 000C109A-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Ejemplos de scripting Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




