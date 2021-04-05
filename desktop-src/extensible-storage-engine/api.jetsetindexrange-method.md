---
description: 'Más información sobre: API. JetSetIndexRange (método)'
title: Método API. JetSetIndexRange
TOCTitle: 'JetSetIndexRange method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetIndexRange(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetindexrange(v=EXCHG.10)
ms:contentKeyID: 55100817
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetIndexRange
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetIndexRange
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3ad13e04674de60aa1c0f55cf4cd4570f8b7ddaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082042"
---
# <a name="apijetsetindexrange-method"></a><span data-ttu-id="6f2a9-103">Método API. JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="6f2a9-103">Api.JetSetIndexRange method</span></span>

<span data-ttu-id="6f2a9-104">Limita temporalmente el conjunto de entradas de índice que el cursor puede recorrer usando [JetMove (JET_SESID, JET_TABLEID, Int32, MoveGrbit)](./api.jetmove-method-jet-sesid-jet-tableid-int32-movegrbit-.md) a las que comienzan en la entrada de índice actual y terminan en la entrada de índice que coincide con los criterios de búsqueda especificados por la clave de búsqueda en ese cursor y los criterios enlazados especificados.</span><span class="sxs-lookup"><span data-stu-id="6f2a9-104">Temporarily limits the set of index entries that the cursor can walk using [JetMove(JET_SESID, JET_TABLEID, Int32, MoveGrbit)](./api.jetmove-method-jet-sesid-jet-tableid-int32-movegrbit-.md) to those starting from the current index entry and ending at the index entry that matches the search criteria specified by the search key in that cursor and the specified bound criteria.</span></span> <span data-ttu-id="6f2a9-105">Una clave de búsqueda se debe haber construido previamente mediante [JetMakeKey (JET_SESID, JET_TABLEID, \[ \] , Int32, MakeKeyGrbit)](./api.jetmakekey-method.md).</span><span class="sxs-lookup"><span data-stu-id="6f2a9-105">A search key must have been previously constructed using [JetMakeKey(JET_SESID, JET_TABLEID, \[\], Int32, MakeKeyGrbit)](./api.jetmakekey-method.md).</span></span> <span data-ttu-id="6f2a9-106">Vea también [TrySetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.trysetindexrange-method.md).</span><span class="sxs-lookup"><span data-stu-id="6f2a9-106">Also see [TrySetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.trysetindexrange-method.md).</span></span>

<span data-ttu-id="6f2a9-107">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6f2a9-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6f2a9-108">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6f2a9-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6f2a9-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f2a9-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetIndexRange ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As SetIndexRangeGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As SetIndexRangeGrbitApi.JetSetIndexRange(sesid, tableid, _
    grbit)
```

``` csharp
public static void JetSetIndexRange(
    JET_SESID sesid,
    JET_TABLEID tableid,
    SetIndexRangeGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="6f2a9-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f2a9-110">Parameters</span></span>

  - <span data-ttu-id="6f2a9-111">sesid</span><span class="sxs-lookup"><span data-stu-id="6f2a9-111">sesid</span></span>  
    <span data-ttu-id="6f2a9-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6f2a9-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="6f2a9-113">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="6f2a9-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="6f2a9-114">TABLEID</span><span class="sxs-lookup"><span data-stu-id="6f2a9-114">tableid</span></span>  
    <span data-ttu-id="6f2a9-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6f2a9-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="6f2a9-116">Cursor en el que se va a establecer el intervalo de índices.</span><span class="sxs-lookup"><span data-stu-id="6f2a9-116">The cursor to set the index range on.</span></span>

<!-- end list -->

  - <span data-ttu-id="6f2a9-117">grbit</span><span class="sxs-lookup"><span data-stu-id="6f2a9-117">grbit</span></span>  
    <span data-ttu-id="6f2a9-118">Tipo: [Microsoft. ISAM. esent. Interop. SetIndexRangeGrbit](./setindexrangegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="6f2a9-118">Type: [Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit](./setindexrangegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="6f2a9-119">Opciones de intervalo de índices.</span><span class="sxs-lookup"><span data-stu-id="6f2a9-119">Index range options.</span></span>

## <a name="see-also"></a><span data-ttu-id="6f2a9-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f2a9-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6f2a9-121">Referencia</span><span class="sxs-lookup"><span data-stu-id="6f2a9-121">Reference</span></span>

[<span data-ttu-id="6f2a9-122">Clase de API</span><span class="sxs-lookup"><span data-stu-id="6f2a9-122">Api class</span></span>](./api-class.md)

[<span data-ttu-id="6f2a9-123">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="6f2a9-123">Api members</span></span>](./api-members.md)

[<span data-ttu-id="6f2a9-124">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="6f2a9-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
