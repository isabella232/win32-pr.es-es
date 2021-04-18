---
description: 'Más información sobre: enumeración SeekGrbit'
title: Enumeración SeekGrbit
TOCTitle: SeekGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SeekGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.seekgrbit(v=EXCHG.10)
ms:contentKeyID: 39515862
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SeekGrbit
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekEQ
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SetIndexRange
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLT
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SetIndexRange
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLE
- Microsoft.Isam.Esent.Interop.SeekGrbit
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekEQ
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9e59072055710676f5f7647130f42ad5acf50527
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687672"
---
# <a name="seekgrbit-enumeration"></a><span data-ttu-id="d0bc3-103">Enumeración SeekGrbit</span><span class="sxs-lookup"><span data-stu-id="d0bc3-103">SeekGrbit enumeration</span></span>

<span data-ttu-id="d0bc3-104">Opciones de JetSeek.</span><span class="sxs-lookup"><span data-stu-id="d0bc3-104">Options for JetSeek.</span></span>

<span data-ttu-id="d0bc3-105">Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.</span><span class="sxs-lookup"><span data-stu-id="d0bc3-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="d0bc3-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d0bc3-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d0bc3-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d0bc3-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d0bc3-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0bc3-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SeekGrbit
'Usage
Dim instance As SeekGrbit
```

``` csharp
[FlagsAttribute]
public enum SeekGrbit
```

## <a name="members"></a><span data-ttu-id="d0bc3-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="d0bc3-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="d0bc3-110">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="d0bc3-110">Member name</span></span></th>
<th><span data-ttu-id="d0bc3-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0bc3-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d0bc3-112">SeekEQ</span><span class="sxs-lookup"><span data-stu-id="d0bc3-112">SeekEQ</span></span></td>
<td><span data-ttu-id="d0bc3-113">El cursor se colocará en la entrada de índice más cercana al inicio del índice que coincida exactamente con la clave de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d0bc3-113">The cursor will be positioned at the index entry closest to the start of the index that exactly matches the search key.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d0bc3-114">SeekLT</span><span class="sxs-lookup"><span data-stu-id="d0bc3-114">SeekLT</span></span></td>
<td><span data-ttu-id="d0bc3-115">El cursor se colocará en la entrada de índice más cercana al final del índice que sea menor que una entrada de índice que coincida exactamente con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d0bc3-115">The cursor will be positioned at the index entry closest to the end of the index that is less than an index entry that would exactly match the search criteria.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d0bc3-116">SeekLE</span><span class="sxs-lookup"><span data-stu-id="d0bc3-116">SeekLE</span></span></td>
<td><span data-ttu-id="d0bc3-117">El cursor se colocará en la entrada de índice más cercana al final del índice que sea menor o igual que una entrada de índice que coincida exactamente con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d0bc3-117">The cursor will be positioned at the index entry closest to the end of the index that is less than or equal to an index entry that would exactly match the search criteria.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d0bc3-118">SeekGE</span><span class="sxs-lookup"><span data-stu-id="d0bc3-118">SeekGE</span></span></td>
<td><span data-ttu-id="d0bc3-119">El cursor se colocará en la entrada de índice más cercana al inicio del índice que sea mayor o igual que una entrada de índice que coincida exactamente con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d0bc3-119">The cursor will be positioned at the index entry closest to the start of the index that is greater than or equal to an index entry that would exactly match the search criteria.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d0bc3-120">SeekGT</span><span class="sxs-lookup"><span data-stu-id="d0bc3-120">SeekGT</span></span></td>
<td><span data-ttu-id="d0bc3-121">El cursor se colocará en la entrada de índice más cercana al inicio del índice que sea mayor que una entrada de índice que coincida exactamente con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d0bc3-121">The cursor will be positioned at the index entry closest to the start of the index that is greater than an index entry that would exactly match the search criteria.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d0bc3-122">SetIndexRange</span><span class="sxs-lookup"><span data-stu-id="d0bc3-122">SetIndexRange</span></span></td>
<td><span data-ttu-id="d0bc3-123">Se configurará automáticamente un intervalo de índice para todas las claves que coincidan exactamente con la clave de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d0bc3-123">An index range will automatically be setup for all keys that exactly match the search key.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="d0bc3-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0bc3-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d0bc3-125">Referencia</span><span class="sxs-lookup"><span data-stu-id="d0bc3-125">Reference</span></span>

[<span data-ttu-id="d0bc3-126">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d0bc3-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
