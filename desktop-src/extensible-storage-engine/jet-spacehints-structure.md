---
description: 'Más información acerca de: estructura de JET_SPACEHINTS'
title: Estructura de JET_SPACEHINTS
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
ms.openlocfilehash: cf786d1f47b5eaae3f9540c8635853020f9b0521
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720308"
---
# <a name="jet_spacehints-structure"></a>Estructura de JET_SPACEHINTS


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_spacehints-structure"></a>Estructura de JET_SPACEHINTS

La estructura **JET_SPACEHINTS** contiene información sobre los patrones de asignación de espacio cuando un árbol b crece a través de las divisiones Append o Hotpoint. Anexar divisiones se producen cuando los registros se agregan al final de un árbol b y se producen divisiones de Hotpoint cuando se agregan varios registros al mismo punto de inserción virtual (por ejemplo, al agregar ' Marie ', ' Mark ', ' Martin' ', ' Mary ' a la mitad de un árbol b que está ordenado alfabéticamente).

**Windows 7:** La estructura de **JET_SPACEHINTS** se presenta en Windows 7.

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

Tamaño, en bytes, de esta estructura. Establezca este miembro en sizeof (JET_SPACEHINTS).

**ulInitialDensity**

El diseño de densidad en (anexar).

**cbInitial**

Tamaño inicial (en bytes) del objeto que se va a crear. Debe ser un múltiplo del tamaño de página de la base de datos.

**grbit**

Grupo de bits que contiene las opciones que se van a usar para esta estructura, que incluyen cero o más de los siguientes elementos.

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
<td><p>JET_bitSpaceHintsUtilizeParentSpace<br />
0x00000001</p></td>
<td><p>Cambia la Directiva de asignación interna para obtener el espacio heirarchically del elemento primario inmediato de un árbol b.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitCreateHintAppendSequential<br />
0x00000002</p></td>
<td><p>Habilita el comportamiento de anexar División para aumentar según la dinámica de crecimiento de la tabla (establecida por cbMinExtent, ulGrowth, cbMaxExtent).</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitCreateHintHotpointSequential<br />
0x00000004</p></td>
<td><p>Permite que el comportamiento de división Hotpoint crezca según la dinámica de crecimiento de la tabla (establecida por cbMinExtent, ulGrowth, cbMaxExtent).</p></td>
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
<td><p>Si se establece, la aplicación espera que esta tabla se limpie en orden secuencial, de la clave más baja a la más alta.</p></td>
</tr>
</tbody>
</table>


**ulMaintDensity**

densidad a mulMaintDensity

Densidad que se debe mantener en. Si las sugerencias de espacio especifican JET_bitRetrieveHintTableScanForward o JET_bitRetrieveHintTableScanBackward, la desfragmentación de la tabla se desencadenará cuando el espacio usado en la tabla caiga por debajo de este umbral. La desfragmentación de tablas se puede deshabilitar estableciendo este miembro en cero. Si se establece este miembro en 100, la desfragmentación de la tabla se ejecutará en cuanto se libere una página.

**ulGrowth**

Porcentaje de crecimiento del último crecimiento o tamaño inicial, redondeado al tamaño de asignación de JET nativo más cercano.

**cbMinExtent demasiado pequeño**

Esto invalida ulGrowth si es demasiado pequeño.

**cbMaxExtent**

Valor máximo para el crecimiento en bytes. Este ulGrowth de mayúsculas.

### <a name="when-a-b-tree-grows-through-append-or-hotpoint-splits-as-opposed-to-random-record-insertions-the-amount-of-space-the-table-will-grow-by-is-calculated-as-follows"></a>Cuando un árbol b crece a través de las divisiones Append o Hotpoint (en lugar de las inserciones de registros aleatorios), la cantidad de espacio en la que crecerá la tabla se calcula de la manera siguiente:

1.  En el momento de su creación, asignamos el árbol b cbInitial, siempre.

2.  Durante la primera asignación de un área determinada, asignaremos: cbInitial \* ulGrowth/100 (redondeado al tamaño de página de la base de BD) o cbMinExtent si es mayor.

3.  Durante la siguiente asignación, cbLastAlloc \* ulGrowth/100 (redondeado al tamaño de página de la base de BD) o cbMinExtent si es mayor.

4.  En alguna asignación (que podría ser la primera asignación), el tamaño calculado superará el cbMaxExtent y tendrá el tamaño de crecimiento a partir de entonces.

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
<td><p>Declarado en esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JET_TABLECREATE3](./jet-tablecreate3-structure.md)
