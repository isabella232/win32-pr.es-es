---
description: 'Más información acerca de: JET_LS'
title: JET_LS
TOCTitle: JET_LS
ms:assetid: 8e4e7902-84b1-404b-8654-bb430a0952aa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269336(v=EXCHG.10)
ms:contentKeyID: 32765625
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3300fd88c0dd1e1fca55722bf58350e28f3c3b08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716531"
---
# <a name="jet_ls"></a><span data-ttu-id="c88dc-103">JET_LS</span><span class="sxs-lookup"><span data-stu-id="c88dc-103">JET_LS</span></span>


<span data-ttu-id="c88dc-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c88dc-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_ls"></a><span data-ttu-id="c88dc-105">JET_LS</span><span class="sxs-lookup"><span data-stu-id="c88dc-105">JET_LS</span></span>

<span data-ttu-id="c88dc-106">El tipo de datos **JET_LS** contiene un identificador de contexto para el almacenamiento local (LS). Este identificador puede estar asociado a un cursor o una tabla y puede hacer referencia a recursos asignados dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="c88dc-106">The **JET_LS** data type contains a context handle to local storage (LS).This handle might be associated with a cursor or a table and might refer to dynamically allocated resources.</span></span>

<span data-ttu-id="c88dc-107">**Windows XP: JET_LS** se presenta en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c88dc-107">**Windows XP:  JET_LS** is introduced in Windows XP.</span></span>

```cpp
    typedef JET_API_PTR JET_LS;
```

### <a name="data-types"></a><span data-ttu-id="c88dc-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c88dc-108">Data Types</span></span>

<span data-ttu-id="c88dc-109">JET_LS</span><span class="sxs-lookup"><span data-stu-id="c88dc-109">JET_LS</span></span>

<span data-ttu-id="c88dc-110">Un valor de JET_LSNil indica un identificador de contexto no válido.</span><span class="sxs-lookup"><span data-stu-id="c88dc-110">A value of JET_LSNil indicates an invalid context handle.</span></span>

### <a name="remarks"></a><span data-ttu-id="c88dc-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c88dc-111">Remarks</span></span>

<span data-ttu-id="c88dc-112">Un identificador de contexto se asocia inicialmente con el tipo de datos **JET_LS** , mediante [JetSetLS](./jetsetls-function.md).</span><span class="sxs-lookup"><span data-stu-id="c88dc-112">A context handle is initially associated with the **JET_LS** data type, using [JetSetLS](./jetsetls-function.md).</span></span> <span data-ttu-id="c88dc-113">El identificador de contexto se puede recuperar desde el tipo de datos **JET_LS** , mediante [JetGetLS](./jetgetls-function.md).</span><span class="sxs-lookup"><span data-stu-id="c88dc-113">The context handle can be retrieved from the **JET_LS** data type, using [JetGetLS](./jetgetls-function.md).</span></span>

<span data-ttu-id="c88dc-114">El identificador de contexto se puede desasociar explícitamente del tipo de datos **JET_LS** mediante [JetGetLS](./jetgetls-function.md) con JET_bitLSReset.</span><span class="sxs-lookup"><span data-stu-id="c88dc-114">The context handle can be explicitly disassociated from the **JET_LS** data type using [JetGetLS](./jetgetls-function.md) with JET_bitLSReset.</span></span> <span data-ttu-id="c88dc-115">También se puede desasociar implícitamente el identificador de contexto del tipo de datos **JET_LS** cuando el motor de base de datos libera el objeto subyacente como resultado de una acción directa o indirecta de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c88dc-115">Alternatively, the context handle can be implicitly disassociated from the **JET_LS** data type when the underlying object is released by the database engine as a result of direct or indirect action by the application.</span></span> <span data-ttu-id="c88dc-116">En el caso implícito, se emite una devolución de llamada en tiempo de ejecución a la aplicación para que pueda limpiar el identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="c88dc-116">In the implicit case, a runtime callback is issued to the application so that it can clean up the context handle.</span></span> <span data-ttu-id="c88dc-117">Para obtener más información sobre la desasociación implícita del tipo de datos **JET_LS** , vea [JetSetLS](./jetsetls-function.md).</span><span class="sxs-lookup"><span data-stu-id="c88dc-117">For more information on implicitly disassociating from the **JET_LS** data type, see [JetSetLS](./jetsetls-function.md).</span></span>

<span data-ttu-id="c88dc-118">Las siguientes marcas están asociadas al tipo de datos JET_LS.</span><span class="sxs-lookup"><span data-stu-id="c88dc-118">The following flags are associated with the JET_LS data type.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c88dc-119">Término</span><span class="sxs-lookup"><span data-stu-id="c88dc-119">Term</span></span></p></th>
<th><p><span data-ttu-id="c88dc-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="c88dc-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c88dc-121">JET_bitLSReset</span><span class="sxs-lookup"><span data-stu-id="c88dc-121">JET_bitLSReset</span></span></p></td>
<td><p><span data-ttu-id="c88dc-122">El identificador de contexto se ha desasociado del objeto.</span><span class="sxs-lookup"><span data-stu-id="c88dc-122">The context handle is disassociated from the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c88dc-123">JET_bitLSCursor</span><span class="sxs-lookup"><span data-stu-id="c88dc-123">JET_bitLSCursor</span></span></p></td>
<td><p><span data-ttu-id="c88dc-124">Establezca o recupere el almacenamiento local asociado a un cursor de tabla.</span><span class="sxs-lookup"><span data-stu-id="c88dc-124">Set or retrieve the local storage associated with a table cursor.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c88dc-125">JET_bitLSTable</span><span class="sxs-lookup"><span data-stu-id="c88dc-125">JET_bitLSTable</span></span></p></td>
<td><p><span data-ttu-id="c88dc-126">Establezca o recupere el almacenamiento local asociado a una tabla.</span><span class="sxs-lookup"><span data-stu-id="c88dc-126">Set or retrieve the local storage associated with a table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c88dc-127">JET_LSNil</span><span class="sxs-lookup"><span data-stu-id="c88dc-127">JET_LSNil</span></span></p></td>
<td><p><span data-ttu-id="c88dc-128">El identificador de contexto no es válido.</span><span class="sxs-lookup"><span data-stu-id="c88dc-128">The context handle is invalid.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="c88dc-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c88dc-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c88dc-130"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="c88dc-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c88dc-131">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c88dc-131">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c88dc-132"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c88dc-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c88dc-133">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c88dc-133">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c88dc-134"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="c88dc-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c88dc-135">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="c88dc-135">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="c88dc-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c88dc-136">See Also</span></span>

[<span data-ttu-id="c88dc-137">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="c88dc-137">JetSetLS</span></span>](./jetsetls-function.md)  
[<span data-ttu-id="c88dc-138">JetGetLS</span><span class="sxs-lookup"><span data-stu-id="c88dc-138">JetGetLS</span></span>](./jetgetls-function.md)
