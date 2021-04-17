---
description: 'Más información sobre: enumeración DefragGrbit'
title: Enumeración DefragGrbit
TOCTitle: DefragGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.DefragGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.defraggrbit(v=EXCHG.10)
ms:contentKeyID: 39516122
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.DefragGrbit
- Microsoft.Isam.Esent.Interop.DefragGrbit.AvailSpaceTreesOnly
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStart
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStop
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.DefragGrbit
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStart
- Microsoft.Isam.Esent.Interop.DefragGrbit.AvailSpaceTreesOnly
- Microsoft.Isam.Esent.Interop.DefragGrbit.BatchStop
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e5da047fbdad20ac40d780dc5b0bba9e986e7672
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717289"
---
# <a name="defraggrbit-enumeration"></a><span data-ttu-id="3adfe-103">Enumeración DefragGrbit</span><span class="sxs-lookup"><span data-stu-id="3adfe-103">DefragGrbit enumeration</span></span>

<span data-ttu-id="3adfe-104">Opciones para [JetDefragment (JET_SESID, JET_DBID, String, Int32, Int32, DefragGrbit)](./api.jetdefragment-method.md).</span><span class="sxs-lookup"><span data-stu-id="3adfe-104">Options for [JetDefragment(JET_SESID, JET_DBID, String, Int32, Int32, DefragGrbit)](./api.jetdefragment-method.md).</span></span>

<span data-ttu-id="3adfe-105">Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.</span><span class="sxs-lookup"><span data-stu-id="3adfe-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="3adfe-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3adfe-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3adfe-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3adfe-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3adfe-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3adfe-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration DefragGrbit
'Usage
Dim instance As DefragGrbit
```

``` csharp
[FlagsAttribute]
public enum DefragGrbit
```

## <a name="members"></a><span data-ttu-id="3adfe-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="3adfe-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="3adfe-110">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="3adfe-110">Member name</span></span></th>
<th><span data-ttu-id="3adfe-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="3adfe-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="3adfe-112">AvailSpaceTreesOnly</span><span class="sxs-lookup"><span data-stu-id="3adfe-112">AvailSpaceTreesOnly</span></span></td>
<td><span data-ttu-id="3adfe-113">Desfragmenta la parte de espacio disponible de la asignación de espacio de la base de datos de ESE.</span><span class="sxs-lookup"><span data-stu-id="3adfe-113">Defragments the available space portion of ESE database space allocation.</span></span> <span data-ttu-id="3adfe-114">El espacio de la base de datos se divide en dos tipos, espacio de propiedad y espacio disponible.</span><span class="sxs-lookup"><span data-stu-id="3adfe-114">Database space is divided into two types, owned space and available space.</span></span> <span data-ttu-id="3adfe-115">El espacio de propiedad se asigna a una tabla o un índice mientras que el espacio disponible está listo para su uso en la tabla o el índice, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="3adfe-115">Owned space is allocated to a table or index while available space is ready for use within the table or index, respectively.</span></span> <span data-ttu-id="3adfe-116">El espacio disponible es mucho más dinámico en el comportamiento y requiere una desfragmentación en línea más que el espacio de propiedad o los datos de la tabla o el índice.</span><span class="sxs-lookup"><span data-stu-id="3adfe-116">Available space is much more dynamic in behavior and requires on-line defragmentation more so than owned space or table or index data.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="3adfe-117">BatchStart</span><span class="sxs-lookup"><span data-stu-id="3adfe-117">BatchStart</span></span></td>
<td><span data-ttu-id="3adfe-118">Inicia una nueva tarea de desfragmentación.</span><span class="sxs-lookup"><span data-stu-id="3adfe-118">Starts a new defragmentation task.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="3adfe-119">BatchStop</span><span class="sxs-lookup"><span data-stu-id="3adfe-119">BatchStop</span></span></td>
<td><span data-ttu-id="3adfe-120">Detiene una tarea de desfragmentación.</span><span class="sxs-lookup"><span data-stu-id="3adfe-120">Stops a defragmentation task.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="3adfe-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="3adfe-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3adfe-122">Referencia</span><span class="sxs-lookup"><span data-stu-id="3adfe-122">Reference</span></span>

[<span data-ttu-id="3adfe-123">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="3adfe-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
