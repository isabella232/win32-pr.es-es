---
description: 'Más información acerca de: JetSetDatabaseSize (función)'
title: JetSetDatabaseSize función)
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
ms.openlocfilehash: cd450a0afed0256b0b80d97a278dccf99418a900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153763"
---
# <a name="jetsetdatabasesize-function"></a>JetSetDatabaseSize función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetsetdatabasesize-function"></a>JetSetDatabaseSize función)

La función **JetSetDatabaseSize** establece el tamaño de un archivo de base de datos no abierto.

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

Identifica el contexto de la sesión de base de datos que se va a usar para la llamada API.

*szDatabaseName*

Identifica el nombre del archivo de base de datos cuyo tamaño se va a modificar.

*CPG*

Especifica el tamaño deseado de la base de datos, en páginas.

*pcpgReal*

Puntero a un número que recibe el tamaño de la base de datos, en páginas, después de la llamada a la API. Si la llamada a la API no se ha realizado correctamente, el contenido de *pcpgReal* no está definido.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Código devuelto</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>La operación se ha completado correctamente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInconsistent<br />
JET_errDatabaseDirtyShutdown</p></td>
<td><p>JET_errDatabaseInconsistent y JET_errDatabaseDirtyShutdown son el mismo valor numérico. La base de datos cuyo tamaño se va a ajustar debe estar en un cierre correcto, conocido como estado coherente. Una base de datos incoherente no está dañada, pero requiere que se reproduzcan los archivos de registro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInvalidPath</p></td>
<td><p><em>szDatabaseName</em> no debe ser una cadena vacía, que no sea NULL.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDiskFull</p></td>
<td><p>No hay suficiente espacio disponible en el volumen para realizar la operación de crecimiento. <strong>JetSetDatabaseSize</strong> también puede devolver muchos errores relacionados con archivos, incluidos, entre otros, los siguientes:</p>
<ul>
<li><p>JET_errDiskIO</p></li>
<li><p>JET_errFileNotFound</p></li>
<li><p>JET_errInvalidPath</p></li>
<li><p>JET_errFileAccessDenied</p></li>
<li><p>JET_errOutOfFileHandles</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Uno de los motivos por los que se puede devolver este error es si <em>CPG</em> cumple el tamaño mínimo de la base de datos. El tamaño mínimo de la base de datos actual es 256 páginas.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>El sistema tiene pocos recursos de memoria.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Observaciones

Si se llama a **JetSetDatabaseSize** antes de insertar grandes cantidades de datos, el archivo de base de datos se incrementará en una sola operación. Esto reducirá la probabilidad de que el archivo de base de datos se fragmente en el nivel del sistema de archivos y también reduce el número de veces que el archivo de base de datos tiene que crecer. El crecimiento del archivo de base de datos una vez puede ser más rápido que crecer varias veces.

Actualmente solo se admite el crecimiento del archivo. Para reducir un archivo, use la característica de desfragmentación del programa esentutl.exe Utility.

Si *CPG* es menor que el tamaño actual de la base de datos, se omitirá la operación. Si *CPG* es menor que el tamaño mínimo de la base de datos (actualmente 256 páginas), devolverá JET_errInvalidParameter.

Para establecer el tamaño de una base de datos que se abre, vea [JetGrowDatabase](./jetgrowdatabase-function.md).

Es posible que el tamaño del archivo no coincida con el número de páginas devueltas en *pcpgReal*. Hay dos páginas reservadas adicionales que pueden no contarse en *pcpgReal*.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en esent. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Library</strong></p></td>
<td><p>Use ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requiere ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Se implementa como <strong>JetSetDatabaseSizeW</strong> (Unicode) y <strong>JetSetDatabaseSizeA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_OBJECTLIST](./jet-objectlist-structure.md)  
[JetGrowDatabase](./jetgrowdatabase-function.md)
