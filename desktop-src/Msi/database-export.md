---
description: El método Export del objeto Database copia la estructura y los datos de una tabla especificada en un archivo de archivo de texto.
ms.assetid: b724595f-ef28-456e-bf0b-5df65c659d17
title: Método Database.Export
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Export
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: faa5e2459eb0fe4ba04fd548bc478c9a0e2c85267e1df8e3d318f4a3f6a082ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745615"
---
# <a name="databaseexport-method"></a>Método Database.Export

El **método Export** del objeto [**Database**](database-object.md) copia la estructura y los datos de una tabla especificada en un archivo de archivo [de texto.](text-archive-files.md)

## <a name="syntax"></a>Sintaxis


```JScript
Database.Export(
  table,
  path,
  file
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*table* 
</dt> <dd>

Nombre necesario de la tabla de base de datos. Distingue mayúsculas de minúsculas si se usa la base de datos del instalador.

</dd> <dt>

*path* 
</dt> <dd>

Cadena necesaria que es la ruta de acceso a la carpeta donde se coloca el archivo de texto.

</dd> <dt>

*file* 
</dt> <dd>

Nombre necesario del archivo que se va a crear. Esto no incluye la carpeta , ya que debe establecerse en el objeto de ruta de acceso.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Si se produce un error en el método , puede obtener información de error extendida mediante el [**método LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IDatabase se define como \_ 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




