---
description: El método Import del objeto Database importa una tabla de base de datos de un archivo de texto y quita cualquier tabla existente.
ms.assetid: 9ecc31d9-bccd-48cc-b205-9ce70aaf638a
title: Método Database.Import
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158640"
---
# <a name="databaseimport-method"></a>Método Database.Import

El **método Import** del objeto [**Database**](database-object.md) importa una tabla de base de datos de un archivo de [texto](text-archive-files.md)y quita cualquier tabla existente.

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

Carpeta obligatoria donde está presente el archivo de texto.

</dd> <dt>

*file* 
</dt> <dd>

Nombre obligatorio del archivo que se va a importar. Esto no incluye la carpeta , ya que debe establecerse en el objeto path. El nombre de la tabla se especifica en el archivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si se produce un error en el método , puede obtener información de error extendida mediante el [**método LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IDatabase se define como \_ 000C109D-0000-0000-C000-00000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Base de datos**](database-object.md)
</dt> <dt>

[**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)
</dt> </dl>

 

 




