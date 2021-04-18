---
description: 'Más información sobre: API. JetCreateIndex (método)'
title: Método API. JetCreateIndex
TOCTitle: 'JetCreateIndex method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateIndex(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.CreateIndexGrbit,System.String,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreateindex(v=EXCHG.10)
ms:contentKeyID: 55100693
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateIndex
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateIndex
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a9b3549461324f396408bb7d370531907248e8c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715054"
---
# <a name="apijetcreateindex-method"></a><span data-ttu-id="3b484-103">Método API. JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="3b484-103">Api.JetCreateIndex method</span></span>

<span data-ttu-id="3b484-104">Crea un índice sobre los datos en una base de datos ESE.</span><span class="sxs-lookup"><span data-stu-id="3b484-104">Creates an index over data in an ESE database.</span></span> <span data-ttu-id="3b484-105">Un índice se puede usar para buscar datos específicos rápidamente.</span><span class="sxs-lookup"><span data-stu-id="3b484-105">An index can be used to locate specific data quickly.</span></span>

<span data-ttu-id="3b484-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3b484-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3b484-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3b484-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3b484-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b484-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateIndex ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexName As String, _
    grbit As CreateIndexGrbit, _
    keyDescription As String, _
    keyDescriptionLength As Integer, _
    density As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexName As String
Dim grbit As CreateIndexGrbit
Dim keyDescription As String
Dim keyDescriptionLength As Integer
Dim density As IntegerApi.JetCreateIndex(sesid, tableid, _
    indexName, grbit, keyDescription, _
    keyDescriptionLength, density)
```

``` csharp
public static void JetCreateIndex(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string indexName,
    CreateIndexGrbit grbit,
    string keyDescription,
    int keyDescriptionLength,
    int density
)
```

#### <a name="parameters"></a><span data-ttu-id="3b484-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b484-109">Parameters</span></span>

  - <span data-ttu-id="3b484-110">sesid</span><span class="sxs-lookup"><span data-stu-id="3b484-110">sesid</span></span>  
    <span data-ttu-id="3b484-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3b484-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="3b484-112">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="3b484-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="3b484-113">TABLEID</span><span class="sxs-lookup"><span data-stu-id="3b484-113">tableid</span></span>  
    <span data-ttu-id="3b484-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3b484-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="3b484-115">Tabla en la que se va a crear el índice.</span><span class="sxs-lookup"><span data-stu-id="3b484-115">The table to create the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="3b484-116">indexName</span><span class="sxs-lookup"><span data-stu-id="3b484-116">indexName</span></span>  
    <span data-ttu-id="3b484-117">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="3b484-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="3b484-118">Puntero a una cadena terminada en null que especifica el nombre del índice que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="3b484-118">Pointer to a null-terminated string that specifies the name of the index to create.</span></span>

<!-- end list -->

  - <span data-ttu-id="3b484-119">grbit</span><span class="sxs-lookup"><span data-stu-id="3b484-119">grbit</span></span>  
    <span data-ttu-id="3b484-120">Tipo: [Microsoft. ISAM. esent. Interop. CreateIndexGrbit](./createindexgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="3b484-120">Type: [Microsoft.Isam.Esent.Interop.CreateIndexGrbit](./createindexgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="3b484-121">Opciones de creación de índices.</span><span class="sxs-lookup"><span data-stu-id="3b484-121">Index creation options.</span></span>

<!-- end list -->

  - <span data-ttu-id="3b484-122">keyDescription</span><span class="sxs-lookup"><span data-stu-id="3b484-122">keyDescription</span></span>  
    <span data-ttu-id="3b484-123">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="3b484-123">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="3b484-124">Puntero a una cadena doble terminada en NULL de tokens delimitados por null.</span><span class="sxs-lookup"><span data-stu-id="3b484-124">Pointer to a double null-terminated string of null-delimited tokens.</span></span>

<!-- end list -->

  - <span data-ttu-id="3b484-125">keyDescriptionLength</span><span class="sxs-lookup"><span data-stu-id="3b484-125">keyDescriptionLength</span></span>  
    <span data-ttu-id="3b484-126">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="3b484-126">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="3b484-127">La longitud, en caracteres, de szKey, incluidos los dos valores NULL de terminación.</span><span class="sxs-lookup"><span data-stu-id="3b484-127">The length, in characters, of szKey including the two terminating nulls.</span></span>

<!-- end list -->

  - <span data-ttu-id="3b484-128">densidad</span><span class="sxs-lookup"><span data-stu-id="3b484-128">density</span></span>  
    <span data-ttu-id="3b484-129">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="3b484-129">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="3b484-130">Densidad de árbol B + inicial.</span><span class="sxs-lookup"><span data-stu-id="3b484-130">Initial B+ tree density.</span></span>

## <a name="see-also"></a><span data-ttu-id="3b484-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b484-131">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3b484-132">Referencia</span><span class="sxs-lookup"><span data-stu-id="3b484-132">Reference</span></span>

[<span data-ttu-id="3b484-133">Clase de API</span><span class="sxs-lookup"><span data-stu-id="3b484-133">Api class</span></span>](./api-class.md)

[<span data-ttu-id="3b484-134">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="3b484-134">Api members</span></span>](./api-members.md)

[<span data-ttu-id="3b484-135">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="3b484-135">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
