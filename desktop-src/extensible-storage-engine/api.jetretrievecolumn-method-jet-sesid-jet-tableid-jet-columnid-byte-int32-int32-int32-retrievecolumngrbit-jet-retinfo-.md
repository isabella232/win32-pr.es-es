---
description: 'Más información sobre: método API. JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, byte, Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)'
title: Método API. JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, byte, Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)
TOCTitle: JetRetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit,Microsoft.Isam.Esent.Interop.JET_RETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100792
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 832e6d6cc123e4a85a2cacb2df688348732fcc0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361519"
---
# <a name="apijetretrievecolumn-method-jet_sesid-jet_tableid-jet_columnid-byte--int32-int32-int32-retrievecolumngrbit-jet_retinfo"></a><span data-ttu-id="b2b0b-103">Método API. JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, byte, Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</span><span class="sxs-lookup"><span data-stu-id="b2b0b-103">Api.JetRetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</span></span>

<span data-ttu-id="b2b0b-104">Recupera un valor de una sola columna del registro actual.</span><span class="sxs-lookup"><span data-stu-id="b2b0b-104">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="b2b0b-105">El registro es el registro asociado a la entrada de índice en la posición actual del cursor.</span><span class="sxs-lookup"><span data-stu-id="b2b0b-105">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="b2b0b-106">Como alternativa, esta función puede recuperar una columna de un registro que se crea en el búfer de copia del cursor.</span><span class="sxs-lookup"><span data-stu-id="b2b0b-106">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="b2b0b-107">Esta función también puede recuperar los datos de columna de una entrada de índice que hace referencia al registro actual.</span><span class="sxs-lookup"><span data-stu-id="b2b0b-107">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="b2b0b-108">Además de recuperar el valor de la columna real, JetRetrieveColumn también se puede usar para recuperar el tamaño de una columna, antes de recuperar los propios datos de la columna para que se pueda ajustar el tamaño adecuado de los búferes de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b2b0b-108">In addition to retrieving the actual column value, JetRetrieveColumn can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span>

<span data-ttu-id="b2b0b-109">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b2b0b-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b2b0b-110">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b2b0b-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b2b0b-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b2b0b-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetRetrieveColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Byte(), _
    dataSize As Integer, _
    dataOffset As Integer, _
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
Dim dataOffset As Integer
Dim actualDataSize As Integer
Dim grbit As RetrieveColumnGrbit
Dim retinfo As JET_RETINFO
Dim returnValue As JET_wrn

returnValue = Api.JetRetrieveColumn(sesid, _
    tableid, columnid, data, dataSize, _
    dataOffset, actualDataSize, grbit, _
    retinfo)
