---
description: 'Más información sobre: método API. GetTableIndexes (JET_SESID, JET_TABLEID)'
title: Método API. GetTableIndexes (JET_SESID, JET_TABLEID)
TOCTitle: GetTableIndexes method (JET_SESID, JET_TABLEID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetTableIndexes(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.gettableindexes(v=EXCHG.10)
ms:contentKeyID: 55107219
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
ms.openlocfilehash: 8708f285445b13ecb1c9d2cb306ec14c7976905b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705522"
---
# <a name="apigettableindexes-method-jet_sesid-jet_tableid"></a><span data-ttu-id="0b799-103">Método API. GetTableIndexes (JET_SESID, JET_TABLEID)</span><span class="sxs-lookup"><span data-stu-id="0b799-103">Api.GetTableIndexes method (JET_SESID, JET_TABLEID)</span></span>

<span data-ttu-id="0b799-104">Recorre en iteración todos los índices de la tabla y devuelve información sobre cada uno de ellos.</span><span class="sxs-lookup"><span data-stu-id="0b799-104">Iterates over all the indexes in the table, returning information about each one.</span></span>

<span data-ttu-id="0b799-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0b799-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0b799-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0b799-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0b799-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0b799-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetTableIndexes ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As IEnumerable(Of IndexInfo)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As IEnumerable(Of IndexInfo)

returnValue = Api.GetTableIndexes(sesid, _
    tableid)
```

``` csharp
public static IEnumerable<IndexInfo> GetTableIndexes(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="0b799-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0b799-108">Parameters</span></span>

  - <span data-ttu-id="0b799-109">sesid</span><span class="sxs-lookup"><span data-stu-id="0b799-109">sesid</span></span>  
    <span data-ttu-id="0b799-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0b799-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="0b799-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="0b799-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="0b799-112">TABLEID</span><span class="sxs-lookup"><span data-stu-id="0b799-112">tableid</span></span>  
    <span data-ttu-id="0b799-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0b799-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="0b799-114">Tabla para la que se va a recuperar información de índice.</span><span class="sxs-lookup"><span data-stu-id="0b799-114">The table to retrieve index information for.</span></span>

#### <a name="return-value"></a><span data-ttu-id="0b799-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0b799-115">Return value</span></span>

<span data-ttu-id="0b799-116">Tipo: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[IndexInfo](./indexinfo-class.md)\></span><span class="sxs-lookup"><span data-stu-id="0b799-116">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[IndexInfo](./indexinfo-class.md)\></span></span>  
<span data-ttu-id="0b799-117">Un iterador sobre un IndexInfo para cada índice de la tabla.</span><span class="sxs-lookup"><span data-stu-id="0b799-117">An iterator over an IndexInfo for each index in the table.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0b799-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b799-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0b799-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="0b799-119">Reference</span></span>

[<span data-ttu-id="0b799-120">Clase de API</span><span class="sxs-lookup"><span data-stu-id="0b799-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="0b799-121">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="0b799-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="0b799-122">Sobrecarga GetTableIndexes</span><span class="sxs-lookup"><span data-stu-id="0b799-122">GetTableIndexes overload</span></span>](./api.gettableindexes-method.md)

[<span data-ttu-id="0b799-123">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="0b799-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
