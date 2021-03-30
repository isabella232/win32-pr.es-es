---
description: 'Más información sobre: método API. RetrieveColumnAsInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: Método API. RetrieveColumnAsInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnAsInt64 method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsInt64(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasint64(v=EXCHG.10)
ms:contentKeyID: 55100858
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsInt64
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4edd9c8a8495a56e14c655357397c5a693239062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907583"
---
# <a name="apiretrievecolumnasint64-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="3d0c6-103">Método API. RetrieveColumnAsInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="3d0c6-103">Api.RetrieveColumnAsInt64 method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="3d0c6-104">Recupera un valor de una sola columna del registro actual.</span><span class="sxs-lookup"><span data-stu-id="3d0c6-104">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="3d0c6-105">El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</span><span class="sxs-lookup"><span data-stu-id="3d0c6-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="3d0c6-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3d0c6-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3d0c6-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3d0c6-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3d0c6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3d0c6-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsInt64 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of Long)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of Long)

returnValue = Api.RetrieveColumnAsInt64(sesid, _
    tableid, columnid)
```

``` csharp
public static Nullable<long> RetrieveColumnAsInt64(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="3d0c6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3d0c6-109">Parameters</span></span>

  - <span data-ttu-id="3d0c6-110">sesid</span><span class="sxs-lookup"><span data-stu-id="3d0c6-110">sesid</span></span>  
    <span data-ttu-id="3d0c6-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3d0c6-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="3d0c6-112">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="3d0c6-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="3d0c6-113">TABLEID</span><span class="sxs-lookup"><span data-stu-id="3d0c6-113">tableid</span></span>  
    <span data-ttu-id="3d0c6-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3d0c6-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="3d0c6-115">Cursor del que se va a recuperar la columna.</span><span class="sxs-lookup"><span data-stu-id="3d0c6-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="3d0c6-116">columnid</span><span class="sxs-lookup"><span data-stu-id="3d0c6-116">columnid</span></span>  
    <span data-ttu-id="3d0c6-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3d0c6-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="3d0c6-118">Columnid que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="3d0c6-118">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="3d0c6-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3d0c6-119">Return value</span></span>

<span data-ttu-id="3d0c6-120">Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[Int64](/dotnet/api/system.int64)\></span><span class="sxs-lookup"><span data-stu-id="3d0c6-120">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Int64](/dotnet/api/system.int64)\></span></span>  
<span data-ttu-id="3d0c6-121">Los datos recuperados de la columna como un valor Long.</span><span class="sxs-lookup"><span data-stu-id="3d0c6-121">The data retrieved from the column as a long.</span></span> <span data-ttu-id="3d0c6-122">Es NULL si la columna es NULL.</span><span class="sxs-lookup"><span data-stu-id="3d0c6-122">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3d0c6-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="3d0c6-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3d0c6-124">Referencia</span><span class="sxs-lookup"><span data-stu-id="3d0c6-124">Reference</span></span>

[<span data-ttu-id="3d0c6-125">Clase de API</span><span class="sxs-lookup"><span data-stu-id="3d0c6-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="3d0c6-126">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="3d0c6-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="3d0c6-127">Sobrecarga RetrieveColumnAsInt64</span><span class="sxs-lookup"><span data-stu-id="3d0c6-127">RetrieveColumnAsInt64 overload</span></span>](./api.retrievecolumnasint64-method.md)

[<span data-ttu-id="3d0c6-128">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="3d0c6-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
