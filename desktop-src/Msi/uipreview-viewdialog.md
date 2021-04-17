---
description: El método ViewDialog del objeto UIPreview muestra un cuadro de diálogo de interfaz de usuario creado almacenado en la base de datos actual.
ms.assetid: 5bc935ac-38ca-4a51-a1dc-6879dee97b05
title: UIPreview. ViewDialog, método
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview.ViewDialog
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d9ad3772ced2dba952a3d3b068aaa307d1c06398
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679279"
---
# <a name="uipreviewviewdialog-method"></a>UIPreview. ViewDialog, método

El método **ViewDialog** del objeto [**UIPreview**](uipreview-object.md) muestra un cuadro de diálogo de interfaz de usuario creado almacenado en la base de datos actual.

## <a name="syntax"></a>Sintaxis


```JScript
UIPreview.ViewDialog(
  dialog
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*diálogo* 
</dt> <dd>

Nombre necesario del cuadro de diálogo, con distinción de mayúsculas y minúsculas, y la clave principal de la tabla de base de datos de cuadros de diálogo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IUIPreview se define como 000C109A-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




