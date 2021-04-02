---
description: 'Más información sobre: API. JetEnumerateColumns (método)'
title: Método API. JetEnumerateColumns
TOCTitle: 'JetEnumerateColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Int32,Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID[],System.Int32@,Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN[]@,Microsoft.Isam.Esent.Interop.JET_PFNREALLOC,System.IntPtr,System.Int32,Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetenumeratecolumns(v=EXCHG.10)
ms:contentKeyID: 55100695
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c9a9848d4470d54cc2a146098343b664c9bd3419
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082052"
---
# <a name="apijetenumeratecolumns-method"></a><span data-ttu-id="01aab-103">Método API. JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="01aab-103">Api.JetEnumerateColumns method</span></span>

<span data-ttu-id="01aab-104">Recupera eficazmente un conjunto de columnas y sus valores del registro actual de un cursor o del búfer de copia de ese cursor.</span><span class="sxs-lookup"><span data-stu-id="01aab-104">Efficiently retrieves a set of columns and their values from the current record of a cursor or the copy buffer of that cursor.</span></span> <span data-ttu-id="01aab-105">Las columnas y los valores recuperados se pueden restringir por una lista de identificadores de columna, números de itagSequence y otras características.</span><span class="sxs-lookup"><span data-stu-id="01aab-105">The columns and values retrieved can be restricted by a list of column IDs, itagSequence numbers, and other characteristics.</span></span> <span data-ttu-id="01aab-106">Esta API de recuperación de columnas es única, ya que devuelve información en memoria asignada dinámicamente que se obtiene mediante una devolución de llamada compatible con realloc proporcionada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="01aab-106">This column retrieval API is unique in that it returns information in dynamically allocated memory that is obtained using a user-provided realloc compatible callback.</span></span> <span data-ttu-id="01aab-107">Esta nueva flexibilidad permite la recuperación eficaz de datos de columna con características específicas (como el tamaño y la multiplicidad) que son desconocidas para el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="01aab-107">This new flexibility permits the efficient retrieval of column data with specific characteristics (such as size and multiplicity) that are unknown to the caller.</span></span> <span data-ttu-id="01aab-108">Esto elimina la necesidad de usar los modos de detección de JetRetrieveColumn para determinar esas características a fin de configurar una llamada final a JetRetrieveColumn que recupere correctamente los datos deseados.</span><span class="sxs-lookup"><span data-stu-id="01aab-108">This eliminates the need for the use of the discovery modes of JetRetrieveColumn to determine those characteristics in order to setup a final call to JetRetrieveColumn that will successfully retrieve the desired data.</span></span>

<span data-ttu-id="01aab-109">Esta API no es conforme a CLS.</span><span class="sxs-lookup"><span data-stu-id="01aab-109">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="01aab-110">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="01aab-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="01aab-111">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="01aab-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="01aab-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="01aab-112">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function JetEnumerateColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    numColumnids As Integer, _
    columnids As JET_ENUMCOLUMNID(), _
    <OutAttribute> ByRef numColumnValues As Integer, _
    <OutAttribute> ByRef columnValues As JET_ENUMCOLUMN(), _
    allocator As JET_PFNREALLOC, _
    allocatorContext As IntPtr, _
    maxDataSize As Integer, _
    grbit As EnumerateColumnsGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim numColumnids As Integer
Dim columnids As JET_ENUMCOLUMNID()
Dim numColumnValues As Integer
Dim columnValues As JET_ENUMCOLUMN()
Dim allocator As JET_PFNREALLOC
Dim allocatorContext As IntPtr
Dim maxDataSize As Integer
Dim grbit As EnumerateColumnsGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetEnumerateColumns(sesid, _
    tableid, numColumnids, columnids, _
    numColumnValues, columnValues, allocator, _
    allocatorContext, maxDataSize, grbit)
```

``` csharp
[CLSCompliantAttribute(false)]
public static JET_wrn JetEnumerateColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    int numColumnids,
    JET_ENUMCOLUMNID[] columnids,
    out int numColumnValues,
    out JET_ENUMCOLUMN[] columnValues,
    JET_PFNREALLOC allocator,
    IntPtr allocatorContext,
    int maxDataSize,
    EnumerateColumnsGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="01aab-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="01aab-113">Parameters</span></span>

  - <span data-ttu-id="01aab-114">sesid</span><span class="sxs-lookup"><span data-stu-id="01aab-114">sesid</span></span>  
    <span data-ttu-id="01aab-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="01aab-115">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="01aab-116">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="01aab-116">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="01aab-117">TABLEID</span><span class="sxs-lookup"><span data-stu-id="01aab-117">tableid</span></span>  
    <span data-ttu-id="01aab-118">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="01aab-118">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="01aab-119">Cursor del que se van a recuperar datos.</span><span class="sxs-lookup"><span data-stu-id="01aab-119">The cursor to retrieve data from.</span></span>

