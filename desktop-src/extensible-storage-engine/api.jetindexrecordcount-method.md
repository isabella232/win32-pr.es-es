---
description: 'Más información sobre: API. JetIndexRecordCount (método)'
title: Método API. JetIndexRecordCount
TOCTitle: 'JetIndexRecordCount method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetIndexRecordCount(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Int32@,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetindexrecordcount(v=EXCHG.10)
ms:contentKeyID: 55100758
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetIndexRecordCount
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetIndexRecordCount
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 429239ab7734a594fd2c5a3510650d8f410e94f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817595"
---
# <a name="apijetindexrecordcount-method"></a><span data-ttu-id="53b66-103">Método API. JetIndexRecordCount</span><span class="sxs-lookup"><span data-stu-id="53b66-103">Api.JetIndexRecordCount method</span></span>

<span data-ttu-id="53b66-104">Cuenta el número de entradas en el índice actual desde la posición actual hacia delante.</span><span class="sxs-lookup"><span data-stu-id="53b66-104">Counts the number of entries in the current index from the current position forward.</span></span> <span data-ttu-id="53b66-105">La posición actual se incluye en el recuento.</span><span class="sxs-lookup"><span data-stu-id="53b66-105">The current position is included in the count.</span></span> <span data-ttu-id="53b66-106">El recuento puede ser mayor que el número total de registros de la tabla si el índice actual está sobre una columna de varios valores y las instancias de la columna tienen varios valores.</span><span class="sxs-lookup"><span data-stu-id="53b66-106">The count can be greater than the total number of records in the table if the current index is over a multi-valued column and instances of the column have multiple-values.</span></span> <span data-ttu-id="53b66-107">Si la tabla está vacía, se devolverá 0 para el recuento.</span><span class="sxs-lookup"><span data-stu-id="53b66-107">If the table is empty, then 0 will be returned for the count.</span></span>

<span data-ttu-id="53b66-108">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="53b66-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="53b66-109">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="53b66-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="53b66-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53b66-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetIndexRecordCount ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef numRecords As Integer, _
    maxRecordsToCount As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim numRecords As Integer
Dim maxRecordsToCount As IntegerApi.JetIndexRecordCount(sesid, _
    tableid, numRecords, maxRecordsToCount)
```

``` csharp
public static void JetIndexRecordCount(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out int numRecords,
    int maxRecordsToCount
)
```

#### <a name="parameters"></a><span data-ttu-id="53b66-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="53b66-111">Parameters</span></span>

  - <span data-ttu-id="53b66-112">sesid</span><span class="sxs-lookup"><span data-stu-id="53b66-112">sesid</span></span>  
    <span data-ttu-id="53b66-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="53b66-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="53b66-114">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="53b66-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="53b66-115">TABLEID</span><span class="sxs-lookup"><span data-stu-id="53b66-115">tableid</span></span>  
    <span data-ttu-id="53b66-116">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="53b66-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="53b66-117">Cursor en el que se van a contar los registros.</span><span class="sxs-lookup"><span data-stu-id="53b66-117">The cursor to count the records in.</span></span>

<!-- end list -->

  - <span data-ttu-id="53b66-118">numRecords</span><span class="sxs-lookup"><span data-stu-id="53b66-118">numRecords</span></span>  
    <span data-ttu-id="53b66-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="53b66-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="53b66-120">Devuelve el número de registros.</span><span class="sxs-lookup"><span data-stu-id="53b66-120">Returns the number of records.</span></span>

<!-- end list -->

  - <span data-ttu-id="53b66-121">maxRecordsToCount</span><span class="sxs-lookup"><span data-stu-id="53b66-121">maxRecordsToCount</span></span>  
    <span data-ttu-id="53b66-122">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="53b66-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="53b66-123">Número máximo de registros que se van a contar.</span><span class="sxs-lookup"><span data-stu-id="53b66-123">The maximum number of records to count.</span></span> <span data-ttu-id="53b66-124">Un valor de 0 indica que el recuento es ilimitado.</span><span class="sxs-lookup"><span data-stu-id="53b66-124">A value of 0 indicates that the count is unlimited.</span></span>

## <a name="see-also"></a><span data-ttu-id="53b66-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="53b66-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="53b66-126">Referencia</span><span class="sxs-lookup"><span data-stu-id="53b66-126">Reference</span></span>

[<span data-ttu-id="53b66-127">Clase de API</span><span class="sxs-lookup"><span data-stu-id="53b66-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="53b66-128">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="53b66-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="53b66-129">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="53b66-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
