---
description: 'Más información sobre: API. JetEscrowUpdate (método)'
title: Método API. JetEscrowUpdate
TOCTitle: 'JetEscrowUpdate method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEscrowUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetescrowupdate(v=EXCHG.10)
ms:contentKeyID: 55100740
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEscrowUpdate
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEscrowUpdate
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 09e74f964fd6018248a3cfc594621bed96f92e60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720347"
---
# <a name="apijetescrowupdate-method"></a><span data-ttu-id="50d32-103">Método API. JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="50d32-103">Api.JetEscrowUpdate method</span></span>

<span data-ttu-id="50d32-104">Realiza una operación de suma atómica en una columna.</span><span class="sxs-lookup"><span data-stu-id="50d32-104">Performs an atomic addition operation on one column.</span></span> <span data-ttu-id="50d32-105">Esta función permite que varias sesiones actualicen el mismo registro simultáneamente sin conflictos.</span><span class="sxs-lookup"><span data-stu-id="50d32-105">This function allows multiple sessions to update the same record concurrently without conflicts.</span></span> <span data-ttu-id="50d32-106">Vea también [EscrowUpdate (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32)](./api.escrowupdate-method.md).</span><span class="sxs-lookup"><span data-stu-id="50d32-106">Also see [EscrowUpdate(JET_SESID, JET_TABLEID, JET_COLUMNID, Int32)](./api.escrowupdate-method.md).</span></span>

<span data-ttu-id="50d32-107">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="50d32-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="50d32-108">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="50d32-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="50d32-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="50d32-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetEscrowUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    delta As Byte(), _
    deltaSize As Integer, _
    previousValue As Byte(), _
    previousValueLength As Integer, _
    <OutAttribute> ByRef actualPreviousValueLength As Integer, _
    grbit As EscrowUpdateGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim delta As Byte()
Dim deltaSize As Integer
Dim previousValue As Byte()
Dim previousValueLength As Integer
Dim actualPreviousValueLength As Integer
Dim grbit As EscrowUpdateGrbitApi.JetEscrowUpdate(sesid, tableid, _
    columnid, delta, deltaSize, previousValue, _
    previousValueLength, actualPreviousValueLength, _
    grbit)
```

``` csharp
public static void JetEscrowUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] delta,
    int deltaSize,
    byte[] previousValue,
    int previousValueLength,
    out int actualPreviousValueLength,
    EscrowUpdateGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="50d32-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="50d32-110">Parameters</span></span>

  - <span data-ttu-id="50d32-111">sesid</span><span class="sxs-lookup"><span data-stu-id="50d32-111">sesid</span></span>  
    <span data-ttu-id="50d32-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="50d32-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="50d32-113">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="50d32-113">The session to use.</span></span> <span data-ttu-id="50d32-114">La sesión debe estar en una transacción.</span><span class="sxs-lookup"><span data-stu-id="50d32-114">The session must be in a transaction.</span></span>

<!-- end list -->

  - <span data-ttu-id="50d32-115">TABLEID</span><span class="sxs-lookup"><span data-stu-id="50d32-115">tableid</span></span>  
    <span data-ttu-id="50d32-116">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="50d32-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="50d32-117">Cursor que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="50d32-117">The cursor to update.</span></span>

<!-- end list -->

  - <span data-ttu-id="50d32-118">columnid</span><span class="sxs-lookup"><span data-stu-id="50d32-118">columnid</span></span>  
    <span data-ttu-id="50d32-119">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="50d32-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="50d32-120">Columna que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="50d32-120">The column to update.</span></span> <span data-ttu-id="50d32-121">Debe ser una columna actualizable de custodia.</span><span class="sxs-lookup"><span data-stu-id="50d32-121">This must be an escrow updatable column.</span></span>

<!-- end list -->

  - <span data-ttu-id="50d32-122">delta</span><span class="sxs-lookup"><span data-stu-id="50d32-122">delta</span></span>  
    <span data-ttu-id="50d32-123">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="50d32-123">Type: \[\]</span></span>  
    
    <span data-ttu-id="50d32-124">Búfer que contiene el addend.</span><span class="sxs-lookup"><span data-stu-id="50d32-124">The buffer containing the addend.</span></span>

<!-- end list -->

  - <span data-ttu-id="50d32-125">deltaS</span><span class="sxs-lookup"><span data-stu-id="50d32-125">deltaSize</span></span>  
    <span data-ttu-id="50d32-126">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="50d32-126">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="50d32-127">Tamaño de addend.</span><span class="sxs-lookup"><span data-stu-id="50d32-127">The size of the addend.</span></span>

<!-- end list -->

  - <span data-ttu-id="50d32-128">previousValue</span><span class="sxs-lookup"><span data-stu-id="50d32-128">previousValue</span></span>  
    <span data-ttu-id="50d32-129">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="50d32-129">Type: \[\]</span></span>  
    
    <span data-ttu-id="50d32-130">Búfer de salida que recibirá el valor actual de la columna.</span><span class="sxs-lookup"><span data-stu-id="50d32-130">An output buffer that will recieve the current value of the column.</span></span> <span data-ttu-id="50d32-131">Este búfer puede ser null.</span><span class="sxs-lookup"><span data-stu-id="50d32-131">This buffer can be null.</span></span>

<!-- end list -->

  - <span data-ttu-id="50d32-132">previousValueLength</span><span class="sxs-lookup"><span data-stu-id="50d32-132">previousValueLength</span></span>  
    <span data-ttu-id="50d32-133">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="50d32-133">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="50d32-134">Tamaño del búfer de previousValue.</span><span class="sxs-lookup"><span data-stu-id="50d32-134">The size of the previousValue buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="50d32-135">actualPreviousValueLength</span><span class="sxs-lookup"><span data-stu-id="50d32-135">actualPreviousValueLength</span></span>  
    <span data-ttu-id="50d32-136">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="50d32-136">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="50d32-137">Devuelve el tamaño real de previousValue.</span><span class="sxs-lookup"><span data-stu-id="50d32-137">Returns the actual size of the previousValue.</span></span>

<!-- end list -->

  - <span data-ttu-id="50d32-138">grbit</span><span class="sxs-lookup"><span data-stu-id="50d32-138">grbit</span></span>  
    <span data-ttu-id="50d32-139">Tipo: [Microsoft. ISAM. esent. Interop. EscrowUpdateGrbit](./escrowupdategrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="50d32-139">Type: [Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit](./escrowupdategrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="50d32-140">Opciones de actualización de custodia.</span><span class="sxs-lookup"><span data-stu-id="50d32-140">Escrow update options.</span></span>

## <a name="see-also"></a><span data-ttu-id="50d32-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="50d32-141">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="50d32-142">Referencia</span><span class="sxs-lookup"><span data-stu-id="50d32-142">Reference</span></span>

[<span data-ttu-id="50d32-143">Clase de API</span><span class="sxs-lookup"><span data-stu-id="50d32-143">Api class</span></span>](./api-class.md)

[<span data-ttu-id="50d32-144">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="50d32-144">Api members</span></span>](./api-members.md)

[<span data-ttu-id="50d32-145">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="50d32-145">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
