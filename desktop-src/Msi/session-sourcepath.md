---
description: La propiedad SourcePath del objeto Session es una propiedad de solo lectura que proporciona la ruta de acceso completa a la carpeta designada en el medio de origen o la imagen del servidor.
ms.assetid: ed8eea4f-e15e-4d56-ac0c-e18f9cb46d07
title: Propiedad Session.SourcePath
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.SourcePath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a868e68e26f28d4fc2137e735ddc6d4c6ab0066
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272439"
---
# <a name="sessionsourcepath-property"></a>Propiedad Session.SourcePath

La **propiedad SourcePath** del objeto [**Session**](session-object.md) es una propiedad de solo lectura que proporciona la ruta de acceso completa a la carpeta designada en el medio de origen o la imagen del servidor.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Session.SourcePath
```



## <a name="property-value"></a>Valor de propiedad

Se requiere un nombre que distingue mayúsculas de minúsculas de una propiedad de carpeta según lo especificado por una clave principal de la [tabla Directory](directory-table.md). Se genera un error si la carpeta no existe.

## <a name="remarks"></a>Observaciones

Si se produce un error en la propiedad , puede obtener información de error extendida mediante el [**método LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession se define como \_ 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




