---
description: 'Más información sobre: Enumeración TempTableGrbit'
title: TempTableGrbit (enumeración)
TOCTitle: TempTableGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.TempTableGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.temptablegrbit(v=EXCHG.10)
ms:contentKeyID: 39515065
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.TempTableGrbit
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ErrorOnDuplicateInsertion
- Microsoft.Isam.Esent.Interop.TempTableGrbit.None
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Unique
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.TempTableGrbit.SortNullsHigh
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ForceMaterialization
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Indexed
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Scrollable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ErrorOnDuplicateInsertion
- Microsoft.Isam.Esent.Interop.TempTableGrbit.None
- Microsoft.Isam.Esent.Interop.TempTableGrbit
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Indexed
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ForceMaterialization
- Microsoft.Isam.Esent.Interop.TempTableGrbit.SortNullsHigh
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Scrollable
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Unique
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 79247bac6e8d3bda9d1aeac4d19b7af894201a57
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126882617"
---
# <a name="temptablegrbit-enumeration"></a>TempTableGrbit (enumeración)

Opciones para la creación de tablas temporales.

Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration TempTableGrbit
'Usage
Dim instance As TempTableGrbit
```

``` csharp
[FlagsAttribute]
public enum TempTableGrbit
```

## <a name="members"></a>Members

<table>
<thead>
<tr class="header">
<th></th>
<th>Nombre del miembro</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>Ninguno</td>
<td>Opciones predeterminadas.</td>
</tr>
<tr class="even">
<td></td>
<td>Indexadas</td>
<td>Esta opción solicita que la tabla temporal sea lo suficientemente flexible como para permitir el uso de JetSeek para buscar registros por clave de índice. Si esta funcionalidad no es necesaria, es mejor no solicitarla. Si no se solicita esta funcionalidad, es posible que el administrador de tablas temporales pueda elegir una estrategia para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</td>
</tr>
<tr class="odd">
<td></td>
<td>Único</td>
<td>Esta opción solicita que los registros con claves de índice duplicadas se quiten del conjunto final de registros de la tabla temporal. Antes de Windows Server 2003, el motor de base de datos siempre supusía que esta opción estaba en vigor debido al hecho de que todos los índices clúster también deben ser una clave principal y, por tanto, deben ser únicos. A partir Windows Server 2003, ahora es posible crear una tabla temporal que NO quite duplicados cuando también se especifique la opción <a href="dn351284(v=exchg.10).md">ForwardOnly.</a> No es posible saber qué duplicados ganarán y qué duplicados se descartarán en general. Sin embargo, cuando se solicita la opción ErrorOnDuplicateInsertion, el primer registro con una clave de índice determinada que se va a insertar en la tabla temporal siempre ganará.</td>
</tr>
<tr class="even">
<td></td>
<td>Actualizable</td>
<td>Esta opción solicita que la tabla temporal sea lo suficientemente flexible como para permitir que los registros que se han insertado previamente se cambien posteriormente. Si esta funcionalidad no es necesaria, es mejor no solicitarla. Si no se solicita esta funcionalidad, es posible que el administrador de tablas temporales pueda elegir una estrategia para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</td>
</tr>
<tr class="odd">
<td></td>
<td>De desplazamiento</td>
<td>Esta opción solicita que la tabla temporal sea lo suficientemente flexible como para permitir que los registros se digitalizarán en orden y dirección arbitrarios mediante <a href="dn292217(v=exchg.10).md">JetMove(JET_SESID, JET_TABLEID, Int32, MoveGrbit).</a> Si esta funcionalidad no es necesaria, es mejor no solicitarla. Si no se solicita esta funcionalidad, es posible que el administrador de tablas temporales pueda elegir una estrategia para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</td>
</tr>
<tr class="even">
<td></td>
<td>SortNullsHigh</td>
<td>Esta opción solicita que los valores de columna de clave NULL se ordenan más cerca del final del índice que los valores de columna de clave no NULL.</td>
</tr>
<tr class="odd">
<td></td>
<td>ForceMaterialization</td>
<td>Esta opción obliga al administrador de tablas temporales a abandonar cualquier intento de elegir una estrategia inteligente para administrar la tabla temporal que dará lugar a un rendimiento mejorado.</td>
</tr>
<tr class="even">
<td></td>
<td>ErrorOnDuplicateInsertion</td>
<td>Esta opción solicita que cualquier intento de insertar un registro con la misma clave de índice que un registro insertado previamente producirá un error inmediatamente <a href="hh564840(v=exchg.10).md">con KeyDuplicate</a>. Si no se solicita esta opción, se puede detectar un duplicado inmediatamente y producir un error o se puede quitar de forma silenciosa más adelante en función de la estrategia elegida por el motor de base de datos para implementar la tabla temporal en función de la funcionalidad solicitada. Si esta funcionalidad no es necesaria, es mejor no solicitarla. Si no se solicita esta funcionalidad, es posible que el administrador de tablas temporales pueda elegir una estrategia para administrar la tabla temporal que dará como resultado un rendimiento mejorado.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

[ForwardOnly](./server2003grbits.forwardonly-field.md)

[IntrinsicLVsOnly](./windows7grbits.intrinsiclvsonly-field.md)
