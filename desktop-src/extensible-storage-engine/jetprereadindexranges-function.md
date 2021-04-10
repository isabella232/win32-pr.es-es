---
description: 'Más información acerca de: JetPrereadIndexRanges (función)'
title: JetPrereadIndexRanges función)
TOCTitle: JetPrereadIndexRanges Function
ms:assetid: ab49abcc-eaeb-438f-8e6d-b08bc94d7bc3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835045(v=EXCHG.10)
ms:contentKeyID: 49894667
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetPrereadIndexRanges
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7cfdd8d25f7008f5fa854cbee32b54fa01942ce2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153769"
---
# <a name="jetprereadindexranges-function"></a>JetPrereadIndexRanges función)


_**Se aplica a:** Windows | Windows Server_

La función **JetPrereadIndexRanges** prelee los índices para mejorar el rendimiento.

La función **JetPrereadIndexRanges** se presentó en el sistema operativo Windows 8.

``` c++
JET_ERR JetPrereadIndexRanges(
  __in          const JET_SESID sesid,
  __in          const JET_TABLEID tableid,
  __in_ecount(cIndexRanges)  const JET_INDEX_RANGE* const rgIndexRanges,
  __in          const unsigned long cIndexRanges,
  __out_opt     unsigned long* const pcRangesPreread,
  __in_ecount(ccolumnidPreread)  const JET_COLUMNID* const rgcolumnidPreread,
  __in          const unsigned long ccolumnidPreread,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se va a usar para la llamada API.

*TABLEID*

Tabla en la que se van a emitir las lecturas preleídas.

*rgIndexRanges*

Intervalos de clave que se van a leer como preleídos.

*cIndexRanges*

Número de intervalos de clave que se van a leer antes, determinado por el número de elementos de *rgIndexRanges*.

*pcRangesPreread*

Número de intervalos de clave que se leyeron realmente.

*rgcolumnidPreread*

Lista de identificadores de columna para las columnas de valor largo que se van a leer como prelectura. De forma predeterminada, solo se prelee el registro en la página. Si es necesario realizar una lectura de las columnas de valores largos fuera de la página, es necesario pasar los identificadores de columna a través de este parámetro.

*ccolumnidPreread*

El número de identificadores de columna para las columnas de valor largo que se van a leer de forma predeterminada, determinado por el número de elementos de *rgcolumnidPreread*.

*grbit*

Grupo de bits que especifica cero o más de los valores de dirección de prelectura enumerados en la tabla siguiente.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Value</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Adelante</p></td>
<td><p>Avance de prelectura.</p></td>
</tr>
<tr class="even">
<td><p>Atrás</p></td>
<td><p>Lectura anterior.</p></td>
</tr>
<tr class="odd">
<td><p>FirstPageOnly</p></td>
<td><p>Preread solo la primera página de cualquier columna de tipo Long.</p></td>
</tr>
<tr class="even">
<td><p>NormalizedKey</p></td>
<td><p>Clave/marcador normalizado proporcionado en lugar de valor de columna.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valor devuelto

Esta función devuelve el tipo de datos [JET_ERR](./jet-err.md) con uno de los códigos de retorno que se enumeran en la tabla siguiente. Para obtener más información sobre los posibles errores del motor de almacenamiento extensible (ESE), vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).

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
</tbody>
</table>


#### <a name="remarks"></a>Observaciones

Si los registros con los intervalos de claves especificados no están en la caché del búfer, debe iniciar lecturas asincrónicas para traer los registros a la memoria caché del búfer de la base de datos.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2012.</p></td>
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


#### <a name="see-also"></a>Vea también

[JET_ERR](./jet-err.md)
