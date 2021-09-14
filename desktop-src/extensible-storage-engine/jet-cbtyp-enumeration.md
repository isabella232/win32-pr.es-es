---
description: 'Más información sobre: enumeración JET_cbtyp datos'
title: JET_cbtyp enumeración
TOCTitle: JET_cbtyp enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_cbtyp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_cbtyp(v=EXCHG.10)
ms:contentKeyID: 39511758
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Finalize
- Microsoft.Isam.Esent.Interop.JET_cbtyp.OnlineDefragCompleted
- Microsoft.Isam.Esent.Interop.JET_cbtyp.UserDefinedDefaultValue
- Microsoft.Isam.Esent.Interop.JET_cbtyp
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeCursorLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeTableLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Null
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeInsert
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterInsert
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeCursorLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeTableLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Null
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.OnlineDefragCompleted
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterInsert
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeInsert
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Finalize
- Microsoft.Isam.Esent.Interop.JET_cbtyp.UserDefinedDefaultValue
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3d2e545fea9c1942dc09df82eb93eafa1d3e4e89
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127263615"
---
# <a name="jet_cbtyp-enumeration"></a>JET_cbtyp enumeración

Tipo de progreso que se notifica.

Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration JET_cbtyp
'Usage
Dim instance As JET_cbtyp
```

``` csharp
[FlagsAttribute]
public enum JET_cbtyp
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
<td>Null</td>
<td>Esta devolución de llamada está reservada y siempre se considera no válida.</td>
</tr>
<tr class="even">
<td></td>
<td>Finalización</td>
<td>Una columna finalizable ha pasado a cero.</td>
</tr>
<tr class="odd">
<td></td>
<td>BeforeInsert</td>
<td>Esta devolución de llamada se producirá justo antes de que se inserte un nuevo registro en una tabla mediante una llamada a JetUpdate.</td>
</tr>
<tr class="even">
<td></td>
<td>AfterInsert</td>
<td>Esta devolución de llamada se producirá justo después de insertar un nuevo registro en una tabla mediante una llamada a JetUpdate, pero antes de que vuelva JetUpdate.</td>
</tr>
<tr class="odd">
<td></td>
<td>BeforeReplace</td>
<td>Esta devolución de llamada se producirá justo antes de que una llamada a JetUpdate cambie un registro existente en una tabla.</td>
</tr>
<tr class="even">
<td></td>
<td>AfterReplace</td>
<td>Esta devolución de llamada se producirá justo después de que se haya cambiado un registro existente en una tabla mediante una llamada a JetUpdate, pero antes de que JetUpdate vuelva.</td>
</tr>
<tr class="odd">
<td></td>
<td>BeforeDelete</td>
<td>Esta devolución de llamada se producirá justo antes de que una llamada a JetDelete elimine un registro existente en una tabla.</td>
</tr>
<tr class="even">
<td></td>
<td>AfterDelete</td>
<td>Esta devolución de llamada se producirá justo después de que una llamada a JetDelete elimine un registro existente en una tabla.</td>
</tr>
<tr class="odd">
<td></td>
<td>UserDefinedDefaultValue</td>
<td>Esta devolución de llamada se producirá cuando el motor necesite recuperar el valor predeterminado definido por el usuario de una columna de la aplicación. Esta devolución de llamada es básicamente una implementación limitada de JetRetrieveColumn que evalúa la aplicación. Se puede devolver un máximo de un valor de columna para un valor predeterminado definido por el usuario.</td>
</tr>
<tr class="even">
<td></td>
<td>OnlineDefragCompleted</td>
<td>Esta devolución de llamada se producirá cuando se haya detenido la desfragmentación en línea de una base de datos iniciada por JetDefragment debido a que se ha completado el proceso o se ha alcanzado el límite de tiempo.</td>
</tr>
<tr class="odd">
<td></td>
<td>FreeCursorLS</td>
<td>Esta devolución de llamada se producirá cuando la aplicación necesite limpiar el identificador de contexto de la Storage local asociada a un cursor que está liberando el motor de base de datos. Para más información, consulte JetSetLS. El delegado para este motivo de devolución de llamada se configura mediante JetSetSystemParameter con JET_paramRuntimeCallback.</td>
</tr>
<tr class="even">
<td></td>
<td>FreeTableLS</td>
<td>Esta devolución de llamada se producirá como resultado de la necesidad de que la aplicación limpie el identificador de contexto para el Storage local asociado a una tabla que el motor de base de datos está liberando. Para más información, consulte JetSetLS. El delegado para este motivo de devolución de llamada se configura mediante JetSetSystemParameter con JET_paramRuntimeCallback.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
