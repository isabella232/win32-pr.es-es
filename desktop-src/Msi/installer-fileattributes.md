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
ms.openlocfilehash: e9a4d2b956c7d325fabcda7d6950274249120a0e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171653"
---
# <a name="installerfileattributes-property"></a>Installer.FileAttributes, propiedad

La **propiedad FileAttributes** del objeto [**Installer**](installer-object.md) devuelve un número que representa los atributos de archivo combinados para la ruta de acceso designada a un archivo o carpeta.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.FileAttributes
```



## <a name="property-value"></a>Valor de propiedad

Ruta de acceso necesaria al archivo o carpeta. Una ruta de acceso parcial asume el directorio actual.

## <a name="remarks"></a>Observaciones

La **propiedad FileAttributes** devuelve los valores siguientes.



| Atributo de archivo              | Value      | Value |
|-----------------------------|------------|-------|
| FILE\_ATTRIBUTE\_READONLY   | 0x00000001 | 1     |
| FILE\_ATTRIBUTE\_HIDDEN     | 0x00000002 | 2     |
| FILE\_ATTRIBUTE\_SYSTEM     | 0x00000004 | 4     |
| FILE\_ATTRIBUTE\_DIRECTORY  | 0x00000010 | 16    |
| ATRIBUTO \_ DE \_ ARCHIVO TEMPORAL  | 0x00000100 | 256   |
| FILE\_ATTRIBUTE\_COMPRESSED | 0x00000800 | 2048  |
| FILE\_ATTRIBUTE\_OFFLINE    | 0x00001000 | 4096  |



 

Devuelve –1 si el archivo o carpeta no existe o no es accesible.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Encabezado<br/>  | <dl> <dt>Windows.storage.h</dt> </dl>                                                                                                                                                            |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller se define como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




