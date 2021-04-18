---
description: 'Más información sobre: método API. RetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)'
title: Método API. RetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)
TOCTitle: RetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit,Microsoft.Isam.Esent.Interop.JET_RETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100853
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43657ec60e521795ba4d474306de9380618cd21f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705435"
---
# <a name="apiretrievecolumn-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit-jet_retinfo"></a><span data-ttu-id="7b8d8-103">Método API. RetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)</span><span class="sxs-lookup"><span data-stu-id="7b8d8-103">Api.RetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)</span></span>

<span data-ttu-id="7b8d8-104">Recupera un valor de una sola columna del registro actual.</span><span class="sxs-lookup"><span data-stu-id="7b8d8-104">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="7b8d8-105">El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</span><span class="sxs-lookup"><span data-stu-id="7b8d8-105">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="7b8d8-106">Como alternativa, esta función puede recuperar una columna de un registro que se crea en el búfer de copia del cursor.</span><span class="sxs-lookup"><span data-stu-id="7b8d8-106">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="7b8d8-107">Esta función también puede recuperar los datos de columna de una entrada de índice que hace referencia al registro actual.</span><span class="sxs-lookup"><span data-stu-id="7b8d8-107">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="7b8d8-108">Además de recuperar el valor de la columna real, JetRetrieveColumn también se puede usar para recuperar el tamaño de una columna, antes de recuperar los propios datos de la columna para que se pueda ajustar el tamaño adecuado de los búferes de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7b8d8-108">In addition to retrieving the actual column value, JetRetrieveColumn can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span>

<span data-ttu-id="7b8d8-109">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7b8d8-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7b8d8-110">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7b8d8-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7b8d8-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7b8d8-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit, _
    retinfo As JET_RETINFO _
) As Byte()
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim retinfo As JET_RETINFO
Dim returnValue As Byte()

returnValue = Api.RetrieveColumn(sesid, _
    tableid, columnid, grbit, retinfo)
```

``` csharp
public static byte[] RetrieveColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit,
    JET_RETINFO retinfo
)
```

#### <a name="parameters"></a><span data-ttu-id="7b8d8-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7b8d8-112">Parameters</span></span>

  - <span data-ttu-id="7b8d8-113">sesid</span><span class="sxs-lookup"><span data-stu-id="7b8d8-113">sesid</span></span>  
    <span data-ttu-id="7b8d8-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7b8d8-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="7b8d8-115">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="7b8d8-115">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="7b8d8-116">TABLEID</span><span class="sxs-lookup"><span data-stu-id="7b8d8-116">tableid</span></span>  
    <span data-ttu-id="7b8d8-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7b8d8-117">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="7b8d8-118">Cursor del que se va a recuperar la columna.</span><span class="sxs-lookup"><span data-stu-id="7b8d8-118">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="7b8d8-119">columnid</span><span class="sxs-lookup"><span data-stu-id="7b8d8-119">columnid</span></span>  
    <span data-ttu-id="7b8d8-120">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7b8d8-120">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="7b8d8-121">Columnid que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="7b8d8-121">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="7b8d8-122">grbit</span><span class="sxs-lookup"><span data-stu-id="7b8d8-122">grbit</span></span>  
    <span data-ttu-id="7b8d8-123">Tipo: [Microsoft. ISAM. esent. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="7b8d8-123">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="7b8d8-124">Recupera opciones de columna.</span><span class="sxs-lookup"><span data-stu-id="7b8d8-124">Retrieve column options.</span></span>

<!-- end list -->

  - <span data-ttu-id="7b8d8-125">retinfo</span><span class="sxs-lookup"><span data-stu-id="7b8d8-125">retinfo</span></span>  
    <span data-ttu-id="7b8d8-126">Tipo: [Microsoft.ISAM.esent.Interop.JET_RETINFO](./jet-retinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="7b8d8-126">Type: [Microsoft.Isam.Esent.Interop.JET_RETINFO](./jet-retinfo-class.md)</span></span>  
    
    <span data-ttu-id="7b8d8-127">Si pretinfo se da como NULL, la función se comporta como si se hubiera proporcionado un valor de itagSequence de 1 y una ibLongValue de 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="7b8d8-127">If pretinfo is give as NULL then the function behaves as though an itagSequence of 1 and an ibLongValue of 0 (zero) were given.</span></span> <span data-ttu-id="7b8d8-128">Esto hace que la recuperación de columnas recupere el primer valor de una columna con varios valores y que recupere datos largos en el desplazamiento 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="7b8d8-128">This causes column retrieval to retrieve the first value of a multi-valued column, and to retrieve long data at offset 0 (zero).</span></span>

#### <a name="return-value"></a><span data-ttu-id="7b8d8-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7b8d8-129">Return value</span></span>

<span data-ttu-id="7b8d8-130">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="7b8d8-130">Type: \[\]</span></span>  
<span data-ttu-id="7b8d8-131">Los datos recuperados de la columna.</span><span class="sxs-lookup"><span data-stu-id="7b8d8-131">The data retrieved from the column.</span></span> <span data-ttu-id="7b8d8-132">Es NULL si la columna es NULL.</span><span class="sxs-lookup"><span data-stu-id="7b8d8-132">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7b8d8-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b8d8-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7b8d8-134">Referencia</span><span class="sxs-lookup"><span data-stu-id="7b8d8-134">Reference</span></span>

[<span data-ttu-id="7b8d8-135">Clase de API</span><span class="sxs-lookup"><span data-stu-id="7b8d8-135">Api class</span></span>](./api-class.md)

[<span data-ttu-id="7b8d8-136">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="7b8d8-136">Api members</span></span>](./api-members.md)

[<span data-ttu-id="7b8d8-137">Sobrecarga RetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="7b8d8-137">RetrieveColumn overload</span></span>](./api.retrievecolumn-method.md)

[<span data-ttu-id="7b8d8-138">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="7b8d8-138">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
