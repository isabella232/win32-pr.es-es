---
description: 'Más información sobre: método API. RetrieveColumnAsDouble (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)'
title: Método API. RetrieveColumnAsDouble (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
TOCTitle: RetrieveColumnAsDouble method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsDouble(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasdouble(v=EXCHG.10)
ms:contentKeyID: 55100884
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsDouble
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a607cb2bbb2d95451b4f9432b488d8016f94caba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907585"
---
# <a name="apiretrievecolumnasdouble-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a><span data-ttu-id="527e7-103">Método API. RetrieveColumnAsDouble (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span><span class="sxs-lookup"><span data-stu-id="527e7-103">Api.RetrieveColumnAsDouble method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="527e7-104">Recupera un valor de columna doble del registro actual.</span><span class="sxs-lookup"><span data-stu-id="527e7-104">Retrieves a double column value from the current record.</span></span> <span data-ttu-id="527e7-105">El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</span><span class="sxs-lookup"><span data-stu-id="527e7-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="527e7-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="527e7-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="527e7-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="527e7-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="527e7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="527e7-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsDouble ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of Double)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of Double)

returnValue = Api.RetrieveColumnAsDouble(sesid, _
    tableid, columnid, grbit)
```

``` csharp
public static Nullable<double> RetrieveColumnAsDouble(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="527e7-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="527e7-109">Parameters</span></span>

  - <span data-ttu-id="527e7-110">sesid</span><span class="sxs-lookup"><span data-stu-id="527e7-110">sesid</span></span>  
    <span data-ttu-id="527e7-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="527e7-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="527e7-112">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="527e7-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="527e7-113">TABLEID</span><span class="sxs-lookup"><span data-stu-id="527e7-113">tableid</span></span>  
    <span data-ttu-id="527e7-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="527e7-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="527e7-115">Cursor del que se va a recuperar la columna.</span><span class="sxs-lookup"><span data-stu-id="527e7-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="527e7-116">columnid</span><span class="sxs-lookup"><span data-stu-id="527e7-116">columnid</span></span>  
    <span data-ttu-id="527e7-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="527e7-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="527e7-118">Columnid que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="527e7-118">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="527e7-119">grbit</span><span class="sxs-lookup"><span data-stu-id="527e7-119">grbit</span></span>  
    <span data-ttu-id="527e7-120">Tipo: [Microsoft. ISAM. esent. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="527e7-120">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="527e7-121">Opciones de recuperación.</span><span class="sxs-lookup"><span data-stu-id="527e7-121">Retrieval options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="527e7-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="527e7-122">Return value</span></span>

<span data-ttu-id="527e7-123">Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[Double](/dotnet/api/system.double)\></span><span class="sxs-lookup"><span data-stu-id="527e7-123">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Double](/dotnet/api/system.double)\></span></span>  
<span data-ttu-id="527e7-124">Los datos recuperados de la columna como un valor de tipo Double.</span><span class="sxs-lookup"><span data-stu-id="527e7-124">The data retrieved from the column as a double.</span></span> <span data-ttu-id="527e7-125">Es NULL si la columna es NULL.</span><span class="sxs-lookup"><span data-stu-id="527e7-125">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="527e7-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="527e7-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="527e7-127">Referencia</span><span class="sxs-lookup"><span data-stu-id="527e7-127">Reference</span></span>

[<span data-ttu-id="527e7-128">Clase de API</span><span class="sxs-lookup"><span data-stu-id="527e7-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="527e7-129">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="527e7-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="527e7-130">Sobrecarga RetrieveColumnAsDouble</span><span class="sxs-lookup"><span data-stu-id="527e7-130">RetrieveColumnAsDouble overload</span></span>](./api.retrievecolumnasdouble-method.md)

[<span data-ttu-id="527e7-131">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="527e7-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
