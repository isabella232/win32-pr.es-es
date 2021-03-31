---
description: 'Más información sobre: enumeración SpaceHintsGrbit'
title: Enumeración SpaceHintsGrbit
TOCTitle: SpaceHintsGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SpaceHintsGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.spacehintsgrbit(v=EXCHG.10)
ms:contentKeyID: 39516304
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.CreateHintHotpointSequential
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.CreateHintAppendSequential
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.DeleteHintTableSequential
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.None
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.RetrieveHintReserve2
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.RetrieveHintReserve1
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.RetrieveHintTableScanForward
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.RetrieveHintTableScanBackward
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.RetrieveHintReserve3
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.SpaceHintUtilizeParentSpace
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.RetrieveHintReserve3
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.CreateHintHotpointSequential
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.CreateHintAppendSequential
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.RetrieveHintTableScanBackward
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.SpaceHintUtilizeParentSpace
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.RetrieveHintReserve2
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.DeleteHintTableSequential
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.RetrieveHintTableScanForward
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.None
- Microsoft.Isam.Esent.Interop.SpaceHintsGrbit.RetrieveHintReserve1
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ffc78aab444c73f7ff0eae7ff0eaa84e134ee9bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001267"
---
# <a name="spacehintsgrbit-enumeration"></a>Enumeración SpaceHintsGrbit

Opciones para [JET_SPACEHINTS](./jet-spacehints-class.md).

Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SpaceHintsGrbit
'Usage
Dim instance As SpaceHintsGrbit
```

``` csharp
[FlagsAttribute]
public enum SpaceHintsGrbit
```

## <a name="members"></a>Miembros

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
<td>None</td>
<td>Opciones predeterminadas.</td>
</tr>
<tr class="even">
<td></td>
<td>SpaceHintUtilizeParentSpace</td>
<td>Esto cambia la Directiva de asignación interna para obtener espacio jerárquicamente desde el elemento primario inmediato del árbol B.</td>
</tr>
<tr class="odd">
<td></td>
<td>CreateHintAppendSequential</td>
<td>Este bit habilitará el comportamiento de anexar División para aumentar según la dinámica de crecimiento de la tabla (establecida por cbMinExtent, ulGrowth, cbMaxExtent).</td>
</tr>
<tr class="even">
<td></td>
<td>CreateHintHotpointSequential</td>
<td>Este bit permitirá que el comportamiento de división Hotpoint crezca según la dinámica de crecimiento de la tabla (establecida por cbMinExtent, ulGrowth, cbMaxExtent).</td>
</tr>
<tr class="odd">
<td></td>
<td>RetrieveHintReserve1</td>
<td>Reservado y omitido.</td>
</tr>
<tr class="even">
<td></td>
<td>RetrieveHintTableScanForward</td>
<td>Al establecer esta opción, el cliente indica que el examen secuencial hacia delante es el patrón de uso predominante de esta tabla.</td>
</tr>
<tr class="odd">
<td></td>
<td>RetrieveHintTableScanBackward</td>
<td>Al establecer esta opción, el cliente indica que el examen secuencial hacia atrás es el patrón de uso predominante de esta tabla.</td>
</tr>
<tr class="even">
<td></td>
<td>RetrieveHintReserve2</td>
<td>Reservado y omitido.</td>
</tr>
<tr class="odd">
<td></td>
<td>RetrieveHintReserve3</td>
<td>Reservado y omitido.</td>
</tr>
<tr class="even">
<td></td>
<td>DeleteHintTableSequential</td>
<td>La aplicación espera que esta tabla se limpie en orden secuencialmente (de la clave más baja a la más alta).</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
