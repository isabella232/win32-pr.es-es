---
description: El objeto UIPreview se usa para ver cuadros de diálogo y paneles de la interfaz de usuario durante la creación. El método EnableUIPreview del objeto Database crea este objeto .
ms.assetid: 5df2a4f3-6352-4575-b822-1811150a86be
title: OBJETO UIPreview
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071818"
---
# <a name="uipreview-object"></a>OBJETO UIPreview

El **objeto UIPreview** se usa para ver cuadros de diálogo y paneles de la interfaz de usuario durante la creación. El método [**EnableUIPreview**](database-enableuipreview.md) del objeto [**Database**](database-object.md) crea este objeto .

## <a name="members"></a>Members

El **objeto UIPreview** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto UIPreview** tiene estos métodos.



| Método                                           | Descripción                                                                                             |
|:-------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**ViewBillboard**](uipreview-viewbillboard.md) | Muestra un cuadro de diálogo escrito con el control host en el cuadro de diálogo que se muestra actualmente.<br/> |
| [**ViewDialog**](uipreview-viewdialog.md)       | Muestra un cuadro de diálogo de interfaz de usuario de creación almacenado en la base de datos actual.<br/>                           |



 

### <a name="properties"></a>Propiedades

El **objeto UIPreview** tiene estas propiedades.



| Propiedad.                                          | Tipo de acceso           | Descripción                                                                                                                                                                       |
|:--------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Propiedad**](uipreview-property.md)<br/> | Lectura y escritura<br/> | Representa el valor de cadena de una propiedad de instalador con nombre o, si tiene como prefijo un signo de porcentaje (%), el valor de una variable de entorno del sistema para el proceso actual.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IUIPreview se define como \_ 000C109A-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Windows Ejemplos de scripting del instalador](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




