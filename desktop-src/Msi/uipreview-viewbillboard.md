---
description: El método ViewBillboard del objeto UIPreview muestra un panel escrito mediante el control host en el cuadro de diálogo mostrado actualmente.
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
ms.openlocfilehash: 9cf1c6ee2a47fdb246fcc847627bb63432b8a67f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071809"
---
# <a name="uipreviewviewbillboard-method"></a>Método UIPreview.ViewBillboard

El **método ViewBillboard** del objeto [**UIPreview**](uipreview-object.md) muestra un panel escrito mediante el control host en el cuadro de diálogo mostrado actualmente.

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

Nombre obligatorio del control que hospeda el tablero, con mayúsculas y minúsculas, junto con el cuadro de diálogo y las claves principales de la tabla de base de datos Control.

</dd> <dt>

*Cartelera* 
</dt> <dd>

Se requiere el nombre de la cadena para mostrar mediante el control y el cuadro de diálogo actual especificados, y la clave principal de la tabla de base de datos Den.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IUIPreview de IID se define como \_ 000C109A-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




