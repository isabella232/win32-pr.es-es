---
description: 'Más información acerca de: JetPrereadKeys (función)'
title: JetPrereadKeys función)
TOCTitle: JetPrereadKeys Function
ms:assetid: fc2f46bc-1f81-4af2-aa63-9757e819efc2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294143(v=EXCHG.10)
ms:contentKeyID: 32765757
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetPrereadKeys
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d35407c171bdcd54eb44e9830f382c08a1e6c6c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497410"
---
# <a name="jetprereadkeys-function"></a>JetPrereadKeys función)


_**Se aplica a:** Windows | Windows Server_

## <a name="jetprereadkeys-function"></a>JetPrereadKeys función)

La función **JetPrereadKeys** Lee los valores de clave para mejorar el rendimiento de la limpieza del almacén de versiones.

**Windows 7:** la función PrereadKeys se presentó en Windows 7.

```cpp
    JET_ERR JET_API JetPrereadKeys(
      __in JET_SESID sesid,
      __in JET_TABLEID tableid,
      __in_ecount(ckeys) const void ** rgpvKeys,
      __in_ecount(ckeys) const unsigned long * rgcbKeys,
      __in long ckeys,
      __out_opt long * pckeysPreread,
      __in JET_GRBIT grbit
     );
```

### <a name="parameters"></a>Parámetros

*sesid*

Contexto de sesión de base de datos que se va a usar para la llamada API.

*TABLEID*

Cursor que se va a usar para esta llamada.

*rgpvKeys*

Matriz de punteros a claves. Las claves se pueden realizar con [JetMakeKey](./jetmakekey-function.md) o recuperar con [JetGetBookmark](./jetgetbookmark-function.md). Las claves deben ordenarse en orden ascendente o descendente, según el grbit pasado. Las claves se pueden ordenar con memcmp.

*rgcbKeys*

Matriz de longitudes de clave. rgpvKeys \[ n \] debe apuntar a una clave de longitud rgcbKeys \[ n\]

*ckeys*

Número de claves. rgpvKeys y rgcbKeys deben apuntar a una matriz con al menos ckeys elementos.

*pckeysPreread*

Devuelve el número de claves para las que se han emitido realmente las lecturas. Este parámetro puede ser NULL.

*grbit*

Debe ser JET_bitPrereadForward o JET_bitPrereadBackward. Si grbit es JET_bitPrereadForward, las claves se deben ordenar en orden ascendente. Si grbit es JET_bitPrereadBackward, las claves se deben ordenar en orden descendente.

### <a name="return-value"></a>Valor devuelto

Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno. Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).

Pueden devolverse varios errores de e/s junto con estos errores de uso de la API:

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
<td><p>JET_errInvalidGrbit</p></td>
<td><p>Grbit no se JET_bitPrereadForward ni JET_bitPrereadBackward.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>Se ha pasado un tamaño de clave incorrecto. Las claves no pueden ser 0 ni mayores que la longitud de clave máxima de la tabla.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Se ha pasado un parámetro no válido. Esto puede deberse a un valor null para un parámetro necesario o puede indicar que la matriz de claves no está ordenada correctamente.</p></td>
</tr>
</tbody>
</table>


**JetPrereadKeys** recorre las páginas internas del árbol b para determinar qué páginas hoja contienen las claves especificadas por RgpvKeys/rgcbKeys. La lista de páginas hoja está ordenada y, a continuación, se emiten las prelectura para los intervalos de páginas. El número de páginas que se pueden leer de forma preleída es limitado, por lo que es posible que no se puedan leer todas las claves. En ese caso, el número de claves realmente leídas se devuelve en pckeysPreread.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows 7.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008 R2.</p></td>
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
