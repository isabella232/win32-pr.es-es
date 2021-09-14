---
description: La propiedad TablePersistent del objeto Database devuelve el estado de persistencia de la tabla como uno de los parámetros siguientes.
ms.assetid: c395e99c-5cdc-4d7b-ac55-a79d4e1477dc
title: Database.TablePersistent, propiedad
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158630"
---
# <a name="databasetablepersistent-property"></a>Database.TablePersistent, propiedad

La **propiedad TablePersistent** del objeto [**Database**](database-object.md) devuelve el estado de persistencia de la tabla como uno de los parámetros siguientes.



| Estado de tabla               | Value | Descripción                    |
|---------------------------|-------|--------------------------------|
| msiEvaluateConditionFalse | 0     | La tabla es temporal.            |
| msiEvaluateConditionTrue  | 1     | La tabla es persistente.           |
| msiEvaluateConditionNone  | 2     | La tabla no está en la base de datos.  |
| msiEvaluateConditionError | 3     | Nombre de tabla no válido o que falta. |



 

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Database.TablePersistent
```



## <a name="property-value"></a>Valor de propiedad

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IDatabase se define como \_ 000C109D-0000-0000-C000-00000000046<br/>                                                                                                                                                                            |



 

 




