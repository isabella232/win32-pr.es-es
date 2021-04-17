---
description: La propiedad Property del objeto de sesión es una propiedad de lectura y escritura que representa el valor de cadena de una propiedad de instalador con nombre, tal y como la mantiene el objeto de sesión.
ms.assetid: 15ce8264-2573-428c-98d9-690cfaae5144
title: Propiedad Session. Property
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681124"
---
# <a name="sessionproperty-property"></a>Propiedad Session. Property

La propiedad **Property** del objeto de [**sesión**](session-object.md) es una propiedad de lectura y escritura que representa el valor de cadena de una propiedad de instalador con nombre, tal como la mantiene el objeto de **sesión** en la tabla de propiedades en memoria, o bien, si tiene como prefijo un signo de porcentaje (%), el valor de una variable de entorno del sistema para el proceso actual. Se pueden proporcionar valores de cadena o enteros. Una propiedad o una variable de entorno inexistente equivale a su valor null.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Session.Property
Session.Property = propVal 
```



## <a name="property-value"></a>Valor de propiedad

Nombre obligatorio que distingue entre mayúsculas y minúsculas de una propiedad o un nombre que no distingue entre mayúsculas y minúsculas de una variable de entorno con un signo de porcentaje (%).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | El IID \_ ISession se define como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




