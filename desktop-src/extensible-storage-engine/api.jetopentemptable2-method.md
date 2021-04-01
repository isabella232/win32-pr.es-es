---
description: 'Más información sobre: API. JetOpenTempTable2 (método)'
title: Método API. JetOpenTempTable2
TOCTitle: 'JetOpenTempTable2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF[],System.Int32,System.Int32,Microsoft.Isam.Esent.Interop.TempTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopentemptable2(v=EXCHG.10)
ms:contentKeyID: 55100777
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8fd3f0e04db6519fbcaa1c2d2fa9060d2d993d27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279086"
---
# <a name="apijetopentemptable2-method"></a><span data-ttu-id="b9ce9-103">Método API. JetOpenTempTable2</span><span class="sxs-lookup"><span data-stu-id="b9ce9-103">Api.JetOpenTempTable2 method</span></span>

<span data-ttu-id="b9ce9-104">Crea una tabla temporal con un índice único.</span><span class="sxs-lookup"><span data-stu-id="b9ce9-104">Creates a temporary table with a single index.</span></span> <span data-ttu-id="b9ce9-105">Una tabla temporal almacena y recupera registros como una tabla normal creada mediante JetCreateTableColumnIndex.</span><span class="sxs-lookup"><span data-stu-id="b9ce9-105">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="b9ce9-106">Sin embargo, las tablas temporales son mucho más rápidas que las normales debido a su naturaleza volátil.</span><span class="sxs-lookup"><span data-stu-id="b9ce9-106">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="b9ce9-107">También se pueden usar para ordenar de forma muy rápida y realizar una eliminación duplicada en conjuntos de registros cuando se tiene acceso a ellos de forma puramente secuencial.</span><span class="sxs-lookup"><span data-stu-id="b9ce9-107">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="b9ce9-108">Vea también [JetOpenTempTable (JET_SESID, \[ \] , Int32, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable-method.md), [JetOpenTempTable3 (JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID \[ \] )](./api.jetopentemptable3-method.md).</span><span class="sxs-lookup"><span data-stu-id="b9ce9-108">Also see [JetOpenTempTable(JET_SESID, \[\], Int32, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable-method.md), [JetOpenTempTable3(JET_SESID, \[\], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable3-method.md).</span></span> <span data-ttu-id="b9ce9-109">[JetOpenTemporaryTable (JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span><span class="sxs-lookup"><span data-stu-id="b9ce9-109">[JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span></span>

<span data-ttu-id="b9ce9-110">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b9ce9-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b9ce9-111">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b9ce9-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b9ce9-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b9ce9-112">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenTempTable2 ( _
    sesid As JET_SESID, _
    columns As JET_COLUMNDEF(), _
    numColumns As Integer, _
    lcid As Integer, _
    grbit As TempTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID, _
    columnids As JET_COLUMNID() _
)
'Usage
Dim sesid As JET_SESID
Dim columns As JET_COLUMNDEF()
Dim numColumns As Integer
Dim lcid As Integer
Dim grbit As TempTableGrbit
Dim tableid As JET_TABLEID
Dim columnids As JET_COLUMNID()

Api.JetOpenTempTable2(sesid, columns, _
    numColumns, lcid, grbit, tableid, _
    columnids)
```

``` csharp
public static void JetOpenTempTable2(
    JET_SESID sesid,
    JET_COLUMNDEF[] columns,
    int numColumns,
    int lcid,
    TempTableGrbit grbit,
    out JET_TABLEID tableid,
    JET_COLUMNID[] columnids
)
```

#### <a name="parameters"></a><span data-ttu-id="b9ce9-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b9ce9-113">Parameters</span></span>

  - <span data-ttu-id="b9ce9-114">sesid</span><span class="sxs-lookup"><span data-stu-id="b9ce9-114">sesid</span></span>  
    <span data-ttu-id="b9ce9-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b9ce9-115">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b9ce9-116">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="b9ce9-116">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="b9ce9-117">columnas</span><span class="sxs-lookup"><span data-stu-id="b9ce9-117">columns</span></span>  
    <span data-ttu-id="b9ce9-118">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="b9ce9-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="b9ce9-119">Definiciones de columna para las columnas creadas en la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="b9ce9-119">Column definitions for the columns created in the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="b9ce9-120">numColumns</span><span class="sxs-lookup"><span data-stu-id="b9ce9-120">numColumns</span></span>  
    <span data-ttu-id="b9ce9-121">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="b9ce9-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="b9ce9-122">Número de definiciones de columna.</span><span class="sxs-lookup"><span data-stu-id="b9ce9-122">Number of column definitions.</span></span>

<!-- end list -->

  - <span data-ttu-id="b9ce9-123">lcid</span><span class="sxs-lookup"><span data-stu-id="b9ce9-123">lcid</span></span>  
    <span data-ttu-id="b9ce9-124">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="b9ce9-124">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="b9ce9-125">IDENTIFICADOR de configuración regional que se va a usar para comparar los datos de columna de clave Unicode de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="b9ce9-125">The locale ID to use to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="b9ce9-126">Se puede usar cualquier configuración regional siempre que se haya instalado en el equipo el paquete de idioma adecuado.</span><span class="sxs-lookup"><span data-stu-id="b9ce9-126">Any locale may be used as long as the appropriate language pack has been installed on the machine.</span></span>

<!-- end list -->

  - <span data-ttu-id="b9ce9-127">grbit</span><span class="sxs-lookup"><span data-stu-id="b9ce9-127">grbit</span></span>  
    <span data-ttu-id="b9ce9-128">Tipo: [Microsoft. ISAM. esent. Interop. TempTableGrbit](./temptablegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="b9ce9-128">Type: [Microsoft.Isam.Esent.Interop.TempTableGrbit](./temptablegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="b9ce9-129">Opciones de creación de tablas.</span><span class="sxs-lookup"><span data-stu-id="b9ce9-129">Table creation options.</span></span>

<!-- end list -->

  - <span data-ttu-id="b9ce9-130">TABLEID</span><span class="sxs-lookup"><span data-stu-id="b9ce9-130">tableid</span></span>  
    <span data-ttu-id="b9ce9-131">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b9ce9-131">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="b9ce9-132">Devuelve el ID. de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="b9ce9-132">Returns the tableid of the temporary table.</span></span> <span data-ttu-id="b9ce9-133">Al cerrar este TABLEID con [JetCloseTable (JET_SESID, JET_TABLEID),](./api.jetclosetable-method.md) se liberan los recursos asociados a la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="b9ce9-133">Closing this tableid with [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) frees the resources associated with the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="b9ce9-134">columnids</span><span class="sxs-lookup"><span data-stu-id="b9ce9-134">columnids</span></span>  
    <span data-ttu-id="b9ce9-135">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="b9ce9-135">Type: \[\]</span></span>  
    
    <span data-ttu-id="b9ce9-136">Búfer de salida que recibe la matriz de identificadores de columna generados durante la creación de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="b9ce9-136">The output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span> <span data-ttu-id="b9ce9-137">Los identificadores de columna de esta matriz se corresponden exactamente con la matriz de entrada de definiciones de columna.</span><span class="sxs-lookup"><span data-stu-id="b9ce9-137">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="b9ce9-138">Como resultado, el tamaño de este búfer debe corresponder al tamaño de la matriz de entrada.</span><span class="sxs-lookup"><span data-stu-id="b9ce9-138">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

## <a name="see-also"></a><span data-ttu-id="b9ce9-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9ce9-139">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b9ce9-140">Referencia</span><span class="sxs-lookup"><span data-stu-id="b9ce9-140">Reference</span></span>

[<span data-ttu-id="b9ce9-141">Clase de API</span><span class="sxs-lookup"><span data-stu-id="b9ce9-141">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b9ce9-142">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="b9ce9-142">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b9ce9-143">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b9ce9-143">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
