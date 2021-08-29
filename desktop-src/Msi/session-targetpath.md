---
description: La propiedad TargetPath del objeto Session es una propiedad de lectura y escritura que proporciona la ruta de acceso completa a la carpeta designada en la unidad de destino de instalación.
ms.assetid: 563b874e-c669-4f5b-b3fa-eeb6b6e578f2
title: Propiedad Session.TargetPath
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
ms.openlocfilehash: bd265602e9a4d517ad01a07e79ace43722fcb6cfe0062091a5f0379a5ab264a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628755"
---
# <a name="sessiontargetpath-property"></a>Propiedad Session.TargetPath

La **propiedad TargetPath** del objeto [**Session**](session-object.md) es una propiedad de lectura y escritura que proporciona la ruta de acceso completa a la carpeta designada en la unidad de destino de instalación.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```JScript
propVal = Session.TargetPath
Session.TargetPath = propVal 
```



## <a name="property-value"></a>Valor de propiedad

Nombre obligatorio que distingue mayúsculas de minúsculas de una propiedad de carpeta, tal y como especifica una clave principal de la [tabla Directory](directory-table.md). Se genera un error si la carpeta no existe.

## <a name="remarks"></a>Comentarios

No intente configurar la ruta de acceso de destino si los componentes que usan esas rutas de acceso ya están instalados para el usuario actual o para otro usuario. Compruebe la [**propiedad ProductState**](productstate.md) para determinar si el producto que contiene el componente está instalado.

Si se produce un error en la propiedad , puede obtener información de error extendida mediante el [**método LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession se define como \_ 000C109E-0000-0000-C000-00000000046<br/>                                                                                                                                                                             |



 

 




