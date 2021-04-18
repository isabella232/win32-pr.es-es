---
description: 'Más información sobre: método API. RetrieveColumnSize (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: Método API. RetrieveColumnSize (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnSize method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnSize(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnsize(v=EXCHG.10)
ms:contentKeyID: 55100868
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
ms.openlocfilehash: 6f75ce51e942cfde7fddc4f9ec0154feae985e02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697718"
---
# <a name="apiretrievecolumnsize-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="9e894-103">Método API. RetrieveColumnSize (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="9e894-103">Api.RetrieveColumnSize method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="9e894-104">Recupera el tamaño de un valor de columna único del registro actual.</span><span class="sxs-lookup"><span data-stu-id="9e894-104">Retrieves the size of a single column value from the current record.</span></span> <span data-ttu-id="9e894-105">El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</span><span class="sxs-lookup"><span data-stu-id="9e894-105">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="9e894-106">Como alternativa, esta función puede recuperar una columna de un registro que se crea en el búfer de copia del cursor.</span><span class="sxs-lookup"><span data-stu-id="9e894-106">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="9e894-107">Esta función también puede recuperar los datos de columna de una entrada de índice que hace referencia al registro actual.</span><span class="sxs-lookup"><span data-stu-id="9e894-107">This function can also retrieve column data from an index entry that references the current record.</span></span>

<span data-ttu-id="9e894-108">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9e894-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9e894-109">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9e894-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9e894-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9e894-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnSize ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of Integer)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of Integer)

returnValue = Api.RetrieveColumnSize(sesid, _
    tableid, columnid)
```

``` csharp
public static Nullable<int> RetrieveColumnSize(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="9e894-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9e894-111">Parameters</span></span>

  - <span data-ttu-id="9e894-112">sesid</span><span class="sxs-lookup"><span data-stu-id="9e894-112">sesid</span></span>  
    <span data-ttu-id="9e894-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9e894-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="9e894-114">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="9e894-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="9e894-115">TABLEID</span><span class="sxs-lookup"><span data-stu-id="9e894-115">tableid</span></span>  
    <span data-ttu-id="9e894-116">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9e894-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="9e894-117">Cursor del que se va a recuperar la columna.</span><span class="sxs-lookup"><span data-stu-id="9e894-117">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="9e894-118">columnid</span><span class="sxs-lookup"><span data-stu-id="9e894-118">columnid</span></span>  
    <span data-ttu-id="9e894-119">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9e894-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="9e894-120">Columnid que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="9e894-120">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="9e894-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9e894-121">Return value</span></span>

<span data-ttu-id="9e894-122">Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span><span class="sxs-lookup"><span data-stu-id="9e894-122">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span></span>  
<span data-ttu-id="9e894-123">Tamaño de la columna.</span><span class="sxs-lookup"><span data-stu-id="9e894-123">The size of the column.</span></span> <span data-ttu-id="9e894-124">0 si la columna es NULL.</span><span class="sxs-lookup"><span data-stu-id="9e894-124">0 if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9e894-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e894-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9e894-126">Referencia</span><span class="sxs-lookup"><span data-stu-id="9e894-126">Reference</span></span>

[<span data-ttu-id="9e894-127">Clase de API</span><span class="sxs-lookup"><span data-stu-id="9e894-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="9e894-128">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="9e894-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="9e894-129">Sobrecarga RetrieveColumnSize</span><span class="sxs-lookup"><span data-stu-id="9e894-129">RetrieveColumnSize overload</span></span>](./api.retrievecolumnsize-method.md)

[<span data-ttu-id="9e894-130">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="9e894-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
