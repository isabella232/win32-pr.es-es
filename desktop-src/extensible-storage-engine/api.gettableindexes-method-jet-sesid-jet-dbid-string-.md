---
description: 'Más información sobre: método API. GetTableIndexes (JET_SESID, JET_DBID, cadena)'
title: Método API. GetTableIndexes (JET_SESID, JET_DBID, cadena)
TOCTitle: GetTableIndexes method (JET_SESID, JET_DBID, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetTableIndexes(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.gettableindexes(v=EXCHG.10)
ms:contentKeyID: 55100648
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetTableIndexes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 90ac8dd014e0594fbffbb12b3ea4f3698f850de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907587"
---
# <a name="apigettableindexes-method-jet_sesid-jet_dbid-string"></a><span data-ttu-id="7b474-103">Método API. GetTableIndexes (JET_SESID, JET_DBID, cadena)</span><span class="sxs-lookup"><span data-stu-id="7b474-103">Api.GetTableIndexes method (JET_SESID, JET_DBID, String)</span></span>

<span data-ttu-id="7b474-104">Recorre en iteración todos los índices de la tabla y devuelve información sobre cada uno de ellos.</span><span class="sxs-lookup"><span data-stu-id="7b474-104">Iterates over all the indexs in the table, returning information about each one.</span></span>

<span data-ttu-id="7b474-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7b474-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7b474-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7b474-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7b474-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7b474-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetTableIndexes ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String _
) As IEnumerable(Of IndexInfo)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim returnValue As IEnumerable(Of IndexInfo)

returnValue = Api.GetTableIndexes(sesid, _
    dbid, tablename)
```

``` csharp
public static IEnumerable<IndexInfo> GetTableIndexes(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename
)
```

#### <a name="parameters"></a><span data-ttu-id="7b474-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7b474-108">Parameters</span></span>

  - <span data-ttu-id="7b474-109">sesid</span><span class="sxs-lookup"><span data-stu-id="7b474-109">sesid</span></span>  
    <span data-ttu-id="7b474-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7b474-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="7b474-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="7b474-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="7b474-112">dbid</span><span class="sxs-lookup"><span data-stu-id="7b474-112">dbid</span></span>  
    <span data-ttu-id="7b474-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7b474-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="7b474-114">Base de datos que contiene la tabla.</span><span class="sxs-lookup"><span data-stu-id="7b474-114">The database containing the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="7b474-115">tablename</span><span class="sxs-lookup"><span data-stu-id="7b474-115">tablename</span></span>  
    <span data-ttu-id="7b474-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="7b474-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="7b474-117">Nombre de la tabla.</span><span class="sxs-lookup"><span data-stu-id="7b474-117">The name of the table.</span></span>

#### <a name="return-value"></a><span data-ttu-id="7b474-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7b474-118">Return value</span></span>

<span data-ttu-id="7b474-119">Tipo: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[IndexInfo](./indexinfo-class.md)\></span><span class="sxs-lookup"><span data-stu-id="7b474-119">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[IndexInfo](./indexinfo-class.md)\></span></span>  
<span data-ttu-id="7b474-120">Un iterador sobre un IndexInfo para cada índice de la tabla.</span><span class="sxs-lookup"><span data-stu-id="7b474-120">An iterator over an IndexInfo for each index in the table.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7b474-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b474-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7b474-122">Referencia</span><span class="sxs-lookup"><span data-stu-id="7b474-122">Reference</span></span>

[<span data-ttu-id="7b474-123">Clase de API</span><span class="sxs-lookup"><span data-stu-id="7b474-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="7b474-124">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="7b474-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="7b474-125">Sobrecarga GetTableIndexes</span><span class="sxs-lookup"><span data-stu-id="7b474-125">GetTableIndexes overload</span></span>](./api.gettableindexes-method.md)

[<span data-ttu-id="7b474-126">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="7b474-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
