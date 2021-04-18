---
description: 'Más información sobre: método API. RetrieveColumnAsUInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: Método API. RetrieveColumnAsUInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnAsUInt32 method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsUInt32(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasuint32(v=EXCHG.10)
ms:contentKeyID: 55100903
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsUInt32
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b889245cd2e2f37907a15e3ec31b04a4d932dd02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539693"
---
# <a name="apiretrievecolumnasuint32-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="f8ba9-103">Método API. RetrieveColumnAsUInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="f8ba9-103">Api.RetrieveColumnAsUInt32 method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="f8ba9-104">Recupera un valor de columna UInt32 del registro actual.</span><span class="sxs-lookup"><span data-stu-id="f8ba9-104">Retrieves a uint32 column value from the current record.</span></span> <span data-ttu-id="f8ba9-105">El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</span><span class="sxs-lookup"><span data-stu-id="f8ba9-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="f8ba9-106">Esta API no es conforme a CLS.</span><span class="sxs-lookup"><span data-stu-id="f8ba9-106">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="f8ba9-107">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f8ba9-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f8ba9-108">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f8ba9-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f8ba9-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f8ba9-109">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function RetrieveColumnAsUInt32 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of UInteger)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of UInteger)

returnValue = Api.RetrieveColumnAsUInt32(sesid, _
    tableid, columnid)
```

``` csharp
[CLSCompliantAttribute(false)]
public static Nullable<uint> RetrieveColumnAsUInt32(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="f8ba9-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8ba9-110">Parameters</span></span>

  - <span data-ttu-id="f8ba9-111">sesid</span><span class="sxs-lookup"><span data-stu-id="f8ba9-111">sesid</span></span>  
    <span data-ttu-id="f8ba9-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f8ba9-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="f8ba9-113">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="f8ba9-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="f8ba9-114">TABLEID</span><span class="sxs-lookup"><span data-stu-id="f8ba9-114">tableid</span></span>  
    <span data-ttu-id="f8ba9-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f8ba9-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="f8ba9-116">Cursor del que se va a recuperar la columna.</span><span class="sxs-lookup"><span data-stu-id="f8ba9-116">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="f8ba9-117">columnid</span><span class="sxs-lookup"><span data-stu-id="f8ba9-117">columnid</span></span>  
    <span data-ttu-id="f8ba9-118">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f8ba9-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="f8ba9-119">Columnid que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="f8ba9-119">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f8ba9-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8ba9-120">Return value</span></span>

<span data-ttu-id="f8ba9-121">Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[UInt32](/dotnet/api/system.uint32)\></span><span class="sxs-lookup"><span data-stu-id="f8ba9-121">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[UInt32](/dotnet/api/system.uint32)\></span></span>  
<span data-ttu-id="f8ba9-122">Los datos recuperados de la columna como un UInt32.</span><span class="sxs-lookup"><span data-stu-id="f8ba9-122">The data retrieved from the column as an UInt32.</span></span> <span data-ttu-id="f8ba9-123">Es NULL si la columna es NULL.</span><span class="sxs-lookup"><span data-stu-id="f8ba9-123">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f8ba9-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8ba9-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f8ba9-125">Referencia</span><span class="sxs-lookup"><span data-stu-id="f8ba9-125">Reference</span></span>

[<span data-ttu-id="f8ba9-126">Clase de API</span><span class="sxs-lookup"><span data-stu-id="f8ba9-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f8ba9-127">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="f8ba9-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f8ba9-128">Sobrecarga RetrieveColumnAsUInt32</span><span class="sxs-lookup"><span data-stu-id="f8ba9-128">RetrieveColumnAsUInt32 overload</span></span>](./api.retrievecolumnasuint32-method.md)

[<span data-ttu-id="f8ba9-129">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f8ba9-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
