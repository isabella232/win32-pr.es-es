---
description: 'Más información acerca de: JetGrowDatabase (función)'
title: JetGrowDatabase función)
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
ms.openlocfilehash: 9ed8ee9888a2e4ab7908b72cc071f7b8143ca6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648423"
---
# <a name="jetgrowdatabase-function"></a>JetGrowDatabase función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetgrowdatabase-function"></a>JetGrowDatabase función)

La función **JetGrowDatabase** extiende el tamaño de una base de datos que está abierta actualmente.

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

Contexto de sesión de base de datos que se va a usar para la llamada API.

*DBID*

La base de datos que se extenderá.

*CPG*

Tamaño deseado de la base de datos, en páginas.

*pcpgReal*

Puntero a un número que recibe el tamaño de la base de datos, en páginas, después de la llamada a la API. Si se produce un error en la llamada API, el contenido de *pcpgReal* no está definido.

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
<td><p>JET_errDiskFull</p></td>
<td><p>No hay suficiente espacio disponible en el volumen para realizar la operación de crecimiento.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDiskIO</p></td>
<td><p><a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>devolvió un error relacionado con el archivo. Para obtener más información sobre otros errores relacionados con archivos que podrían devolverse, vea <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Observaciones

Si se llama a **JetGrowDatabase** antes de insertar grandes cantidades de datos, el archivo de base de datos se incrementará en una sola operación. Esto reducirá la probabilidad de que el archivo de base de datos se fragmente en el nivel del sistema de archivos y también reduce el número de veces que el archivo de base de datos tiene que crecer. El crecimiento del archivo de base de datos una vez puede ser más rápido que crecer varias veces.

Actualmente solo se admite el crecimiento del archivo. Para reducir un archivo, use la característica de desfragmentación del programa **esentutl.exe** Utility.

Para establecer el tamaño de una base de datos que no está abierta, vea [JetSetDatabaseSize](./jetsetdatabasesize-function.md).

El tamaño del archivo podría no coincidir con el número de páginas que se devuelven en *pcpgReal*. Hay dos páginas reservadas adicionales que podrían no contarse en *pcpgReal*.

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
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_OBJECTLIST](./jet-objectlist-structure.md)  
[JetSetDatabaseSize](./jetsetdatabasesize-function.md)
