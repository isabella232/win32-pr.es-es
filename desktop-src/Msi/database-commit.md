---
description: El método Commit del objeto Database completa la forma persistente de la base de datos.
ms.assetid: 39253ccd-08f1-4a6f-87cb-3678ae5221a4
title: Método Database.Commit
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Commit
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d62c998a70e0a4a036695be10b2bf1d983044241
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158655"
---
# <a name="databasecommit-method"></a>Método Database.Commit

El **método Commit** del objeto [**Database**](database-object.md) completa la forma persistente de la base de datos. Todos los datos persistentes se escriben en la base de datos que se puede escribir y no se escriben columnas o filas temporales. Este método no tiene ningún efecto en una base de datos abierta como de solo lectura. Se puede llamar a este método varias veces para guardar el estado actual de las tablas cargadas en la memoria. Cuando la base de datos se cierra finalmente, se revierten los cambios realizados después de **la** última confirmación. Normalmente, se llama a este método antes del cierre cuando se han finalizado todos los cambios en la base de datos.

## <a name="syntax"></a>Sintaxis


```JScript
Database.Commit()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

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



 

 




