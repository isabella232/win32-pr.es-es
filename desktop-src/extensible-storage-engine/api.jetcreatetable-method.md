---
description: 'Más información sobre: API. JetCreateTable (método)'
title: Método API. JetCreateTable
TOCTitle: 'JetCreateTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.Int32,System.Int32,Microsoft.Isam.Esent.Interop.JET_TABLEID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreatetable(v=EXCHG.10)
ms:contentKeyID: 55100676
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateTable
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8025e35746d921fda3b601d289a9b361aefefb83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497158"
---
# <a name="apijetcreatetable-method"></a><span data-ttu-id="c4641-103">Método API. JetCreateTable</span><span class="sxs-lookup"><span data-stu-id="c4641-103">Api.JetCreateTable method</span></span>

<span data-ttu-id="c4641-104">Cree una tabla vacía.</span><span class="sxs-lookup"><span data-stu-id="c4641-104">Create an empty table.</span></span> <span data-ttu-id="c4641-105">La tabla recién creada se abre exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="c4641-105">The newly created table is opened exclusively.</span></span>

<span data-ttu-id="c4641-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c4641-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c4641-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c4641-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c4641-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c4641-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateTable ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    table As String, _
    pages As Integer, _
    density As Integer, _
    <OutAttribute> ByRef tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim table As String
Dim pages As Integer
Dim density As Integer
Dim tableid As JET_TABLEIDApi.JetCreateTable(sesid, dbid, _
    table, pages, density, tableid)
```

``` csharp
public static void JetCreateTable(
    JET_SESID sesid,
    JET_DBID dbid,
    string table,
    int pages,
    int density,
    out JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="c4641-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c4641-109">Parameters</span></span>

  - <span data-ttu-id="c4641-110">sesid</span><span class="sxs-lookup"><span data-stu-id="c4641-110">sesid</span></span>  
    <span data-ttu-id="c4641-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c4641-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c4641-112">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="c4641-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c4641-113">dbid</span><span class="sxs-lookup"><span data-stu-id="c4641-113">dbid</span></span>  
    <span data-ttu-id="c4641-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c4641-114">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="c4641-115">Base de datos en la que se va a crear la tabla.</span><span class="sxs-lookup"><span data-stu-id="c4641-115">The database to create the table in.</span></span>

<!-- end list -->

  - <span data-ttu-id="c4641-116">table</span><span class="sxs-lookup"><span data-stu-id="c4641-116">table</span></span>  
    <span data-ttu-id="c4641-117">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="c4641-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="c4641-118">El objeto de la tabla que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="c4641-118">The name of the table to create.</span></span>

<!-- end list -->

  - <span data-ttu-id="c4641-119">páginas</span><span class="sxs-lookup"><span data-stu-id="c4641-119">pages</span></span>  
    <span data-ttu-id="c4641-120">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="c4641-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="c4641-121">Número inicial de páginas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="c4641-121">Initial number of pages in the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="c4641-122">densidad</span><span class="sxs-lookup"><span data-stu-id="c4641-122">density</span></span>  
    <span data-ttu-id="c4641-123">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="c4641-123">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="c4641-124">Densidad predeterminada de la tabla.</span><span class="sxs-lookup"><span data-stu-id="c4641-124">The default density of the table.</span></span> <span data-ttu-id="c4641-125">Se usa al realizar inserciones secuenciales.</span><span class="sxs-lookup"><span data-stu-id="c4641-125">This is used when doing sequential inserts.</span></span>

<!-- end list -->

  - <span data-ttu-id="c4641-126">TABLEID</span><span class="sxs-lookup"><span data-stu-id="c4641-126">tableid</span></span>  
    <span data-ttu-id="c4641-127">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c4641-127">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="c4641-128">Devuelve el ID. de la nueva tabla.</span><span class="sxs-lookup"><span data-stu-id="c4641-128">Returns the tableid of the new table.</span></span>

## <a name="see-also"></a><span data-ttu-id="c4641-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="c4641-129">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c4641-130">Referencia</span><span class="sxs-lookup"><span data-stu-id="c4641-130">Reference</span></span>

[<span data-ttu-id="c4641-131">Clase de API</span><span class="sxs-lookup"><span data-stu-id="c4641-131">Api class</span></span>](./api-class.md)

[<span data-ttu-id="c4641-132">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="c4641-132">Api members</span></span>](./api-members.md)

[<span data-ttu-id="c4641-133">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c4641-133">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
