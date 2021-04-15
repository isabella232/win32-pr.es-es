---
description: 'Más información sobre: método API. RetrieveColumnAsString (JET_SESID, JET_TABLEID, JET_COLUMNID, codificación)'
title: Método API. RetrieveColumnAsString (JET_SESID, JET_TABLEID, JET_COLUMNID, codificación)
TOCTitle: RetrieveColumnAsString method (JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsString(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Text.Encoding)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasstring(v=EXCHG.10)
ms:contentKeyID: 55100899
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsString
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1d7ec3bac73f5b82f82d2762a34084de25b63f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696206"
---
# <a name="apiretrievecolumnasstring-method-jet_sesid-jet_tableid-jet_columnid-encoding"></a><span data-ttu-id="6a408-103">Método API. RetrieveColumnAsString (JET_SESID, JET_TABLEID, JET_COLUMNID, codificación)</span><span class="sxs-lookup"><span data-stu-id="6a408-103">Api.RetrieveColumnAsString method (JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding)</span></span>

<span data-ttu-id="6a408-104">Recupera un valor de columna de cadena del registro actual.</span><span class="sxs-lookup"><span data-stu-id="6a408-104">Retrieves a string column value from the current record.</span></span> <span data-ttu-id="6a408-105">El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</span><span class="sxs-lookup"><span data-stu-id="6a408-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="6a408-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6a408-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6a408-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6a408-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6a408-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6a408-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsString ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    encoding As Encoding _
) As String
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim encoding As Encoding
Dim returnValue As String

returnValue = Api.RetrieveColumnAsString(sesid, _
    tableid, columnid, encoding)
```

``` csharp
public static string RetrieveColumnAsString(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    Encoding encoding
)
```

#### <a name="parameters"></a><span data-ttu-id="6a408-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6a408-109">Parameters</span></span>

  - <span data-ttu-id="6a408-110">sesid</span><span class="sxs-lookup"><span data-stu-id="6a408-110">sesid</span></span>  
    <span data-ttu-id="6a408-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6a408-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="6a408-112">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="6a408-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="6a408-113">TABLEID</span><span class="sxs-lookup"><span data-stu-id="6a408-113">tableid</span></span>  
    <span data-ttu-id="6a408-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6a408-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="6a408-115">Cursor del que se va a recuperar la columna.</span><span class="sxs-lookup"><span data-stu-id="6a408-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="6a408-116">columnid</span><span class="sxs-lookup"><span data-stu-id="6a408-116">columnid</span></span>  
    <span data-ttu-id="6a408-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6a408-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="6a408-118">Columnid que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="6a408-118">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="6a408-119">encoding</span><span class="sxs-lookup"><span data-stu-id="6a408-119">encoding</span></span>  
    <span data-ttu-id="6a408-120">Tipo: [System. Text. Encoding](/dotnet/api/system.text.encoding)</span><span class="sxs-lookup"><span data-stu-id="6a408-120">Type: [System.Text.Encoding](/dotnet/api/system.text.encoding)</span></span>  
    
    <span data-ttu-id="6a408-121">Codificación de cadena que se va a usar al convertir datos.</span><span class="sxs-lookup"><span data-stu-id="6a408-121">The string encoding to use when converting data.</span></span>

#### <a name="return-value"></a><span data-ttu-id="6a408-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6a408-122">Return value</span></span>

<span data-ttu-id="6a408-123">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="6a408-123">Type: [System.String](/dotnet/api/system.string)</span></span>  
<span data-ttu-id="6a408-124">Los datos recuperados de la columna como una cadena.</span><span class="sxs-lookup"><span data-stu-id="6a408-124">The data retrieved from the column as a string.</span></span> <span data-ttu-id="6a408-125">Es NULL si la columna es NULL.</span><span class="sxs-lookup"><span data-stu-id="6a408-125">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6a408-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a408-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6a408-127">Referencia</span><span class="sxs-lookup"><span data-stu-id="6a408-127">Reference</span></span>

[<span data-ttu-id="6a408-128">Clase de API</span><span class="sxs-lookup"><span data-stu-id="6a408-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="6a408-129">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="6a408-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="6a408-130">Sobrecarga RetrieveColumnAsString</span><span class="sxs-lookup"><span data-stu-id="6a408-130">RetrieveColumnAsString overload</span></span>](./api.retrievecolumnasstring-method.md)

[<span data-ttu-id="6a408-131">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="6a408-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
