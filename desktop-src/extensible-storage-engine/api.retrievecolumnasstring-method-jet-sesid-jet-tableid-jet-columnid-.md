---
description: 'Más información sobre: método API. RetrieveColumnAsString (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: Método API. RetrieveColumnAsString (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnAsString method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsString(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasstring(v=EXCHG.10)
ms:contentKeyID: 55100860
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsString
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 64500e9827d55fab4771963b95dbfd0efffdc5c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697635"
---
# <a name="apiretrievecolumnasstring-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="c99bd-103">Método API. RetrieveColumnAsString (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="c99bd-103">Api.RetrieveColumnAsString method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="c99bd-104">Recupera un valor de una sola columna del registro actual.</span><span class="sxs-lookup"><span data-stu-id="c99bd-104">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="c99bd-105">El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</span><span class="sxs-lookup"><span data-stu-id="c99bd-105">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="c99bd-106">Se usa la codificación Unicode.</span><span class="sxs-lookup"><span data-stu-id="c99bd-106">The Unicode encoding is used.</span></span>

<span data-ttu-id="c99bd-107">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c99bd-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c99bd-108">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c99bd-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c99bd-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c99bd-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsString ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As String
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As String

returnValue = Api.RetrieveColumnAsString(sesid, _
    tableid, columnid)
```

``` csharp
public static string RetrieveColumnAsString(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="c99bd-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c99bd-110">Parameters</span></span>

  - <span data-ttu-id="c99bd-111">sesid</span><span class="sxs-lookup"><span data-stu-id="c99bd-111">sesid</span></span>  
    <span data-ttu-id="c99bd-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c99bd-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c99bd-113">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="c99bd-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c99bd-114">TABLEID</span><span class="sxs-lookup"><span data-stu-id="c99bd-114">tableid</span></span>  
    <span data-ttu-id="c99bd-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c99bd-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="c99bd-116">Cursor del que se va a recuperar la columna.</span><span class="sxs-lookup"><span data-stu-id="c99bd-116">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="c99bd-117">columnid</span><span class="sxs-lookup"><span data-stu-id="c99bd-117">columnid</span></span>  
    <span data-ttu-id="c99bd-118">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c99bd-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="c99bd-119">Columnid que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="c99bd-119">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="c99bd-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c99bd-120">Return value</span></span>

<span data-ttu-id="c99bd-121">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="c99bd-121">Type: [System.String](/dotnet/api/system.string)</span></span>  
<span data-ttu-id="c99bd-122">Los datos recuperados de la columna como una cadena.</span><span class="sxs-lookup"><span data-stu-id="c99bd-122">The data retrieved from the column as a string.</span></span> <span data-ttu-id="c99bd-123">Es NULL si la columna es NULL.</span><span class="sxs-lookup"><span data-stu-id="c99bd-123">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c99bd-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="c99bd-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c99bd-125">Referencia</span><span class="sxs-lookup"><span data-stu-id="c99bd-125">Reference</span></span>

[<span data-ttu-id="c99bd-126">Clase de API</span><span class="sxs-lookup"><span data-stu-id="c99bd-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="c99bd-127">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="c99bd-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="c99bd-128">Sobrecarga RetrieveColumnAsString</span><span class="sxs-lookup"><span data-stu-id="c99bd-128">RetrieveColumnAsString overload</span></span>](./api.retrievecolumnasstring-method.md)

[<span data-ttu-id="c99bd-129">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c99bd-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
