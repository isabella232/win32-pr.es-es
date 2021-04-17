---
description: El método Import del objeto de base de datos importa una tabla de base de datos de un archivo de almacenamiento de texto, quitando cualquier tabla existente.
ms.assetid: 9ecc31d9-bccd-48cc-b205-9ce70aaf638a
title: Database. Import (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Import
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b931b77e6cf736bc291079532d20d9c6b48dd243
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670794"
---
# <a name="databaseimport-method"></a>Database. Import (método)

El método **Import** del objeto de [**base de datos**](database-object.md) importa una tabla de base de datos de un archivo de almacenamiento de [texto](text-archive-files.md), quitando cualquier tabla existente.

## <a name="syntax"></a>Sintaxis


```JScript
Database.Import(
  path,
  file
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*path* 
</dt> <dd>

Carpeta requerida en la que está presente el archivo de texto.

</dd> <dt>

*file* 
</dt> <dd>

Nombre necesario del archivo que se va a importar. Esto no incluye la carpeta, ya que se debe establecer en el objeto de ruta de acceso. El nombre de la tabla se especifica en el archivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si se produce un error en el método, puede obtener información de error extendida mediante el método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase se define como 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Base de datos**](database-object.md)
</dt> <dt>

[**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)
</dt> </dl>

 

 




