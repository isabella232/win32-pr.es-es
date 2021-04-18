---
description: 'Más información sobre: API. JetGotoPosition (método)'
title: Método API. JetGotoPosition
TOCTitle: 'JetGotoPosition method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGotoPosition(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_RECPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgotoposition(v=EXCHG.10)
ms:contentKeyID: 55100756
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGotoPosition
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGotoPosition
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5917e729d1a9ae5ae0a3715d6a2a2a81f45f75e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705837"
---
# <a name="apijetgotoposition-method"></a><span data-ttu-id="734ed-103">Método API. JetGotoPosition</span><span class="sxs-lookup"><span data-stu-id="734ed-103">Api.JetGotoPosition method</span></span>

<span data-ttu-id="734ed-104">Mueve un cursor a una nueva ubicación que es una fracción del camino a través del índice actual.</span><span class="sxs-lookup"><span data-stu-id="734ed-104">Moves a cursor to a new location that is a fraction of the way through the current index.</span></span> <span data-ttu-id="734ed-105">Vea también [JetGetRecordPosition (JET_SESID, JET_TABLEID, JET_RECPOS)](./api.jetgetrecordposition-method.md).</span><span class="sxs-lookup"><span data-stu-id="734ed-105">Also see [JetGetRecordPosition(JET_SESID, JET_TABLEID, JET_RECPOS)](./api.jetgetrecordposition-method.md).</span></span>

<span data-ttu-id="734ed-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="734ed-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="734ed-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="734ed-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="734ed-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="734ed-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGotoPosition ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    recpos As JET_RECPOS _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim recpos As JET_RECPOSApi.JetGotoPosition(sesid, tableid, _
    recpos)
```

``` csharp
public static void JetGotoPosition(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_RECPOS recpos
)
```

#### <a name="parameters"></a><span data-ttu-id="734ed-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="734ed-109">Parameters</span></span>

  - <span data-ttu-id="734ed-110">sesid</span><span class="sxs-lookup"><span data-stu-id="734ed-110">sesid</span></span>  
    <span data-ttu-id="734ed-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="734ed-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="734ed-112">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="734ed-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="734ed-113">TABLEID</span><span class="sxs-lookup"><span data-stu-id="734ed-113">tableid</span></span>  
    <span data-ttu-id="734ed-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="734ed-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="734ed-115">Cursor que se va a colocar.</span><span class="sxs-lookup"><span data-stu-id="734ed-115">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="734ed-116">recpos</span><span class="sxs-lookup"><span data-stu-id="734ed-116">recpos</span></span>  
    <span data-ttu-id="734ed-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_RECPOS](./jet-recpos-class.md)</span><span class="sxs-lookup"><span data-stu-id="734ed-117">Type: [Microsoft.Isam.Esent.Interop.JET_RECPOS](./jet-recpos-class.md)</span></span>  
    
    <span data-ttu-id="734ed-118">Posición aproximada a la que se va a mover.</span><span class="sxs-lookup"><span data-stu-id="734ed-118">The approximate position to move to.</span></span>

## <a name="see-also"></a><span data-ttu-id="734ed-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="734ed-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="734ed-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="734ed-120">Reference</span></span>

[<span data-ttu-id="734ed-121">Clase de API</span><span class="sxs-lookup"><span data-stu-id="734ed-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="734ed-122">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="734ed-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="734ed-123">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="734ed-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
