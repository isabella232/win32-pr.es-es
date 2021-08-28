---
description: 'Más información sobre: JetSetDatabaseSize (Función)'
title: JetSetDatabaseSize (Función)
TOCTitle: JetSetDatabaseSize Function
ms:assetid: 4a87bf43-c8f7-4966-9f1f-68c16d1cb558
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269242(v=EXCHG.10)
ms:contentKeyID: 32765544
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetDatabaseSizeW
- JetSetDatabaseSize
- JetSetDatabaseSizeA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 55a7625de4c8e1ef96740650313d3036cbb605f7
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988868"
---
# <a name="jetsetdatabasesize-function"></a>JetSetDatabaseSize (Función)


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jetsetdatabasesize-function"></a>JetSetDatabaseSize (Función)

La **función JetSetDatabaseSize** establece el tamaño de un archivo de base de datos sin abrir.

```cpp
    JET_ERR JET_API JetSetDatabaseSize(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szDatabaseName,
      __in          unsigned long cpg,
      __out         unsigned long* pcpgReal
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Identifica el contexto de sesión de base de datos que se usará para la llamada API.

*szDatabaseName*

Identifica el nombre del archivo de base de datos cuyo tamaño se va a modificar.

*Cpg*

Especifica el tamaño deseado de la base de datos, en páginas.

*pcpgReal*

Puntero a un número que recibe el tamaño de la base de datos, en páginas, después de la llamada API. Si la llamada API no se ha hecho correctamente, el contenido de *pcpgReal* no está definido.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el [JET_ERR](./jet-err.md) de datos con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and Error Handling [Parameters](./error-handling-parameters.md).


| <p>Código devuelto</p> | <p>Descripción</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>La operación se ha completado correctamente.</p> | 
| <p>JET_errDatabaseInconsistent<br />JET_errDatabaseDirtyShutdown</p> | <p>JET_errDatabaseInconsistent y JET_errDatabaseDirtyShutdown son el mismo valor numérico. La base de datos cuyo tamaño se va a ajustar debe estar en un apagado limpio, conocido como estado coherente. Una base de datos incoherente no está dañada, pero requiere la reproducción de archivos de registro.</p> | 
| <p>JET_errDatabaseInvalidPath</p> | <p><em>szDatabaseName</em> no debe ser una cadena vacía que no sea NULL.</p> | 
| <p>JET_errDiskFull</p> | <p>No hay suficiente espacio libre en el volumen para realizar la operación de crecimiento. <strong>JetSetDatabaseSize también</strong> puede devolver muchos errores relacionados con archivos, incluidos, entre otros:</p><ul><li><p>JET_errDiskIO</p></li><li><p>JET_errFileNotFound</p></li><li><p>JET_errInvalidPath</p></li><li><p>JET_errFileAccessDenied</p></li><li><p>JET_errOutOfFileHandles</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>Uno de los motivos por los que se puede devolver este error es si <em>cpg</em> cumple el tamaño mínimo de la base de datos. El tamaño mínimo actual de la base de datos es de 256 páginas.</p> | 
| <p>JET_errOutOfMemory</p> | <p>El sistema tiene pocos recursos de memoria.</p> | 



#### <a name="remarks"></a>Observaciones

Si **se llama a JetSetDatabaseSize** antes de insertar grandes cantidades de datos, el archivo de base de datos se crecerá en una sola operación. Esto reducirá la probabilidad de que el archivo de base de datos se fragmente en el nivel del sistema de archivos y también reducirá el número de veces que el archivo de base de datos tiene que crecer. El crecimiento del archivo de base de datos una vez puede ser más rápido que aumentarlo varias veces.

Actualmente solo se admite el crecimiento del archivo. Para reducir un archivo, use la característica de desfragmentación del esentutl.exe programa de utilidad.

Si *cpg* es menor que el tamaño actual de la base de datos, se omitirá la operación. Si *cpg es* menor que el tamaño mínimo de la base de datos (actualmente 256 páginas), devolverá JET_errInvalidParameter.

Para establecer el tamaño de una base de datos abierta, vea [JetGrowDatabase](./jetgrowdatabase-function.md).

Es posible que el tamaño del archivo no coincida con el número de páginas devueltas en *pcpgReal.* Hay dos páginas reservadas adicionales que no se pueden contar en *pcpgReal.*

#### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 
| <p><strong>Library</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requiere ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Se implementa como <strong>JetSetDatabaseSizeW</strong> (Unicode) y <strong>JetSetDatabaseSizeA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_OBJECTLIST](./jet-objectlist-structure.md)  
[JetGrowDatabase](./jetgrowdatabase-function.md)
