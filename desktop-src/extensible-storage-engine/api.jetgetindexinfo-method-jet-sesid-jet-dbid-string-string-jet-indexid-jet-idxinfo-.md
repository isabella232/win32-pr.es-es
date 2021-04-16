---
description: 'Más información sobre: método API. JetGetIndexInfo (JET_SESID, JET_DBID, cadena, cadena, JET_INDEXID, JET_IdxInfo)'
title: Método API. JetGetIndexInfo (JET_SESID, JET_DBID, cadena, cadena, JET_INDEXID, JET_IdxInfo)
TOCTitle: JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, JET_INDEXID, JET_IdxInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_INDEXID@,Microsoft.Isam.Esent.Interop.JET_IdxInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100772
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ac8a622f3b653885374888fa9fa6b2835ef8ede0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677315"
---
# <a name="apijetgetindexinfo-method-jet_sesid-jet_dbid-string-string-jet_indexid-jet_idxinfo"></a><span data-ttu-id="1f235-103">Método API. JetGetIndexInfo (JET_SESID, JET_DBID, cadena, cadena, JET_INDEXID, JET_IdxInfo)</span><span class="sxs-lookup"><span data-stu-id="1f235-103">Api.JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, JET_INDEXID, JET_IdxInfo)</span></span>

<span data-ttu-id="1f235-104">Recupera información acerca de los índices de una tabla.</span><span class="sxs-lookup"><span data-stu-id="1f235-104">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="1f235-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1f235-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1f235-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1f235-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1f235-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1f235-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetIndexInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    indexname As String, _
    <OutAttribute> ByRef result As JET_INDEXID, _
    infoLevel As JET_IdxInfo _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim indexname As String
Dim result As JET_INDEXID
Dim infoLevel As JET_IdxInfoApi.JetGetIndexInfo(sesid, dbid, _
    tablename, indexname, result, infoLevel)
```

``` csharp
public static void JetGetIndexInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string indexname,
    out JET_INDEXID result,
    JET_IdxInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="1f235-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1f235-108">Parameters</span></span>

  - <span data-ttu-id="1f235-109">sesid</span><span class="sxs-lookup"><span data-stu-id="1f235-109">sesid</span></span>  
    <span data-ttu-id="1f235-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1f235-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="1f235-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="1f235-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="1f235-112">dbid</span><span class="sxs-lookup"><span data-stu-id="1f235-112">dbid</span></span>  
    <span data-ttu-id="1f235-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1f235-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="1f235-114">Base de datos que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="1f235-114">The database to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="1f235-115">tablename</span><span class="sxs-lookup"><span data-stu-id="1f235-115">tablename</span></span>  
    <span data-ttu-id="1f235-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="1f235-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="1f235-117">Nombre de la tabla sobre la que se va a recuperar información de índice.</span><span class="sxs-lookup"><span data-stu-id="1f235-117">The name of the table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="1f235-118">IndexName</span><span class="sxs-lookup"><span data-stu-id="1f235-118">indexname</span></span>  
    <span data-ttu-id="1f235-119">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="1f235-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="1f235-120">Nombre del índice del que se va a recuperar información.</span><span class="sxs-lookup"><span data-stu-id="1f235-120">The name of the index to retrieve information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="1f235-121">resultado</span><span class="sxs-lookup"><span data-stu-id="1f235-121">result</span></span>  
    <span data-ttu-id="1f235-122">Tipo: [Microsoft.ISAM.esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="1f235-122">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span></span>  
    
    <span data-ttu-id="1f235-123">Se rellena con información acerca de los índices de la tabla.</span><span class="sxs-lookup"><span data-stu-id="1f235-123">Filled in with information about indexes on the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="1f235-124">infoLevel</span><span class="sxs-lookup"><span data-stu-id="1f235-124">infoLevel</span></span>  
    <span data-ttu-id="1f235-125">Tipo: [Microsoft.ISAM.esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="1f235-125">Type: [Microsoft.Isam.Esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="1f235-126">Tipo de información que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="1f235-126">The type of information to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="1f235-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="1f235-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1f235-128">Referencia</span><span class="sxs-lookup"><span data-stu-id="1f235-128">Reference</span></span>

[<span data-ttu-id="1f235-129">Clase de API</span><span class="sxs-lookup"><span data-stu-id="1f235-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="1f235-130">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="1f235-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="1f235-131">Sobrecarga JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="1f235-131">JetGetIndexInfo overload</span></span>](./api.jetgetindexinfo-method.md)

[<span data-ttu-id="1f235-132">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="1f235-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
