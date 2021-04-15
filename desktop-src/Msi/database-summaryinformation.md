---
description: La propiedad SummaryInformation del objeto de base de datos devuelve un objeto SummaryInfo que se puede usar para examinar, actualizar y agregar propiedades a la secuencia de información de resumen.
ms.assetid: 6892a8c0-c99e-4dcb-b6cb-d470ffceab69
title: Propiedad Database. SummaryInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.SummaryInformation
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 524c4fa2fe5014436f122f0a5460aced820e30ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653982"
---
# <a name="databasesummaryinformation-property"></a>Propiedad Database. SummaryInformation

La propiedad **SummaryInformation** del objeto de [**base de datos**](database-object.md) devuelve un objeto [**SummaryInfo**](summaryinfo-object.md) que se puede usar para examinar, actualizar y agregar propiedades a la secuencia de [información de Resumen](summary-information-stream.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Database.SummaryInformation
```



## <a name="property-value"></a>Valor de propiedad

Número máximo de propiedades que se van a agregar o modificar. Este parámetro es necesario y se usa para asignar suficiente memoria de trabajo durante la generación del flujo. No es necesario almacenar este número de propiedades. Se debe utilizar un valor de cero si la base de datos se abre como de solo lectura para evitar que se actualice la secuencia.

## <a name="remarks"></a>Observaciones

Si se usa un valor de *maxProperties* mayor que 0 para abrir una secuencia de información de Resumen existente, se debe llamar al método [**Persist**](summaryinfo-persist.md) antes de cerrar el objeto. Si no lo hace, perderá la información de la secuencia existente.

Si se produce un error en la propiedad, puede obtener información de error extendida mediante el método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase se define como 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




