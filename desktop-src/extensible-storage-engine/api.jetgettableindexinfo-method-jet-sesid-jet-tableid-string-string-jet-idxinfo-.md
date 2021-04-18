---
description: 'Más información sobre: método API. JetGetTableIndexInfo (JET_SESID, JET_TABLEID, cadena, cadena JET_IdxInfo)'
title: Método API. JetGetTableIndexInfo (JET_SESID, JET_TABLEID, cadena, cadena, JET_IdxInfo)
TOCTitle: JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, String, JET_IdxInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,System.String@,Microsoft.Isam.Esent.Interop.JET_IdxInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100750
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableIndexInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 62291587ca1c07da74c2b646870751f3b8af981b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715433"
---
# <a name="apijetgettableindexinfo-method-jet_sesid-jet_tableid-string-string-jet_idxinfo"></a><span data-ttu-id="66ac1-103">Método API. JetGetTableIndexInfo (JET_SESID, JET_TABLEID, cadena, cadena, JET_IdxInfo)</span><span class="sxs-lookup"><span data-stu-id="66ac1-103">Api.JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, String, JET_IdxInfo)</span></span>

<span data-ttu-id="66ac1-104">Recupera información acerca de los índices de una tabla.</span><span class="sxs-lookup"><span data-stu-id="66ac1-104">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="66ac1-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="66ac1-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="66ac1-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="66ac1-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="66ac1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="66ac1-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTableIndexInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexname As String, _
    <OutAttribute> ByRef result As String, _
    infoLevel As JET_IdxInfo _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexname As String
Dim result As String
Dim infoLevel As JET_IdxInfoApi.JetGetTableIndexInfo(sesid, _
    tableid, indexname, result, infoLevel)
```

``` csharp
public static void JetGetTableIndexInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string indexname,
    out string result,
    JET_IdxInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="66ac1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="66ac1-108">Parameters</span></span>

  - <span data-ttu-id="66ac1-109">sesid</span><span class="sxs-lookup"><span data-stu-id="66ac1-109">sesid</span></span>  
    <span data-ttu-id="66ac1-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="66ac1-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="66ac1-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="66ac1-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="66ac1-112">TABLEID</span><span class="sxs-lookup"><span data-stu-id="66ac1-112">tableid</span></span>  
    <span data-ttu-id="66ac1-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="66ac1-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="66ac1-114">Tabla de la que se va a recuperar información de índice.</span><span class="sxs-lookup"><span data-stu-id="66ac1-114">The table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="66ac1-115">IndexName</span><span class="sxs-lookup"><span data-stu-id="66ac1-115">indexname</span></span>  
    <span data-ttu-id="66ac1-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="66ac1-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="66ac1-117">El nombre del índice.</span><span class="sxs-lookup"><span data-stu-id="66ac1-117">The name of the index.</span></span>

<!-- end list -->

  - <span data-ttu-id="66ac1-118">resultado</span><span class="sxs-lookup"><span data-stu-id="66ac1-118">result</span></span>  
    <span data-ttu-id="66ac1-119">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="66ac1-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="66ac1-120">Se rellena con información acerca de los índices de la tabla.</span><span class="sxs-lookup"><span data-stu-id="66ac1-120">Filled in with information about indexes on the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="66ac1-121">infoLevel</span><span class="sxs-lookup"><span data-stu-id="66ac1-121">infoLevel</span></span>  
    <span data-ttu-id="66ac1-122">Tipo: [Microsoft.ISAM.esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="66ac1-122">Type: [Microsoft.Isam.Esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="66ac1-123">Tipo de información que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="66ac1-123">The type of information to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="66ac1-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="66ac1-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="66ac1-125">Referencia</span><span class="sxs-lookup"><span data-stu-id="66ac1-125">Reference</span></span>

[<span data-ttu-id="66ac1-126">Clase de API</span><span class="sxs-lookup"><span data-stu-id="66ac1-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="66ac1-127">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="66ac1-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="66ac1-128">Sobrecarga JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="66ac1-128">JetGetTableIndexInfo overload</span></span>](./api.jetgettableindexinfo-method.md)

[<span data-ttu-id="66ac1-129">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="66ac1-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
