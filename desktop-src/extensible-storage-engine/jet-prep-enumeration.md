---
description: 'Más información acerca de: enumeración JET_prep'
title: Enumeración JET_prep
TOCTitle: JET_prep enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_prep
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_prep(v=EXCHG.10)
ms:contentKeyID: 39510193
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_prep.Replace
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopy
- Microsoft.Isam.Esent.Interop.JET_prep.Cancel
- Microsoft.Isam.Esent.Interop.JET_prep.Insert
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopyDeleteOriginal
- Microsoft.Isam.Esent.Interop.JET_prep
- Microsoft.Isam.Esent.Interop.JET_prep.ReplaceNoLock
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopyDeleteOriginal
- Microsoft.Isam.Esent.Interop.JET_prep.ReplaceNoLock
- Microsoft.Isam.Esent.Interop.JET_prep
- Microsoft.Isam.Esent.Interop.JET_prep.Cancel
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopy
- Microsoft.Isam.Esent.Interop.JET_prep.Insert
- Microsoft.Isam.Esent.Interop.JET_prep.Replace
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: edeaef8144fe6e13674ec6d3dfcb8adf7522e148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697528"
---
# <a name="jet_prep-enumeration"></a>Enumeración JET_prep

Tipos de actualización para JetPrepareUpdate.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
Public Enumeration JET_prep
'Usage
Dim instance As JET_prep
```

``` csharp
public enum JET_prep
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
<td>Insertar</td>
<td>Esta marca hace que el cursor se prepare para una inserción de un nuevo registro. Todos los datos se inicializan en el estado predeterminado del registro. Si la tabla tiene una columna de incremento automático, se asigna un nuevo valor a este registro independientemente de si la actualización se realiza en última instancia, si se produce un error o se cancela.</td>
</tr>
<tr class="even">
<td></td>
<td>Replace</td>
<td>Esta marca hace que el cursor se prepare para un reemplazo del registro actual. Si la tabla tiene una columna de versión, la columna versión se establece en el valor siguiente en su secuencia. Si esta actualización no se completa, el valor de versión del registro no se verá afectado. Se realiza un bloqueo de actualización en el registro para evitar que otras sesiones actualicen este registro antes de que se complete esta sesión.</td>
</tr>
<tr class="odd">
<td></td>
<td>Cancelar</td>
<td>Esta marca hace que JetPrepareUpdate cancele la actualización de este cursor.</td>
</tr>
<tr class="even">
<td></td>
<td>ReplaceNoLock</td>
<td>Esta marca es similar a JET_prepReplace, pero no se realiza ningún bloqueo para evitar que otras sesiones actualicen este registro. En su lugar, esta sesión puede recibir JET_errWriteConflict cuando llama a JetUpdate para completar la actualización.</td>
</tr>
<tr class="odd">
<td></td>
<td>InsertCopy</td>
<td>Esta marca hace que el cursor se prepare para una inserción de una copia del registro existente. Debe haber un registro actual si se usa esta opción. El estado inicial del nuevo registro se copia del registro actual. Los valores Long que se almacenan fuera de registro se copian de manera virtual.</td>
</tr>
<tr class="even">
<td></td>
<td>InsertCopyDeleteOriginal</td>
<td>Esta marca hace que el cursor se prepare para una inserción del mismo registro, y una eliminación o el registro original. Se utiliza en casos en los que la clave principal ha cambiado.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
