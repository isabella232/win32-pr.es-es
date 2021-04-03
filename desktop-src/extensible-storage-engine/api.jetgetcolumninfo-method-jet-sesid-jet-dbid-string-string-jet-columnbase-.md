---
description: 'Más información sobre: método API. JetGetColumnInfo (JET_SESID, JET_DBID, cadena, cadena JET_COLUMNBASE)'
title: Método API. JetGetColumnInfo (JET_SESID, JET_DBID, cadena, cadena, JET_COLUMNBASE)
TOCTitle: JetGetColumnInfo method (JET_SESID, JET_DBID, String, String, JET_COLUMNBASE)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNBASE@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetcolumninfo(v=EXCHG.10)
ms:contentKeyID: 55100705
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetColumnInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e690dbb2a4b82698440b3be3c483bb46b2eca8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907785"
---
# <a name="apijetgetcolumninfo-method-jet_sesid-jet_dbid-string-string-jet_columnbase"></a><span data-ttu-id="9d8c2-103">Método API. JetGetColumnInfo (JET_SESID, JET_DBID, cadena, cadena, JET_COLUMNBASE)</span><span class="sxs-lookup"><span data-stu-id="9d8c2-103">Api.JetGetColumnInfo method (JET_SESID, JET_DBID, String, String, JET_COLUMNBASE)</span></span>

<span data-ttu-id="9d8c2-104">Recupera información sobre una columna de una tabla.</span><span class="sxs-lookup"><span data-stu-id="9d8c2-104">Retrieves information about a column in a table.</span></span>

<span data-ttu-id="9d8c2-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9d8c2-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9d8c2-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9d8c2-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9d8c2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9d8c2-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetColumnInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    columnName As String, _
    <OutAttribute> ByRef columnbase As JET_COLUMNBASE _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim columnName As String
Dim columnbase As JET_COLUMNBASEApi.JetGetColumnInfo(sesid, dbid, _
    tablename, columnName, columnbase)
```

``` csharp
public static void JetGetColumnInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string columnName,
    out JET_COLUMNBASE columnbase
)
```

#### <a name="parameters"></a><span data-ttu-id="9d8c2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9d8c2-108">Parameters</span></span>

  - <span data-ttu-id="9d8c2-109">sesid</span><span class="sxs-lookup"><span data-stu-id="9d8c2-109">sesid</span></span>  
    <span data-ttu-id="9d8c2-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9d8c2-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="9d8c2-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="9d8c2-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="9d8c2-112">dbid</span><span class="sxs-lookup"><span data-stu-id="9d8c2-112">dbid</span></span>  
    <span data-ttu-id="9d8c2-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9d8c2-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="9d8c2-114">La base de datos que contiene la tabla.</span><span class="sxs-lookup"><span data-stu-id="9d8c2-114">The database that contains the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="9d8c2-115">tablename</span><span class="sxs-lookup"><span data-stu-id="9d8c2-115">tablename</span></span>  
    <span data-ttu-id="9d8c2-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="9d8c2-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="9d8c2-117">Nombre de la tabla que contiene la columna.</span><span class="sxs-lookup"><span data-stu-id="9d8c2-117">The name of the table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="9d8c2-118">columnName</span><span class="sxs-lookup"><span data-stu-id="9d8c2-118">columnName</span></span>  
    <span data-ttu-id="9d8c2-119">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="9d8c2-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="9d8c2-120">El nombre de la columna.</span><span class="sxs-lookup"><span data-stu-id="9d8c2-120">The name of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="9d8c2-121">columnbase</span><span class="sxs-lookup"><span data-stu-id="9d8c2-121">columnbase</span></span>  
    <span data-ttu-id="9d8c2-122">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNBASE](./jet-columnbase-class.md)</span><span class="sxs-lookup"><span data-stu-id="9d8c2-122">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNBASE](./jet-columnbase-class.md)</span></span>  
    
    <span data-ttu-id="9d8c2-123">Se rellena con información acerca de las columnas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="9d8c2-123">Filled in with information about the columns in the table.</span></span>

## <a name="see-also"></a><span data-ttu-id="9d8c2-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="9d8c2-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9d8c2-125">Referencia</span><span class="sxs-lookup"><span data-stu-id="9d8c2-125">Reference</span></span>

[<span data-ttu-id="9d8c2-126">Clase de API</span><span class="sxs-lookup"><span data-stu-id="9d8c2-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="9d8c2-127">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="9d8c2-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="9d8c2-128">Sobrecarga JetGetColumnInfo</span><span class="sxs-lookup"><span data-stu-id="9d8c2-128">JetGetColumnInfo overload</span></span>](./api.jetgetcolumninfo-method.md)

[<span data-ttu-id="9d8c2-129">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="9d8c2-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
