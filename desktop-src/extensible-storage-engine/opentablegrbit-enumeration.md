---
description: 'Más información sobre: enumeración OpenTableGrbit'
title: Enumeración OpenTableGrbit
TOCTitle: OpenTableGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.OpenTableGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.opentablegrbit(v=EXCHG.10)
ms:contentKeyID: 39510721
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.NoCache
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.DenyWrite
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.DenyRead
- Microsoft.Isam.Esent.Interop.OpenTableGrbit
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Preread
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass9
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass15
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass6
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass14
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass3
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass8
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass7
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Sequential
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass5
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass2
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.ReadOnly
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass4
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.None
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass10
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass13
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass12
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass1
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.PermitDDL
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass11
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass1
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass11
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass14
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Sequential
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass2
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass5
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass8
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.DenyRead
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.DenyWrite
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.PermitDDL
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass10
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass12
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass3
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.NoCache
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass9
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.OpenTableGrbit
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.None
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass4
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass7
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Preread
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.ReadOnly
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass13
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass15
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass6
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dfb2d75fc17e37dc669acf1fd84f38c957d467f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687687"
---
# <a name="opentablegrbit-enumeration"></a>Enumeración OpenTableGrbit

Opciones de JetOpenTable.

Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.

**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxis

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration OpenTableGrbit
'Usage
Dim instance As OpenTableGrbit
```

``` csharp
[FlagsAttribute]
public enum OpenTableGrbit
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
<td>DenyWrite</td>
<td>No se puede abrir esta tabla para acceso de escritura en otra sesión.</td>
</tr>
<tr class="odd">
<td></td>
<td>DenyRead</td>
<td>Esta tabla no se puede abrir para acceso de lectura en otra sesión.</td>
</tr>
<tr class="even">
<td></td>
<td>ReadOnly</td>
<td>Solicitar acceso de solo lectura a la tabla.</td>
</tr>
<tr class="odd">
<td></td>
<td>Actualizable</td>
<td>Solicitar acceso de escritura a la tabla.</td>
</tr>
<tr class="even">
<td></td>
<td>PermitDDL</td>
<td>Permitir modificaciones de DDL en una tabla marcada como FixedDDL. Esta opción debe usarse con DenyRead.</td>
</tr>
<tr class="odd">
<td></td>
<td>NoCache</td>
<td>No almacenar en caché las páginas de esta tabla.</td>
</tr>
<tr class="even">
<td></td>
<td>Lectura preleída</td>
<td>Proporciona una sugerencia que indica que la tabla probablemente no está en la caché del búfer y que la lectura previa puede ser beneficiosa para el rendimiento.</td>
</tr>
<tr class="odd">
<td></td>
<td>Secuencial</td>
<td>Asuma un patrón de acceso secuencial y páginas de base de datos de captura previa.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass1</td>
<td>La tabla pertenece a la clase de estadísticas 1.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass2</td>
<td>La tabla pertenece a la clase de estadísticas 2.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass3</td>
<td>La tabla pertenece a la clase de estadísticas 3.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass4</td>
<td>La tabla pertenece a la clase de estadísticas 4.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass5</td>
<td>La tabla pertenece a la clase de estadísticas 5.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass6</td>
<td>La tabla pertenece a la clase de estadísticas 6.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass7</td>
<td>La tabla pertenece a la clase de estadísticas 7.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass8</td>
<td>La tabla pertenece a la clase de estadísticas 8.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass9</td>
<td>La tabla pertenece a la clase de estadísticas 9.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass10</td>
<td>La tabla pertenece a la clase de estadísticas 10.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass11</td>
<td>La tabla pertenece a la clase de estadísticas 11.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass12</td>
<td>La tabla pertenece a la clase de estadísticas 12.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass13</td>
<td>La tabla pertenece a la clase de estadísticas 13.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass14</td>
<td>La tabla pertenece a la clase de estadísticas 14.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass15</td>
<td>La tabla pertenece a la clase de estadísticas 15.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Espacio de nombres Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
