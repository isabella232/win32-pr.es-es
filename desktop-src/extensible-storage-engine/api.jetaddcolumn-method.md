---
description: 'Más información sobre: API. JetAddColumn (método)'
title: Método API. JetAddColumn
TOCTitle: 'JetAddColumn method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetAddColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.JET_COLUMNID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetaddcolumn(v=EXCHG.10)
ms:contentKeyID: 55100651
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetAddColumn
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetAddColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a864bab9c3b888622640e6226c3e7ee542a096d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705521"
---
# <a name="apijetaddcolumn-method"></a><span data-ttu-id="69fb5-103">Método API. JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="69fb5-103">Api.JetAddColumn method</span></span>

<span data-ttu-id="69fb5-104">Agregue una nueva columna a una tabla existente.</span><span class="sxs-lookup"><span data-stu-id="69fb5-104">Add a new column to an existing table.</span></span>

<span data-ttu-id="69fb5-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="69fb5-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="69fb5-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="69fb5-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="69fb5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69fb5-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetAddColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    column As String, _
    columndef As JET_COLUMNDEF, _
    defaultValue As Byte(), _
    defaultValueSize As Integer, _
    <OutAttribute> ByRef columnid As JET_COLUMNID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim column As String
Dim columndef As JET_COLUMNDEF
Dim defaultValue As Byte()
Dim defaultValueSize As Integer
Dim columnid As JET_COLUMNIDApi.JetAddColumn(sesid, tableid, _
    column, columndef, defaultValue, _
    defaultValueSize, columnid)
```

``` csharp
public static void JetAddColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string column,
    JET_COLUMNDEF columndef,
    byte[] defaultValue,
    int defaultValueSize,
    out JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="69fb5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69fb5-108">Parameters</span></span>

  - <span data-ttu-id="69fb5-109">sesid</span><span class="sxs-lookup"><span data-stu-id="69fb5-109">sesid</span></span>  
    <span data-ttu-id="69fb5-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="69fb5-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="69fb5-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="69fb5-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="69fb5-112">TABLEID</span><span class="sxs-lookup"><span data-stu-id="69fb5-112">tableid</span></span>  
    <span data-ttu-id="69fb5-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="69fb5-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="69fb5-114">Tabla a la que se va a agregar la columna.</span><span class="sxs-lookup"><span data-stu-id="69fb5-114">The table to add the column to.</span></span>

<!-- end list -->

  - <span data-ttu-id="69fb5-115">columna</span><span class="sxs-lookup"><span data-stu-id="69fb5-115">column</span></span>  
    <span data-ttu-id="69fb5-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="69fb5-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="69fb5-117">El nombre de la columna.</span><span class="sxs-lookup"><span data-stu-id="69fb5-117">The name of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="69fb5-118">columndef</span><span class="sxs-lookup"><span data-stu-id="69fb5-118">columndef</span></span>  
    <span data-ttu-id="69fb5-119">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span><span class="sxs-lookup"><span data-stu-id="69fb5-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span></span>  
    
    <span data-ttu-id="69fb5-120">Definición de la columna.</span><span class="sxs-lookup"><span data-stu-id="69fb5-120">The definition of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="69fb5-121">defaultValue</span><span class="sxs-lookup"><span data-stu-id="69fb5-121">defaultValue</span></span>  
    <span data-ttu-id="69fb5-122">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="69fb5-122">Type: \[\]</span></span>  
    
    <span data-ttu-id="69fb5-123">Valor predeterminado de la columna.</span><span class="sxs-lookup"><span data-stu-id="69fb5-123">The default value of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="69fb5-124">defaultValueSize</span><span class="sxs-lookup"><span data-stu-id="69fb5-124">defaultValueSize</span></span>  
    <span data-ttu-id="69fb5-125">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="69fb5-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="69fb5-126">Tamaño del valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="69fb5-126">The size of the default value.</span></span>

<!-- end list -->

  - <span data-ttu-id="69fb5-127">columnid</span><span class="sxs-lookup"><span data-stu-id="69fb5-127">columnid</span></span>  
    <span data-ttu-id="69fb5-128">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="69fb5-128">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="69fb5-129">Devuelve el columnid de la nueva columna.</span><span class="sxs-lookup"><span data-stu-id="69fb5-129">Returns the columnid of the new column.</span></span>

## <a name="see-also"></a><span data-ttu-id="69fb5-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="69fb5-130">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="69fb5-131">Referencia</span><span class="sxs-lookup"><span data-stu-id="69fb5-131">Reference</span></span>

[<span data-ttu-id="69fb5-132">Clase de API</span><span class="sxs-lookup"><span data-stu-id="69fb5-132">Api class</span></span>](./api-class.md)

[<span data-ttu-id="69fb5-133">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="69fb5-133">Api members</span></span>](./api-members.md)

[<span data-ttu-id="69fb5-134">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="69fb5-134">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
