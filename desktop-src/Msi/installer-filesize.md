---
description: El método FileSize del objeto Installer usa llamadas API de Win32 para devolver el tamaño del archivo especificado en Path.
ms.assetid: d7119e5e-9315-4b20-a904-bc1104f3a4e4
title: Installer.FileSize (método)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072152"
---
# <a name="installerfilesize-method"></a>Installer.FileSize (método)

El **método FileSize** del objeto [**Installer**](installer-object.md) usa llamadas API de Win32 para devolver el tamaño del archivo especificado en *Path*.

## <a name="syntax"></a>Sintaxis


```JScript
Installer.FileSize(
  Path
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Path* 
</dt> <dd>

Cadena necesaria que contiene la ruta de acceso al archivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IInstaller de IID se define como \_ 000C1090-0000-0000-C000-00000000046<br/>                                                                                                                                                                           |



 

 




