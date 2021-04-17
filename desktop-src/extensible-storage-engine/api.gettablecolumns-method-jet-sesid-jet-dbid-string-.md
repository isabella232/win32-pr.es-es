---
description: 'Más información sobre: método API. GetTableColumns (JET_SESID, JET_DBID, cadena)'
title: Método API. GetTableColumns (JET_SESID, JET_DBID, cadena)
TOCTitle: GetTableColumns method (JET_SESID, JET_DBID, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetTableColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.gettablecolumns(v=EXCHG.10)
ms:contentKeyID: 55107216
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetTableColumns
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 68a05ee3d0887f4396df0b2ba3159737791c413d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539741"
---
# <a name="apigettablecolumns-method-jet_sesid-jet_dbid-string"></a><span data-ttu-id="9ec5f-103">Método API. GetTableColumns (JET_SESID, JET_DBID, cadena)</span><span class="sxs-lookup"><span data-stu-id="9ec5f-103">Api.GetTableColumns method (JET_SESID, JET_DBID, String)</span></span>

<span data-ttu-id="9ec5f-104">Recorre en iteración todas las columnas de la tabla y devuelve información sobre cada una de ellas.</span><span class="sxs-lookup"><span data-stu-id="9ec5f-104">Iterates over all the columns in the table, returning information about each one.</span></span>

<span data-ttu-id="9ec5f-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9ec5f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9ec5f-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9ec5f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9ec5f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9ec5f-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetTableColumns ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String _
) As IEnumerable(Of ColumnInfo)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim returnValue As IEnumerable(Of ColumnInfo)

returnValue = Api.GetTableColumns(sesid, _
    dbid, tablename)
```

``` csharp
public static IEnumerable<ColumnInfo> GetTableColumns(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename
)
```

#### <a name="parameters"></a><span data-ttu-id="9ec5f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9ec5f-108">Parameters</span></span>

  - <span data-ttu-id="9ec5f-109">sesid</span><span class="sxs-lookup"><span data-stu-id="9ec5f-109">sesid</span></span>  
    <span data-ttu-id="9ec5f-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9ec5f-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="9ec5f-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="9ec5f-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="9ec5f-112">dbid</span><span class="sxs-lookup"><span data-stu-id="9ec5f-112">dbid</span></span>  
    <span data-ttu-id="9ec5f-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9ec5f-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="9ec5f-114">Base de datos que contiene la tabla.</span><span class="sxs-lookup"><span data-stu-id="9ec5f-114">The database containing the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="9ec5f-115">tablename</span><span class="sxs-lookup"><span data-stu-id="9ec5f-115">tablename</span></span>  
    <span data-ttu-id="9ec5f-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="9ec5f-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="9ec5f-117">Nombre de la tabla.</span><span class="sxs-lookup"><span data-stu-id="9ec5f-117">The name of the table.</span></span>

#### <a name="return-value"></a><span data-ttu-id="9ec5f-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9ec5f-118">Return value</span></span>

<span data-ttu-id="9ec5f-119">Tipo: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[ColumnInfo](./columninfo-class.md)\></span><span class="sxs-lookup"><span data-stu-id="9ec5f-119">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[ColumnInfo](./columninfo-class.md)\></span></span>  
<span data-ttu-id="9ec5f-120">Un iterador sobre ColumnInfo para cada columna de la tabla.</span><span class="sxs-lookup"><span data-stu-id="9ec5f-120">An iterator over ColumnInfo for each column in the table.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9ec5f-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ec5f-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9ec5f-122">Referencia</span><span class="sxs-lookup"><span data-stu-id="9ec5f-122">Reference</span></span>

[<span data-ttu-id="9ec5f-123">Clase de API</span><span class="sxs-lookup"><span data-stu-id="9ec5f-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="9ec5f-124">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="9ec5f-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="9ec5f-125">Sobrecarga GetTableColumns</span><span class="sxs-lookup"><span data-stu-id="9ec5f-125">GetTableColumns overload</span></span>](./api.gettablecolumns-method.md)

[<span data-ttu-id="9ec5f-126">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="9ec5f-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
