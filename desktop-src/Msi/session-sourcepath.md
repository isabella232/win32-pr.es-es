---
description: La propiedad SourcePath del objeto de sesión es una propiedad de solo lectura que proporciona la ruta de acceso completa a la carpeta designada en el medio de origen o la imagen del servidor.
ms.assetid: ed8eea4f-e15e-4d56-ac0c-e18f9cb46d07
title: Session. SourcePath (propiedad)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681123"
---
# <a name="sessionsourcepath-property"></a>Session. SourcePath (propiedad)

La propiedad **SourcePath** del objeto de [**sesión**](session-object.md) es una propiedad de solo lectura que proporciona la ruta de acceso completa a la carpeta designada en el medio de origen o la imagen del servidor.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Session.SourcePath
```



## <a name="property-value"></a>Valor de propiedad

Nombre obligatorio que distingue entre mayúsculas y minúsculas de una propiedad de carpeta según lo especificado por una clave principal de la [tabla de directorio](directory-table.md). Si la carpeta no existe, se genera un error.

## <a name="remarks"></a>Observaciones

Si se produce un error en la propiedad, puede obtener información de error extendida mediante el método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | El IID \_ ISession se define como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




