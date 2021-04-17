---
description: 'Más información sobre: método API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Int64)'
title: Método API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Int64)
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Int64)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Int64)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100926
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.SetColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 925d8483a799a23bc6551e6d3d13731c7f1f392a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688308"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-int64"></a><span data-ttu-id="c593a-103">Método API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Int64)</span><span class="sxs-lookup"><span data-stu-id="c593a-103">Api.SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Int64)</span></span>

<span data-ttu-id="c593a-104">Modifica un valor de columna única en un registro modificado que se va a insertar o actualizar el registro actual.</span><span class="sxs-lookup"><span data-stu-id="c593a-104">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span>

<span data-ttu-id="c593a-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c593a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c593a-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c593a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c593a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c593a-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub SetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Long _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As LongApi.SetColumn(sesid, tableid, columnid, _
    data)
```

``` csharp
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    long data
)
```

#### <a name="parameters"></a><span data-ttu-id="c593a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c593a-108">Parameters</span></span>

  - <span data-ttu-id="c593a-109">sesid</span><span class="sxs-lookup"><span data-stu-id="c593a-109">sesid</span></span>  
    <span data-ttu-id="c593a-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c593a-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c593a-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="c593a-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c593a-112">TABLEID</span><span class="sxs-lookup"><span data-stu-id="c593a-112">tableid</span></span>  
    <span data-ttu-id="c593a-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c593a-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="c593a-114">Cursor que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="c593a-114">The cursor to update.</span></span> <span data-ttu-id="c593a-115">Se debe preparar una actualización.</span><span class="sxs-lookup"><span data-stu-id="c593a-115">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="c593a-116">columnid</span><span class="sxs-lookup"><span data-stu-id="c593a-116">columnid</span></span>  
    <span data-ttu-id="c593a-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c593a-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="c593a-118">Columnid que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="c593a-118">The columnid to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="c593a-119">datos</span><span class="sxs-lookup"><span data-stu-id="c593a-119">data</span></span>  
    <span data-ttu-id="c593a-120">Tipo: [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="c593a-120">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
    
    <span data-ttu-id="c593a-121">Datos que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="c593a-121">The data to set.</span></span>

## <a name="see-also"></a><span data-ttu-id="c593a-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="c593a-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c593a-123">Referencia</span><span class="sxs-lookup"><span data-stu-id="c593a-123">Reference</span></span>

[<span data-ttu-id="c593a-124">Clase de API</span><span class="sxs-lookup"><span data-stu-id="c593a-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="c593a-125">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="c593a-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="c593a-126">Sobrecarga SetColumn</span><span class="sxs-lookup"><span data-stu-id="c593a-126">SetColumn overload</span></span>](./api.setcolumn-method.md)

[<span data-ttu-id="c593a-127">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c593a-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
