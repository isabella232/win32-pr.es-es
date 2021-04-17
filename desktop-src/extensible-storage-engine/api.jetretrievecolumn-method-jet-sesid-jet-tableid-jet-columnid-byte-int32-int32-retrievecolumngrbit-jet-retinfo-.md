---
description: 'Más información sobre: método API. JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, byte, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)'
title: Método API. JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, byte, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)
TOCTitle: JetRetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit,Microsoft.Isam.Esent.Interop.JET_RETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100790
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d417e188c72914f871df4b46dede204f6633a8b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696304"
---
# <a name="apijetretrievecolumn-method-jet_sesid-jet_tableid-jet_columnid-byte--int32-int32-retrievecolumngrbit-jet_retinfo"></a><span data-ttu-id="afa4f-103">Método API. JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, byte, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</span><span class="sxs-lookup"><span data-stu-id="afa4f-103">Api.JetRetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</span></span>

<span data-ttu-id="afa4f-104">Recupera un valor de una sola columna del registro actual.</span><span class="sxs-lookup"><span data-stu-id="afa4f-104">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="afa4f-105">El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</span><span class="sxs-lookup"><span data-stu-id="afa4f-105">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="afa4f-106">Como alternativa, esta función puede recuperar una columna de un registro que se crea en el búfer de copia del cursor.</span><span class="sxs-lookup"><span data-stu-id="afa4f-106">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="afa4f-107">Esta función también puede recuperar los datos de columna de una entrada de índice que hace referencia al registro actual.</span><span class="sxs-lookup"><span data-stu-id="afa4f-107">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="afa4f-108">Además de recuperar el valor de la columna real, JetRetrieveColumn también se puede usar para recuperar el tamaño de una columna, antes de recuperar los propios datos de la columna para que se pueda ajustar el tamaño adecuado de los búferes de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="afa4f-108">In addition to retrieving the actual column value, JetRetrieveColumn can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span>

<span data-ttu-id="afa4f-109">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="afa4f-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="afa4f-110">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="afa4f-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="afa4f-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="afa4f-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetRetrieveColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Byte(), _
    dataSize As Integer, _
    <OutAttribute> ByRef actualDataSize As Integer, _
    grbit As RetrieveColumnGrbit, _
    retinfo As JET_RETINFO _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As Byte()
Dim dataSize As Integer
Dim actualDataSize As Integer
Dim grbit As RetrieveColumnGrbit
Dim retinfo As JET_RETINFO
Dim returnValue As JET_wrn

returnValue = Api.JetRetrieveColumn(sesid, _
    tableid, columnid, data, dataSize, _
    actualDataSize, grbit, retinfo)
