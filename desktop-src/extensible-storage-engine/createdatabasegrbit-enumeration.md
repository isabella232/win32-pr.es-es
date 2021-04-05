---
description: 'Más información sobre: enumeración CreateDatabaseGrbit'
title: Enumeración CreateDatabaseGrbit
TOCTitle: CreateDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.createdatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 39515634
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.OverwriteExisting
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.RecoveryOff
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.OverwriteExisting
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.RecoveryOff
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8e23b7b875863b747fc5d2ba021c90d5f7f71048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082248"
---
# <a name="createdatabasegrbit-enumeration"></a>Enumeración CreateDatabaseGrbit

Opciones para [JetCreateDatabase (JET_SESID, cadena, cadena, JET_DBID, CreateDatabaseGrbit)](./api.jetcreatedatabase-method.md).

Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CreateDatabaseGrbit
'Usage
Dim instance As CreateDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum CreateDatabaseGrbit
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
<td>OverwriteExisting</td>
<td>De forma predeterminada, si se llama a JetCreateDatabase y la base de datos ya existe, se producirá un error en la llamada a la API y no se sobrescribirá la base de datos original. OverwriteExisting cambia este comportamiento y la antigua base de datos se sobrescribirá con otra nueva.</td>
</tr>
<tr class="odd">
<td></td>
<td>RecoveryOff</td>
<td>Desactiva el registro. La configuración de este bit pierde la capacidad de reproducir archivos de registro y de recuperar la base de datos a un estado utilizable coherente después de un bloqueo.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
