---
description: 'Más información sobre: método API. RetrieveColumnAsUInt16 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)'
title: Método API. RetrieveColumnAsUInt16 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
TOCTitle: RetrieveColumnAsUInt16 method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsUInt16(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasuint16(v=EXCHG.10)
ms:contentKeyID: 55100902
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsUInt16
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ca82b1c2f5a9a1be7fa0ddbd5082e55820263a10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539694"
---
# <a name="apiretrievecolumnasuint16-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a><span data-ttu-id="c9c1b-103">Método API. RetrieveColumnAsUInt16 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span><span class="sxs-lookup"><span data-stu-id="c9c1b-103">Api.RetrieveColumnAsUInt16 method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="c9c1b-104">Recupera un valor de columna UInt16 del registro actual.</span><span class="sxs-lookup"><span data-stu-id="c9c1b-104">Retrieves a uint16 column value from the current record.</span></span> <span data-ttu-id="c9c1b-105">El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</span><span class="sxs-lookup"><span data-stu-id="c9c1b-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="c9c1b-106">Esta API no es conforme a CLS.</span><span class="sxs-lookup"><span data-stu-id="c9c1b-106">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="c9c1b-107">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c9c1b-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c9c1b-108">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c9c1b-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c9c1b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9c1b-109">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function RetrieveColumnAsUInt16 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of UShort)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of UShort)

returnValue = Api.RetrieveColumnAsUInt16(sesid, _
    tableid, columnid, grbit)
```

``` csharp
[CLSCompliantAttribute(false)]
public static Nullable<ushort> RetrieveColumnAsUInt16(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="c9c1b-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9c1b-110">Parameters</span></span>

  - <span data-ttu-id="c9c1b-111">sesid</span><span class="sxs-lookup"><span data-stu-id="c9c1b-111">sesid</span></span>  
    <span data-ttu-id="c9c1b-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c9c1b-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c9c1b-113">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="c9c1b-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c9c1b-114">TABLEID</span><span class="sxs-lookup"><span data-stu-id="c9c1b-114">tableid</span></span>  
    <span data-ttu-id="c9c1b-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c9c1b-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="c9c1b-116">Cursor del que se va a recuperar la columna.</span><span class="sxs-lookup"><span data-stu-id="c9c1b-116">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="c9c1b-117">columnid</span><span class="sxs-lookup"><span data-stu-id="c9c1b-117">columnid</span></span>  
    <span data-ttu-id="c9c1b-118">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c9c1b-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="c9c1b-119">Columnid que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="c9c1b-119">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="c9c1b-120">grbit</span><span class="sxs-lookup"><span data-stu-id="c9c1b-120">grbit</span></span>  
    <span data-ttu-id="c9c1b-121">Tipo: [Microsoft. ISAM. esent. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="c9c1b-121">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="c9c1b-122">Opciones de recuperación.</span><span class="sxs-lookup"><span data-stu-id="c9c1b-122">Retrieval options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="c9c1b-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9c1b-123">Return value</span></span>

<span data-ttu-id="c9c1b-124">Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[UInt16](/dotnet/api/system.uint16)\></span><span class="sxs-lookup"><span data-stu-id="c9c1b-124">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[UInt16](/dotnet/api/system.uint16)\></span></span>  
<span data-ttu-id="c9c1b-125">Los datos recuperados de la columna como UInt16.</span><span class="sxs-lookup"><span data-stu-id="c9c1b-125">The data retrieved from the column as an UInt16.</span></span> <span data-ttu-id="c9c1b-126">Es NULL si la columna es NULL.</span><span class="sxs-lookup"><span data-stu-id="c9c1b-126">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c9c1b-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9c1b-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c9c1b-128">Referencia</span><span class="sxs-lookup"><span data-stu-id="c9c1b-128">Reference</span></span>

[<span data-ttu-id="c9c1b-129">Clase de API</span><span class="sxs-lookup"><span data-stu-id="c9c1b-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="c9c1b-130">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="c9c1b-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="c9c1b-131">Sobrecarga RetrieveColumnAsUInt16</span><span class="sxs-lookup"><span data-stu-id="c9c1b-131">RetrieveColumnAsUInt16 overload</span></span>](./api.retrievecolumnasuint16-method.md)

[<span data-ttu-id="c9c1b-132">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c9c1b-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
