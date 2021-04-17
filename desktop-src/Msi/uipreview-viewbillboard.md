---
description: El método ViewBillboard del objeto UIPreview muestra una cartelera creada mediante el control host del cuadro de diálogo que se muestra actualmente.
ms.assetid: c51c1a5b-af53-47a8-9281-e790efadcfc4
title: UIPreview. ViewBillboard, método
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview.ViewBillboard
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9cf1c6ee2a47fdb246fcc847627bb63432b8a67f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653606"
---
# <a name="uipreviewviewbillboard-method"></a>UIPreview. ViewBillboard, método

El método **ViewBillboard** del objeto [**UIPreview**](uipreview-object.md) muestra una cartelera creada mediante el control host del cuadro de diálogo que se muestra actualmente.

## <a name="syntax"></a>Sintaxis


```JScript
UIPreview.ViewBillboard(
  control,
  billboard
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*control* 
</dt> <dd>

Nombre necesario del control que hospeda la cartelera, con distinción de mayúsculas y minúsculas, junto con el cuadro de diálogo y las claves principales de la tabla de base de datos de control.

</dd> <dt>

*valla* 
</dt> <dd>

Nombre necesario de la cartelera que se va a mostrar mediante el control especificado y el cuadro de diálogo actual, y la clave principal de la tabla de la base de datos de la cartelera.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IUIPreview se define como 000C109A-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




