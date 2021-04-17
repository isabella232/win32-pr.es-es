---
description: 'Más información sobre: enumeración RetrieveColumnGrbit'
title: Enumeración RetrieveColumnGrbit
TOCTitle: RetrieveColumnGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.retrievecolumngrbit(v=EXCHG.10)
ms:contentKeyID: 39511391
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.None
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromPrimaryBookmark
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveCopy
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromIndex
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveNull
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveIgnoreDefault
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveTag
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromIndex
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveCopy
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveNull
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.None
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromPrimaryBookmark
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveIgnoreDefault
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveTag
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a223a288b8ad2d2e976be3bb9f2f524f78b9a8fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687675"
---
# <a name="retrievecolumngrbit-enumeration"></a>Enumeración RetrieveColumnGrbit

Opciones de JetRetrieveColumn.

Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration RetrieveColumnGrbit
'Usage
Dim instance As RetrieveColumnGrbit
```

``` csharp
[FlagsAttribute]
public enum RetrieveColumnGrbit
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
<td>RetrieveCopy</td>
<td>Esta marca hace que la columna de recuperación recupere el valor modificado en lugar del valor original. Si el valor no se ha modificado, se recupera el valor original. De esta manera, se puede recuperar un valor que todavía no se ha insertado o actualizado durante la operación de inserción o actualización de un registro.</td>
</tr>
<tr class="odd">
<td></td>
<td>RetrieveFromIndex</td>
<td>Esta opción se utiliza para recuperar los valores de columna del índice, si es posible, sin tener acceso al registro. De esta manera, se puede evitar la carga innecesaria de registros cuando los datos necesarios están disponibles en las propias entradas de índice.</td>
</tr>
<tr class="even">
<td></td>
<td>RetrieveFromPrimaryBookmark</td>
<td>Esta opción se usa para recuperar valores de columna del marcador de índice y puede diferir del valor de índice cuando una columna aparece en el índice principal y en el índice actual. Esta opción no se debe especificar si el índice actual es el índice clúster o principal. No se puede establecer este bit si también se establece RetrieveFromIndex.</td>
</tr>
<tr class="odd">
<td></td>
<td>RetrieveTag</td>
<td>Esta opción se usa para recuperar el número de secuencia de un valor de columna de varios valores en JET_RETINFO. itagSequence. Recuperar el número de secuencia puede ser una operación costosa y solo debe realizarse si es necesario.</td>
</tr>
<tr class="even">
<td></td>
<td>RetrieveNull</td>
<td>Esta opción se usa para recuperar los valores NULL de las columnas con varios valores. Si no se especifica esta opción, se omitirán automáticamente los valores NULL de las columnas con varios valores.</td>
</tr>
<tr class="odd">
<td></td>
<td>RetrieveIgnoreDefault</td>
<td>Esta opción solo afecta a las columnas con varios valores y hace que se devuelva un valor NULL cuando el número de secuencia solicitado es 1 y no hay valores establecidos para la columna en el registro.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
