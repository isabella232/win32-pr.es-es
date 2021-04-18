---
description: 'Más información sobre: enumeración PrereadIndexRangesGrbit'
title: Enumeración PrereadIndexRangesGrbit (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: PrereadIndexRangesGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.prereadindexrangesgrbit(v=EXCHG.10)
ms:contentKeyID: 55104328
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.Backwards
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.FirstPageOnly
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.Forward
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.NormalizedKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.FirstPageOnly
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.Forward
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.Backwards
- Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit.NormalizedKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d4bc1b9877d4548a68aa71ea4def536af09d9693
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687686"
---
# <a name="prereadindexrangesgrbit-enumeration"></a><span data-ttu-id="7d1c4-103">Enumeración PrereadIndexRangesGrbit</span><span class="sxs-lookup"><span data-stu-id="7d1c4-103">PrereadIndexRangesGrbit enumeration</span></span>

<span data-ttu-id="7d1c4-104">Opciones para [JetPrereadIndexRanges (JET_SESID, JET_TABLEID, \[ \] , Int32, Int32, Int32, \[ \] , PrereadIndexRangesGrbit)](./windows8api.jetprereadindexranges-method.md).</span><span class="sxs-lookup"><span data-stu-id="7d1c4-104">Options for [JetPrereadIndexRanges(JET_SESID, JET_TABLEID, \[\], Int32, Int32, Int32, \[\], PrereadIndexRangesGrbit)](./windows8api.jetprereadindexranges-method.md).</span></span>

<span data-ttu-id="7d1c4-105">Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.</span><span class="sxs-lookup"><span data-stu-id="7d1c4-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="7d1c4-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7d1c4-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="7d1c4-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7d1c4-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7d1c4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7d1c4-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration PrereadIndexRangesGrbit
'Usage
Dim instance As PrereadIndexRangesGrbit
```

``` csharp
[FlagsAttribute]
public enum PrereadIndexRangesGrbit
```

## <a name="members"></a><span data-ttu-id="7d1c4-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="7d1c4-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="7d1c4-110">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="7d1c4-110">Member name</span></span></th>
<th><span data-ttu-id="7d1c4-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="7d1c4-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="7d1c4-112">Adelante</span><span class="sxs-lookup"><span data-stu-id="7d1c4-112">Forward</span></span></td>
<td><span data-ttu-id="7d1c4-113">Avance de prelectura.</span><span class="sxs-lookup"><span data-stu-id="7d1c4-113">Preread forward.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="7d1c4-114">Atrás</span><span class="sxs-lookup"><span data-stu-id="7d1c4-114">Backwards</span></span></td>
<td><span data-ttu-id="7d1c4-115">Lectura inversa.</span><span class="sxs-lookup"><span data-stu-id="7d1c4-115">Preread backwards.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="7d1c4-116">FirstPageOnly</span><span class="sxs-lookup"><span data-stu-id="7d1c4-116">FirstPageOnly</span></span></td>
<td><span data-ttu-id="7d1c4-117">Primera página de solo lectura de cualquier columna larga.</span><span class="sxs-lookup"><span data-stu-id="7d1c4-117">Preread only first page of any long column.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="7d1c4-118">NormalizedKey</span><span class="sxs-lookup"><span data-stu-id="7d1c4-118">NormalizedKey</span></span></td>
<td><span data-ttu-id="7d1c4-119">Clave/marcador normalizado proporcionado en lugar de valor de columna.</span><span class="sxs-lookup"><span data-stu-id="7d1c4-119">Normalized key/bookmark provided instead of column value.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="7d1c4-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="7d1c4-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7d1c4-121">Referencia</span><span class="sxs-lookup"><span data-stu-id="7d1c4-121">Reference</span></span>

[<span data-ttu-id="7d1c4-122">Espacio de nombres Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="7d1c4-122">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
