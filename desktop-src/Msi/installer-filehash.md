---
description: El método FileHash del objeto Installer toma la ruta de acceso a un archivo y devuelve un hash de 128 bits de ese archivo. La información de hash de archivo se devuelve como un objeto de registro. Todo el hash de archivo de 128 bits se devuelve como campos de propiedades IntegerData de 4 32 bits.
ms.assetid: 065ffde1-4d7c-4e71-9315-7926d4cd38ed
title: Instalador. FileHash (método)
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
ms.openlocfilehash: 1a38ef741c5c3a33c526cc78fbdc4551716ed3ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653336"
---
# <a name="installerfilehash-method"></a>Instalador. FileHash (método)

El método **FileHash** del [**objeto Installer**](installer-object.md) toma la ruta de acceso a un archivo y devuelve un hash de 128 bits de ese archivo. La información de hash de archivo se devuelve como un [**objeto de registro**](record-object.md). Todo el hash de archivo de 128 bits se devuelve como campos de propiedades [**IntegerData**](record-integerdata.md) de 4 32 bits.

Los valores devueltos en el [**objeto de registro**](record-object.md) se corresponden con los cuatro campos de la estructura [**MSIFILEHASHINFO**](/windows/desktop/api/Msi/ns-msi-msifilehashinfo) devuelta por [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha). La numeración de cuatro campos se basa en 1 en la [tabla MsiFileHash](msifilehash-table.md).

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

Ruta de acceso al archivo al que se va a aplicar un algoritmo hash.

</dd> <dt>

*Opciones* 
</dt> <dd>

Reservado para uso futuro.

El valor de este parámetro debe ser 0 (cero).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si es correcto, este método devuelve un [**objeto de registro**](record-object.md) que contiene el hash del archivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Control de versiones de archivo predeterminado](default-file-versioning.md)
</dt> <dt>

[Administrar versiones y tamaños de archivo](manage-file-sizes-and-versions.md)
</dt> <dt>

[Tabla MsiFileHash](msifilehash-table.md)
</dt> <dt>

[**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)
</dt> </dl>

 

 




