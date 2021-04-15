---
description: 'Más información sobre: API. IntersectIndexes (método)'
title: Método API. IntersectIndexes
TOCTitle: 'IntersectIndexes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.IntersectIndexes(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.intersectindexes(v=EXCHG.10)
ms:contentKeyID: 55107220
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.IntersectIndexes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.IntersectIndexes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8dfe5784ecd5ab517e183f8eeeb5f79315fe585a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539735"
---
# <a name="apiintersectindexes-method"></a><span data-ttu-id="f4577-103">Método API. IntersectIndexes</span><span class="sxs-lookup"><span data-stu-id="f4577-103">Api.IntersectIndexes method</span></span>

<span data-ttu-id="f4577-104">Intersecte un grupo de intervalos de índice y devuelva los marcadores de los registros que se encuentran en todos los intervalos de índice.</span><span class="sxs-lookup"><span data-stu-id="f4577-104">Intersect a group of index ranges and return the bookmarks of the records which are found in all the index ranges.</span></span> <span data-ttu-id="f4577-105">Vea también [JetIntersectIndexes (JET_SESID, \[ \] , Int32, JET_RECORDLIST, IntersectIndexesGrbit)](./api.jetintersectindexes-method.md).</span><span class="sxs-lookup"><span data-stu-id="f4577-105">Also see [JetIntersectIndexes(JET_SESID, \[\], Int32, JET_RECORDLIST, IntersectIndexesGrbit)](./api.jetintersectindexes-method.md).</span></span>

<span data-ttu-id="f4577-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f4577-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f4577-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f4577-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f4577-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f4577-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function IntersectIndexes ( _
    sesid As JET_SESID, _
    ParamArray tableids As JET_TABLEID() _
) As IEnumerable(Of Byte())
'Usage
Dim sesid As JET_SESID
Dim tableids As JET_TABLEID()
Dim returnValue As IEnumerable(Of Byte())

returnValue = Api.IntersectIndexes(sesid, _
    tableids)
```

``` csharp
public static IEnumerable<byte[]> IntersectIndexes(
    JET_SESID sesid,
    params JET_TABLEID[] tableids
)
```

#### <a name="parameters"></a><span data-ttu-id="f4577-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f4577-109">Parameters</span></span>

  - <span data-ttu-id="f4577-110">sesid</span><span class="sxs-lookup"><span data-stu-id="f4577-110">sesid</span></span>  
    <span data-ttu-id="f4577-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f4577-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="f4577-112">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="f4577-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="f4577-113">tableids</span><span class="sxs-lookup"><span data-stu-id="f4577-113">tableids</span></span>  
    <span data-ttu-id="f4577-114">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="f4577-114">Type: \[\]</span></span>  
    
    <span data-ttu-id="f4577-115">Tableids que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="f4577-115">The tableids to use.</span></span> <span data-ttu-id="f4577-116">Cada TABLEID debe ser de un índice diferente en la misma tabla y tener un intervalo de índice activo.</span><span class="sxs-lookup"><span data-stu-id="f4577-116">Each tableid must be from a different index on the same table and have an active index range.</span></span> <span data-ttu-id="f4577-117">Use [JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md) para crear un intervalo de índices.</span><span class="sxs-lookup"><span data-stu-id="f4577-117">Use [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md) to create an index range.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f4577-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f4577-118">Return value</span></span>

<span data-ttu-id="f4577-119">Tipo: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<\[\]\></span><span class="sxs-lookup"><span data-stu-id="f4577-119">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<\[\]\></span></span>  
<span data-ttu-id="f4577-120">Marcadores de los registros que se encuentran en todos los intervalos de índice.</span><span class="sxs-lookup"><span data-stu-id="f4577-120">The bookmarks of the records which are found in all the index ranges.</span></span> <span data-ttu-id="f4577-121">Los marcadores se devuelven en el orden de la clave principal.</span><span class="sxs-lookup"><span data-stu-id="f4577-121">The bookmarks are returned in primary key order.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f4577-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4577-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f4577-123">Referencia</span><span class="sxs-lookup"><span data-stu-id="f4577-123">Reference</span></span>

[<span data-ttu-id="f4577-124">Clase de API</span><span class="sxs-lookup"><span data-stu-id="f4577-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f4577-125">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="f4577-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f4577-126">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f4577-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