<!-- end list -->

  - <span data-ttu-id="01aab-120">numColumnids</span><span class="sxs-lookup"><span data-stu-id="01aab-120">numColumnids</span></span>  
    <span data-ttu-id="01aab-121">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="01aab-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="01aab-122">Número de JET_ENUMCOLUMNIDS.</span><span class="sxs-lookup"><span data-stu-id="01aab-122">The numbers of JET_ENUMCOLUMNIDS.</span></span>

<!-- end list -->

  - <span data-ttu-id="01aab-123">columnids</span><span class="sxs-lookup"><span data-stu-id="01aab-123">columnids</span></span>  
    <span data-ttu-id="01aab-124">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="01aab-124">Type: \[\]</span></span>  
    
    <span data-ttu-id="01aab-125">Una matriz opcional de identificadores de columna, cada uno con una matriz opcional de números itagSequence para enumerar.</span><span class="sxs-lookup"><span data-stu-id="01aab-125">An optional array of column IDs, each with an optional array of itagSequence numbers to enumerate.</span></span>

<!-- end list -->

  - <span data-ttu-id="01aab-126">numColumnValues</span><span class="sxs-lookup"><span data-stu-id="01aab-126">numColumnValues</span></span>  
    <span data-ttu-id="01aab-127">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="01aab-127">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="01aab-128">Devuelve el número de valores de columna recuperados.</span><span class="sxs-lookup"><span data-stu-id="01aab-128">Returns the number of column values retrieved.</span></span>

<!-- end list -->

  - <span data-ttu-id="01aab-129">columnValues</span><span class="sxs-lookup"><span data-stu-id="01aab-129">columnValues</span></span>  
    <span data-ttu-id="01aab-130">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="01aab-130">Type: \[\]</span></span>  
    
    <span data-ttu-id="01aab-131">Devuelve los valores de columna enumerados.</span><span class="sxs-lookup"><span data-stu-id="01aab-131">Returns the enumerated column values.</span></span>

<!-- end list -->

  - <span data-ttu-id="01aab-132">allocator</span><span class="sxs-lookup"><span data-stu-id="01aab-132">allocator</span></span>  
    <span data-ttu-id="01aab-133">Tipo: [Microsoft.ISAM.esent.Interop.JET_PFNREALLOC](./jet-pfnrealloc-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="01aab-133">Type: [Microsoft.Isam.Esent.Interop.JET_PFNREALLOC](./jet-pfnrealloc-delegate.md)</span></span>  
    
    <span data-ttu-id="01aab-134">Devolución de llamada usada para asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="01aab-134">Callback used to allocate memory.</span></span>

<!-- end list -->

  - <span data-ttu-id="01aab-135">allocatorContext</span><span class="sxs-lookup"><span data-stu-id="01aab-135">allocatorContext</span></span>  
    <span data-ttu-id="01aab-136">Tipo: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="01aab-136">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="01aab-137">Contexto para la devolución de llamada de asignación.</span><span class="sxs-lookup"><span data-stu-id="01aab-137">Context for the allocation callback.</span></span>

<!-- end list -->

  - <span data-ttu-id="01aab-138">maxDataSize</span><span class="sxs-lookup"><span data-stu-id="01aab-138">maxDataSize</span></span>  
    <span data-ttu-id="01aab-139">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="01aab-139">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="01aab-140">Establece un límite en la cantidad de datos que se van a devolver de una columna de texto largo o binario largo.</span><span class="sxs-lookup"><span data-stu-id="01aab-140">Sets a cap on the amount of data to return from a long text or long binary column.</span></span> <span data-ttu-id="01aab-141">Este parámetro se puede utilizar para evitar la enumeración de un valor de columna extremadamente grande.</span><span class="sxs-lookup"><span data-stu-id="01aab-141">This parameter can be used to prevent the enumeration of an extremely large column value.</span></span>

<!-- end list -->

  - <span data-ttu-id="01aab-142">grbit</span><span class="sxs-lookup"><span data-stu-id="01aab-142">grbit</span></span>  
    <span data-ttu-id="01aab-143">Tipo: [Microsoft. ISAM. esent. Interop. EnumerateColumnsGrbit](./enumeratecolumnsgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="01aab-143">Type: [Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit](./enumeratecolumnsgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="01aab-144">Opciones de recuperación.</span><span class="sxs-lookup"><span data-stu-id="01aab-144">Retrieve options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="01aab-145">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="01aab-145">Return value</span></span>

<span data-ttu-id="01aab-146">Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="01aab-146">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="01aab-147">ADVERTENCIA o éxito.</span><span class="sxs-lookup"><span data-stu-id="01aab-147">A warning or success.</span></span>  

## <a name="see-also"></a><span data-ttu-id="01aab-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="01aab-148">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="01aab-149">Referencia</span><span class="sxs-lookup"><span data-stu-id="01aab-149">Reference</span></span>

[<span data-ttu-id="01aab-150">Clase de API</span><span class="sxs-lookup"><span data-stu-id="01aab-150">Api class</span></span>](./api-class.md)

[<span data-ttu-id="01aab-151">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="01aab-151">Api members</span></span>](./api-members.md)

[<span data-ttu-id="01aab-152">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="01aab-152">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
