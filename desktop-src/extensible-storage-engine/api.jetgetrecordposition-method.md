---
description: 'Más información sobre: API. JetGetRecordPosition (método)'
title: Método API. JetGetRecordPosition
TOCTitle: 'JetGetRecordPosition method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetRecordPosition(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_RECPOS@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetrecordposition(v=EXCHG.10)
ms:contentKeyID: 55100722
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetRecordPosition
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetRecordPosition
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 00350853172d784c270c197e7c58ad6fa616560f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540835"
---
# <a name="apijetgetrecordposition-method"></a><span data-ttu-id="4bede-103">Método API. JetGetRecordPosition</span><span class="sxs-lookup"><span data-stu-id="4bede-103">Api.JetGetRecordPosition method</span></span>

<span data-ttu-id="4bede-104">Devuelve la posición fraccionaria del registro actual en el índice actual en forma de estructura de [JET_RECPOS](./jet-recpos-class.md) .</span><span class="sxs-lookup"><span data-stu-id="4bede-104">Returns the fractional position of the current record in the current index in the form of a [JET_RECPOS](./jet-recpos-class.md) structure.</span></span> <span data-ttu-id="4bede-105">Vea también [JetGotoPosition (JET_SESID, JET_TABLEID, JET_RECPOS)](./api.jetgotoposition-method.md).</span><span class="sxs-lookup"><span data-stu-id="4bede-105">Also see [JetGotoPosition(JET_SESID, JET_TABLEID, JET_RECPOS)](./api.jetgotoposition-method.md).</span></span>

<span data-ttu-id="4bede-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4bede-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4bede-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4bede-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4bede-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4bede-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetRecordPosition ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef recpos As JET_RECPOS _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim recpos As JET_RECPOSApi.JetGetRecordPosition(sesid, _
    tableid, recpos)
```

``` csharp
public static void JetGetRecordPosition(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out JET_RECPOS recpos
)
```

#### <a name="parameters"></a><span data-ttu-id="4bede-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4bede-109">Parameters</span></span>

  - <span data-ttu-id="4bede-110">sesid</span><span class="sxs-lookup"><span data-stu-id="4bede-110">sesid</span></span>  
    <span data-ttu-id="4bede-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4bede-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="4bede-112">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="4bede-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="4bede-113">TABLEID</span><span class="sxs-lookup"><span data-stu-id="4bede-113">tableid</span></span>  
    <span data-ttu-id="4bede-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4bede-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="4bede-115">Cursor situado en el registro.</span><span class="sxs-lookup"><span data-stu-id="4bede-115">The cursor positioned on the record.</span></span>

<!-- end list -->

  - <span data-ttu-id="4bede-116">recpos</span><span class="sxs-lookup"><span data-stu-id="4bede-116">recpos</span></span>  
    <span data-ttu-id="4bede-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_RECPOS](./jet-recpos-class.md)</span><span class="sxs-lookup"><span data-stu-id="4bede-117">Type: [Microsoft.Isam.Esent.Interop.JET_RECPOS](./jet-recpos-class.md)</span></span>  
    
    <span data-ttu-id="4bede-118">Devuelve la posición fraccionaria aproximada del registro.</span><span class="sxs-lookup"><span data-stu-id="4bede-118">Returns the approximate fractional position of the record.</span></span>

## <a name="see-also"></a><span data-ttu-id="4bede-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="4bede-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4bede-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="4bede-120">Reference</span></span>

[<span data-ttu-id="4bede-121">Clase de API</span><span class="sxs-lookup"><span data-stu-id="4bede-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="4bede-122">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="4bede-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="4bede-123">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="4bede-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
