---
description: El método FileVersion del objeto Installer devuelve la cadena de versión o la cadena de idioma de la ruta de acceso especificada en Ruta de acceso con el formato en el que el instalador espera encontrarlos en la base de datos.
ms.assetid: 387cf269-5a7a-476b-811e-d576da1c752f
title: Installer.FileVersion (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileVersion
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a36a92b42815a1b2df913ba6bd9f687cdd1b609b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072150"
---
# <a name="installerfileversion-method"></a>Installer.FileVersion (método)

El **método FileVersion** del objeto [**Installer**](installer-object.md) devuelve la cadena de versión o la cadena de idioma de la ruta de acceso especificada en *Ruta* de acceso con el formato en el que el instalador espera encontrarlos en la base de datos. En el caso de las versiones, se trata de una cadena con el formato \# " . . " \# \# \# . En el caso del idioma, este es el identificador de idioma decimal.

## <a name="syntax"></a>Sintaxis


```JScript
Installer.FileVersion(
  Path,
  Language
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Path* 
</dt> <dd>

Cadena necesaria que contiene la ruta de acceso al archivo.

</dd> <dt>

*Lenguaje* 
</dt> <dd>

Marca para designar si el valor devuelto es un identificador de idioma o una cadena de versión. TRUE devuelve el idioma, FALSE devuelve la versión. Este parámetro es opcional, con un valor predeterminado de FALSE.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IInstaller de IID se define como \_ 000C1090-0000-0000-C000-00000000046<br/>                                                                                                                                                                           |



 

 




