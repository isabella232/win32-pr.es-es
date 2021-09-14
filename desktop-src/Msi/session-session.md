---
description: La propiedad Property del objeto Session es una propiedad de lectura y escritura que representa el valor de cadena de una propiedad de instalador con nombre, tal y como mantiene el objeto Session.
ms.assetid: 15ce8264-2573-428c-98d9-690cfaae5144
title: Propiedad Session.Property
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9635d5b9ee093f270e4ee7993f78609d60caa13a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272452"
---
# <a name="sessionproperty-property"></a>Propiedad Session.Property

La propiedad **Property** del objeto [**Session**](session-object.md) es una propiedad de lectura y escritura que representa el valor de cadena de una propiedad de instalador con nombre, tal como la mantiene el objeto **Session** en la tabla Property en memoria o, si tiene como prefijo un signo de porcentaje (%), el valor de una variable de entorno del sistema para el proceso actual. Se pueden proporcionar valores de cadena o enteros. Una propiedad inexistente o una variable de entorno equivale a que su valor sea Null.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Session.Property
Session.Property = propVal 
```



## <a name="property-value"></a>Valor de propiedad

Nombre necesario que distingue mayúsculas de minúsculas de una propiedad o un nombre que no distingue mayúsculas de minúsculas de una variable de entorno precedido por un signo de porcentaje (%).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession se define como \_ 000C109E-0000-0000-C000-00000000046<br/>                                                                                                                                                                             |



 

 




