---
description: 'Más información sobre: método API. RetrieveColumnAsUInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)'
title: Método API. RetrieveColumnAsUInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
TOCTitle: RetrieveColumnAsUInt32 method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsUInt32(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasuint32(v=EXCHG.10)
ms:contentKeyID: 55100866
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsUInt32
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 17babe091d4ae6a2c0219d97b240ee3198260147
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697587"
---
# <a name="apiretrievecolumnasuint32-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a><span data-ttu-id="d87c5-103">Método API. RetrieveColumnAsUInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span><span class="sxs-lookup"><span data-stu-id="d87c5-103">Api.RetrieveColumnAsUInt32 method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="d87c5-104">Recupera un valor de columna UInt32 del registro actual.</span><span class="sxs-lookup"><span data-stu-id="d87c5-104">Retrieves a uint32 column value from the current record.</span></span> <span data-ttu-id="d87c5-105">El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</span><span class="sxs-lookup"><span data-stu-id="d87c5-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="d87c5-106">Esta API no es conforme a CLS.</span><span class="sxs-lookup"><span data-stu-id="d87c5-106">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="d87c5-107">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d87c5-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d87c5-108">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d87c5-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d87c5-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d87c5-109">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function RetrieveColumnAsUInt32 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of UInteger)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of UInteger)

returnValue = Api.RetrieveColumnAsUInt32(sesid, _
    tableid, columnid, grbit)
```

``` csharp
[CLSCompliantAttribute(false)]
public static Nullable<uint> RetrieveColumnAsUInt32(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="d87c5-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d87c5-110">Parameters</span></span>

  - <span data-ttu-id="d87c5-111">sesid</span><span class="sxs-lookup"><span data-stu-id="d87c5-111">sesid</span></span>  
    <span data-ttu-id="d87c5-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d87c5-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="d87c5-113">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="d87c5-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="d87c5-114">TABLEID</span><span class="sxs-lookup"><span data-stu-id="d87c5-114">tableid</span></span>  
    <span data-ttu-id="d87c5-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d87c5-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="d87c5-116">Cursor del que se va a recuperar la columna.</span><span class="sxs-lookup"><span data-stu-id="d87c5-116">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="d87c5-117">columnid</span><span class="sxs-lookup"><span data-stu-id="d87c5-117">columnid</span></span>  
    <span data-ttu-id="d87c5-118">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d87c5-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="d87c5-119">Columnid que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="d87c5-119">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="d87c5-120">grbit</span><span class="sxs-lookup"><span data-stu-id="d87c5-120">grbit</span></span>  
    <span data-ttu-id="d87c5-121">Tipo: [Microsoft. ISAM. esent. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="d87c5-121">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="d87c5-122">Opciones de recuperación.</span><span class="sxs-lookup"><span data-stu-id="d87c5-122">Retrieval options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d87c5-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d87c5-123">Return value</span></span>

<span data-ttu-id="d87c5-124">Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[UInt32](/dotnet/api/system.uint32)\></span><span class="sxs-lookup"><span data-stu-id="d87c5-124">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[UInt32](/dotnet/api/system.uint32)\></span></span>  
<span data-ttu-id="d87c5-125">Los datos recuperados de la columna como un UInt32.</span><span class="sxs-lookup"><span data-stu-id="d87c5-125">The data retrieved from the column as an UInt32.</span></span> <span data-ttu-id="d87c5-126">Es NULL si la columna es NULL.</span><span class="sxs-lookup"><span data-stu-id="d87c5-126">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d87c5-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="d87c5-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d87c5-128">Referencia</span><span class="sxs-lookup"><span data-stu-id="d87c5-128">Reference</span></span>

[<span data-ttu-id="d87c5-129">Clase de API</span><span class="sxs-lookup"><span data-stu-id="d87c5-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d87c5-130">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="d87c5-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d87c5-131">Sobrecarga RetrieveColumnAsUInt32</span><span class="sxs-lookup"><span data-stu-id="d87c5-131">RetrieveColumnAsUInt32 overload</span></span>](./api.retrievecolumnasuint32-method.md)

[<span data-ttu-id="d87c5-132">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d87c5-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
