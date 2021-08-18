---
description: El método FileHash del objeto Installer toma la ruta de acceso a un archivo y devuelve un hash de 128 bits de ese archivo. La información hash del archivo se devuelve como un objeto Record. El hash de archivo de 128 bits completo se devuelve como cuatro campos de propiedad IntegerData de 32 bits.
ms.assetid: 065ffde1-4d7c-4e71-9315-7926d4cd38ed
title: Installer.FileHash (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileHash
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a2da76ef3f0606002e26e8c320f83ca45e46bbbeb573d509c235c9fca8932247
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630796"
---
# <a name="installerfilehash-method"></a>Installer.FileHash (método)

El **método FileHash** del objeto [**Installer**](installer-object.md) toma la ruta de acceso a un archivo y devuelve un hash de 128 bits de ese archivo. La información hash del archivo se devuelve como un [**objeto Record**](record-object.md). El hash de archivo de 128 bits completo se devuelve como cuatro campos de propiedad [**IntegerData de**](record-integerdata.md) 32 bits.

Los valores devueltos en [**el objeto Record corresponden**](record-object.md) a los cuatro campos de la estructura [**MSIFILEHASHINFO**](/windows/desktop/api/Msi/ns-msi-msifilehashinfo) devuelta [**por MsiGetFileHash.**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) La numeración de cuatro campos se basa en 1 en la [tabla MsiFileHash](msifilehash-table.md).

-   El campo 1 corresponde a la columna HashPart1.
-   El campo 2 corresponde a la columna HashPart2.
-   El campo 3 corresponde a la columna HashPart3.
-   El campo 4 corresponde a la columna HashPart4.

## <a name="syntax"></a>Sintaxis


```JScript
Installer.FileHash(
  FilePath,
  Options
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FilePath* 
</dt> <dd>

Ruta de acceso al archivo que se va a hash.

</dd> <dt>

*Opciones* 
</dt> <dd>

Reservado para uso futuro.

El valor de este parámetro debe ser 0 (cero).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, este método devuelve un [**objeto Record**](record-object.md) que contiene el hash del archivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller se define como \_ 000C1090-0000-0000-C000-00000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Control de versiones de archivo predeterminado](default-file-versioning.md)
</dt> <dt>

[Administrar tamaños y versiones de archivos](manage-file-sizes-and-versions.md)
</dt> <dt>

[Tabla MsiFileHash](msifilehash-table.md)
</dt> <dt>

[**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)
</dt> </dl>

 

 




