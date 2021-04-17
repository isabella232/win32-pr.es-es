---
description: 'Más información sobre: enumeración CompactGrbit'
title: Enumeración CompactGrbit
TOCTitle: CompactGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CompactGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.compactgrbit(v=EXCHG.10)
ms:contentKeyID: 39509676
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CompactGrbit
- Microsoft.Isam.Esent.Interop.CompactGrbit.None
- Microsoft.Isam.Esent.Interop.CompactGrbit.Stats
- Microsoft.Isam.Esent.Interop.CompactGrbit.Repair
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CompactGrbit.Repair
- Microsoft.Isam.Esent.Interop.CompactGrbit.Stats
- Microsoft.Isam.Esent.Interop.CompactGrbit
- Microsoft.Isam.Esent.Interop.CompactGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c7bbe6c88a0a52ab852e3cde9af8871833948949
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652487"
---
# <a name="compactgrbit-enumeration"></a><span data-ttu-id="460c4-103">Enumeración CompactGrbit</span><span class="sxs-lookup"><span data-stu-id="460c4-103">CompactGrbit enumeration</span></span>

<span data-ttu-id="460c4-104">Opciones para [JetCompact (JET_SESID, cadena, cadena, JET_PFNSTATUS, JET_CONVERT, CompactGrbit)](./api.jetcompact-method.md).</span><span class="sxs-lookup"><span data-stu-id="460c4-104">Options for [JetCompact(JET_SESID, String, String, JET_PFNSTATUS, JET_CONVERT, CompactGrbit)](./api.jetcompact-method.md).</span></span>

<span data-ttu-id="460c4-105">Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.</span><span class="sxs-lookup"><span data-stu-id="460c4-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="460c4-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="460c4-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="460c4-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="460c4-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="460c4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="460c4-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CompactGrbit
'Usage
Dim instance As CompactGrbit
```

``` csharp
[FlagsAttribute]
public enum CompactGrbit
```

## <a name="members"></a><span data-ttu-id="460c4-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="460c4-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="460c4-110">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="460c4-110">Member name</span></span></th>
<th><span data-ttu-id="460c4-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="460c4-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="460c4-112">None</span><span class="sxs-lookup"><span data-stu-id="460c4-112">None</span></span></td>
<td><span data-ttu-id="460c4-113">Opciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="460c4-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="460c4-114">Estadísticas</span><span class="sxs-lookup"><span data-stu-id="460c4-114">Stats</span></span></td>
<td><span data-ttu-id="460c4-115">Hace que JetCompact vuelque las estadísticas de la base de datos de origen en un archivo denominado DFRGINFO.TXT.</span><span class="sxs-lookup"><span data-stu-id="460c4-115">Causes JetCompact to dump statistics on the source database to a file named DFRGINFO.TXT.</span></span> <span data-ttu-id="460c4-116">Las estadísticas incluyen el nombre de cada tabla en la base de datos de origen, el número de filas de cada tabla, el tamaño total en bytes de todas las filas de cada tabla, el tamaño total en bytes de todas las columnas de tipo <a href="hh577895(v=exchg.10).md">LongText</a> o <a href="hh577895(v=exchg.10).md">LongBinary</a> que eran lo suficientemente grandes como para almacenarse por separado del registro, el número de páginas hoja del índice clúster y el número de páginas</span><span class="sxs-lookup"><span data-stu-id="460c4-116">Statistics include the name of each table in source database, number of rows in each table, total size in bytes of all rows in each table, total size in bytes of all columns of type <a href="hh577895(v=exchg.10).md">LongText</a> or <a href="hh577895(v=exchg.10).md">LongBinary</a> that were large enough to be stored separate from the record, number of clustered index leaf pages, and the number of long value leaf pages.</span></span> <span data-ttu-id="460c4-117">Además, también se vuelcan todas las estadísticas de Resumen, incluido el tamaño de la base de datos de origen, la base de datos de destino, el tiempo necesario para la compactación de bases de datos.</span><span class="sxs-lookup"><span data-stu-id="460c4-117">In addition, summary statistics including the size of the source database, destination database, time required for database compaction, temporary database space are all dumped as well.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="460c4-118">Reparación</span><span class="sxs-lookup"><span data-stu-id="460c4-118">Repair</span></span></td>
<td><span data-ttu-id="460c4-119"><strong>Obsoleto.</strong></span><span class="sxs-lookup"><span data-stu-id="460c4-119"><strong>Obsolete.</strong></span></span> <span data-ttu-id="460c4-120">Se usa cuando se sabe que la base de datos de origen está dañada.</span><span class="sxs-lookup"><span data-stu-id="460c4-120">Used when the source database is known to be corrupt.</span></span> <span data-ttu-id="460c4-121">Habilita un conjunto completo de nuevos comportamientos para recuperar tantos datos como sea posible de la base de datos de origen.</span><span class="sxs-lookup"><span data-stu-id="460c4-121">It enables a whole set of new behaviors intended to salvage as much data as possible from the source database.</span></span> <span data-ttu-id="460c4-122">JetCompact con este conjunto de opciones puede devolver <a href="hh564840(v=exchg.10).md">Success</a> pero no copiar todos los datos creados en la base de datos de origen.</span><span class="sxs-lookup"><span data-stu-id="460c4-122">JetCompact with this option set may return <a href="hh564840(v=exchg.10).md">Success</a> but not copy all of the data created in the source database.</span></span> <span data-ttu-id="460c4-123">Se omitirán los datos que se encontraban en partes dañadas de la base de datos de origen.</span><span class="sxs-lookup"><span data-stu-id="460c4-123">Data that was in damaged portions of the source database will be skipped.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="460c4-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="460c4-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="460c4-125">Referencia</span><span class="sxs-lookup"><span data-stu-id="460c4-125">Reference</span></span>

[<span data-ttu-id="460c4-126">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="460c4-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
