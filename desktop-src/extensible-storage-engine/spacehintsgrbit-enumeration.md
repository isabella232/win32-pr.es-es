---
description: 'Más información sobre: Enumeración SpaceHintsGrbit'
title: SpaceHintsGrbit (enumeración)
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
ms.openlocfilehash: 8a2ee172355b48e64f62f2b18477373269d81ae060460ad34ff45dbad33a91b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978535"
---
# <a name="spacehintsgrbit-enumeration"></a>SpaceHintsGrbit (enumeración)

Opciones para [JET_SPACEHINTS](./jet-spacehints-class.md).

Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

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
<td>Ninguno</td>
<td>Opciones predeterminadas.</td>
</tr>
<tr class="even">
<td></td>
<td>SpaceHintUtilizeParentSpace</td>
<td>Esto cambia la directiva de asignación interna para obtener espacio jerárquicamente del elemento primario inmediato de un árbol B.</td>
</tr>
<tr class="odd">
<td></td>
<td>CreateHintAppendSequential</td>
<td>Este bit permitirá que el comportamiento de división append crezca según la dinámica de crecimiento de la tabla (establecido por cbMinExtent, ulGrowth, cbMaxExtent).</td>
</tr>
<tr class="even">
<td></td>
<td>CreateHintHotpointSequential</td>
<td>Este bit permitirá que el comportamiento de división de punto de acceso rápido crezca según la dinámica de crecimiento de la tabla (establecida por cbMinExtent, ulGrowth, cbMaxExtent).</td>
</tr>
<tr class="odd">
<td></td>
<td>RetrieveHintReserve1</td>
<td>Reservado y omitido.</td>
</tr>
<tr class="even">
<td></td>
<td>RetrieveHintTableScanForward</td>
<td>Al establecer esto, el cliente indica que el examen secuencial hacia delante es el patrón de uso predominante de esta tabla.</td>
</tr>
<tr class="odd">
<td></td>
<td>RetrieveHintTableScanBackward</td>
<td>Al establecer esto, el cliente indica que el examen secuencial hacia atrás es el patrón de uso predominante de esta tabla.</td>
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
<td>La aplicación espera que esta tabla se limpie en orden secuencialmente (de la clave más baja a la clave más alta).</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
