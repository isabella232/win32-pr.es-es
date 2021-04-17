---
description: 'Más información sobre: método API. RetrieveColumnAsDateTime (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)'
title: Método API. RetrieveColumnAsDateTime (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
TOCTitle: RetrieveColumnAsDateTime method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsDateTime(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasdatetime(v=EXCHG.10)
ms:contentKeyID: 55100843
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsDateTime
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: befd4e7256c9d1ca52d6f0239f5e56c21842a85d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717106"
---
# <a name="apiretrievecolumnasdatetime-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a><span data-ttu-id="b6669-103">Método API. RetrieveColumnAsDateTime (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span><span class="sxs-lookup"><span data-stu-id="b6669-103">Api.RetrieveColumnAsDateTime method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="b6669-104">Recupera un valor de columna DateTime del registro actual.</span><span class="sxs-lookup"><span data-stu-id="b6669-104">Retrieves a datetime column value from the current record.</span></span> <span data-ttu-id="b6669-105">El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</span><span class="sxs-lookup"><span data-stu-id="b6669-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="b6669-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b6669-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b6669-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b6669-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b6669-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b6669-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsDateTime ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of DateTime)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of DateTime)

returnValue = Api.RetrieveColumnAsDateTime(sesid, _
    tableid, columnid, grbit)
```

``` csharp
public static Nullable<DateTime> RetrieveColumnAsDateTime(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="b6669-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b6669-109">Parameters</span></span>

  - <span data-ttu-id="b6669-110">sesid</span><span class="sxs-lookup"><span data-stu-id="b6669-110">sesid</span></span>  
    <span data-ttu-id="b6669-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b6669-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b6669-112">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="b6669-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="b6669-113">TABLEID</span><span class="sxs-lookup"><span data-stu-id="b6669-113">tableid</span></span>  
    <span data-ttu-id="b6669-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b6669-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="b6669-115">Cursor del que se va a recuperar la columna.</span><span class="sxs-lookup"><span data-stu-id="b6669-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="b6669-116">columnid</span><span class="sxs-lookup"><span data-stu-id="b6669-116">columnid</span></span>  
    <span data-ttu-id="b6669-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b6669-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="b6669-118">Columnid que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="b6669-118">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="b6669-119">grbit</span><span class="sxs-lookup"><span data-stu-id="b6669-119">grbit</span></span>  
    <span data-ttu-id="b6669-120">Tipo: [Microsoft. ISAM. esent. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="b6669-120">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="b6669-121">Opciones de recuperación.</span><span class="sxs-lookup"><span data-stu-id="b6669-121">Retrieval options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="b6669-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b6669-122">Return value</span></span>

<span data-ttu-id="b6669-123">Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[DateTime](/dotnet/api/system.datetime)\></span><span class="sxs-lookup"><span data-stu-id="b6669-123">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[DateTime](/dotnet/api/system.datetime)\></span></span>  
<span data-ttu-id="b6669-124">Los datos recuperados de la columna como un valor de fecha y hora.</span><span class="sxs-lookup"><span data-stu-id="b6669-124">The data retrieved from the column as a datetime.</span></span> <span data-ttu-id="b6669-125">Es NULL si la columna es NULL.</span><span class="sxs-lookup"><span data-stu-id="b6669-125">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b6669-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6669-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b6669-127">Referencia</span><span class="sxs-lookup"><span data-stu-id="b6669-127">Reference</span></span>

[<span data-ttu-id="b6669-128">Clase de API</span><span class="sxs-lookup"><span data-stu-id="b6669-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b6669-129">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="b6669-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b6669-130">Sobrecarga RetrieveColumnAsDateTime</span><span class="sxs-lookup"><span data-stu-id="b6669-130">RetrieveColumnAsDateTime overload</span></span>](./api.retrievecolumnasdatetime-method.md)

[<span data-ttu-id="b6669-131">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b6669-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
