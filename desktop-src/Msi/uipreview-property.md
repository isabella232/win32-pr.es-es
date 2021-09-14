---
description: La propiedad Property del objeto UIPreview es una propiedad de lectura y escritura que representa el valor de cadena de una propiedad de instalador con nombre o, si tiene como prefijo un signo de porcentaje (%), el valor de una variable de entorno del sistema para el proceso actual.
ms.assetid: 92900426-8fb5-4a94-a982-438267ad756e
title: UIPreview.Property, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 430c6f75b03fe69f8054bb2b0a61bab59dcc4d58
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071810"
---
# <a name="uipreviewproperty-property"></a>UIPreview.Property, propiedad

La **propiedad Property** del objeto [**UIPreview**](uipreview-object.md) es una propiedad de lectura y escritura que representa el valor de cadena de una propiedad de instalador con nombre o, si tiene como prefijo un signo de porcentaje (%), el valor de una variable de entorno del sistema para el proceso actual. Esto se expone para permitir la presentación adecuada de los cuadros de diálogo que dependen de los valores de propiedad. Se pueden proporcionar valores de cadena o enteros. Una propiedad o variable de entorno inexistente equivale a que su valor sea NULL.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = UIPreview.Property
UIPreview.Property = propVal 
```



## <a name="property-value"></a>Valor de propiedad

Nombre que distingue mayúsculas de minúsculas de una propiedad o un nombre que no distingue mayúsculas de minúsculas de una variable de entorno precedida por un signo de porcentaje (%).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IUIPreview se define como \_ 000C109A-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




