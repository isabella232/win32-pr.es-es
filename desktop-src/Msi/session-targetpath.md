---
description: La propiedad TargetPath del objeto de sesión es una propiedad de lectura y escritura que proporciona la ruta de acceso completa a la carpeta designada en la unidad de destino de la instalación.
ms.assetid: 563b874e-c669-4f5b-b3fa-eeb6b6e578f2
title: Session. TargetPath (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.TargetPath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6c5917f845da0eec944e797d5f49f52d0ec26913
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653971"
---
# <a name="sessiontargetpath-property"></a>Session. TargetPath (propiedad)

La propiedad **TargetPath** del objeto de [**sesión**](session-object.md) es una propiedad de lectura y escritura que proporciona la ruta de acceso completa a la carpeta designada en la unidad de destino de la instalación.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Session.TargetPath
Session.TargetPath = propVal 
```



## <a name="property-value"></a>Valor de propiedad

Nombre obligatorio que distingue entre mayúsculas y minúsculas de una propiedad de carpeta según lo especificado por una clave principal de la [tabla de directorio](directory-table.md). Si la carpeta no existe, se genera un error.

## <a name="remarks"></a>Observaciones

No intente configurar la ruta de acceso de destino si los componentes que usan esas rutas ya están instalados para el usuario actual o para otro usuario. Compruebe la propiedad [**ProductState**](productstate.md) para determinar si el producto que contiene el componente está instalado.

Si se produce un error en la propiedad, puede obtener información de error extendida mediante el método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | El IID \_ ISession se define como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




