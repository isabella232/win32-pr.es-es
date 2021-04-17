---
description: 'Más información acerca de: JetCreateIndex (función)'
title: Función JetCreateIndex
TOCTitle: JetCreateIndex Function
ms:assetid: d164e74a-7719-4587-9059-8fb18b365133
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294099(v=EXCHG.10)
ms:contentKeyID: 32765714
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndexA
- JetCreateIndex
- JetCreateIndexW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c0208a5f0adac4ff5128b506123f3b68589cd0d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716166"
---
# <a name="jetcreateindex-function"></a>Función JetCreateIndex


_**Se aplica a:** Windows | Windows Server_

## <a name="jetcreateindex-function"></a>Función JetCreateIndex

La función **JetCreateIndex** le permite crear un índice de datos en una base de datos del motor de almacenamiento extensible (ese), que puede usar para buscar datos específicos rápidamente.

```cpp
    JET_ERR JET_API JetCreateIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szIndexName,
      __in          JET_GRBIT grbit,
      __in          const tchar* szKey,
      __in          unsigned long cbKey,
      __in          unsigned long lDensity
    );
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se va a usar para una llamada de API determinada.

*TABLEID*

Tabla para la que se creará un índice.

*szIndexName*

Puntero a una cadena terminada en null que especifica el nombre del índice que se va a crear.

El nombre del índice debe cumplir las siguientes directrices:

  - Debe contener menos caracteres que JET_cbNameMost, sin incluir el carácter nulo de terminación.

  - Solo debe contener caracteres de las categorías siguientes: de 0 a 9, de la a a la Z, de la a a la z y de todos los caracteres de puntuación, excepto " \! " (signo de exclamación), "," (coma), " \[ " (corchete de apertura) y " \] " (corchete de cierre); es decir, los caracteres ASCII 0x20, 0x22 a 0x2d, 0x2f a 0x5a, 0x5c y 0x5d a 0x7F.

  - No debe comenzar con un espacio.

  - Debe contener al menos un carácter que no sea un espacio.

*grbit*

Grupo de bits que contiene las opciones que se van a utilizar para una llamada determinada. Este parámetro puede incluir cero o más de las opciones que se encuentran en la estructura [JET_INDEXCREATE](./jet-indexcreate-structure.md) .

*szKey*

Un puntero a una cadena doble terminada en NULL de tokens delimitados por null.

Para obtener más información sobre este parámetro, vea la estructura [JET_INDEXCREATE](./jet-indexcreate-structure.md) .

*cbKey*

La longitud, en bytes, del parámetro *szKey* , incluidos los dos caracteres nulos de terminación.

*lDensity*

Densidad porcentual del árbol B + del índice inicial.

Para obtener más información sobre este parámetro, vea la estructura [JET_INDEXCREATE](./jet-indexcreate-structure.md) .

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el tipo de datos [JET_ERR](./jet-err.md) con uno de los códigos de retorno que se enumeran en la tabla siguiente. Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Código de retorno</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>La operación se ha completado correctamente.</p></td>
</tr>
</tbody>
</table>


Para obtener una lista de errores adicionales que pueden ser devueltos por la función **JetCreateIndex** , vea [JetCreateIndex2](./jetcreateindex2-function.md).

#### <a name="remarks"></a>Observaciones

Llamar a la función **JetCreateIndex** es idéntico a llamar a la función [JetCreateIndex2](./jetcreateindex2-function.md) con una estructura [JET_INDEXCREATE](./jet-indexcreate-structure.md) que contiene la misma configuración que los parámetros de **JetCreateIndex** y un parámetro *cIndexCreate* igual a 1. En el caso de los campos de la estructura [JET_INDEXCREATE](./jet-indexcreate-structure.md) que no tienen los parámetros correspondientes en **JetCreateIndex**, se supone un valor de 0.

Tenga en cuenta que **JetCreateIndex** se ha reemplazado por [JetCreateIndex2](./jetcreateindex2-function.md).

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Remoto</p></td>
<td><p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p>Servidor</p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p>Encabezado</p></td>
<td><p>Se declara en esent. h.</p></td>
</tr>
<tr class="even">
<td><p>Biblioteca</p></td>
<td><p>Utiliza ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p>Archivo DLL</p></td>
<td><p>Requiere ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p>Unicode</p></td>
<td><p>Se implementa como <strong>JetCreateIndexW</strong> (Unicode) y <strong>JetCreateIndexA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte también

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
