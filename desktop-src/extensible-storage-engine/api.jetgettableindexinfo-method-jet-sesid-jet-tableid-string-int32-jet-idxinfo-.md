---
description: 'Más información sobre: método API. JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String, Int32, JET_IdxInfo)'
title: Método API. JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String, Int32, JET_IdxInfo)
TOCTitle: JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, Int32, JET_IdxInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,System.Int32@,Microsoft.Isam.Esent.Interop.JET_IdxInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100742
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableIndexInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bc9c3432e34f36d13b2a12880118f2b5c36a8ade
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001372"
---
# <a name="apijetgettableindexinfo-method-jet_sesid-jet_tableid-string-int32-jet_idxinfo"></a><span data-ttu-id="e9b5c-103">Método API. JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String, Int32, JET_IdxInfo)</span><span class="sxs-lookup"><span data-stu-id="e9b5c-103">Api.JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, Int32, JET_IdxInfo)</span></span>

<span data-ttu-id="e9b5c-104">Recupera información acerca de los índices de una tabla.</span><span class="sxs-lookup"><span data-stu-id="e9b5c-104">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="e9b5c-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e9b5c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e9b5c-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e9b5c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e9b5c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e9b5c-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTableIndexInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexname As String, _
    <OutAttribute> ByRef result As Integer, _
    infoLevel As JET_IdxInfo _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexname As String
Dim result As Integer
Dim infoLevel As JET_IdxInfoApi.JetGetTableIndexInfo(sesid, _
    tableid, indexname, result, infoLevel)
```

``` csharp
public static void JetGetTableIndexInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string indexname,
    out int result,
    JET_IdxInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="e9b5c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e9b5c-108">Parameters</span></span>

  - <span data-ttu-id="e9b5c-109">sesid</span><span class="sxs-lookup"><span data-stu-id="e9b5c-109">sesid</span></span>  
    <span data-ttu-id="e9b5c-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e9b5c-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e9b5c-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="e9b5c-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="e9b5c-112">TABLEID</span><span class="sxs-lookup"><span data-stu-id="e9b5c-112">tableid</span></span>  
    <span data-ttu-id="e9b5c-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e9b5c-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e9b5c-114">Tabla de la que se va a recuperar información de índice.</span><span class="sxs-lookup"><span data-stu-id="e9b5c-114">The table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="e9b5c-115">IndexName</span><span class="sxs-lookup"><span data-stu-id="e9b5c-115">indexname</span></span>  
    <span data-ttu-id="e9b5c-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="e9b5c-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="e9b5c-117">El nombre del índice.</span><span class="sxs-lookup"><span data-stu-id="e9b5c-117">The name of the index.</span></span>

<!-- end list -->

  - <span data-ttu-id="e9b5c-118">resultado</span><span class="sxs-lookup"><span data-stu-id="e9b5c-118">result</span></span>  
    <span data-ttu-id="e9b5c-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e9b5c-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="e9b5c-120">Se rellena con información acerca de los índices de la tabla.</span><span class="sxs-lookup"><span data-stu-id="e9b5c-120">Filled in with information about indexes on the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="e9b5c-121">infoLevel</span><span class="sxs-lookup"><span data-stu-id="e9b5c-121">infoLevel</span></span>  
    <span data-ttu-id="e9b5c-122">Tipo: [Microsoft.ISAM.esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e9b5c-122">Type: [Microsoft.Isam.Esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="e9b5c-123">Tipo de información que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="e9b5c-123">The type of information to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="e9b5c-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="e9b5c-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e9b5c-125">Referencia</span><span class="sxs-lookup"><span data-stu-id="e9b5c-125">Reference</span></span>

[<span data-ttu-id="e9b5c-126">Clase de API</span><span class="sxs-lookup"><span data-stu-id="e9b5c-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="e9b5c-127">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="e9b5c-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="e9b5c-128">Sobrecarga JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="e9b5c-128">JetGetTableIndexInfo overload</span></span>](./api.jetgettableindexinfo-method.md)

[<span data-ttu-id="e9b5c-129">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e9b5c-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
