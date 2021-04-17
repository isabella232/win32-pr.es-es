---
description: 'Más información sobre: método API. JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String, UInt16, JET_IdxInfo)'
title: Método API. JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String, UInt16, JET_IdxInfo)
TOCTitle: JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, UInt16, JET_IdxInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,System.UInt16@,Microsoft.Isam.Esent.Interop.JET_IdxInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100747
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
ms.openlocfilehash: 5a5e1f5e6908f33d211c5a32a3b9d34e55098101
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716758"
---
# <a name="apijetgettableindexinfo-method-jet_sesid-jet_tableid-string-uint16-jet_idxinfo"></a><span data-ttu-id="46352-103">Método API. JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String, UInt16, JET_IdxInfo)</span><span class="sxs-lookup"><span data-stu-id="46352-103">Api.JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, UInt16, JET_IdxInfo)</span></span>

<span data-ttu-id="46352-104">Recupera información acerca de los índices de una tabla.</span><span class="sxs-lookup"><span data-stu-id="46352-104">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="46352-105">Esta API no es conforme a CLS.</span><span class="sxs-lookup"><span data-stu-id="46352-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="46352-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="46352-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="46352-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="46352-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="46352-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46352-108">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Sub JetGetTableIndexInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexname As String, _
    <OutAttribute> ByRef result As UShort, _
    infoLevel As JET_IdxInfo _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexname As String
Dim result As UShort
Dim infoLevel As JET_IdxInfoApi.JetGetTableIndexInfo(sesid, _
    tableid, indexname, result, infoLevel)
```

``` csharp
[CLSCompliantAttribute(false)]
public static void JetGetTableIndexInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string indexname,
    out ushort result,
    JET_IdxInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="46352-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46352-109">Parameters</span></span>

  - <span data-ttu-id="46352-110">sesid</span><span class="sxs-lookup"><span data-stu-id="46352-110">sesid</span></span>  
    <span data-ttu-id="46352-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="46352-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="46352-112">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="46352-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="46352-113">TABLEID</span><span class="sxs-lookup"><span data-stu-id="46352-113">tableid</span></span>  
    <span data-ttu-id="46352-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="46352-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="46352-115">Tabla de la que se va a recuperar información de índice.</span><span class="sxs-lookup"><span data-stu-id="46352-115">The table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="46352-116">IndexName</span><span class="sxs-lookup"><span data-stu-id="46352-116">indexname</span></span>  
    <span data-ttu-id="46352-117">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="46352-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="46352-118">El nombre del índice.</span><span class="sxs-lookup"><span data-stu-id="46352-118">The name of the index.</span></span>

<!-- end list -->

  - <span data-ttu-id="46352-119">resultado</span><span class="sxs-lookup"><span data-stu-id="46352-119">result</span></span>  
    <span data-ttu-id="46352-120">Tipo: [System. UInt16](/dotnet/api/system.uint16)</span><span class="sxs-lookup"><span data-stu-id="46352-120">Type: [System.UInt16](/dotnet/api/system.uint16)</span></span>  
    
    <span data-ttu-id="46352-121">Se rellena con información acerca de los índices de la tabla.</span><span class="sxs-lookup"><span data-stu-id="46352-121">Filled in with information about indexes on the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="46352-122">infoLevel</span><span class="sxs-lookup"><span data-stu-id="46352-122">infoLevel</span></span>  
    <span data-ttu-id="46352-123">Tipo: [Microsoft.ISAM.esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="46352-123">Type: [Microsoft.Isam.Esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="46352-124">Tipo de información que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="46352-124">The type of information to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="46352-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="46352-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="46352-126">Referencia</span><span class="sxs-lookup"><span data-stu-id="46352-126">Reference</span></span>

[<span data-ttu-id="46352-127">Clase de API</span><span class="sxs-lookup"><span data-stu-id="46352-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="46352-128">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="46352-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="46352-129">Sobrecarga JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="46352-129">JetGetTableIndexInfo overload</span></span>](./api.jetgettableindexinfo-method.md)

[<span data-ttu-id="46352-130">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="46352-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
