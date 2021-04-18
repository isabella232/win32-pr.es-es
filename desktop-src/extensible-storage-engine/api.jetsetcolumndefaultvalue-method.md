---
description: 'Más información sobre: API. JetSetColumnDefaultValue (método)'
title: Método API. JetSetColumnDefaultValue
TOCTitle: 'JetSetColumnDefaultValue method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetColumnDefaultValue(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.SetColumnDefaultValueGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcolumndefaultvalue(v=EXCHG.10)
ms:contentKeyID: 55100802
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumnDefaultValue
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumnDefaultValue
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 24fdb3a885e7aa558e1b3db3c4014fc65a28fcde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707339"
---
# <a name="apijetsetcolumndefaultvalue-method"></a><span data-ttu-id="4e2be-103">Método API. JetSetColumnDefaultValue</span><span class="sxs-lookup"><span data-stu-id="4e2be-103">Api.JetSetColumnDefaultValue method</span></span>

<span data-ttu-id="4e2be-104">Cambia el valor predeterminado de una columna existente.</span><span class="sxs-lookup"><span data-stu-id="4e2be-104">Changes the default value of an existing column.</span></span>

<span data-ttu-id="4e2be-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4e2be-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4e2be-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4e2be-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4e2be-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e2be-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetColumnDefaultValue ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableName As String, _
    columnName As String, _
    data As Byte(), _
    dataSize As Integer, _
    grbit As SetColumnDefaultValueGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tableName As String
Dim columnName As String
Dim data As Byte()
Dim dataSize As Integer
Dim grbit As SetColumnDefaultValueGrbitApi.JetSetColumnDefaultValue(sesid, _
    dbid, tableName, columnName, data, _
    dataSize, grbit)
```

``` csharp
public static void JetSetColumnDefaultValue(
    JET_SESID sesid,
    JET_DBID dbid,
    string tableName,
    string columnName,
    byte[] data,
    int dataSize,
    SetColumnDefaultValueGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="4e2be-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4e2be-108">Parameters</span></span>

  - <span data-ttu-id="4e2be-109">sesid</span><span class="sxs-lookup"><span data-stu-id="4e2be-109">sesid</span></span>  
    <span data-ttu-id="4e2be-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4e2be-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="4e2be-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="4e2be-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="4e2be-112">dbid</span><span class="sxs-lookup"><span data-stu-id="4e2be-112">dbid</span></span>  
    <span data-ttu-id="4e2be-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4e2be-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="4e2be-114">Base de datos que contiene la columna.</span><span class="sxs-lookup"><span data-stu-id="4e2be-114">The database containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="4e2be-115">tableName</span><span class="sxs-lookup"><span data-stu-id="4e2be-115">tableName</span></span>  
    <span data-ttu-id="4e2be-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="4e2be-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="4e2be-117">Nombre de la tabla que contiene la columna.</span><span class="sxs-lookup"><span data-stu-id="4e2be-117">The name of the table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="4e2be-118">columnName</span><span class="sxs-lookup"><span data-stu-id="4e2be-118">columnName</span></span>  
    <span data-ttu-id="4e2be-119">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="4e2be-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="4e2be-120">El nombre de la columna.</span><span class="sxs-lookup"><span data-stu-id="4e2be-120">The name of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="4e2be-121">datos</span><span class="sxs-lookup"><span data-stu-id="4e2be-121">data</span></span>  
    <span data-ttu-id="4e2be-122">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="4e2be-122">Type: \[\]</span></span>  
    
    <span data-ttu-id="4e2be-123">Nuevo valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4e2be-123">The new default value.</span></span>

<!-- end list -->

  - <span data-ttu-id="4e2be-124">dataSize</span><span class="sxs-lookup"><span data-stu-id="4e2be-124">dataSize</span></span>  
    <span data-ttu-id="4e2be-125">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4e2be-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="4e2be-126">Tamaño del nuevo valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4e2be-126">Size of the new default value.</span></span>

<!-- end list -->

  - <span data-ttu-id="4e2be-127">grbit</span><span class="sxs-lookup"><span data-stu-id="4e2be-127">grbit</span></span>  
    <span data-ttu-id="4e2be-128">Tipo: [Microsoft. ISAM. esent. Interop. SetColumnDefaultValueGrbit](./setcolumndefaultvaluegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="4e2be-128">Type: [Microsoft.Isam.Esent.Interop.SetColumnDefaultValueGrbit](./setcolumndefaultvaluegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="4e2be-129">Opciones de valor predeterminado de columna.</span><span class="sxs-lookup"><span data-stu-id="4e2be-129">Column default value options.</span></span>

## <a name="see-also"></a><span data-ttu-id="4e2be-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e2be-130">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4e2be-131">Referencia</span><span class="sxs-lookup"><span data-stu-id="4e2be-131">Reference</span></span>

[<span data-ttu-id="4e2be-132">Clase de API</span><span class="sxs-lookup"><span data-stu-id="4e2be-132">Api class</span></span>](./api-class.md)

[<span data-ttu-id="4e2be-133">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="4e2be-133">Api members</span></span>](./api-members.md)

[<span data-ttu-id="4e2be-134">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="4e2be-134">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