```

``` csharp
public static JET_wrn JetRetrieveColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] data,
    int dataSize,
    out int actualDataSize,
    RetrieveColumnGrbit grbit,
    JET_RETINFO retinfo
)
```

#### <a name="parameters"></a><span data-ttu-id="afa4f-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="afa4f-112">Parameters</span></span>

  - <span data-ttu-id="afa4f-113">sesid</span><span class="sxs-lookup"><span data-stu-id="afa4f-113">sesid</span></span>  
    <span data-ttu-id="afa4f-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="afa4f-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="afa4f-115">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="afa4f-115">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="afa4f-116">TABLEID</span><span class="sxs-lookup"><span data-stu-id="afa4f-116">tableid</span></span>  
    <span data-ttu-id="afa4f-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="afa4f-117">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="afa4f-118">Cursor del que se va a recuperar la columna.</span><span class="sxs-lookup"><span data-stu-id="afa4f-118">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="afa4f-119">columnid</span><span class="sxs-lookup"><span data-stu-id="afa4f-119">columnid</span></span>  
    <span data-ttu-id="afa4f-120">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="afa4f-120">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="afa4f-121">Columnid que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="afa4f-121">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="afa4f-122">datos</span><span class="sxs-lookup"><span data-stu-id="afa4f-122">data</span></span>  
    <span data-ttu-id="afa4f-123">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="afa4f-123">Type: \[\]</span></span>  
    
    <span data-ttu-id="afa4f-124">Búfer de datos que se va a recuperar en.</span><span class="sxs-lookup"><span data-stu-id="afa4f-124">The data buffer to be retrieved into.</span></span>

<!-- end list -->

  - <span data-ttu-id="afa4f-125">dataSize</span><span class="sxs-lookup"><span data-stu-id="afa4f-125">dataSize</span></span>  
    <span data-ttu-id="afa4f-126">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="afa4f-126">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="afa4f-127">Tamaño del búfer de datos.</span><span class="sxs-lookup"><span data-stu-id="afa4f-127">The size of the data buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="afa4f-128">actualDataSize</span><span class="sxs-lookup"><span data-stu-id="afa4f-128">actualDataSize</span></span>  
    <span data-ttu-id="afa4f-129">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="afa4f-129">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="afa4f-130">Devuelve el tamaño real del búfer de datos.</span><span class="sxs-lookup"><span data-stu-id="afa4f-130">Returns the actual size of the data buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="afa4f-131">grbit</span><span class="sxs-lookup"><span data-stu-id="afa4f-131">grbit</span></span>  
    <span data-ttu-id="afa4f-132">Tipo: [Microsoft. ISAM. esent. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="afa4f-132">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="afa4f-133">Recupera opciones de columna.</span><span class="sxs-lookup"><span data-stu-id="afa4f-133">Retrieve column options.</span></span>

<!-- end list -->

  - <span data-ttu-id="afa4f-134">retinfo</span><span class="sxs-lookup"><span data-stu-id="afa4f-134">retinfo</span></span>  
    <span data-ttu-id="afa4f-135">Tipo: [Microsoft.ISAM.esent.Interop.JET_RETINFO](./jet-retinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="afa4f-135">Type: [Microsoft.Isam.Esent.Interop.JET_RETINFO](./jet-retinfo-class.md)</span></span>  
    
    <span data-ttu-id="afa4f-136">Si pretinfo se da como NULL, la función se comporta como si se hubiera proporcionado un valor de itagSequence de 1 y una ibLongValue de 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="afa4f-136">If pretinfo is give as NULL then the function behaves as though an itagSequence of 1 and an ibLongValue of 0 (zero) were given.</span></span> <span data-ttu-id="afa4f-137">Esto hace que la recuperación de columnas recupere el primer valor de una columna con varios valores y que recupere datos largos en el desplazamiento 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="afa4f-137">This causes column retrieval to retrieve the first value of a multi-valued column, and to retrieve long data at offset 0 (zero).</span></span>

#### <a name="return-value"></a><span data-ttu-id="afa4f-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="afa4f-138">Return value</span></span>

<span data-ttu-id="afa4f-139">Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="afa4f-139">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="afa4f-140">Código de advertencia de ESENT.</span><span class="sxs-lookup"><span data-stu-id="afa4f-140">An ESENT warning code.</span></span>  

## <a name="remarks"></a><span data-ttu-id="afa4f-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="afa4f-141">Remarks</span></span>

<span data-ttu-id="afa4f-142">Las funciones RetrieveColumnAs proporcionan funciones de recuperación específicas del tipo de información.</span><span class="sxs-lookup"><span data-stu-id="afa4f-142">The RetrieveColumnAs functions provide datatype-specific retrieval functions.</span></span>

## <a name="see-also"></a><span data-ttu-id="afa4f-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="afa4f-143">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="afa4f-144">Referencia</span><span class="sxs-lookup"><span data-stu-id="afa4f-144">Reference</span></span>

[<span data-ttu-id="afa4f-145">Clase de API</span><span class="sxs-lookup"><span data-stu-id="afa4f-145">Api class</span></span>](./api-class.md)

[<span data-ttu-id="afa4f-146">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="afa4f-146">Api members</span></span>](./api-members.md)

[<span data-ttu-id="afa4f-147">Sobrecarga JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="afa4f-147">JetRetrieveColumn overload</span></span>](./api.jetretrievecolumn-method.md)

[<span data-ttu-id="afa4f-148">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="afa4f-148">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
