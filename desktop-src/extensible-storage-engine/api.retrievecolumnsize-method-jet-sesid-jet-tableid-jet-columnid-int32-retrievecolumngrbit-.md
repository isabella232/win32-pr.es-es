---
description: 'Más información sobre: método API. RetrieveColumnSize (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, RetrieveColumnGrbit)'
title: Método API. RetrieveColumnSize (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, RetrieveColumnGrbit)
TOCTitle: RetrieveColumnSize method (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnSize(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Int32,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnsize(v=EXCHG.10)
ms:contentKeyID: 55100912
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnSize
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: afd09ecca0362487d6c8e78f8e7c8d943f2f3269
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000877"
---
# <a name="apiretrievecolumnsize-method-jet_sesid-jet_tableid-jet_columnid-int32-retrievecolumngrbit"></a><span data-ttu-id="cc32d-103">Método API. RetrieveColumnSize (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, RetrieveColumnGrbit)</span><span class="sxs-lookup"><span data-stu-id="cc32d-103">Api.RetrieveColumnSize method (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="cc32d-104">Recupera el tamaño de un valor de columna único del registro actual.</span><span class="sxs-lookup"><span data-stu-id="cc32d-104">Retrieves the size of a single column value from the current record.</span></span> <span data-ttu-id="cc32d-105">El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</span><span class="sxs-lookup"><span data-stu-id="cc32d-105">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="cc32d-106">Como alternativa, esta función puede recuperar una columna de un registro que se crea en el búfer de copia del cursor.</span><span class="sxs-lookup"><span data-stu-id="cc32d-106">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="cc32d-107">Esta función también puede recuperar los datos de columna de una entrada de índice que hace referencia al registro actual.</span><span class="sxs-lookup"><span data-stu-id="cc32d-107">This function can also retrieve column data from an index entry that references the current record.</span></span>

<span data-ttu-id="cc32d-108">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cc32d-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cc32d-109">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cc32d-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cc32d-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cc32d-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnSize ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    itagSequence As Integer, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of Integer)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim itagSequence As Integer
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of Integer)

returnValue = Api.RetrieveColumnSize(sesid, _
    tableid, columnid, itagSequence, _
    grbit)
```

``` csharp
public static Nullable<int> RetrieveColumnSize(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    int itagSequence,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="cc32d-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cc32d-111">Parameters</span></span>

  - <span data-ttu-id="cc32d-112">sesid</span><span class="sxs-lookup"><span data-stu-id="cc32d-112">sesid</span></span>  
    <span data-ttu-id="cc32d-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="cc32d-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="cc32d-114">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="cc32d-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="cc32d-115">TABLEID</span><span class="sxs-lookup"><span data-stu-id="cc32d-115">tableid</span></span>  
    <span data-ttu-id="cc32d-116">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="cc32d-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="cc32d-117">Cursor del que se va a recuperar la columna.</span><span class="sxs-lookup"><span data-stu-id="cc32d-117">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="cc32d-118">columnid</span><span class="sxs-lookup"><span data-stu-id="cc32d-118">columnid</span></span>  
    <span data-ttu-id="cc32d-119">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="cc32d-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="cc32d-120">Columnid que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="cc32d-120">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="cc32d-121">itagSequence</span><span class="sxs-lookup"><span data-stu-id="cc32d-121">itagSequence</span></span>  
    <span data-ttu-id="cc32d-122">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="cc32d-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="cc32d-123">Número de secuencia del valor de una columna con varios valores.</span><span class="sxs-lookup"><span data-stu-id="cc32d-123">The sequence number of value in a multi-valued column.</span></span> <span data-ttu-id="cc32d-124">La matriz de valores se basa en uno.</span><span class="sxs-lookup"><span data-stu-id="cc32d-124">The array of values is one-based.</span></span> <span data-ttu-id="cc32d-125">El primer valor es Sequence 1, no 0.</span><span class="sxs-lookup"><span data-stu-id="cc32d-125">The first value is sequence 1, not 0.</span></span> <span data-ttu-id="cc32d-126">Si la columna de registro solo tiene un valor, se debe pasar 1 como itagSequence.</span><span class="sxs-lookup"><span data-stu-id="cc32d-126">If the record column has only one value then 1 should be passed as the itagSequence.</span></span>

<!-- end list -->

  - <span data-ttu-id="cc32d-127">grbit</span><span class="sxs-lookup"><span data-stu-id="cc32d-127">grbit</span></span>  
    <span data-ttu-id="cc32d-128">Tipo: [Microsoft. ISAM. esent. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="cc32d-128">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="cc32d-129">Recupera opciones de columna.</span><span class="sxs-lookup"><span data-stu-id="cc32d-129">Retrieve column options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="cc32d-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cc32d-130">Return value</span></span>

<span data-ttu-id="cc32d-131">Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span><span class="sxs-lookup"><span data-stu-id="cc32d-131">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span></span>  
<span data-ttu-id="cc32d-132">Tamaño de la columna.</span><span class="sxs-lookup"><span data-stu-id="cc32d-132">The size of the column.</span></span> <span data-ttu-id="cc32d-133">0 si la columna es NULL.</span><span class="sxs-lookup"><span data-stu-id="cc32d-133">0 if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="cc32d-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc32d-134">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cc32d-135">Referencia</span><span class="sxs-lookup"><span data-stu-id="cc32d-135">Reference</span></span>

[<span data-ttu-id="cc32d-136">Clase de API</span><span class="sxs-lookup"><span data-stu-id="cc32d-136">Api class</span></span>](./api-class.md)

[<span data-ttu-id="cc32d-137">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="cc32d-137">Api members</span></span>](./api-members.md)

[<span data-ttu-id="cc32d-138">Sobrecarga RetrieveColumnSize</span><span class="sxs-lookup"><span data-stu-id="cc32d-138">RetrieveColumnSize overload</span></span>](./api.retrievecolumnsize-method.md)

[<span data-ttu-id="cc32d-139">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="cc32d-139">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
