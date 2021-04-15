---
description: 'Más información sobre: método API. RetrieveColumnAsBoolean (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: Método API. RetrieveColumnAsBoolean (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnAsBoolean method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsBoolean(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasboolean(v=EXCHG.10)
ms:contentKeyID: 55100837
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsBoolean
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a2f7f38841248910bd23dd15b6cec06a638640d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539723"
---
# <a name="apiretrievecolumnasboolean-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="b779a-103">Método API. RetrieveColumnAsBoolean (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="b779a-103">Api.RetrieveColumnAsBoolean method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="b779a-104">Recupera un valor de columna booleano del registro actual.</span><span class="sxs-lookup"><span data-stu-id="b779a-104">Retrieves a boolean column value from the current record.</span></span> <span data-ttu-id="b779a-105">El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</span><span class="sxs-lookup"><span data-stu-id="b779a-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="b779a-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b779a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b779a-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b779a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b779a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b779a-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsBoolean ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of Boolean)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of Boolean)

returnValue = Api.RetrieveColumnAsBoolean(sesid, _
    tableid, columnid)
```

``` csharp
public static Nullable<bool> RetrieveColumnAsBoolean(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="b779a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b779a-109">Parameters</span></span>

  - <span data-ttu-id="b779a-110">sesid</span><span class="sxs-lookup"><span data-stu-id="b779a-110">sesid</span></span>  
    <span data-ttu-id="b779a-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b779a-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b779a-112">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="b779a-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="b779a-113">TABLEID</span><span class="sxs-lookup"><span data-stu-id="b779a-113">tableid</span></span>  
    <span data-ttu-id="b779a-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b779a-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="b779a-115">Cursor del que se va a recuperar la columna.</span><span class="sxs-lookup"><span data-stu-id="b779a-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="b779a-116">columnid</span><span class="sxs-lookup"><span data-stu-id="b779a-116">columnid</span></span>  
    <span data-ttu-id="b779a-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b779a-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="b779a-118">Columnid que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="b779a-118">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="b779a-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b779a-119">Return value</span></span>

<span data-ttu-id="b779a-120">Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[Boolean](/dotnet/api/system.boolean)\></span><span class="sxs-lookup"><span data-stu-id="b779a-120">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Boolean](/dotnet/api/system.boolean)\></span></span>  
<span data-ttu-id="b779a-121">Los datos recuperados de la columna como un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="b779a-121">The data retrieved from the column as a boolean.</span></span> <span data-ttu-id="b779a-122">Es NULL si la columna es NULL.</span><span class="sxs-lookup"><span data-stu-id="b779a-122">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b779a-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="b779a-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b779a-124">Referencia</span><span class="sxs-lookup"><span data-stu-id="b779a-124">Reference</span></span>

[<span data-ttu-id="b779a-125">Clase de API</span><span class="sxs-lookup"><span data-stu-id="b779a-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b779a-126">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="b779a-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b779a-127">Sobrecarga RetrieveColumnAsBoolean</span><span class="sxs-lookup"><span data-stu-id="b779a-127">RetrieveColumnAsBoolean overload</span></span>](./api.retrievecolumnasboolean-method.md)

[<span data-ttu-id="b779a-128">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b779a-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
