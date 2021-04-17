---
description: 'Más información sobre: enumeración SetIndexRangeGrbit'
title: Enumeración SetIndexRangeGrbit
TOCTitle: SetIndexRangeGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.setindexrangegrbit(v=EXCHG.10)
ms:contentKeyID: 39515181
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.None
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeInclusive
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeInstantDuration
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeRemove
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeUpperLimit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeInstantDuration
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeUpperLimit
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.None
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeInclusive
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeRemove
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6cda73597f88d2c8fca911ebb96d7a3c6399ed9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686979"
---
# <a name="setindexrangegrbit-enumeration"></a><span data-ttu-id="1fdc9-103">Enumeración SetIndexRangeGrbit</span><span class="sxs-lookup"><span data-stu-id="1fdc9-103">SetIndexRangeGrbit enumeration</span></span>

<span data-ttu-id="1fdc9-104">Opciones de JetSetIndexRange.</span><span class="sxs-lookup"><span data-stu-id="1fdc9-104">Options for JetSetIndexRange.</span></span>

<span data-ttu-id="1fdc9-105">Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.</span><span class="sxs-lookup"><span data-stu-id="1fdc9-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="1fdc9-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1fdc9-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1fdc9-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1fdc9-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1fdc9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1fdc9-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SetIndexRangeGrbit
'Usage
Dim instance As SetIndexRangeGrbit
```

``` csharp
[FlagsAttribute]
public enum SetIndexRangeGrbit
```

## <a name="members"></a><span data-ttu-id="1fdc9-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="1fdc9-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="1fdc9-110">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="1fdc9-110">Member name</span></span></th>
<th><span data-ttu-id="1fdc9-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="1fdc9-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="1fdc9-112">None</span><span class="sxs-lookup"><span data-stu-id="1fdc9-112">None</span></span></td>
<td><span data-ttu-id="1fdc9-113">Opciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="1fdc9-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="1fdc9-114">RangeInclusive</span><span class="sxs-lookup"><span data-stu-id="1fdc9-114">RangeInclusive</span></span></td>
<td><span data-ttu-id="1fdc9-115">Esta opción indica que el límite del intervalo de índice es inclusivo.</span><span class="sxs-lookup"><span data-stu-id="1fdc9-115">This option indicates that the limit of the index range is inclusive.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="1fdc9-116">RangeUpperLimit</span><span class="sxs-lookup"><span data-stu-id="1fdc9-116">RangeUpperLimit</span></span></td>
<td><span data-ttu-id="1fdc9-117">La clave de búsqueda en el cursor representa los criterios de búsqueda para la entrada de índice más cercana al final del índice que coincidirá con el intervalo de índices.</span><span class="sxs-lookup"><span data-stu-id="1fdc9-117">The search key in the cursor represents the search criteria for the index entry closest to the end of the index that will match the index range.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="1fdc9-118">RangeInstantDuration</span><span class="sxs-lookup"><span data-stu-id="1fdc9-118">RangeInstantDuration</span></span></td>
<td><span data-ttu-id="1fdc9-119">El intervalo de índice debe quitarse en cuanto se haya establecido.</span><span class="sxs-lookup"><span data-stu-id="1fdc9-119">The index range should be removed as soon as it has been established.</span></span> <span data-ttu-id="1fdc9-120">Esto resulta útil para probar la existencia de entradas de índice que coinciden con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="1fdc9-120">This is useful for testing for the existence of index entries that match the search criteria.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="1fdc9-121">RangeRemove</span><span class="sxs-lookup"><span data-stu-id="1fdc9-121">RangeRemove</span></span></td>
<td><span data-ttu-id="1fdc9-122">Cancela y el intervalo de índice existente.</span><span class="sxs-lookup"><span data-stu-id="1fdc9-122">Cancel and existing index range.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="1fdc9-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="1fdc9-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1fdc9-124">Referencia</span><span class="sxs-lookup"><span data-stu-id="1fdc9-124">Reference</span></span>

[<span data-ttu-id="1fdc9-125">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="1fdc9-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
