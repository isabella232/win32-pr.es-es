---
description: El método FileVersion del objeto Installer devuelve la cadena de versión o la cadena de idioma de la ruta de acceso especificada en path con el formato en el que el instalador espera encontrarlos en la base de datos.
ms.assetid: 387cf269-5a7a-476b-811e-d576da1c752f
title: Installer. FileVersion (método)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653332"
---
# <a name="installerfileversion-method"></a>Installer. FileVersion (método)

El método **fileversion** del objeto [**Installer**](installer-object.md) devuelve la cadena de versión o la cadena de idioma de la ruta de acceso especificada en *path* con el formato en el que el instalador espera encontrarlos en la base de datos. En el caso de las versiones, se trata de una cadena con el \# formato ". \# . \# . \# ". En idioma, es el identificador de idioma decimal.

## <a name="syntax"></a>Sintaxis


```JScript
Installer.FileVersion(
  Path,
  Language
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Ruta de acceso* 
</dt> <dd>

Cadena requerida que contiene la ruta de acceso al archivo.

</dd> <dt>

*Lenguaje* 
</dt> <dd>

Marca que designa si el valor devuelto es un identificador de idioma o una cadena de versión. TRUE devuelve el idioma, FALSE devuelve la versión. Este parámetro es opcional y su valor predeterminado es FALSE.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




