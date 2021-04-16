---
description: La propiedad TablePersistent del objeto de base de datos devuelve el estado de persistencia de la tabla como uno de los parámetros siguientes.
ms.assetid: c395e99c-5cdc-4d7b-ac55-a79d4e1477dc
title: Propiedad Database. TablePersistent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.TablePersistent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1a1e91e1c01ca3fe2efc45855583031e84dc2b47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671679"
---
# <a name="databasetablepersistent-property"></a>Propiedad Database. TablePersistent

La propiedad **TablePersistent** del objeto de [**base de datos**](database-object.md) devuelve el estado de persistencia de la tabla como uno de los parámetros siguientes.



| Estado de tabla               | Value | Descripción                    |
|---------------------------|-------|--------------------------------|
| msiEvaluateConditionFalse | 0     | La tabla es temporal.            |
| msiEvaluateConditionTrue  | 1     | La tabla es persistente.           |
| msiEvaluateConditionNone  | 2     | La tabla no está en la base de datos.  |
| msiEvaluateConditionError | 3     | Falta el nombre de tabla o no es válido. |



 

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Database.TablePersistent
```



## <a name="property-value"></a>Valor de propiedad

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase se define como 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




