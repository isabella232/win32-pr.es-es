---
description: 'Más información sobre: método API. RetrieveColumnAsByte (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)'
title: Método API. RetrieveColumnAsByte (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
TOCTitle: RetrieveColumnAsByte method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsByte(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasbyte(v=EXCHG.10)
ms:contentKeyID: 55100865
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsByte
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 68ea6a2b461799006edd0d82f69a20bc52d2c721
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539718"
---
# <a name="apiretrievecolumnasbyte-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a><span data-ttu-id="d40f4-103">Método API. RetrieveColumnAsByte (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span><span class="sxs-lookup"><span data-stu-id="d40f4-103">Api.RetrieveColumnAsByte method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="d40f4-104">Recupera un valor de columna de bytes del registro actual.</span><span class="sxs-lookup"><span data-stu-id="d40f4-104">Retrieves a byte column value from the current record.</span></span> <span data-ttu-id="d40f4-105">El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</span><span class="sxs-lookup"><span data-stu-id="d40f4-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="d40f4-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d40f4-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d40f4-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d40f4-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d40f4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d40f4-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsByte ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of Byte)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of Byte)

returnValue = Api.RetrieveColumnAsByte(sesid, _
    tableid, columnid, grbit)
```

``` csharp
public static Nullable<byte> RetrieveColumnAsByte(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="d40f4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d40f4-109">Parameters</span></span>

  - <span data-ttu-id="d40f4-110">sesid</span><span class="sxs-lookup"><span data-stu-id="d40f4-110">sesid</span></span>  
    <span data-ttu-id="d40f4-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d40f4-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="d40f4-112">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="d40f4-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="d40f4-113">TABLEID</span><span class="sxs-lookup"><span data-stu-id="d40f4-113">tableid</span></span>  
    <span data-ttu-id="d40f4-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d40f4-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="d40f4-115">Cursor del que se va a recuperar la columna.</span><span class="sxs-lookup"><span data-stu-id="d40f4-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="d40f4-116">columnid</span><span class="sxs-lookup"><span data-stu-id="d40f4-116">columnid</span></span>  
    <span data-ttu-id="d40f4-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d40f4-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="d40f4-118">Columnid que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="d40f4-118">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="d40f4-119">grbit</span><span class="sxs-lookup"><span data-stu-id="d40f4-119">grbit</span></span>  
    <span data-ttu-id="d40f4-120">Tipo: [Microsoft. ISAM. esent. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="d40f4-120">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="d40f4-121">Opciones de recuperación.</span><span class="sxs-lookup"><span data-stu-id="d40f4-121">Retrieval options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d40f4-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d40f4-122">Return value</span></span>

<span data-ttu-id="d40f4-123">Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[Byte](/dotnet/api/system.byte)\></span><span class="sxs-lookup"><span data-stu-id="d40f4-123">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Byte](/dotnet/api/system.byte)\></span></span>  
<span data-ttu-id="d40f4-124">Los datos recuperados de la columna como un byte.</span><span class="sxs-lookup"><span data-stu-id="d40f4-124">The data retrieved from the column as a byte.</span></span> <span data-ttu-id="d40f4-125">Es NULL si la columna es NULL.</span><span class="sxs-lookup"><span data-stu-id="d40f4-125">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d40f4-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="d40f4-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d40f4-127">Referencia</span><span class="sxs-lookup"><span data-stu-id="d40f4-127">Reference</span></span>

[<span data-ttu-id="d40f4-128">Clase de API</span><span class="sxs-lookup"><span data-stu-id="d40f4-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d40f4-129">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="d40f4-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d40f4-130">Sobrecarga RetrieveColumnAsByte</span><span class="sxs-lookup"><span data-stu-id="d40f4-130">RetrieveColumnAsByte overload</span></span>](./api.retrievecolumnasbyte-method.md)

[<span data-ttu-id="d40f4-131">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d40f4-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
