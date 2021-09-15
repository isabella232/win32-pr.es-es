---
description: 'Más información sobre: Enumeración GetRecordSizeGrbit'
title: GetRecordSizeGrbit (enumeración)
TOCTitle: GetRecordSizeGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.getrecordsizegrbit(v=EXCHG.10)
ms:contentKeyID: 39514742
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.InCopyBuffer
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.Local
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.None
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.RunningTotal
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.None
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.RunningTotal
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.InCopyBuffer
- Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit.Local
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ee95d29ed1913993aa37062137807bf8d635eecc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127269831"
---
# <a name="getrecordsizegrbit-enumeration"></a>GetRecordSizeGrbit (enumeración)

Opciones de [JetGetRecordSize(JET_SESID, JET_TABLEID, JET_RECSIZE, GetRecordSizeGrbit).](./vistaapi.jetgetrecordsize-method.md)

Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration GetRecordSizeGrbit
'Usage
Dim instance As GetRecordSizeGrbit
```

``` csharp
[FlagsAttribute]
public enum GetRecordSizeGrbit
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
<td>None</td>
<td>Opciones predeterminadas.</td>
</tr>
<tr class="even">
<td></td>
<td>InCopyBuffer</td>
<td>Recupere el tamaño del registro que se encuentra en el búfer de copia preparado o actualizado. De lo contrario, el tableid debe colocarse en un registro y se usará ese registro.</td>
</tr>
<tr class="odd">
<td></td>
<td>RunningTotal</td>
<td>La JET_RECSIZE no se reduce a cero antes de rellenar el contenido, actuando eficazmente como una acumulación de las estadísticas de varios registros visitados o actualizados.</td>
</tr>
<tr class="even">
<td></td>
<td>Local</td>
<td>Omitir valores long no intrínsecos. Solo se usará el registro local de la página.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
