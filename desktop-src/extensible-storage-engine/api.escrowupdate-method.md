---
description: 'Más información sobre: API. EscrowUpdate (método)'
title: Método API. EscrowUpdate
TOCTitle: 'EscrowUpdate method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.EscrowUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.escrowupdate(v=EXCHG.10)
ms:contentKeyID: 55100668
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.EscrowUpdate
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.EscrowUpdate
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dde632f01bd7ac9cbdf8bc4dc09e1337f32014b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808281"
---
# <a name="apiescrowupdate-method"></a><span data-ttu-id="1979d-103">Método API. EscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="1979d-103">Api.EscrowUpdate method</span></span>

<span data-ttu-id="1979d-104">Realizar la adición atómica en una columna.</span><span class="sxs-lookup"><span data-stu-id="1979d-104">Perform atomic addition on one column.</span></span> <span data-ttu-id="1979d-105">La columna debe ser de tipo [Long](./jet-coltyp-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="1979d-105">The column must be of type [Long](./jet-coltyp-enumeration.md).</span></span> <span data-ttu-id="1979d-106">Esta función permite que varias sesiones actualicen el mismo registro simultáneamente sin conflictos.</span><span class="sxs-lookup"><span data-stu-id="1979d-106">This function allows multiple sessions to update the same record concurrently without conflicts.</span></span>

<span data-ttu-id="1979d-107">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1979d-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1979d-108">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1979d-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1979d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1979d-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Function EscrowUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    delta As Integer _
) As Integer
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim delta As Integer
Dim returnValue As Integer

returnValue = Api.EscrowUpdate(sesid, _
    tableid, columnid, delta)
```

``` csharp
public static int EscrowUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    int delta
)
```

#### <a name="parameters"></a><span data-ttu-id="1979d-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1979d-110">Parameters</span></span>

  - <span data-ttu-id="1979d-111">sesid</span><span class="sxs-lookup"><span data-stu-id="1979d-111">sesid</span></span>  
    <span data-ttu-id="1979d-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1979d-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="1979d-113">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="1979d-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="1979d-114">TABLEID</span><span class="sxs-lookup"><span data-stu-id="1979d-114">tableid</span></span>  
    <span data-ttu-id="1979d-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1979d-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="1979d-116">Cursor que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="1979d-116">The cursor to update.</span></span>

<!-- end list -->

  - <span data-ttu-id="1979d-117">columnid</span><span class="sxs-lookup"><span data-stu-id="1979d-117">columnid</span></span>  
    <span data-ttu-id="1979d-118">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1979d-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="1979d-119">Columna que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="1979d-119">The column to update.</span></span> <span data-ttu-id="1979d-120">Debe ser una columna que se pueda actualizar con custodia.</span><span class="sxs-lookup"><span data-stu-id="1979d-120">This must be an escrow-updatable column.</span></span>

<!-- end list -->

  - <span data-ttu-id="1979d-121">delta</span><span class="sxs-lookup"><span data-stu-id="1979d-121">delta</span></span>  
    <span data-ttu-id="1979d-122">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="1979d-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="1979d-123">Delta que se va a aplicar a la columna.</span><span class="sxs-lookup"><span data-stu-id="1979d-123">The delta to apply to the column.</span></span>

#### <a name="return-value"></a><span data-ttu-id="1979d-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1979d-124">Return value</span></span>

<span data-ttu-id="1979d-125">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="1979d-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
<span data-ttu-id="1979d-126">Valor actual de la columna tal y como se almacena en la base de datos (se omite el control de versiones).</span><span class="sxs-lookup"><span data-stu-id="1979d-126">The current value of the column as stored in the database (versioning is ignored).</span></span>  

## <a name="remarks"></a><span data-ttu-id="1979d-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1979d-127">Remarks</span></span>

<span data-ttu-id="1979d-128">Este método encapsula [JetEscrowUpdate (JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, \[ \] , Int32, Int32, EscrowUpdateGrbit)](./api.jetescrowupdate-method.md).</span><span class="sxs-lookup"><span data-stu-id="1979d-128">This method wraps [JetEscrowUpdate(JET_SESID, JET_TABLEID, JET_COLUMNID, \[\], Int32, \[\], Int32, Int32, EscrowUpdateGrbit)](./api.jetescrowupdate-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="1979d-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="1979d-129">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1979d-130">Referencia</span><span class="sxs-lookup"><span data-stu-id="1979d-130">Reference</span></span>

[<span data-ttu-id="1979d-131">Clase de API</span><span class="sxs-lookup"><span data-stu-id="1979d-131">Api class</span></span>](./api-class.md)

[<span data-ttu-id="1979d-132">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="1979d-132">Api members</span></span>](./api-members.md)

[<span data-ttu-id="1979d-133">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="1979d-133">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
