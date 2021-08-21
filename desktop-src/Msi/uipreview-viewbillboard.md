---
description: El método ViewBillboard del objeto UIPreview muestra un panel de creación mediante el control host en el cuadro de diálogo que se muestra actualmente.
ms.assetid: c51c1a5b-af53-47a8-9281-e790efadcfc4
title: Método UIPreview.ViewBillboard
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
ms.openlocfilehash: 9892dc68ae5edb66759e4c19499af56d06fb6efac56b823821cd74c4a28644b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810375"
---
# <a name="uipreviewviewbillboard-method"></a>Método UIPreview.ViewBillboard

El **método ViewBillboard** del objeto [**UIPreview**](uipreview-object.md) muestra un panel de creación mediante el control host en el cuadro de diálogo que se muestra actualmente.

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

Nombre necesario del control que hospeda la tabla, distingue mayúsculas de minúsculas, junto con el cuadro de diálogo y las claves principales de la tabla de base de datos Control.

</dd> <dt>

*Cartelera* 
</dt> <dd>

Nombre obligatorio del cuadro de diálogo que se muestra con el control y el cuadro de diálogo actual especificados, y la clave principal de la tabla de base de datos DeÓn.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IUIPreview se define como \_ 000C109A-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




