---
description: 'Más información sobre: método API. JetGetIndexInfo (JET_SESID, JET_DBID, cadena, cadena JET_INDEXLIST)'
title: Método API. JetGetIndexInfo (JET_SESID, JET_DBID, cadena, cadena, JET_INDEXLIST)
TOCTitle: JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, JET_INDEXLIST)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_INDEXLIST@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100770
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
ms.openlocfilehash: 2320b72a90ff97326c027b00cfeb5bf38453f68c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677313"
---
# <a name="apijetgetindexinfo-method-jet_sesid-jet_dbid-string-string-jet_indexlist"></a><span data-ttu-id="23a69-103">Método API. JetGetIndexInfo (JET_SESID, JET_DBID, cadena, cadena, JET_INDEXLIST)</span><span class="sxs-lookup"><span data-stu-id="23a69-103">Api.JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, JET_INDEXLIST)</span></span>

<span data-ttu-id="23a69-104">**Nota: esta API ya está obsoleta.**</span><span class="sxs-lookup"><span data-stu-id="23a69-104">**NOTE: This API is now obsolete.**</span></span>

<span data-ttu-id="23a69-105">Recupera información acerca de los índices de una tabla.</span><span class="sxs-lookup"><span data-stu-id="23a69-105">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="23a69-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="23a69-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="23a69-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="23a69-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="23a69-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="23a69-108">Syntax</span></span>

``` vb
'Declaration
<ObsoleteAttribute("Use the overload that takes a JET_IdxInfo parameter, passing in JET_IdxInfo.List")> _
Public Shared Sub JetGetIndexInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    ignored As String, _
    <OutAttribute> ByRef indexlist As JET_INDEXLIST _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim ignored As String
Dim indexlist As JET_INDEXLISTApi.JetGetIndexInfo(sesid, dbid, _
    tablename, ignored, indexlist)
```

``` csharp
[ObsoleteAttribute("Use the overload that takes a JET_IdxInfo parameter, passing in JET_IdxInfo.List")]
public static void JetGetIndexInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string ignored,
    out JET_INDEXLIST indexlist
)
```

#### <a name="parameters"></a><span data-ttu-id="23a69-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="23a69-109">Parameters</span></span>

  - <span data-ttu-id="23a69-110">sesid</span><span class="sxs-lookup"><span data-stu-id="23a69-110">sesid</span></span>  
    <span data-ttu-id="23a69-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="23a69-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="23a69-112">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="23a69-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="23a69-113">dbid</span><span class="sxs-lookup"><span data-stu-id="23a69-113">dbid</span></span>  
    <span data-ttu-id="23a69-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="23a69-114">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="23a69-115">Base de datos que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="23a69-115">The database to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="23a69-116">tablename</span><span class="sxs-lookup"><span data-stu-id="23a69-116">tablename</span></span>  
    <span data-ttu-id="23a69-117">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="23a69-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="23a69-118">Nombre de la tabla sobre la que se va a recuperar información de índice.</span><span class="sxs-lookup"><span data-stu-id="23a69-118">The name of the table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="23a69-119">no se tiene en cuenta</span><span class="sxs-lookup"><span data-stu-id="23a69-119">ignored</span></span>  
    <span data-ttu-id="23a69-120">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="23a69-120">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="23a69-121">Este parámetro se ignora.</span><span class="sxs-lookup"><span data-stu-id="23a69-121">This parameter is ignored.</span></span>

<!-- end list -->

  - <span data-ttu-id="23a69-122">indexlist</span><span class="sxs-lookup"><span data-stu-id="23a69-122">indexlist</span></span>  
    <span data-ttu-id="23a69-123">Tipo: [Microsoft.ISAM.esent.Interop.JET_INDEXLIST](./jet-indexlist-class.md)</span><span class="sxs-lookup"><span data-stu-id="23a69-123">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXLIST](./jet-indexlist-class.md)</span></span>  
    
    <span data-ttu-id="23a69-124">Se rellena con información acerca de los índices de la tabla.</span><span class="sxs-lookup"><span data-stu-id="23a69-124">Filled in with information about indexes on the table.</span></span>

## <a name="see-also"></a><span data-ttu-id="23a69-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="23a69-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="23a69-126">Referencia</span><span class="sxs-lookup"><span data-stu-id="23a69-126">Reference</span></span>

[<span data-ttu-id="23a69-127">Clase de API</span><span class="sxs-lookup"><span data-stu-id="23a69-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="23a69-128">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="23a69-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="23a69-129">Sobrecarga JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="23a69-129">JetGetIndexInfo overload</span></span>](./api.jetgetindexinfo-method.md)

[<span data-ttu-id="23a69-130">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="23a69-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
