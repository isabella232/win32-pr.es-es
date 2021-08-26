---
description: El método ViewDialog del objeto UIPreview muestra un cuadro de diálogo de interfaz de usuario escrito almacenado en la base de datos actual.
ms.assetid: 5bc935ac-38ca-4a51-a1dc-6879dee97b05
title: Método UIPreview.ViewDialog
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
ms.openlocfilehash: 40797da833576c0a829234d6036cb1d583464dea96dbe4e625dcd63c1c1bd4c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893405"
---
# <a name="uipreviewviewdialog-method"></a>Método UIPreview.ViewDialog

El **método ViewDialog** del objeto [**UIPreview**](uipreview-object.md) muestra un cuadro de diálogo de interfaz de usuario escrito almacenado en la base de datos actual.

## <a name="syntax"></a>Sintaxis


```JScript
UIPreview.ViewDialog(
  dialog
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Diálogo* 
</dt> <dd>

Nombre obligatorio del cuadro de diálogo, que distingue mayúsculas de minúsculas y la clave principal de la tabla de base de datos Dialog.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IUIPreview de IID se define como \_ 000C109A-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




