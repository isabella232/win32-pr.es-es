---
description: 'Más información sobre: método API. JetGetColumnInfo (JET_SESID, JET_DBID, cadena, cadena JET_COLUMNLIST)'
title: Método API. JetGetColumnInfo (JET_SESID, JET_DBID, cadena, cadena, JET_COLUMNLIST)
TOCTitle: JetGetColumnInfo method (JET_SESID, JET_DBID, String, String, JET_COLUMNLIST)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNLIST@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetcolumninfo(v=EXCHG.10)
ms:contentKeyID: 55100703
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
ms.openlocfilehash: 6f3f0ea95e82217f0d9b44e6a00558d3530a7616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705517"
---
# <a name="apijetgetcolumninfo-method-jet_sesid-jet_dbid-string-string-jet_columnlist"></a><span data-ttu-id="f7742-103">Método API. JetGetColumnInfo (JET_SESID, JET_DBID, cadena, cadena, JET_COLUMNLIST)</span><span class="sxs-lookup"><span data-stu-id="f7742-103">Api.JetGetColumnInfo method (JET_SESID, JET_DBID, String, String, JET_COLUMNLIST)</span></span>

<span data-ttu-id="f7742-104">Recupera información acerca de todas las columnas de una tabla.</span><span class="sxs-lookup"><span data-stu-id="f7742-104">Retrieves information about all columns in a table.</span></span>

<span data-ttu-id="f7742-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f7742-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f7742-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f7742-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f7742-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f7742-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetColumnInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    columnName As String, _
    <OutAttribute> ByRef columnlist As JET_COLUMNLIST _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim columnName As String
Dim columnlist As JET_COLUMNLISTApi.JetGetColumnInfo(sesid, dbid, _
    tablename, columnName, columnlist)
```

``` csharp
public static void JetGetColumnInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string columnName,
    out JET_COLUMNLIST columnlist
)
```

#### <a name="parameters"></a><span data-ttu-id="f7742-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f7742-108">Parameters</span></span>

  - <span data-ttu-id="f7742-109">sesid</span><span class="sxs-lookup"><span data-stu-id="f7742-109">sesid</span></span>  
    <span data-ttu-id="f7742-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f7742-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="f7742-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="f7742-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="f7742-112">dbid</span><span class="sxs-lookup"><span data-stu-id="f7742-112">dbid</span></span>  
    <span data-ttu-id="f7742-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f7742-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="f7742-114">La base de datos que contiene la tabla.</span><span class="sxs-lookup"><span data-stu-id="f7742-114">The database that contains the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="f7742-115">tablename</span><span class="sxs-lookup"><span data-stu-id="f7742-115">tablename</span></span>  
    <span data-ttu-id="f7742-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="f7742-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="f7742-117">Nombre de la tabla que contiene la columna.</span><span class="sxs-lookup"><span data-stu-id="f7742-117">The name of the table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="f7742-118">columnName</span><span class="sxs-lookup"><span data-stu-id="f7742-118">columnName</span></span>  
    <span data-ttu-id="f7742-119">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="f7742-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="f7742-120">Este parámetro se ignora.</span><span class="sxs-lookup"><span data-stu-id="f7742-120">This parameter is ignored.</span></span>

<!-- end list -->

  - <span data-ttu-id="f7742-121">columnlist</span><span class="sxs-lookup"><span data-stu-id="f7742-121">columnlist</span></span>  
    <span data-ttu-id="f7742-122">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNLIST](./jet-columnlist-class.md)</span><span class="sxs-lookup"><span data-stu-id="f7742-122">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNLIST](./jet-columnlist-class.md)</span></span>  
    
    <span data-ttu-id="f7742-123">Se rellena con información acerca de las columnas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="f7742-123">Filled in with information about the columns in the table.</span></span>

## <a name="see-also"></a><span data-ttu-id="f7742-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="f7742-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f7742-125">Referencia</span><span class="sxs-lookup"><span data-stu-id="f7742-125">Reference</span></span>

[<span data-ttu-id="f7742-126">Clase de API</span><span class="sxs-lookup"><span data-stu-id="f7742-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f7742-127">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="f7742-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f7742-128">Sobrecarga JetGetColumnInfo</span><span class="sxs-lookup"><span data-stu-id="f7742-128">JetGetColumnInfo overload</span></span>](./api.jetgetcolumninfo-method.md)

[<span data-ttu-id="f7742-129">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f7742-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
