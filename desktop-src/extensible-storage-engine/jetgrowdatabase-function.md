---
description: 'Más información sobre: JetGrowDatabase (Función)'
title: JetGrowDatabase (Función)
TOCTitle: JetGrowDatabase Function
ms:assetid: d9719991-6c80-4dcb-a1d6-f0c7de61f459
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294109(v=EXCHG.10)
ms:contentKeyID: 32765724
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGrowDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 710e41b29c55ec435db6eb1b9e1536740819478e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479071"
---
# <a name="jetgrowdatabase-function"></a>JetGrowDatabase (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetgrowdatabase-function"></a>JetGrowDatabase (Función)

La **función JetGrowDatabase** amplía el tamaño de una base de datos que está abierta actualmente.

```cpp
    JET_ERR JET_API JetGrowDatabase(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          unsigned long cpg,
      __in          unsigned long* pcpgReal
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se usará para la llamada API.

*Dbid*

Base de datos que se extenderá.

*Cpg*

Tamaño deseado de la base de datos, en páginas.

*pcpgReal*

Puntero a un número que recibe el tamaño de la base de datos, en páginas, después de la llamada API. Si se produce un error en la llamada API, el contenido de *pcpgReal* no está definido.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errDiskFull</p> | <p>No hay suficiente espacio libre en el volumen para realizar la operación de crecimiento.</p> | 
| <p>JET_errDiskIO</p> | <p><a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>devolvió un error relacionado con el archivo . Para obtener más información sobre otros errores relacionados con archivos que se pueden devolver, vea <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</p> | 



#### <a name="remarks"></a>Comentarios

Si **se llama a JetGrowDatabase** antes de insertar grandes cantidades de datos, el archivo de base de datos se crecerá en una sola operación. Esto reducirá la probabilidad de que el archivo de base de datos se fragmente en el nivel del sistema de archivos y también reducirá el número de veces que el archivo de base de datos tiene que crecer. El crecimiento del archivo de base de datos una vez puede ser más rápido que aumentarlo varias veces.

Actualmente solo se admite el crecimiento del archivo. Para reducir un archivo, use la característica de desfragmentación delesentutl.exeprograma **de** utilidad.

Para establecer el tamaño de una base de datos que no está abierta, vea [JetSetDatabaseSize](./jetsetdatabasesize-function.md).

Es posible que el tamaño del archivo no coincida con el número de páginas que se devuelven en *pcpgReal.* Hay dos páginas reservadas adicionales que podrían no contarse en *pcpgReal.*

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | | <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_OBJECTLIST](./jet-objectlist-structure.md)  
[JetSetDatabaseSize](./jetsetdatabasesize-function.md)
