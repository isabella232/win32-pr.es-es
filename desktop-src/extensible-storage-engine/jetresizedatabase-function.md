---
description: 'Más información sobre: JetResizeDatabase (Función)'
title: JetResizeDatabase (Función)
TOCTitle: JetResizeDatabase Function
ms:assetid: b6420de7-acff-480e-838b-f0e5acc29c65
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835047(v=EXCHG.10)
ms:contentKeyID: 49894669
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetResizeDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f12fc06b915f5462c9209416cf54436ef3d7239b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126962760"
---
# <a name="jetresizedatabase-function"></a>JetResizeDatabase (Función)


_**Se aplica a:** Windows | Windows Servidor_

La **función JetResizeDatabase** amplía o reduce el tamaño de una base de datos que está abierta actualmente.

La **función JetResizeDatabase** se introdujo en el Windows 8 operativo.

``` c++
JET_ERR JET_API JetResizeDatabase(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in          unsigned long cpg,
  __out         unsigned long* pcpgActual,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se usará para la llamada API.

*Dbid*

Base de datos que se extenderá.

*Cpg*

Tamaño solicitado de la base de datos, en páginas.

*pcpgActual*

Puntero a un número que recibe el tamaño de la base de datos, en páginas, después de la llamada API. Si se produce un error en la llamada API, el contenido *del parámetro pcpgActual* no está definido.

*grbit*

Grupo de bits que especifica cero o más de los valores enumerados en la tabla siguiente.


| <p>Value</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitResizeDatabaseOnlyGrow</p> | <p>Aumentar solo la base de datos. Si la llamada de cambio de tamaño reduciría la base de datos, no haga nada.</p> | 



### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los códigos de retorno enumerados en la tabla siguiente. Para obtener más información sobre los posibles errores extensibles Storage Engine (ESE), vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errDiskFull</p> | <p>No hay suficiente espacio libre en el volumen para realizar la operación de crecimiento.</p> | 
| <p>JET_errDiskIO</p> | <p>La función <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a> devolvió un error relacionado con el archivo. Para obtener más información sobre otros errores relacionados con archivos que se pueden devolver, vea <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</p> | 



#### <a name="remarks"></a>Observaciones

Si se llama a la función **JetResizeDatabase** antes de insertar grandes cantidades de datos, el archivo de base de datos se crecerá en una sola operación. Esto reducirá la probabilidad de que el archivo de base de datos se fragmente en el nivel del sistema de archivos y también reducirá el número de veces que el archivo de base de datos tiene que crecer. El crecimiento del archivo de base de datos una vez puede ser más rápido que aumentarlo varias veces.

Para establecer el tamaño de una base de datos que no está abierta, vea [JetSetDatabaseSize](./jetsetdatabasesize-function.md).

Es posible que el tamaño del archivo no coincida con el número de páginas que se devuelven en el *parámetro pcpgReal.* Es posible que no se cuenten dos páginas reservadas adicionales en el *parámetro pcpgReal.*

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows 8.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2012.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>Archivo DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_OBJECTLIST](./jet-objectlist-structure.md)  
[JetSetDatabaseSize](./jetsetdatabasesize-function.md)
