---
description: 'Más información sobre: API. TrySetIndexRange (método)'
title: Método API. TrySetIndexRange
TOCTitle: 'TrySetIndexRange method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TrySetIndexRange(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.trysetindexrange(v=EXCHG.10)
ms:contentKeyID: 55100893
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TrySetIndexRange
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TrySetIndexRange
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d175fdfc931d24742d61f962a45e690a5c49c2be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818451"
---
# <a name="apitrysetindexrange-method"></a><span data-ttu-id="78fa0-103">Método API. TrySetIndexRange</span><span class="sxs-lookup"><span data-stu-id="78fa0-103">Api.TrySetIndexRange method</span></span>

<span data-ttu-id="78fa0-104">Limita temporalmente el conjunto de entradas de índice que el cursor puede recorrer usando JetMove para que empiecen a partir de la entrada de índice actual y terminen en la entrada de índice que coincide con los criterios de búsqueda especificados por la clave de búsqueda en ese cursor y los criterios enlazados especificados.</span><span class="sxs-lookup"><span data-stu-id="78fa0-104">Temporarily limits the set of index entries that the cursor can walk using JetMove to those starting from the current index entry and ending at the index entry that matches the search criteria specified by the search key in that cursor and the specified bound criteria.</span></span> <span data-ttu-id="78fa0-105">Una clave de búsqueda se debe haber construido previamente mediante JetMakeKey.</span><span class="sxs-lookup"><span data-stu-id="78fa0-105">A search key must have been previously constructed using JetMakeKey.</span></span> <span data-ttu-id="78fa0-106">Devuelve true si el intervalo de índice no está vacío; en caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="78fa0-106">Returns true if the index range is non-empty, false otherwise.</span></span>

<span data-ttu-id="78fa0-107">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="78fa0-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="78fa0-108">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="78fa0-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="78fa0-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="78fa0-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TrySetIndexRange ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As SetIndexRangeGrbit _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As SetIndexRangeGrbit
Dim returnValue As Boolean

returnValue = Api.TrySetIndexRange(sesid, _
    tableid, grbit)
```

``` csharp
public static bool TrySetIndexRange(
    JET_SESID sesid,
    JET_TABLEID tableid,
    SetIndexRangeGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="78fa0-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="78fa0-110">Parameters</span></span>

  - <span data-ttu-id="78fa0-111">sesid</span><span class="sxs-lookup"><span data-stu-id="78fa0-111">sesid</span></span>  
    <span data-ttu-id="78fa0-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="78fa0-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="78fa0-113">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="78fa0-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="78fa0-114">TABLEID</span><span class="sxs-lookup"><span data-stu-id="78fa0-114">tableid</span></span>  
    <span data-ttu-id="78fa0-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="78fa0-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="78fa0-116">Cursor que se va a colocar.</span><span class="sxs-lookup"><span data-stu-id="78fa0-116">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="78fa0-117">grbit</span><span class="sxs-lookup"><span data-stu-id="78fa0-117">grbit</span></span>  
    <span data-ttu-id="78fa0-118">Tipo: [Microsoft. ISAM. esent. Interop. SetIndexRangeGrbit](./setindexrangegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="78fa0-118">Type: [Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit](./setindexrangegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="78fa0-119">Opción de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="78fa0-119">Seek option.</span></span>

#### <a name="return-value"></a><span data-ttu-id="78fa0-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="78fa0-120">Return value</span></span>

<span data-ttu-id="78fa0-121">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="78fa0-121">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="78fa0-122">True si la búsqueda se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="78fa0-122">True if the seek was successful.</span></span>  

## <a name="see-also"></a><span data-ttu-id="78fa0-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="78fa0-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="78fa0-124">Referencia</span><span class="sxs-lookup"><span data-stu-id="78fa0-124">Reference</span></span>

[<span data-ttu-id="78fa0-125">Clase de API</span><span class="sxs-lookup"><span data-stu-id="78fa0-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="78fa0-126">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="78fa0-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="78fa0-127">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="78fa0-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
