---
description: La propiedad FileAttributes del objeto Installer devuelve un número que representa los atributos de archivo combinados para la ruta de acceso designada a un archivo o carpeta.
ms.assetid: a09ac346-4e4d-440f-bfbe-ff8fb3f69823
title: Propiedad Installer.FileAttributes (Windows.storage.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileAttributes
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7fe43028d856ca26b1c5e8fa21a88a3b77381670ccc044a79f10d3b922f38c21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630918"
---
# <a name="installerfileattributes-property"></a>Installer.FileAttributes, propiedad

La **propiedad FileAttributes** del objeto [**Installer**](installer-object.md) devuelve un número que representa los atributos de archivo combinados para la ruta de acceso designada a un archivo o carpeta.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.FileAttributes
```



## <a name="property-value"></a>Valor de propiedad

Ruta de acceso necesaria al archivo o carpeta. Una ruta de acceso parcial supone el directorio actual.

## <a name="remarks"></a>Observaciones

La **propiedad FileAttributes** devuelve los valores siguientes.



| Atributo file              | Value      | Value |
|-----------------------------|------------|-------|
| FILE\_ATTRIBUTE\_READONLY   | 0x00000001 | 1     |
| FILE\_ATTRIBUTE\_HIDDEN     | 0x00000002 | 2     |
| FILE\_ATTRIBUTE\_SYSTEM     | 0x00000004 | 4     |
| FILE\_ATTRIBUTE\_DIRECTORY  | 0x00000010 | 16    |
| FILE \_ ATTRIBUTE \_ TEMPORARY  | 0x00000100 | 256   |
| FILE\_ATTRIBUTE\_COMPRESSED | 0x00000800 | 2048  |
| FILE\_ATTRIBUTE\_OFFLINE    | 0x00001000 | 4096  |



 

Devuelve –1 si el archivo o carpeta no existe o no es accesible.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Header<br/>  | <dl> <dt>Windows.storage.h</dt> </dl>                                                                                                                                                            |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IInstaller de IID se define como \_ 000C1090-0000-0000-C000-00000000046<br/>                                                                                                                                                                           |



 

 




