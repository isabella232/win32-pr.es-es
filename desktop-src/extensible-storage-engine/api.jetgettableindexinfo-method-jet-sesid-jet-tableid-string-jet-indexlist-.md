---
description: 'Más información sobre: método API. JetGetTableIndexInfo (JET_SESID, JET_TABLEID, cadena, JET_INDEXLIST)'
title: Método API. JetGetTableIndexInfo (JET_SESID, JET_TABLEID, cadena, JET_INDEXLIST)
TOCTitle: JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, JET_INDEXLIST)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.JET_INDEXLIST@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100752
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
ms.openlocfilehash: 5a39fba54463f7a55fd6a8521f5c905da4afb4e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275742"
---
# <a name="apijetgettableindexinfo-method-jet_sesid-jet_tableid-string-jet_indexlist"></a><span data-ttu-id="dfff3-103">Método API. JetGetTableIndexInfo (JET_SESID, JET_TABLEID, cadena, JET_INDEXLIST)</span><span class="sxs-lookup"><span data-stu-id="dfff3-103">Api.JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, JET_INDEXLIST)</span></span>

<span data-ttu-id="dfff3-104">**Nota: esta API ya está obsoleta.**</span><span class="sxs-lookup"><span data-stu-id="dfff3-104">**NOTE: This API is now obsolete.**</span></span>

<span data-ttu-id="dfff3-105">Recupera información acerca de los índices de una tabla.</span><span class="sxs-lookup"><span data-stu-id="dfff3-105">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="dfff3-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="dfff3-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="dfff3-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="dfff3-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="dfff3-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dfff3-108">Syntax</span></span>

``` vb
'Declaration
<ObsoleteAttribute("Use the overload that takes a JET_IdxInfo parameter, passing in JET_IdxInfo.List")> _
Public Shared Sub JetGetTableIndexInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexname As String, _
    <OutAttribute> ByRef indexlist As JET_INDEXLIST _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexname As String
Dim indexlist As JET_INDEXLISTApi.JetGetTableIndexInfo(sesid, _
    tableid, indexname, indexlist)
```

``` csharp
[ObsoleteAttribute("Use the overload that takes a JET_IdxInfo parameter, passing in JET_IdxInfo.List")]
public static void JetGetTableIndexInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string indexname,
    out JET_INDEXLIST indexlist
)
```

#### <a name="parameters"></a><span data-ttu-id="dfff3-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dfff3-109">Parameters</span></span>

  - <span data-ttu-id="dfff3-110">sesid</span><span class="sxs-lookup"><span data-stu-id="dfff3-110">sesid</span></span>  
    <span data-ttu-id="dfff3-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="dfff3-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="dfff3-112">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="dfff3-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="dfff3-113">TABLEID</span><span class="sxs-lookup"><span data-stu-id="dfff3-113">tableid</span></span>  
    <span data-ttu-id="dfff3-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="dfff3-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="dfff3-115">Tabla de la que se va a recuperar información de índice.</span><span class="sxs-lookup"><span data-stu-id="dfff3-115">The table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="dfff3-116">IndexName</span><span class="sxs-lookup"><span data-stu-id="dfff3-116">indexname</span></span>  
    <span data-ttu-id="dfff3-117">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="dfff3-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="dfff3-118">Este parámetro se ignora.</span><span class="sxs-lookup"><span data-stu-id="dfff3-118">This parameter is ignored.</span></span>

<!-- end list -->

  - <span data-ttu-id="dfff3-119">indexlist</span><span class="sxs-lookup"><span data-stu-id="dfff3-119">indexlist</span></span>  
    <span data-ttu-id="dfff3-120">Tipo: [Microsoft.ISAM.esent.Interop.JET_INDEXLIST](./jet-indexlist-class.md)</span><span class="sxs-lookup"><span data-stu-id="dfff3-120">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXLIST](./jet-indexlist-class.md)</span></span>  
    
    <span data-ttu-id="dfff3-121">Se rellena con información acerca de los índices de la tabla.</span><span class="sxs-lookup"><span data-stu-id="dfff3-121">Filled in with information about indexes on the table.</span></span>

## <a name="see-also"></a><span data-ttu-id="dfff3-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="dfff3-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="dfff3-123">Referencia</span><span class="sxs-lookup"><span data-stu-id="dfff3-123">Reference</span></span>

[<span data-ttu-id="dfff3-124">Clase de API</span><span class="sxs-lookup"><span data-stu-id="dfff3-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="dfff3-125">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="dfff3-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="dfff3-126">Sobrecarga JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="dfff3-126">JetGetTableIndexInfo overload</span></span>](./api.jetgettableindexinfo-method.md)

[<span data-ttu-id="dfff3-127">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="dfff3-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
