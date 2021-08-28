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
ms.openlocfilehash: 77c452fb78916fdcdf935ec6ad890db055e63b9a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479321"
---
# <a name="jet_spacehints-structure"></a>JET_SPACEHINTS estructura


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_spacehints-structure"></a>JET_SPACEHINTS estructura

La **JET_SPACEHINTS** contiene información sobre los patrones de asignación de espacio cuando un árbol b crece a través de divisiones de anexar o punto de acceso. Las divisiones de anexión se suceden cuando se agregan registros al final de un árbol b y las divisiones de punto de acceso rápido se suceden cuando se agregan varios registros al mismo punto de inserción virtual (por ejemplo, al agregar "Ana", "Mark", "Martin", "Mary" al centro de un árbol b ordenado alfabéticamente).

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


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitSpaceHintsUtilizeParentSpace<br />0x00000001</p> | <p>Cambia la directiva de asignación interna para obtener espacio heirarchicalmente del elemento primario inmediato de un árbol b.</p> | 
| <p>JET_bitCreateHintAppendSequential<br />0x00000002</p> | <p>Permite que el comportamiento de división de anexos crezca según la dinámica de crecimiento de la tabla (establecida por cbMinExtent, ulGrowth, cbMaxExtent).</p> | 
| <p>JET_bitCreateHintHotpointSequential<br />0x00000004</p> | <p>Permite que el comportamiento de división de punto de acceso rápido crezca según la dinámica de crecimiento de la tabla (establecida por cbMinExtent, ulGrowth, cbMaxExtent).</p> | 
| <p>JET_bitRetrieveHintTableScanForward<br />0x00000010</p> | <p>Si se establece, el cliente indica que el examen secuencial hacia delante es el patrón de uso predominante de esta tabla.</p> | 
| <p>JET_bitRetrieveHintTableScanBackward<br />0x00000020</p> | <p>Si se establece, el cliente indica que el examen secuencial hacia atrás es el patrón de uso predominante de esta tabla.</p> | 
| <p>JET_bitDeleteHintTableSequential<br />0x00000100</p> | <p>Si se establece, la aplicación espera que esta tabla se limpie en orden secuencial, de la clave más baja a la clave más alta.</p> | 



**ulMaintDensity**

densidad a mulMaintDensity

Densidad en la que se debe mantener. Si las sugerencias de espacio especifican JET_bitRetrieveHintTableScanForward o JET_bitRetrieveHintTableScanBackward, la desfragmentación de la tabla se desencadenará cuando el espacio usado en la tabla esté por debajo de este umbral. La desfragmentación de tablas se puede deshabilitar estableciendo este miembro en cero. Establecer este miembro en 100 hará que la desfragmentación de la tabla se ejecute en cuanto se libera una página.

**ulGrowth**

Porcentaje de crecimiento desde el último crecimiento o tamaño inicial, redondeado al tamaño de asignación jet nativo más cercano.

**cbMinExtent demasiado pequeño**

Esto invalida ulGrowth si es demasiado pequeño.

**cbMaxExtent**

Valor máximo para el crecimiento en bytes. Esto tiene como límite ulGrowth.

### <a name="when-a-b-tree-grows-through-append-or-hotpoint-splits-as-opposed-to-random-record-insertions-the-amount-of-space-the-table-will-grow-by-is-calculated-as-follows"></a>Cuando un árbol b crece a través de divisiones de anexión o punto de acceso rápido (en lugar de inserciones de registros aleatorias), la cantidad de espacio por el que crecerá la tabla se calcula de la siguiente manera:

1.  En la creación, se da al árbol b cbInitial, siempre.

2.  Durante la primera asignación de un área determinada, asignaremos: cbInitial ulGrowth/ 100 (redondeado al tamaño de página de la base de datos) o cbMinExtent si es \* mayor.

3.  Durante la asignación siguiente, cbLastAlloc ulGrowth/ 100 (redondeado al tamaño de página de la base de datos) o \* cbMinExtent si es mayor.

4.  En alguna asignación (que podría ser la primera asignación), el tamaño calculado superará cbMaxExtent y ese será el tamaño de crecimiento posteriormente.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JET_TABLECREATE3](./jet-tablecreate3-structure.md)
