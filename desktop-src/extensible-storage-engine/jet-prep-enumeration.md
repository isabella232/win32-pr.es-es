---
description: 'Más información sobre: enumeración JET_prep datos'
title: JET_prep enumeración
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
ms.openlocfilehash: 0246114eef784fea2fc145f7cab737c815c17626fc2580b33aa6d09229418066
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118765061"
---
# <a name="jet_prep-enumeration"></a>JET_prep enumeración

Tipos de actualización para JetPrepareUpdate.

**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)

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
<td>Esta marca hace que el cursor se prepare para una inserción de un nuevo registro. Todos los datos se inicializan en el estado predeterminado del registro. Si la tabla tiene una columna de incremento automático, se asigna un nuevo valor a este registro independientemente de si la actualización se realiza correctamente, se produce un error o se cancela.</td>
</tr>
<tr class="even">
<td></td>
<td>Replace</td>
<td>Esta marca hace que el cursor se prepare para reemplazar el registro actual. Si la tabla tiene una columna de versión, la columna de versión se establece en el siguiente valor de su secuencia. Si esta actualización no se completa, el valor de versión del registro no se verá afectado. Se toma un bloqueo de actualización en el registro para evitar que otras sesiones actualicen este registro antes de que se complete esta sesión.</td>
</tr>
<tr class="odd">
<td></td>
<td>Cancelar</td>
<td>Esta marca hace que JetPrepareUpdate cancele la actualización de este cursor.</td>
</tr>
<tr class="even">
<td></td>
<td>ReplaceNoLock</td>
<td>Esta marca es similar a JET_prepReplace, pero no se toma ningún bloqueo para impedir que otras sesiones actualicen este registro. En su lugar, esta sesión puede recibir JET_errWriteConflict cuando llama a JetUpdate para completar la actualización.</td>
</tr>
<tr class="odd">
<td></td>
<td>InsertCopy</td>
<td>Esta marca hace que el cursor se prepare para una inserción de una copia del registro existente. Debe haber un registro actual si se usa esta opción. El estado inicial del nuevo registro se copia del registro actual. Los valores largos almacenados fuera de registro se copian virtualmente.</td>
</tr>
<tr class="even">
<td></td>
<td>InsertCopyDeleteOriginal</td>
<td>Esta marca hace que el cursor se prepare para una inserción del mismo registro y una eliminación o el registro original. Se usa en los casos en los que la clave principal ha cambiado.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
