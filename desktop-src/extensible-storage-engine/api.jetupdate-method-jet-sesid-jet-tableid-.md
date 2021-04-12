---
description: 'Más información sobre: método API. JetUpdate (JET_SESID, JET_TABLEID)'
title: Método API. JetUpdate (JET_SESID, JET_TABLEID)
TOCTitle: JetUpdate method (JET_SESID, JET_TABLEID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetupdate(v=EXCHG.10)
ms:contentKeyID: 55100831
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
ms.openlocfilehash: f1875353e8a5b4a23302a5f008af2cfa42a89b11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361516"
---
# <a name="apijetupdate-method-jet_sesid-jet_tableid"></a><span data-ttu-id="71970-103">Método API. JetUpdate (JET_SESID, JET_TABLEID)</span><span class="sxs-lookup"><span data-stu-id="71970-103">Api.JetUpdate method (JET_SESID, JET_TABLEID)</span></span>

<span data-ttu-id="71970-104">La función JetUpdate realiza una operación de actualización que incluye la inserción de una nueva fila en una tabla o la actualización de una fila existente.</span><span class="sxs-lookup"><span data-stu-id="71970-104">The JetUpdate function performs an update operation including inserting a new row into a table or updating an existing row.</span></span> <span data-ttu-id="71970-105">La eliminación de una fila de tabla se realiza mediante una llamada a [JetDelete (JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).</span><span class="sxs-lookup"><span data-stu-id="71970-105">Deleting a table row is performed by calling [JetDelete(JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).</span></span>

<span data-ttu-id="71970-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="71970-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="71970-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="71970-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="71970-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71970-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.JetUpdate(sesid, tableid)
```

``` csharp
public static void JetUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="71970-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="71970-109">Parameters</span></span>

  - <span data-ttu-id="71970-110">sesid</span><span class="sxs-lookup"><span data-stu-id="71970-110">sesid</span></span>  
    <span data-ttu-id="71970-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="71970-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="71970-112">La sesión que inició la actualización.</span><span class="sxs-lookup"><span data-stu-id="71970-112">The session which started the update.</span></span>

<!-- end list -->

  - <span data-ttu-id="71970-113">TABLEID</span><span class="sxs-lookup"><span data-stu-id="71970-113">tableid</span></span>  
    <span data-ttu-id="71970-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="71970-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="71970-115">Cursor que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="71970-115">The cursor to update.</span></span> <span data-ttu-id="71970-116">Se debe preparar una actualización.</span><span class="sxs-lookup"><span data-stu-id="71970-116">An update should be prepared.</span></span>

## <a name="remarks"></a><span data-ttu-id="71970-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="71970-117">Remarks</span></span>

<span data-ttu-id="71970-118">JetUpdate es el último paso para realizar una inserción o una actualización.</span><span class="sxs-lookup"><span data-stu-id="71970-118">JetUpdate is the final step in performing an insert or an update.</span></span> <span data-ttu-id="71970-119">La actualización se inicia llamando a [JetPrepareUpdate (JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) y llamando a [JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) una o varias veces para establecer el estado del registro.</span><span class="sxs-lookup"><span data-stu-id="71970-119">The update is begun by calling [JetPrepareUpdate(JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) and then by calling [JetSetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, \[\], Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) one or more times to set the record state.</span></span> <span data-ttu-id="71970-120">Por último, se llama a [JetUpdate (JET_SESID, JET_TABLEID, \[ \] , Int32, Int32)](./api.jetupdate-method-jet-sesid-jet-tableid-byte-int32-int32-.md) para completar la operación de actualización.</span><span class="sxs-lookup"><span data-stu-id="71970-120">Finally, [JetUpdate(JET_SESID, JET_TABLEID, \[\], Int32, Int32)](./api.jetupdate-method-jet-sesid-jet-tableid-byte-int32-int32-.md) is called to complete the update operation.</span></span> <span data-ttu-id="71970-121">Los índices solo se actualizan mediante JetUpdate o y no durante JetSetColumn.</span><span class="sxs-lookup"><span data-stu-id="71970-121">Indexes are updated only by JetUpdate or and not during JetSetColumn.</span></span>

## <a name="see-also"></a><span data-ttu-id="71970-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="71970-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="71970-123">Referencia</span><span class="sxs-lookup"><span data-stu-id="71970-123">Reference</span></span>

[<span data-ttu-id="71970-124">Clase de API</span><span class="sxs-lookup"><span data-stu-id="71970-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="71970-125">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="71970-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="71970-126">Sobrecarga JetUpdate</span><span class="sxs-lookup"><span data-stu-id="71970-126">JetUpdate overload</span></span>](./api.jetupdate-method.md)

[<span data-ttu-id="71970-127">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="71970-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
