---
description: 'Más información sobre: método API. MakeKey (JET_SESID, JET_TABLEID, GUID, MakeKeyGrbit)'
title: Método API. MakeKey (JET_SESID, JET_TABLEID, GUID, MakeKeyGrbit)
TOCTitle: MakeKey method (JET_SESID, JET_TABLEID, Guid, MakeKeyGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.MakeKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Guid,Microsoft.Isam.Esent.Interop.MakeKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.makekey(v=EXCHG.10)
ms:contentKeyID: 55100823
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.MakeKey
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 73096598f8173def29b40273bbeec28738d762a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707487"
---
# <a name="apimakekey-method-jet_sesid-jet_tableid-guid-makekeygrbit"></a><span data-ttu-id="38d0e-103">Método API. MakeKey (JET_SESID, JET_TABLEID, GUID, MakeKeyGrbit)</span><span class="sxs-lookup"><span data-stu-id="38d0e-103">Api.MakeKey method (JET_SESID, JET_TABLEID, Guid, MakeKeyGrbit)</span></span>

<span data-ttu-id="38d0e-104">Construye una clave de búsqueda que puede usar [JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) y [JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span><span class="sxs-lookup"><span data-stu-id="38d0e-104">Constructs a search key that may then be used by [JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) and [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span></span>

<span data-ttu-id="38d0e-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="38d0e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="38d0e-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="38d0e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="38d0e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="38d0e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub MakeKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As Guid, _
    grbit As MakeKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As Guid
Dim grbit As MakeKeyGrbitApi.MakeKey(sesid, tableid, data, _
    grbit)
```

``` csharp
public static void MakeKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    Guid data,
    MakeKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="38d0e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="38d0e-108">Parameters</span></span>

  - <span data-ttu-id="38d0e-109">sesid</span><span class="sxs-lookup"><span data-stu-id="38d0e-109">sesid</span></span>  
    <span data-ttu-id="38d0e-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="38d0e-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="38d0e-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="38d0e-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="38d0e-112">TABLEID</span><span class="sxs-lookup"><span data-stu-id="38d0e-112">tableid</span></span>  
    <span data-ttu-id="38d0e-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="38d0e-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="38d0e-114">Cursor en el que se va a crear la clave.</span><span class="sxs-lookup"><span data-stu-id="38d0e-114">The cursor to create the key on.</span></span>

<!-- end list -->

  - <span data-ttu-id="38d0e-115">datos</span><span class="sxs-lookup"><span data-stu-id="38d0e-115">data</span></span>  
    <span data-ttu-id="38d0e-116">Tipo: [System. GUID](/dotnet/api/system.guid)</span><span class="sxs-lookup"><span data-stu-id="38d0e-116">Type: [System.Guid](/dotnet/api/system.guid)</span></span>  
    
    <span data-ttu-id="38d0e-117">Datos de columna para la columna de clave actual del índice actual.</span><span class="sxs-lookup"><span data-stu-id="38d0e-117">Column data for the current key column of the current index.</span></span>

<!-- end list -->

  - <span data-ttu-id="38d0e-118">grbit</span><span class="sxs-lookup"><span data-stu-id="38d0e-118">grbit</span></span>  
    <span data-ttu-id="38d0e-119">Tipo: [Microsoft. ISAM. esent. Interop. MakeKeyGrbit](./makekeygrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="38d0e-119">Type: [Microsoft.Isam.Esent.Interop.MakeKeyGrbit](./makekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="38d0e-120">Opciones de clave.</span><span class="sxs-lookup"><span data-stu-id="38d0e-120">Key options.</span></span>

## <a name="see-also"></a><span data-ttu-id="38d0e-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="38d0e-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="38d0e-122">Referencia</span><span class="sxs-lookup"><span data-stu-id="38d0e-122">Reference</span></span>

[<span data-ttu-id="38d0e-123">Clase de API</span><span class="sxs-lookup"><span data-stu-id="38d0e-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="38d0e-124">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="38d0e-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="38d0e-125">Sobrecarga MakeKey</span><span class="sxs-lookup"><span data-stu-id="38d0e-125">MakeKey overload</span></span>](./api.makekey-method.md)

[<span data-ttu-id="38d0e-126">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="38d0e-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
