---
description: El método commit del objeto de base de datos finaliza el formulario persistente de la base de datos.
ms.assetid: 39253ccd-08f1-4a6f-87cb-3678ae5221a4
title: Database. Commit (método)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653862"
---
# <a name="databasecommit-method"></a>Database. Commit (método)

El método **commit** del objeto de [**base de datos**](database-object.md) finaliza el formulario persistente de la base de datos. Todos los datos persistentes se escriben en la base de datos grabable y no se escriben columnas ni filas temporales. Este método no tiene ningún efecto en una base de datos abierta como de solo lectura. Se puede llamar a este método varias veces para guardar el estado actual de las tablas cargadas en la memoria. Cuando se cierra la base de datos, se revierten los cambios realizados después de la última **confirmación** . Normalmente, se llama a este método antes de cerrarse cuando se han finalizado todos los cambios en la base de datos.

## <a name="syntax"></a>Sintaxis


```JScript
Database.Commit()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

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



 

 




