---
description: 'Más información sobre: API. JetDupCursor (método)'
title: Método API. JetDupCursor
TOCTitle: 'JetDupCursor method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDupCursor(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_TABLEID@,Microsoft.Isam.Esent.Interop.DupCursorGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdupcursor(v=EXCHG.10)
ms:contentKeyID: 55100686
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDupCursor
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDupCursor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5fce19d23838f3dfeab5317bfa7ea1aaacfcb508
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540867"
---
# <a name="apijetdupcursor-method"></a><span data-ttu-id="e8e75-103">Método API. JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="e8e75-103">Api.JetDupCursor method</span></span>

<span data-ttu-id="e8e75-104">Duplica un cursor abierto y devuelve un identificador al cursor duplicado.</span><span class="sxs-lookup"><span data-stu-id="e8e75-104">Duplicates an open cursor and returns a handle to the duplicated cursor.</span></span> <span data-ttu-id="e8e75-105">Si el cursor que se duplicó era un cursor de solo lectura, el cursor duplicado también es un cursor de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e8e75-105">If the cursor that was duplicated was a read-only cursor then the duplicated cursor is also a read-only cursor.</span></span> <span data-ttu-id="e8e75-106">Cualquier estado relacionado con la creación de una clave de búsqueda o la actualización de un registro no se copia en el cursor duplicado.</span><span class="sxs-lookup"><span data-stu-id="e8e75-106">Any state related to constructing a search key or updating a record is not copied into the duplicated cursor.</span></span> <span data-ttu-id="e8e75-107">Además, la ubicación del cursor original no se duplica en el cursor duplicado.</span><span class="sxs-lookup"><span data-stu-id="e8e75-107">In addition, the location of the original cursor is not duplicated into the duplicated cursor.</span></span> <span data-ttu-id="e8e75-108">El cursor duplicado siempre se abre en el índice clúster y su ubicación siempre está en la primera fila de la tabla.</span><span class="sxs-lookup"><span data-stu-id="e8e75-108">The duplicated cursor is always opened on the clustered index and its location is always on the first row of the table.</span></span>

<span data-ttu-id="e8e75-109">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e8e75-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e8e75-110">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e8e75-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e8e75-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8e75-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDupCursor ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef newTableid As JET_TABLEID, _
    grbit As DupCursorGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim newTableid As JET_TABLEID
Dim grbit As DupCursorGrbitApi.JetDupCursor(sesid, tableid, _
    newTableid, grbit)
```

``` csharp
public static void JetDupCursor(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out JET_TABLEID newTableid,
    DupCursorGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="e8e75-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e8e75-112">Parameters</span></span>

  - <span data-ttu-id="e8e75-113">sesid</span><span class="sxs-lookup"><span data-stu-id="e8e75-113">sesid</span></span>  
    <span data-ttu-id="e8e75-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e8e75-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e8e75-115">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="e8e75-115">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="e8e75-116">TABLEID</span><span class="sxs-lookup"><span data-stu-id="e8e75-116">tableid</span></span>  
    <span data-ttu-id="e8e75-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e8e75-117">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e8e75-118">Cursor que se va a duplicar.</span><span class="sxs-lookup"><span data-stu-id="e8e75-118">The cursor to duplicate.</span></span>

<!-- end list -->

  - <span data-ttu-id="e8e75-119">newTableid</span><span class="sxs-lookup"><span data-stu-id="e8e75-119">newTableid</span></span>  
    <span data-ttu-id="e8e75-120">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e8e75-120">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e8e75-121">Cursor duplicado.</span><span class="sxs-lookup"><span data-stu-id="e8e75-121">The duplicated cursor.</span></span>

<!-- end list -->

  - <span data-ttu-id="e8e75-122">grbit</span><span class="sxs-lookup"><span data-stu-id="e8e75-122">grbit</span></span>  
    <span data-ttu-id="e8e75-123">Tipo: [Microsoft. ISAM. esent. Interop. DupCursorGrbit](./dupcursorgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e8e75-123">Type: [Microsoft.Isam.Esent.Interop.DupCursorGrbit](./dupcursorgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="e8e75-124">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="e8e75-124">Reserved for future use.</span></span>

## <a name="see-also"></a><span data-ttu-id="e8e75-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8e75-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e8e75-126">Referencia</span><span class="sxs-lookup"><span data-stu-id="e8e75-126">Reference</span></span>

[<span data-ttu-id="e8e75-127">Clase de API</span><span class="sxs-lookup"><span data-stu-id="e8e75-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="e8e75-128">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="e8e75-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="e8e75-129">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e8e75-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