```

``` csharp
public static JET_wrn JetRetrieveColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] data,
    int dataSize,
    int dataOffset,
    out int actualDataSize,
    RetrieveColumnGrbit grbit,
    JET_RETINFO retinfo
)
```

#### <a name="parameters"></a><span data-ttu-id="b2b0b-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b2b0b-112">Parameters</span></span>

  - <span data-ttu-id="b2b0b-113">sesid</span><span class="sxs-lookup"><span data-stu-id="b2b0b-113">sesid</span></span>  
    <span data-ttu-id="b2b0b-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b2b0b-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b2b0b-115">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="b2b0b-115">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="b2b0b-116">TABLEID</span><span class="sxs-lookup"><span data-stu-id="b2b0b-116">tableid</span></span>  
    <span data-ttu-id="b2b0b-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b2b0b-117">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="b2b0b-118">Cursor del que se va a recuperar la columna.</span><span class="sxs-lookup"><span data-stu-id="b2b0b-118">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="b2b0b-119">columnid</span><span class="sxs-lookup"><span data-stu-id="b2b0b-119">columnid</span></span>  
    <span data-ttu-id="b2b0b-120">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b2b0b-120">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="b2b0b-121">Columnid que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="b2b0b-121">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="b2b0b-122">datos</span><span class="sxs-lookup"><span data-stu-id="b2b0b-122">data</span></span>  
    <span data-ttu-id="b2b0b-123">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="b2b0b-123">Type: \[\]</span></span>  
    
    <span data-ttu-id="b2b0b-124">Búfer de datos que se va a recuperar en.</span><span class="sxs-lookup"><span data-stu-id="b2b0b-124">The data buffer to be retrieved into.</span></span>

<!-- end list -->

  - <span data-ttu-id="b2b0b-125">dataSize</span><span class="sxs-lookup"><span data-stu-id="b2b0b-125">dataSize</span></span>  
    <span data-ttu-id="b2b0b-126">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="b2b0b-126">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="b2b0b-127">Tamaño del búfer de datos.</span><span class="sxs-lookup"><span data-stu-id="b2b0b-127">The size of the data buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="b2b0b-128">dataOffset</span><span class="sxs-lookup"><span data-stu-id="b2b0b-128">dataOffset</span></span>  
    <span data-ttu-id="b2b0b-129">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="b2b0b-129">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="b2b0b-130">Desplazamiento en el búfer de datos en el que se van a leer los datos.</span><span class="sxs-lookup"><span data-stu-id="b2b0b-130">Offset into the data buffer to read data into.</span></span>

<!-- end list -->

  - <span data-ttu-id="b2b0b-131">actualDataSize</span><span class="sxs-lookup"><span data-stu-id="b2b0b-131">actualDataSize</span></span>  
    <span data-ttu-id="b2b0b-132">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="b2b0b-132">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="b2b0b-133">Devuelve el tamaño real del búfer de datos.</span><span class="sxs-lookup"><span data-stu-id="b2b0b-133">Returns the actual size of the data buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="b2b0b-134">grbit</span><span class="sxs-lookup"><span data-stu-id="b2b0b-134">grbit</span></span>  
    <span data-ttu-id="b2b0b-135">Tipo: [Microsoft. ISAM. esent. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="b2b0b-135">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="b2b0b-136">Recupera opciones de columna.</span><span class="sxs-lookup"><span data-stu-id="b2b0b-136">Retrieve column options.</span></span>

<!-- end list -->

  - <span data-ttu-id="b2b0b-137">retinfo</span><span class="sxs-lookup"><span data-stu-id="b2b0b-137">retinfo</span></span>  
    <span data-ttu-id="b2b0b-138">Tipo: [Microsoft.ISAM.esent.Interop.JET_RETINFO](./jet-retinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="b2b0b-138">Type: [Microsoft.Isam.Esent.Interop.JET_RETINFO](./jet-retinfo-class.md)</span></span>  
    
    <span data-ttu-id="b2b0b-139">Si pretinfo se da como NULL, la función se comporta como si se hubiera proporcionado un valor de itagSequence de 1 y una ibLongValue de 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="b2b0b-139">If pretinfo is give as NULL then the function behaves as though an itagSequence of 1 and an ibLongValue of 0 (zero) were given.</span></span> <span data-ttu-id="b2b0b-140">Esto hace que la recuperación de columnas recupere el primer valor de una columna con varios valores y que recupere datos largos en el desplazamiento 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="b2b0b-140">This causes column retrieval to retrieve the first value of a multi-valued column, and to retrieve long data at offset 0 (zero).</span></span>

#### <a name="return-value"></a><span data-ttu-id="b2b0b-141">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b2b0b-141">Return value</span></span>

<span data-ttu-id="b2b0b-142">Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="b2b0b-142">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="b2b0b-143">Código de advertencia de ESENT.</span><span class="sxs-lookup"><span data-stu-id="b2b0b-143">An ESENT warning code.</span></span>  

## <a name="remarks"></a><span data-ttu-id="b2b0b-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b2b0b-144">Remarks</span></span>

<span data-ttu-id="b2b0b-145">Se trata de un método interno que toma un desplazamiento del búfer y el tamaño.</span><span class="sxs-lookup"><span data-stu-id="b2b0b-145">This is an internal method that takes a buffer offset as well as size.</span></span>

## <a name="see-also"></a><span data-ttu-id="b2b0b-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="b2b0b-146">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b2b0b-147">Referencia</span><span class="sxs-lookup"><span data-stu-id="b2b0b-147">Reference</span></span>

[<span data-ttu-id="b2b0b-148">Clase de API</span><span class="sxs-lookup"><span data-stu-id="b2b0b-148">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b2b0b-149">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="b2b0b-149">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b2b0b-150">Sobrecarga JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="b2b0b-150">JetRetrieveColumn overload</span></span>](./api.jetretrievecolumn-method.md)

[<span data-ttu-id="b2b0b-151">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b2b0b-151">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
