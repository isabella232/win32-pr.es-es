---
description: 'Más información sobre: JET_SPACEHINTS estructura'
title: JET_SPACEHINTS estructura
TOCTitle: JET_SPACEHINTS Structure
ms:assetid: 23328993-93c9-4a23-892b-e6a9f434d1d6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269205(v=EXCHG.10)
ms:contentKeyID: 32765508
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f829e78ff54e77011346ae1bfd39f909411cbee12c18d19781f8fe5d62865097
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118252260"
---
# <a name="jet_spacehints-structure"></a>JET_SPACEHINTS estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_spacehints-structure"></a>JET_SPACEHINTS estructura

La **JET_SPACEHINTS** contiene información sobre los patrones de asignación de espacio cuando un árbol b crece a través de divisiones de anexo o punto de acceso. Las divisiones de anexión se suceden cuando se agregan registros al final de un árbol b y las divisiones de punto de acceso rápido se suceden cuando se agregan varios registros al mismo punto de inserción virtual (por ejemplo, al agregar "Ana", "Mark", "Martin", "Mary" al centro de un árbol b ordenado alfabéticamente).

**Windows 7:** La **JET_SPACEHINTS** estructura se introduce en Windows 7.

```cpp
    typedef struct tagJET_SPACEHINTS {
      unsigned long cbStruct;
      unsigned long ulInitialDensity;
      unsigned long cbInitial;
      JET_GRBIT grbit;
      unsigned long ulMaintDensity;
      unsigned long ulGrowth;
      unsigned long cbMinExtent;
      unsigned long cbMaxExtent;
    } JET_SPACEHINTS;
```

### <a name="members"></a>Miembros

**cbStruct**

Tamaño, en bytes, de esta estructura. Establezca este miembro en sizeof( JET_SPACEHINTS ).

**ulInitialDensity**

Densidad en el diseño (anexar).

**cbInitial**

Tamaño inicial (en bytes) del objeto que se va a crear. Debe ser un múltiplo del tamaño de página de la base de datos.

**grbit**

Un grupo de bits que contienen las opciones que se usarán para esta estructura, que incluyen cero o más de lo siguiente.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitSpaceHintsUtilizeParentSpace<br />
0x00000001</p></td>
<td><p>Cambia la directiva de asignación interna para obtener espacio heirarchicalmente del elemento primario inmediato de un árbol b.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitCreateHintAppendSequential<br />
0x00000002</p></td>
<td><p>Permite que el comportamiento de división de anexos crezca según la dinámica de crecimiento de la tabla (establecida por cbMinExtent, ulGrowth, cbMaxExtent).</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitCreateHintHotpointSequential<br />
0x00000004</p></td>
<td><p>Permite que el comportamiento de división de punto de acceso rápido crezca según la dinámica de crecimiento de la tabla (establecida por cbMinExtent, ulGrowth, cbMaxExtent).</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveHintTableScanForward<br />
0x00000010</p></td>
<td><p>Si se establece, el cliente indica que el examen secuencial hacia delante es el patrón de uso predominante de esta tabla.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveHintTableScanBackward<br />
0x00000020</p></td>
<td><p>Si se establece, el cliente indica que el examen secuencial hacia atrás es el patrón de uso predominante de esta tabla.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDeleteHintTableSequential<br />
0x00000100</p></td>
<td><p>Si se establece, la aplicación espera que esta tabla se limpie en orden secuencial, desde la clave más baja a la clave más alta.</p></td>
</tr>
</tbody>
</table>


**ulMaintDensity**

densidad a mulMaintDensity

Densidad en la que se debe mantener. Si las sugerencias de espacio especifican JET_bitRetrieveHintTableScanForward o JET_bitRetrieveHintTableScanBackward, la desfragmentación de la tabla se desencadenará cuando el espacio usado en la tabla cae por debajo de este umbral. La desfragmentación de tablas se puede deshabilitar estableciendo este miembro en cero. Establecer este miembro en 100 hará que la desfragmentación de tablas se ejecute en cuanto se libera una página.

**ulGrowth**

Porcentaje de crecimiento desde el último crecimiento o tamaño inicial, redondeado al tamaño de asignación jet nativo más cercano.

**cbMinExtent demasiado pequeño**

Esto invalida ulGrowth si es demasiado pequeño.

**cbMaxExtent**

Valor máximo para el crecimiento en bytes. Esto tiene como límite ulGrowth.

### <a name="when-a-b-tree-grows-through-append-or-hotpoint-splits-as-opposed-to-random-record-insertions-the-amount-of-space-the-table-will-grow-by-is-calculated-as-follows"></a>Cuando un árbol b crece a través de divisiones de anexión o punto de acceso rápido (en lugar de inserciones de registros aleatorias), la cantidad de espacio por el que crecerá la tabla se calcula de la siguiente manera:

1.  En la creación, se le da al árbol b cbInitial, siempre.

2.  Durante la primera asignación de un área determinada, asignaremos: cbInitial ulGrowth/ 100 (redondeado al tamaño de página de la base de datos) o cbMinExtent si es \* mayor.

3.  Durante la asignación siguiente, cbLastAlloc ulGrowth/ 100 (redondeado al tamaño de página de la base de datos) o \* cbMinExtent si es mayor.

4.  En alguna asignación (que podría ser la primera asignación), el tamaño calculado superará cbMaxExtent y ese será el tamaño de crecimiento posterior.

### <a name="requirements"></a>Requisitos

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
<td><p>Declarado en Esent.h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JET_TABLECREATE3](./jet-tablecreate3-structure.md)
