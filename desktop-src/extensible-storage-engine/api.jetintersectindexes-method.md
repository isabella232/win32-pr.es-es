---
description: 'Más información sobre: API. JetIntersectIndexes (método)'
title: Método API. JetIntersectIndexes
TOCTitle: 'JetIntersectIndexes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetIntersectIndexes(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_INDEXRANGE[],System.Int32,Microsoft.Isam.Esent.Interop.JET_RECORDLIST@,Microsoft.Isam.Esent.Interop.IntersectIndexesGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetintersectindexes(v=EXCHG.10)
ms:contentKeyID: 55100761
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetIntersectIndexes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetIntersectIndexes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3bae632f386ef944e79a17813d1cc86451441e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003106"
---
# <a name="apijetintersectindexes-method"></a><span data-ttu-id="627ac-103">Método API. JetIntersectIndexes</span><span class="sxs-lookup"><span data-stu-id="627ac-103">Api.JetIntersectIndexes method</span></span>

<span data-ttu-id="627ac-104">Calcula la intersección entre varios conjuntos de entradas de índice de distintos índices secundarios en la misma tabla.</span><span class="sxs-lookup"><span data-stu-id="627ac-104">Computes the intersection between multiple sets of index entries from different secondary indices over the same table.</span></span> <span data-ttu-id="627ac-105">Esta operación es útil para buscar el conjunto de registros de una tabla que coinciden con dos o más criterios que se pueden expresar mediante intervalos de índice.</span><span class="sxs-lookup"><span data-stu-id="627ac-105">This operation is useful for finding the set of records in a table that match two or more criteria that can be expressed using index ranges.</span></span> <span data-ttu-id="627ac-106">Vea también [IntersectIndexes (JET_SESID, \[ \] )](./api.intersectindexes-method.md).</span><span class="sxs-lookup"><span data-stu-id="627ac-106">Also see [IntersectIndexes(JET_SESID, \[\])](./api.intersectindexes-method.md).</span></span>

<span data-ttu-id="627ac-107">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="627ac-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="627ac-108">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="627ac-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="627ac-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="627ac-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetIntersectIndexes ( _
    sesid As JET_SESID, _
    ranges As JET_INDEXRANGE(), _
    numRanges As Integer, _
    <OutAttribute> ByRef recordlist As JET_RECORDLIST, _
    grbit As IntersectIndexesGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim ranges As JET_INDEXRANGE()
Dim numRanges As Integer
Dim recordlist As JET_RECORDLIST
Dim grbit As IntersectIndexesGrbitApi.JetIntersectIndexes(sesid, _
    ranges, numRanges, recordlist, grbit)
```

``` csharp
public static void JetIntersectIndexes(
    JET_SESID sesid,
    JET_INDEXRANGE[] ranges,
    int numRanges,
    out JET_RECORDLIST recordlist,
    IntersectIndexesGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="627ac-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="627ac-110">Parameters</span></span>

  - <span data-ttu-id="627ac-111">sesid</span><span class="sxs-lookup"><span data-stu-id="627ac-111">sesid</span></span>  
    <span data-ttu-id="627ac-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="627ac-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="627ac-113">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="627ac-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="627ac-114">ranges</span><span class="sxs-lookup"><span data-stu-id="627ac-114">ranges</span></span>  
    <span data-ttu-id="627ac-115">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="627ac-115">Type: \[\]</span></span>  
    
    <span data-ttu-id="627ac-116">El índice va a formar una intersección.</span><span class="sxs-lookup"><span data-stu-id="627ac-116">An the index ranges to intersect.</span></span> <span data-ttu-id="627ac-117">Los tableids de los intervalos deben tener establecidos intervalos de índice.</span><span class="sxs-lookup"><span data-stu-id="627ac-117">The tableids in the ranges must have index ranges set on them.</span></span> <span data-ttu-id="627ac-118">Use [JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md) para crear un intervalo de índices.</span><span class="sxs-lookup"><span data-stu-id="627ac-118">Use [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md) to create an index range.</span></span>

<!-- end list -->

  - <span data-ttu-id="627ac-119">numRanges</span><span class="sxs-lookup"><span data-stu-id="627ac-119">numRanges</span></span>  
    <span data-ttu-id="627ac-120">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="627ac-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="627ac-121">Número de intervalos de índice.</span><span class="sxs-lookup"><span data-stu-id="627ac-121">The number of index ranges.</span></span>

<!-- end list -->

  - <span data-ttu-id="627ac-122">recordlist</span><span class="sxs-lookup"><span data-stu-id="627ac-122">recordlist</span></span>  
    <span data-ttu-id="627ac-123">Tipo: [Microsoft.ISAM.esent.Interop.JET_RECORDLIST](./jet-recordlist-class.md)</span><span class="sxs-lookup"><span data-stu-id="627ac-123">Type: [Microsoft.Isam.Esent.Interop.JET_RECORDLIST](./jet-recordlist-class.md)</span></span>  
    
    <span data-ttu-id="627ac-124">Devuelve información sobre la tabla temporal que contiene los resultados de la intersección.</span><span class="sxs-lookup"><span data-stu-id="627ac-124">Returns information about the temporary table containing the intersection results.</span></span>

<!-- end list -->

  - <span data-ttu-id="627ac-125">grbit</span><span class="sxs-lookup"><span data-stu-id="627ac-125">grbit</span></span>  
    <span data-ttu-id="627ac-126">Tipo: [Microsoft. ISAM. esent. Interop. IntersectIndexesGrbit](./intersectindexesgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="627ac-126">Type: [Microsoft.Isam.Esent.Interop.IntersectIndexesGrbit](./intersectindexesgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="627ac-127">Opciones de intersección.</span><span class="sxs-lookup"><span data-stu-id="627ac-127">Intersection options.</span></span>

## <a name="see-also"></a><span data-ttu-id="627ac-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="627ac-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="627ac-129">Referencia</span><span class="sxs-lookup"><span data-stu-id="627ac-129">Reference</span></span>

[<span data-ttu-id="627ac-130">Clase de API</span><span class="sxs-lookup"><span data-stu-id="627ac-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="627ac-131">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="627ac-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="627ac-132">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="627ac-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
