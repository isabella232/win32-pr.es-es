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
ms.openlocfilehash: 31bd306475460b03e9b4b5137cbd8fe214128dbec0dac516d2d9557de137a82f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075035"
---
# <a name="databaseimport-method"></a>Método Database.Import

El **método Import** del objeto [**Database**](database-object.md) importa una tabla de base de datos [de](text-archive-files.md)un archivo de texto y quita cualquier tabla existente.

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

Nombre necesario del archivo que se va a importar. Esto no incluye la carpeta , ya que debe establecerse en el objeto de ruta de acceso. El nombre de la tabla se especifica en el archivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Si se produce un error en el método , puede obtener información de error extendida mediante el [**método LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IDatabase se define como \_ 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Base de datos**](database-object.md)
</dt> <dt>

[**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)
</dt> </dl>

 

 




