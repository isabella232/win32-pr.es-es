---
description: 'Más información sobre: API. JetOpenTempTable3 (método)'
title: Método Api.JetOpenTempTable3
TOCTitle: 'JetOpenTempTable3 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable3(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF[],System.Int32,Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX,Microsoft.Isam.Esent.Interop.TempTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopentemptable3(v=EXCHG.10)
ms:contentKeyID: 55100774
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable3
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable3
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9e88b5413492c0ae00ed41e569afb49ca6c18e51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697724"
---
# <a name="apijetopentemptable3-method"></a><span data-ttu-id="faf94-103">Método Api.JetOpenTempTable3</span><span class="sxs-lookup"><span data-stu-id="faf94-103">Api.JetOpenTempTable3 method</span></span>

<span data-ttu-id="faf94-104">Crea una tabla temporal con un índice único.</span><span class="sxs-lookup"><span data-stu-id="faf94-104">Creates a temporary table with a single index.</span></span> <span data-ttu-id="faf94-105">Una tabla temporal almacena y recupera registros como una tabla normal creada mediante JetCreateTableColumnIndex.</span><span class="sxs-lookup"><span data-stu-id="faf94-105">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="faf94-106">Sin embargo, las tablas temporales son mucho más rápidas que las normales debido a su naturaleza volátil.</span><span class="sxs-lookup"><span data-stu-id="faf94-106">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="faf94-107">También se pueden usar para ordenar de forma muy rápida y realizar una eliminación duplicada en conjuntos de registros cuando se tiene acceso a ellos de forma puramente secuencial.</span><span class="sxs-lookup"><span data-stu-id="faf94-107">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="faf94-108">Vea también [JetOpenTempTable (JET_SESID, \[ \] , Int32, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable-method.md), [JetOpenTemporaryTable (JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span><span class="sxs-lookup"><span data-stu-id="faf94-108">Also see [JetOpenTempTable(JET_SESID, \[\], Int32, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable-method.md), [JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span></span>

<span data-ttu-id="faf94-109">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="faf94-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="faf94-110">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="faf94-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="faf94-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="faf94-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenTempTable3 ( _
    sesid As JET_SESID, _
    columns As JET_COLUMNDEF(), _
    numColumns As Integer, _
    unicodeindex As JET_UNICODEINDEX, _
    grbit As TempTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID, _
    columnids As JET_COLUMNID() _
)
'Usage
Dim sesid As JET_SESID
Dim columns As JET_COLUMNDEF()
Dim numColumns As Integer
Dim unicodeindex As JET_UNICODEINDEX
Dim grbit As TempTableGrbit
Dim tableid As JET_TABLEID
Dim columnids As JET_COLUMNID()

Api.JetOpenTempTable3(sesid, columns, _
    numColumns, unicodeindex, grbit, _
    tableid, columnids)
```

``` csharp
public static void JetOpenTempTable3(
    JET_SESID sesid,
    JET_COLUMNDEF[] columns,
    int numColumns,
    JET_UNICODEINDEX unicodeindex,
    TempTableGrbit grbit,
    out JET_TABLEID tableid,
    JET_COLUMNID[] columnids
)
```

#### <a name="parameters"></a><span data-ttu-id="faf94-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="faf94-112">Parameters</span></span>

  - <span data-ttu-id="faf94-113">sesid</span><span class="sxs-lookup"><span data-stu-id="faf94-113">sesid</span></span>  
    <span data-ttu-id="faf94-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="faf94-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="faf94-115">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="faf94-115">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="faf94-116">columnas</span><span class="sxs-lookup"><span data-stu-id="faf94-116">columns</span></span>  
    <span data-ttu-id="faf94-117">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="faf94-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="faf94-118">Definiciones de columna para las columnas creadas en la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="faf94-118">Column definitions for the columns created in the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="faf94-119">numColumns</span><span class="sxs-lookup"><span data-stu-id="faf94-119">numColumns</span></span>  
    <span data-ttu-id="faf94-120">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="faf94-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="faf94-121">Número de definiciones de columna.</span><span class="sxs-lookup"><span data-stu-id="faf94-121">Number of column definitions.</span></span>

<!-- end list -->

  - <span data-ttu-id="faf94-122">unicodeindex</span><span class="sxs-lookup"><span data-stu-id="faf94-122">unicodeindex</span></span>  
    <span data-ttu-id="faf94-123">Tipo: [Microsoft.ISAM.esent.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)</span><span class="sxs-lookup"><span data-stu-id="faf94-123">Type: [Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)</span></span>  
    
    <span data-ttu-id="faf94-124">El identificador de configuración regional y las marcas de normalización que se utilizarán para comparar los datos de columna de clave Unicode en la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="faf94-124">The Locale ID and normalization flags that will be used to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="faf94-125">Si no está presente, se usan las opciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="faf94-125">When this is not present then the default options are used.</span></span>

<!-- end list -->

  - <span data-ttu-id="faf94-126">grbit</span><span class="sxs-lookup"><span data-stu-id="faf94-126">grbit</span></span>  
    <span data-ttu-id="faf94-127">Tipo: [Microsoft. ISAM. esent. Interop. TempTableGrbit](./temptablegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="faf94-127">Type: [Microsoft.Isam.Esent.Interop.TempTableGrbit](./temptablegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="faf94-128">Opciones de creación de tablas.</span><span class="sxs-lookup"><span data-stu-id="faf94-128">Table creation options.</span></span>

<!-- end list -->

  - <span data-ttu-id="faf94-129">TABLEID</span><span class="sxs-lookup"><span data-stu-id="faf94-129">tableid</span></span>  
    <span data-ttu-id="faf94-130">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="faf94-130">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="faf94-131">Devuelve el ID. de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="faf94-131">Returns the tableid of the temporary table.</span></span> <span data-ttu-id="faf94-132">Al cerrar este TABLEID con [JetCloseTable (JET_SESID, JET_TABLEID),](./api.jetclosetable-method.md) se liberan los recursos asociados a la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="faf94-132">Closing this tableid with [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) frees the resources associated with the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="faf94-133">columnids</span><span class="sxs-lookup"><span data-stu-id="faf94-133">columnids</span></span>  
    <span data-ttu-id="faf94-134">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="faf94-134">Type: \[\]</span></span>  
    
    <span data-ttu-id="faf94-135">Búfer de salida que recibe la matriz de identificadores de columna generados durante la creación de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="faf94-135">The output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span> <span data-ttu-id="faf94-136">Los identificadores de columna de esta matriz se corresponden exactamente con la matriz de entrada de definiciones de columna.</span><span class="sxs-lookup"><span data-stu-id="faf94-136">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="faf94-137">Como resultado, el tamaño de este búfer debe corresponder al tamaño de la matriz de entrada.</span><span class="sxs-lookup"><span data-stu-id="faf94-137">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

## <a name="see-also"></a><span data-ttu-id="faf94-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="faf94-138">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="faf94-139">Referencia</span><span class="sxs-lookup"><span data-stu-id="faf94-139">Reference</span></span>

[<span data-ttu-id="faf94-140">Clase de API</span><span class="sxs-lookup"><span data-stu-id="faf94-140">Api class</span></span>](./api-class.md)

[<span data-ttu-id="faf94-141">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="faf94-141">Api members</span></span>](./api-members.md)

[<span data-ttu-id="faf94-142">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="faf94-142">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
