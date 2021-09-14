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
ms.openlocfilehash: e9fbd5be6523db54be5f71b806bf278861f14709
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158645"
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

Nombre obligatorio de la tabla de base de datos. Distingue mayúsculas de minúsculas si se usa la base de datos del instalador.

</dd> <dt>

*path* 
</dt> <dd>

Cadena necesaria que es la ruta de acceso a la carpeta donde se coloca el archivo de texto.

</dd> <dt>

*file* 
</dt> <dd>

Nombre obligatorio del archivo que se va a crear. Esto no incluye la carpeta , ya que debe establecerse en el objeto path.

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



 

 




