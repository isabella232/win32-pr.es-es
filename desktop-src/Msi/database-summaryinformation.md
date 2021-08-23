---
description: La propiedad SummaryInformation del objeto Database devuelve un objeto SummaryInfo que se puede usar para examinar, actualizar y agregar propiedades al flujo de información de resumen.
ms.assetid: 6892a8c0-c99e-4dcb-b6cb-d470ffceab69
title: Database.SummaryInformation, propiedad
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
ms.openlocfilehash: cf181b35457b8f4be5737bfa31cf284d86ed21f48800dcab6044cef444a5b640
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947582"
---
# <a name="databasesummaryinformation-property"></a>Database.SummaryInformation, propiedad

La **propiedad SummaryInformation** del objeto [**Database**](database-object.md) devuelve un objeto [**SummaryInfo**](summaryinfo-object.md) que se puede usar para examinar, actualizar y agregar propiedades al flujo de información [de resumen](summary-information-stream.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Database.SummaryInformation
```



## <a name="property-value"></a>Valor de propiedad

Número máximo de propiedades que se van a agregar o modificar. Este parámetro es necesario y se usa para asignar suficiente memoria de trabajo durante la generación de secuencias. No es necesario almacenar este número de propiedades. Se debe usar un valor de cero si la base de datos se abre de solo lectura para evitar que se actualice la secuencia.

## <a name="remarks"></a>Comentarios

Si se usa un valor de *maxProperties* mayor que 0 para abrir un flujo de información de resumen existente, se debe llamar al método [**Persist**](summaryinfo-persist.md) antes de cerrar el objeto. Si no lo hace, perderá la información de flujo existente.

Si se produce un error en la propiedad , puede obtener información de error extendida mediante el [**método LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IDatabase se define como \_ 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




