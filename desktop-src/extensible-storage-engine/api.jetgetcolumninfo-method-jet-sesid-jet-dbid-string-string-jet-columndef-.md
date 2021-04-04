---
description: 'Más información sobre: método API. JetGetColumnInfo (JET_SESID, JET_DBID, cadena, cadena JET_COLUMNDEF)'
title: Método API. JetGetColumnInfo (JET_SESID, JET_DBID, cadena, cadena, JET_COLUMNDEF)
TOCTitle: JetGetColumnInfo method (JET_SESID, JET_DBID, String, String, JET_COLUMNDEF)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetcolumninfo(v=EXCHG.10)
ms:contentKeyID: 55100708
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetColumnInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e4af99e7cfdc9f2f1fe83095ad92797ce0b34bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154039"
---
# <a name="apijetgetcolumninfo-method-jet_sesid-jet_dbid-string-string-jet_columndef"></a><span data-ttu-id="d61b5-103">Método API. JetGetColumnInfo (JET_SESID, JET_DBID, cadena, cadena, JET_COLUMNDEF)</span><span class="sxs-lookup"><span data-stu-id="d61b5-103">Api.JetGetColumnInfo method (JET_SESID, JET_DBID, String, String, JET_COLUMNDEF)</span></span>

<span data-ttu-id="d61b5-104">Recupera información sobre una columna de la tabla.</span><span class="sxs-lookup"><span data-stu-id="d61b5-104">Retrieves information about a table column.</span></span>

<span data-ttu-id="d61b5-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d61b5-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d61b5-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d61b5-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d61b5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d61b5-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetColumnInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    columnName As String, _
    <OutAttribute> ByRef columndef As JET_COLUMNDEF _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim columnName As String
Dim columndef As JET_COLUMNDEFApi.JetGetColumnInfo(sesid, dbid, _
    tablename, columnName, columndef)
```

``` csharp
public static void JetGetColumnInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string columnName,
    out JET_COLUMNDEF columndef
)
```

#### <a name="parameters"></a><span data-ttu-id="d61b5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d61b5-108">Parameters</span></span>

  - <span data-ttu-id="d61b5-109">sesid</span><span class="sxs-lookup"><span data-stu-id="d61b5-109">sesid</span></span>  
    <span data-ttu-id="d61b5-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d61b5-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="d61b5-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="d61b5-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="d61b5-112">dbid</span><span class="sxs-lookup"><span data-stu-id="d61b5-112">dbid</span></span>  
    <span data-ttu-id="d61b5-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d61b5-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="d61b5-114">La base de datos que contiene la tabla.</span><span class="sxs-lookup"><span data-stu-id="d61b5-114">The database that contains the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="d61b5-115">tablename</span><span class="sxs-lookup"><span data-stu-id="d61b5-115">tablename</span></span>  
    <span data-ttu-id="d61b5-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="d61b5-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="d61b5-117">Nombre de la tabla que contiene la columna.</span><span class="sxs-lookup"><span data-stu-id="d61b5-117">The name of the table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="d61b5-118">columnName</span><span class="sxs-lookup"><span data-stu-id="d61b5-118">columnName</span></span>  
    <span data-ttu-id="d61b5-119">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="d61b5-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="d61b5-120">El nombre de la columna.</span><span class="sxs-lookup"><span data-stu-id="d61b5-120">The name of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="d61b5-121">columndef</span><span class="sxs-lookup"><span data-stu-id="d61b5-121">columndef</span></span>  
    <span data-ttu-id="d61b5-122">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span><span class="sxs-lookup"><span data-stu-id="d61b5-122">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span></span>  
    
    <span data-ttu-id="d61b5-123">Se rellena con información sobre la columna.</span><span class="sxs-lookup"><span data-stu-id="d61b5-123">Filled in with information about the column.</span></span>

## <a name="see-also"></a><span data-ttu-id="d61b5-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d61b5-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d61b5-125">Referencia</span><span class="sxs-lookup"><span data-stu-id="d61b5-125">Reference</span></span>

[<span data-ttu-id="d61b5-126">Clase de API</span><span class="sxs-lookup"><span data-stu-id="d61b5-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d61b5-127">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="d61b5-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d61b5-128">Sobrecarga JetGetColumnInfo</span><span class="sxs-lookup"><span data-stu-id="d61b5-128">JetGetColumnInfo overload</span></span>](./api.jetgetcolumninfo-method.md)

[<span data-ttu-id="d61b5-129">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d61b5-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
