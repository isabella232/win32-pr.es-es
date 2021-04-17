---
description: La propiedad FileAttributes del objeto Installer devuelve un número que representa los atributos de archivo combinados para la ruta de acceso designada a un archivo o carpeta.
ms.assetid: a09ac346-4e4d-440f-bfbe-ff8fb3f69823
title: Installer. FileAttributes (propiedad, Windows. Storage. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653337"
---
# <a name="installerfileattributes-property"></a>Installer. FileAttributes (propiedad)

La propiedad **FileAttributes** del objeto [**Installer**](installer-object.md) devuelve un número que representa los atributos de archivo combinados para la ruta de acceso designada a un archivo o carpeta.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.FileAttributes
```



## <a name="property-value"></a>Valor de propiedad

La ruta de acceso necesaria para el archivo o la carpeta. Una ruta de acceso parcial supone el directorio actual.

## <a name="remarks"></a>Observaciones

La propiedad **FileAttributes** devuelve los valores siguientes.



| Atributo de archivo              | Value      | Value |
|-----------------------------|------------|-------|
| FILE\_ATTRIBUTE\_READONLY   | 0x00000001 | 1     |
| FILE\_ATTRIBUTE\_HIDDEN     | 0x00000002 | 2     |
| FILE\_ATTRIBUTE\_SYSTEM     | 0x00000004 | 4     |
| FILE\_ATTRIBUTE\_DIRECTORY  | 0x00000010 | 16    |
| atributo de archivo \_ \_ temporal  | 0x00000100 | 256   |
| FILE\_ATTRIBUTE\_COMPRESSED | 0x00000800 | 2048  |
| FILE\_ATTRIBUTE\_OFFLINE    | 0x00001000 | 4096  |



 

Devuelve – 1 si el archivo o la carpeta no existen o no se puede obtener acceso a ellos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Encabezado<br/>  | <dl> <dt>Windows. Storage. h</dt> </dl>                                                                                                                                                            |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




