---
description: 'Más información sobre: Server2003Api. JetUpdate2 (método)'
title: Método Server2003Api. JetUpdate2 (Microsoft. ISAM. esent. Interop. Server2003)
TOCTitle: 'JetUpdate2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003api.jetupdate2(v=EXCHG.10)
ms:contentKeyID: 55104110
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fff3687d42160df331bfe52660be232fe3b41d5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153765"
---
# <a name="server2003apijetupdate2-method"></a><span data-ttu-id="019d1-103">Server2003Api. JetUpdate2, método</span><span class="sxs-lookup"><span data-stu-id="019d1-103">Server2003Api.JetUpdate2 method</span></span>

<span data-ttu-id="019d1-104">La función JetUpdate realiza una operación de actualización que incluye la inserción de una nueva fila en una tabla o la actualización de una fila existente.</span><span class="sxs-lookup"><span data-stu-id="019d1-104">The JetUpdate function performs an update operation including inserting a new row into a table or updating an existing row.</span></span> <span data-ttu-id="019d1-105">La eliminación de una fila de tabla se realiza mediante una llamada a [JetDelete (JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).</span><span class="sxs-lookup"><span data-stu-id="019d1-105">Deleting a table row is performed by calling [JetDelete(JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).</span></span>

<span data-ttu-id="019d1-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="019d1-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span></span>  
<span data-ttu-id="019d1-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="019d1-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="019d1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="019d1-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetUpdate2 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer, _
    grbit As UpdateGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As Integer
Dim grbit As UpdateGrbitServer2003Api.JetUpdate2(sesid, tableid, bookmark, _
    bookmarkSize, actualBookmarkSize, _
    grbit)
```

``` csharp
public static void JetUpdate2(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize,
    UpdateGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="019d1-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="019d1-109">Parameters</span></span>

  - <span data-ttu-id="019d1-110">sesid</span><span class="sxs-lookup"><span data-stu-id="019d1-110">sesid</span></span>  
    <span data-ttu-id="019d1-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="019d1-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="019d1-112">La sesión que inició la actualización.</span><span class="sxs-lookup"><span data-stu-id="019d1-112">The session which started the update.</span></span>

<!-- end list -->

  - <span data-ttu-id="019d1-113">TABLEID</span><span class="sxs-lookup"><span data-stu-id="019d1-113">tableid</span></span>  
    <span data-ttu-id="019d1-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="019d1-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="019d1-115">Cursor que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="019d1-115">The cursor to update.</span></span> <span data-ttu-id="019d1-116">Se debe preparar una actualización.</span><span class="sxs-lookup"><span data-stu-id="019d1-116">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="019d1-117">marcador</span><span class="sxs-lookup"><span data-stu-id="019d1-117">bookmark</span></span>  
    <span data-ttu-id="019d1-118">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="019d1-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="019d1-119">Devuelve el marcador del registro actualizado.</span><span class="sxs-lookup"><span data-stu-id="019d1-119">Returns the bookmark of the updated record.</span></span> <span data-ttu-id="019d1-120">Puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="019d1-120">This can be null.</span></span>

<!-- end list -->

  - <span data-ttu-id="019d1-121">bookmarkSize</span><span class="sxs-lookup"><span data-stu-id="019d1-121">bookmarkSize</span></span>  
    <span data-ttu-id="019d1-122">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="019d1-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="019d1-123">Tamaño del búfer del marcador.</span><span class="sxs-lookup"><span data-stu-id="019d1-123">The size of the bookmark buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="019d1-124">actualBookmarkSize</span><span class="sxs-lookup"><span data-stu-id="019d1-124">actualBookmarkSize</span></span>  
    <span data-ttu-id="019d1-125">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="019d1-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="019d1-126">Devuelve el tamaño real del marcador.</span><span class="sxs-lookup"><span data-stu-id="019d1-126">Returns the actual size of the bookmark.</span></span>

<!-- end list -->

  - <span data-ttu-id="019d1-127">grbit</span><span class="sxs-lookup"><span data-stu-id="019d1-127">grbit</span></span>  
    <span data-ttu-id="019d1-128">Tipo: [Microsoft. ISAM. esent. Interop. Server2003. UpdateGrbit](./updategrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="019d1-128">Type: [Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit](./updategrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="019d1-129">Opciones de actualización.</span><span class="sxs-lookup"><span data-stu-id="019d1-129">Update options.</span></span>

## <a name="remarks"></a><span data-ttu-id="019d1-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="019d1-130">Remarks</span></span>

<span data-ttu-id="019d1-131">JetUpdate es el último paso para realizar una inserción o una actualización.</span><span class="sxs-lookup"><span data-stu-id="019d1-131">JetUpdate is the final step in performing an insert or an update.</span></span> <span data-ttu-id="019d1-132">La actualización se inicia llamando a [JetPrepareUpdate (JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) y llamando a [JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) una o varias veces para establecer el estado del registro.</span><span class="sxs-lookup"><span data-stu-id="019d1-132">The update is begun by calling [JetPrepareUpdate(JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) and then by calling [JetSetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, \[\], Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) one or more times to set the record state.</span></span> <span data-ttu-id="019d1-133">Por último, se llama a JetUpdate2 (JET_SESID, JET_TABLEID, \[ \] , Int32, Int32, UpdateGrbit) para completar la operación de actualización.</span><span class="sxs-lookup"><span data-stu-id="019d1-133">Finally, JetUpdate2(JET_SESID, JET_TABLEID, \[\], Int32, Int32, UpdateGrbit) is called to complete the update operation.</span></span> <span data-ttu-id="019d1-134">Los índices solo se actualizan mediante JetUpdate o y no durante JetSetColumn.</span><span class="sxs-lookup"><span data-stu-id="019d1-134">Indexes are updated only by JetUpdate or and not during JetSetColumn.</span></span>

## <a name="see-also"></a><span data-ttu-id="019d1-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="019d1-135">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="019d1-136">Referencia</span><span class="sxs-lookup"><span data-stu-id="019d1-136">Reference</span></span>

[<span data-ttu-id="019d1-137">Clase Server2003Api</span><span class="sxs-lookup"><span data-stu-id="019d1-137">Server2003Api class</span></span>](./server2003api-class.md)

[<span data-ttu-id="019d1-138">Miembros de Server2003Api</span><span class="sxs-lookup"><span data-stu-id="019d1-138">Server2003Api members</span></span>](./server2003api-members.md)

[<span data-ttu-id="019d1-139">Espacio de nombres Microsoft. ISAM. esent. Interop. Server2003</span><span class="sxs-lookup"><span data-stu-id="019d1-139">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
