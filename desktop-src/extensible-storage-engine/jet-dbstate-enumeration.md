---
description: 'Más información sobre: enumeración JET_dbstate datos'
title: JET_dbstate enumeración
TOCTitle: JET_dbstate enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_dbstate
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbstate(v=EXCHG.10)
ms:contentKeyID: 39511841
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_dbstate
- Microsoft.Isam.Esent.Interop.JET_dbstate.BeingConverted
- Microsoft.Isam.Esent.Interop.JET_dbstate.CleanShutdown
- Microsoft.Isam.Esent.Interop.JET_dbstate.DirtyShutdown
- Microsoft.Isam.Esent.Interop.JET_dbstate.ForceDetach
- Microsoft.Isam.Esent.Interop.JET_dbstate.JustCreated
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_dbstate.JustCreated
- Microsoft.Isam.Esent.Interop.JET_dbstate.BeingConverted
- Microsoft.Isam.Esent.Interop.JET_dbstate.CleanShutdown
- Microsoft.Isam.Esent.Interop.JET_dbstate.ForceDetach
- Microsoft.Isam.Esent.Interop.JET_dbstate.DirtyShutdown
- Microsoft.Isam.Esent.Interop.JET_dbstate
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a83c8a4313e5e6f21ee885ee7936c90503bfbd3c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063478"
---
# <a name="jet_dbstate-enumeration"></a>JET_dbstate enumeración

Estados de base de datos (usados [en JET_DBINFOMISC](./jet-dbinfomisc-class.md)).

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Enumeration JET_dbstate
'Usage
Dim instance As JET_dbstate
```

``` csharp
public enum JET_dbstate
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
<td>JustCreated</td>
<td>La base de datos se acaba de crear.</td>
</tr>
<tr class="even">
<td></td>
<td>DirtyShutdown</td>
<td>Base de datos de apagado incorrecto (incoherente).</td>
</tr>
<tr class="odd">
<td></td>
<td>CleanShutdown</td>
<td>Limpieza de la base de datos de apagado (coherente).</td>
</tr>
<tr class="even">
<td></td>
<td>BeingConverted</td>
<td>La base de datos se está convirtiendo.</td>
</tr>
<tr class="odd">
<td></td>
<td>ForceDetach</td>
<td>La base de datos se desasociaba por fuerza.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
