---
description: El método de archivo del objeto de instalador utiliza las llamadas de la API Win32 para devolver el tamaño del archivo especificado en la ruta de acceso.
ms.assetid: d7119e5e-9315-4b20-a904-bc1104f3a4e4
title: Installer. método de archivo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileSize
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 593319b88e3942ae6caa1399adbe2e596bf6e737
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653333"
---
# <a name="installerfilesize-method"></a>Installer. método de archivo

El **método de archivo del** objeto de [**instalador**](installer-object.md) utiliza las llamadas de la API Win32 para devolver el tamaño del archivo especificado en la *ruta de acceso*.

## <a name="syntax"></a>Sintaxis


```JScript
Installer.FileSize(
  Path
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Ruta de acceso* 
</dt> <dd>

Cadena requerida que contiene la ruta de acceso al archivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




