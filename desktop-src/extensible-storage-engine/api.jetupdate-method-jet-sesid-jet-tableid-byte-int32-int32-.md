---
description: 'Más información sobre: método API. JetUpdate (JET_SESID, JET_TABLEID, byte, Int32, Int32)'
title: Método API. JetUpdate (JET_SESID, JET_TABLEID, byte, Int32, Int32)
TOCTitle: JetUpdate method (JET_SESID, JET_TABLEID, Byte , Int32, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetupdate(v=EXCHG.10)
ms:contentKeyID: 55100814
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetUpdate
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2c85e424fc9b672944801da3d03cbaff0ca48017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908275"
---
# <a name="apijetupdate-method-jet_sesid-jet_tableid-byte--int32-int32"></a><span data-ttu-id="ebac8-103">Método API. JetUpdate (JET_SESID, JET_TABLEID, byte, Int32, Int32)</span><span class="sxs-lookup"><span data-stu-id="ebac8-103">Api.JetUpdate method (JET_SESID, JET_TABLEID, Byte , Int32, Int32)</span></span>

<span data-ttu-id="ebac8-104">La función JetUpdate realiza una operación de actualización que incluye la inserción de una nueva fila en una tabla o la actualización de una fila existente.</span><span class="sxs-lookup"><span data-stu-id="ebac8-104">The JetUpdate function performs an update operation including inserting a new row into a table or updating an existing row.</span></span> <span data-ttu-id="ebac8-105">La eliminación de una fila de tabla se realiza mediante una llamada a [JetDelete (JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).</span><span class="sxs-lookup"><span data-stu-id="ebac8-105">Deleting a table row is performed by calling [JetDelete(JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).</span></span>

<span data-ttu-id="ebac8-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ebac8-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ebac8-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ebac8-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ebac8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ebac8-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As IntegerApi.JetUpdate(sesid, tableid, bookmark, _
    bookmarkSize, actualBookmarkSize)
```

``` csharp
public static void JetUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize
)
```

#### <a name="parameters"></a><span data-ttu-id="ebac8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ebac8-109">Parameters</span></span>

  - <span data-ttu-id="ebac8-110">sesid</span><span class="sxs-lookup"><span data-stu-id="ebac8-110">sesid</span></span>  
    <span data-ttu-id="ebac8-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ebac8-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="ebac8-112">La sesión que inició la actualización.</span><span class="sxs-lookup"><span data-stu-id="ebac8-112">The session which started the update.</span></span>

<!-- end list -->

  - <span data-ttu-id="ebac8-113">TABLEID</span><span class="sxs-lookup"><span data-stu-id="ebac8-113">tableid</span></span>  
    <span data-ttu-id="ebac8-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ebac8-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="ebac8-115">Cursor que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="ebac8-115">The cursor to update.</span></span> <span data-ttu-id="ebac8-116">Se debe preparar una actualización.</span><span class="sxs-lookup"><span data-stu-id="ebac8-116">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="ebac8-117">marcador</span><span class="sxs-lookup"><span data-stu-id="ebac8-117">bookmark</span></span>  
    <span data-ttu-id="ebac8-118">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="ebac8-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="ebac8-119">Devuelve el marcador del registro actualizado.</span><span class="sxs-lookup"><span data-stu-id="ebac8-119">Returns the bookmark of the updated record.</span></span> <span data-ttu-id="ebac8-120">Puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="ebac8-120">This can be null.</span></span>

<!-- end list -->

  - <span data-ttu-id="ebac8-121">bookmarkSize</span><span class="sxs-lookup"><span data-stu-id="ebac8-121">bookmarkSize</span></span>  
    <span data-ttu-id="ebac8-122">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="ebac8-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="ebac8-123">Tamaño del búfer del marcador.</span><span class="sxs-lookup"><span data-stu-id="ebac8-123">The size of the bookmark buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="ebac8-124">actualBookmarkSize</span><span class="sxs-lookup"><span data-stu-id="ebac8-124">actualBookmarkSize</span></span>  
    <span data-ttu-id="ebac8-125">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="ebac8-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="ebac8-126">Devuelve el tamaño real del marcador.</span><span class="sxs-lookup"><span data-stu-id="ebac8-126">Returns the actual size of the bookmark.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebac8-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ebac8-127">Remarks</span></span>

<span data-ttu-id="ebac8-128">JetUpdate es el último paso para realizar una inserción o una actualización.</span><span class="sxs-lookup"><span data-stu-id="ebac8-128">JetUpdate is the final step in performing an insert or an update.</span></span> <span data-ttu-id="ebac8-129">La actualización se inicia llamando a [JetPrepareUpdate (JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) y llamando a [JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) una o varias veces para establecer el estado del registro.</span><span class="sxs-lookup"><span data-stu-id="ebac8-129">The update is begun by calling [JetPrepareUpdate(JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) and then by calling [JetSetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, \[\], Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) one or more times to set the record state.</span></span> <span data-ttu-id="ebac8-130">Por último, se llama a JetUpdate (JET_SESID, JET_TABLEID, \[ \] , Int32, Int32) para completar la operación de actualización.</span><span class="sxs-lookup"><span data-stu-id="ebac8-130">Finally, JetUpdate(JET_SESID, JET_TABLEID, \[\], Int32, Int32) is called to complete the update operation.</span></span> <span data-ttu-id="ebac8-131">Los índices solo se actualizan mediante JetUpdate o y no durante JetSetColumn.</span><span class="sxs-lookup"><span data-stu-id="ebac8-131">Indexes are updated only by JetUpdate or and not during JetSetColumn.</span></span>

## <a name="see-also"></a><span data-ttu-id="ebac8-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="ebac8-132">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ebac8-133">Referencia</span><span class="sxs-lookup"><span data-stu-id="ebac8-133">Reference</span></span>

[<span data-ttu-id="ebac8-134">Clase de API</span><span class="sxs-lookup"><span data-stu-id="ebac8-134">Api class</span></span>](./api-class.md)

[<span data-ttu-id="ebac8-135">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="ebac8-135">Api members</span></span>](./api-members.md)

[<span data-ttu-id="ebac8-136">Sobrecarga JetUpdate</span><span class="sxs-lookup"><span data-stu-id="ebac8-136">JetUpdate overload</span></span>](./api.jetupdate-method.md)

[<span data-ttu-id="ebac8-137">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="ebac8-137">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
