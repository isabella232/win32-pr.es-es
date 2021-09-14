---
description: El método GenerateTransform del objeto Database crea una transformación que, cuando se aplica a la base de datos de objetos, da como resultado la base de datos de referencia. La transformación se almacena en el objeto de almacenamiento.
ms.assetid: 51cd70a0-6eda-4ca6-b468-9cb36ad942f8
title: Método Database.GenerateTransform
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.GenerateTransform
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5f7fca94c0765722dc2d0b21524c15265f99e7b0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158641"
---
# <a name="databasegeneratetransform-method"></a>Método Database.GenerateTransform

El **método GenerateTransform** del objeto [**Database**](database-object.md) crea una [*transformación*](t-gly.md) que, cuando se aplica a la base de datos de objetos, da como resultado la base de datos de referencia. La transformación se almacena en el objeto de almacenamiento.

Si la transformación se va a aplicar durante una instalación, debe usar el [**método CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md) para rellenar el flujo de información de resumen.

## <a name="syntax"></a>Sintaxis


```JScript
Database.GenerateTransform(
  reference,
  storage
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*reference* 
</dt> <dd>

Base de datos necesaria que no incluye los cambios.

</dd> <dt>

*storage* 
</dt> <dd>

Nombre del archivo de transformación generado. Esta información es opcional.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Una transformación puede agregar columnas de clave no principal al final de una tabla. No se puede crear una transformación que agrega columnas de clave principal a una tabla. No se puede crear una transformación que cambie el orden, los nombres o las definiciones de las columnas.

Este método devuelve un valor booleano. Devuelve TRUE si se genera una transformación. Devuelve FALSE si no se genera una transformación porque no hay diferencias entre las dos bases de datos. Si se produce un error en el método, genera un error.

Si se produce un error en el método , puede obtener información de error extendida mediante el [**método LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IDatabase se define como \_ 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Base de datos**](database-object.md)
</dt> <dt>

[Transformaciones de base de datos](database-transforms.md)
</dt> </dl>

 

 




