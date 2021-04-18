---
description: 'Más información sobre: método API. RetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: Método API. RetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100833
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2c29a591064c573e168903aaf83dcdd15f5b9a5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707400"
---
# <a name="apiretrievecolumn-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="36682-103">Método API. RetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="36682-103">Api.RetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="36682-104">Recupera un valor de una sola columna del registro actual.</span><span class="sxs-lookup"><span data-stu-id="36682-104">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="36682-105">El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</span><span class="sxs-lookup"><span data-stu-id="36682-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="36682-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="36682-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="36682-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="36682-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="36682-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="36682-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Byte()
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Byte()

returnValue = Api.RetrieveColumn(sesid, _
    tableid, columnid)
```

``` csharp
public static byte[] RetrieveColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="36682-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="36682-109">Parameters</span></span>

  - <span data-ttu-id="36682-110">sesid</span><span class="sxs-lookup"><span data-stu-id="36682-110">sesid</span></span>  
    <span data-ttu-id="36682-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="36682-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="36682-112">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="36682-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="36682-113">TABLEID</span><span class="sxs-lookup"><span data-stu-id="36682-113">tableid</span></span>  
    <span data-ttu-id="36682-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="36682-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="36682-115">Cursor del que se va a recuperar la columna.</span><span class="sxs-lookup"><span data-stu-id="36682-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="36682-116">columnid</span><span class="sxs-lookup"><span data-stu-id="36682-116">columnid</span></span>  
    <span data-ttu-id="36682-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="36682-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="36682-118">Columnid que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="36682-118">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="36682-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="36682-119">Return value</span></span>

<span data-ttu-id="36682-120">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="36682-120">Type: \[\]</span></span>  
<span data-ttu-id="36682-121">Los datos recuperados de la columna.</span><span class="sxs-lookup"><span data-stu-id="36682-121">The data retrieved from the column.</span></span> <span data-ttu-id="36682-122">Es NULL si la columna es NULL.</span><span class="sxs-lookup"><span data-stu-id="36682-122">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="36682-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="36682-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="36682-124">Referencia</span><span class="sxs-lookup"><span data-stu-id="36682-124">Reference</span></span>

[<span data-ttu-id="36682-125">Clase de API</span><span class="sxs-lookup"><span data-stu-id="36682-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="36682-126">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="36682-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="36682-127">Sobrecarga RetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="36682-127">RetrieveColumn overload</span></span>](./api.retrievecolumn-method.md)

[<span data-ttu-id="36682-128">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="36682-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
