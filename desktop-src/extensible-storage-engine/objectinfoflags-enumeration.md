---
description: 'Más información sobre: enumeración ObjectInfoFlags'
title: Enumeración ObjectInfoFlags
TOCTitle: ObjectInfoFlags enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.ObjectInfoFlags
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.objectinfoflags(v=EXCHG.10)
ms:contentKeyID: 39515824
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.None
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.System
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableDerived
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableTemplate
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableFixedDDL
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableNoFixedVarColumnsInDerivedTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.System
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableDerived
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.None
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableFixedDDL
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableNoFixedVarColumnsInDerivedTables
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableTemplate
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b3f301f1e786d126dbd57c071fe89356e0acc891
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910241"
---
# <a name="objectinfoflags-enumeration"></a>Enumeración ObjectInfoFlags

Marcas para objetos ESENT (tablas). Se usa en [JET_OBJECTINFO](./jet-objectinfo-class.md).

Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ObjectInfoFlags
'Usage
Dim instance As ObjectInfoFlags
```

``` csharp
[FlagsAttribute]
public enum ObjectInfoFlags
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
<td>System</td>
<td>El objeto solo es para uso interno.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableFixedDDL</td>
<td>El DDL de la tabla es fijo.</td>
</tr>
<tr class="even">
<td></td>
<td>TableTemplate</td>
<td>El DDL de la tabla es heredable.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableDerived</td>
<td>El DDL de la tabla se hereda de una tabla de plantillas.</td>
</tr>
<tr class="even">
<td></td>
<td>TableNoFixedVarColumnsInDerivedTables</td>
<td>Columnas fijas o variables en las tablas derivadas (de modo que se puedan agregar columnas fijas o de variables a la plantilla en el futuro). Se usa junto con TableTemplate.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
