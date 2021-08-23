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
ms.openlocfilehash: 7f47efd603f10378e6cf5b09144d57776a42cd515f3bd6194174d94bc2583514
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628835"
---
# <a name="sessionproperty-property"></a>Propiedad Session.Property

La propiedad **Property** del objeto [**Session**](session-object.md) es una propiedad de lectura y escritura que representa el valor de cadena de una propiedad de instalador con nombre, tal como la mantiene el objeto **Session** en la tabla Property en memoria o, si tiene como prefijo un signo de porcentaje (%), el valor de una variable de entorno del sistema para el proceso actual. Se pueden proporcionar valores de cadena o enteros. Una propiedad inexistente o una variable de entorno equivale a que su valor sea Null.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```JScript
propVal = Session.Property
Session.Property = propVal 
```



## <a name="property-value"></a>Valor de propiedad

Nombre necesario que distingue mayúsculas de minúsculas de una propiedad o un nombre que no distingue mayúsculas de minúsculas de una variable de entorno precedido por un signo de porcentaje (%).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession se define como \_ 000C109E-0000-0000-C000-00000000046<br/>                                                                                                                                                                             |



 

 




