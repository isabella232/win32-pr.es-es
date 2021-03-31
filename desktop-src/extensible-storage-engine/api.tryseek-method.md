---
description: 'Más información sobre: API. TrySeek (método)'
title: Método API. TrySeek
TOCTitle: 'TrySeek method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TrySeek(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.SeekGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.tryseek(v=EXCHG.10)
ms:contentKeyID: 55100941
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TrySeek
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TrySeek
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 46472c59c14bd515e744a7ccfa908752783d27fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907777"
---
# <a name="apitryseek-method"></a><span data-ttu-id="14c3f-103">Método API. TrySeek</span><span class="sxs-lookup"><span data-stu-id="14c3f-103">Api.TrySeek method</span></span>

<span data-ttu-id="14c3f-104">Coloca de forma eficaz un cursor en una entrada de índice que coincide con los criterios de búsqueda especificados por la clave de búsqueda en ese cursor y la desigualdad especificada.</span><span class="sxs-lookup"><span data-stu-id="14c3f-104">Efficiently positions a cursor to an index entry that matches the search criteria specified by the search key in that cursor and the specified inequality.</span></span> <span data-ttu-id="14c3f-105">Una clave de búsqueda se debe haber construido previamente mediante JetMakeKey.</span><span class="sxs-lookup"><span data-stu-id="14c3f-105">A search key must have been previously constructed using JetMakeKey.</span></span>

<span data-ttu-id="14c3f-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="14c3f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="14c3f-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="14c3f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="14c3f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="14c3f-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TrySeek ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As SeekGrbit _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As SeekGrbit
Dim returnValue As Boolean

returnValue = Api.TrySeek(sesid, _
    tableid, grbit)
```

``` csharp
public static bool TrySeek(
    JET_SESID sesid,
    JET_TABLEID tableid,
    SeekGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="14c3f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="14c3f-109">Parameters</span></span>

  - <span data-ttu-id="14c3f-110">sesid</span><span class="sxs-lookup"><span data-stu-id="14c3f-110">sesid</span></span>  
    <span data-ttu-id="14c3f-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="14c3f-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="14c3f-112">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="14c3f-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="14c3f-113">TABLEID</span><span class="sxs-lookup"><span data-stu-id="14c3f-113">tableid</span></span>  
    <span data-ttu-id="14c3f-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="14c3f-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="14c3f-115">Cursor que se va a colocar.</span><span class="sxs-lookup"><span data-stu-id="14c3f-115">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="14c3f-116">grbit</span><span class="sxs-lookup"><span data-stu-id="14c3f-116">grbit</span></span>  
    <span data-ttu-id="14c3f-117">Tipo: [Microsoft. ISAM. esent. Interop. SeekGrbit](./seekgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="14c3f-117">Type: [Microsoft.Isam.Esent.Interop.SeekGrbit](./seekgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="14c3f-118">Opción de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="14c3f-118">Seek option.</span></span>

#### <a name="return-value"></a><span data-ttu-id="14c3f-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="14c3f-119">Return value</span></span>

<span data-ttu-id="14c3f-120">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="14c3f-120">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="14c3f-121">True si se encontró un registro que coincide con los criterios.</span><span class="sxs-lookup"><span data-stu-id="14c3f-121">True if a record matching the criteria was found.</span></span>  

## <a name="see-also"></a><span data-ttu-id="14c3f-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="14c3f-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="14c3f-123">Referencia</span><span class="sxs-lookup"><span data-stu-id="14c3f-123">Reference</span></span>

[<span data-ttu-id="14c3f-124">Clase de API</span><span class="sxs-lookup"><span data-stu-id="14c3f-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="14c3f-125">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="14c3f-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="14c3f-126">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="14c3f-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
