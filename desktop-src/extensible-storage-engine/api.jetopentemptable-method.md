---
description: 'Más información sobre: API. JetOpenTempTable (método)'
title: Método API. JetOpenTempTable
TOCTitle: 'JetOpenTempTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF[],System.Int32,Microsoft.Isam.Esent.Interop.TempTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopentemptable(v=EXCHG.10)
ms:contentKeyID: 55100773
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fa41ce62b8bc2d7f2429acb5de809ad0be44a609
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697725"
---
# <a name="apijetopentemptable-method"></a><span data-ttu-id="a93b6-103">Método API. JetOpenTempTable</span><span class="sxs-lookup"><span data-stu-id="a93b6-103">Api.JetOpenTempTable method</span></span>

<span data-ttu-id="a93b6-104">Crea una tabla temporal con un índice único.</span><span class="sxs-lookup"><span data-stu-id="a93b6-104">Creates a temporary table with a single index.</span></span> <span data-ttu-id="a93b6-105">Una tabla temporal almacena y recupera registros como una tabla normal creada mediante JetCreateTableColumnIndex.</span><span class="sxs-lookup"><span data-stu-id="a93b6-105">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="a93b6-106">Sin embargo, las tablas temporales son mucho más rápidas que las normales debido a su naturaleza volátil.</span><span class="sxs-lookup"><span data-stu-id="a93b6-106">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="a93b6-107">También se pueden usar para ordenar de forma muy rápida y realizar una eliminación duplicada en conjuntos de registros cuando se tiene acceso a ellos de forma puramente secuencial.</span><span class="sxs-lookup"><span data-stu-id="a93b6-107">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="a93b6-108">Vea también [JetOpenTempTable3 (JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md).</span><span class="sxs-lookup"><span data-stu-id="a93b6-108">Also see [JetOpenTempTable3(JET_SESID, \[\], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable3-method.md).</span></span> <span data-ttu-id="a93b6-109">[JetOpenTemporaryTable (JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span><span class="sxs-lookup"><span data-stu-id="a93b6-109">[JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span></span>

<span data-ttu-id="a93b6-110">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a93b6-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a93b6-111">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a93b6-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a93b6-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a93b6-112">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenTempTable ( _
    sesid As JET_SESID, _
    columns As JET_COLUMNDEF(), _
    numColumns As Integer, _
    grbit As TempTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID, _
    columnids As JET_COLUMNID() _
)
'Usage
Dim sesid As JET_SESID
Dim columns As JET_COLUMNDEF()
Dim numColumns As Integer
Dim grbit As TempTableGrbit
Dim tableid As JET_TABLEID
Dim columnids As JET_COLUMNID()

Api.JetOpenTempTable(sesid, columns, _
    numColumns, grbit, tableid, columnids)
```

``` csharp
public static void JetOpenTempTable(
    JET_SESID sesid,
    JET_COLUMNDEF[] columns,
    int numColumns,
    TempTableGrbit grbit,
    out JET_TABLEID tableid,
    JET_COLUMNID[] columnids
)
```

#### <a name="parameters"></a><span data-ttu-id="a93b6-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a93b6-113">Parameters</span></span>

  - <span data-ttu-id="a93b6-114">sesid</span><span class="sxs-lookup"><span data-stu-id="a93b6-114">sesid</span></span>  
    <span data-ttu-id="a93b6-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a93b6-115">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="a93b6-116">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="a93b6-116">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="a93b6-117">columnas</span><span class="sxs-lookup"><span data-stu-id="a93b6-117">columns</span></span>  
    <span data-ttu-id="a93b6-118">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="a93b6-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="a93b6-119">Definiciones de columna para las columnas creadas en la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="a93b6-119">Column definitions for the columns created in the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="a93b6-120">numColumns</span><span class="sxs-lookup"><span data-stu-id="a93b6-120">numColumns</span></span>  
    <span data-ttu-id="a93b6-121">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a93b6-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="a93b6-122">Número de definiciones de columna.</span><span class="sxs-lookup"><span data-stu-id="a93b6-122">Number of column definitions.</span></span>

<!-- end list -->

  - <span data-ttu-id="a93b6-123">grbit</span><span class="sxs-lookup"><span data-stu-id="a93b6-123">grbit</span></span>  
    <span data-ttu-id="a93b6-124">Tipo: [Microsoft. ISAM. esent. Interop. TempTableGrbit](./temptablegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="a93b6-124">Type: [Microsoft.Isam.Esent.Interop.TempTableGrbit](./temptablegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="a93b6-125">Opciones de creación de tablas.</span><span class="sxs-lookup"><span data-stu-id="a93b6-125">Table creation options.</span></span>

<!-- end list -->

  - <span data-ttu-id="a93b6-126">TABLEID</span><span class="sxs-lookup"><span data-stu-id="a93b6-126">tableid</span></span>  
    <span data-ttu-id="a93b6-127">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a93b6-127">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="a93b6-128">Devuelve el ID. de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="a93b6-128">Returns the tableid of the temporary table.</span></span> <span data-ttu-id="a93b6-129">Al cerrar este TABLEID con [JetCloseTable (JET_SESID, JET_TABLEID),](./api.jetclosetable-method.md) se liberan los recursos asociados a la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="a93b6-129">Closing this tableid with [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) frees the resources associated with the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="a93b6-130">columnids</span><span class="sxs-lookup"><span data-stu-id="a93b6-130">columnids</span></span>  
    <span data-ttu-id="a93b6-131">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="a93b6-131">Type: \[\]</span></span>  
    
    <span data-ttu-id="a93b6-132">Búfer de salida que recibe la matriz de identificadores de columna generados durante la creación de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="a93b6-132">The output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span> <span data-ttu-id="a93b6-133">Los identificadores de columna de esta matriz se corresponden exactamente con la matriz de entrada de definiciones de columna.</span><span class="sxs-lookup"><span data-stu-id="a93b6-133">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="a93b6-134">Como resultado, el tamaño de este búfer debe corresponder al tamaño de la matriz de entrada.</span><span class="sxs-lookup"><span data-stu-id="a93b6-134">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

## <a name="see-also"></a><span data-ttu-id="a93b6-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="a93b6-135">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a93b6-136">Referencia</span><span class="sxs-lookup"><span data-stu-id="a93b6-136">Reference</span></span>

[<span data-ttu-id="a93b6-137">Clase de API</span><span class="sxs-lookup"><span data-stu-id="a93b6-137">Api class</span></span>](./api-class.md)

[<span data-ttu-id="a93b6-138">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="a93b6-138">Api members</span></span>](./api-members.md)

[<span data-ttu-id="a93b6-139">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a93b6-139">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
