---
description: 'Más información acerca de: JetGetInstanceInfo (función)'
title: JetGetInstanceInfo función)
TOCTitle: JetGetInstanceInfo Function
ms:assetid: ffccdac0-3631-4753-876a-90ddfdd0252f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294149(v=EXCHG.10)
ms:contentKeyID: 32765763
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceInfoW
- JetGetInstanceInfo
- JetGetInstanceInfoA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8c8e9a279f536622cfdfccb8bc8882914aeee64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911442"
---
# <a name="jetgetinstanceinfo-function"></a><span data-ttu-id="a721a-103">JetGetInstanceInfo función)</span><span class="sxs-lookup"><span data-stu-id="a721a-103">JetGetInstanceInfo Function</span></span>


<span data-ttu-id="a721a-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a721a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetinstanceinfo-function"></a><span data-ttu-id="a721a-105">JetGetInstanceInfo función)</span><span class="sxs-lookup"><span data-stu-id="a721a-105">JetGetInstanceInfo Function</span></span>

<span data-ttu-id="a721a-106">La función **JetGetInstanceInfo** recupera información sobre las instancias de que se están ejecutando.</span><span class="sxs-lookup"><span data-stu-id="a721a-106">The **JetGetInstanceInfo** function retrieves information about the instances that are running.</span></span>

<span data-ttu-id="a721a-107">**Windows XP: JetGetInstanceInfo** se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a721a-107">**Windows XP:  JetGetInstanceInfo** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetInstanceInfo(
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo
    );
```

### <a name="parameters"></a><span data-ttu-id="a721a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a721a-108">Parameters</span></span>

<span data-ttu-id="a721a-109">*pcInstanceInfo*</span><span class="sxs-lookup"><span data-stu-id="a721a-109">*pcInstanceInfo*</span></span>

<span data-ttu-id="a721a-110">Un puntero a un búfer que recibirá el número de elementos almacenados en *paInstanceInfo*.</span><span class="sxs-lookup"><span data-stu-id="a721a-110">A pointer to a buffer which will receive the number of elements stored in *paInstanceInfo*.</span></span>

<span data-ttu-id="a721a-111">*paInstanceInfo*</span><span class="sxs-lookup"><span data-stu-id="a721a-111">*paInstanceInfo*</span></span>

<span data-ttu-id="a721a-112">Un puntero a un búfer que recibirá la dirección del primer elemento de una matriz de estructuras.</span><span class="sxs-lookup"><span data-stu-id="a721a-112">A pointer to a buffer which will receive the address of the first element of an array of structures.</span></span>

### <a name="return-value"></a><span data-ttu-id="a721a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a721a-113">Return Value</span></span>

<span data-ttu-id="a721a-114">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="a721a-114">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a721a-115">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a721a-115">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a721a-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a721a-116">Return code</span></span></p></th>
<th><p><span data-ttu-id="a721a-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="a721a-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a721a-118">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a721a-118">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a721a-119">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="a721a-119">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a721a-120">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="a721a-120">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="a721a-121">Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro.</span><span class="sxs-lookup"><span data-stu-id="a721a-121">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="a721a-122">Este error lo devolverá <strong>JetGetInstanceInfo</strong> cuando:</span><span class="sxs-lookup"><span data-stu-id="a721a-122">This error will be returned by <strong>JetGetInstanceInfo</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="a721a-123"><em>pcInstanceInfo</em> o <em>paInstanceInfo</em> son NULL.</span><span class="sxs-lookup"><span data-stu-id="a721a-123"><em>pcInstanceInfo</em> or <em>paInstanceInfo</em> are NULL.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a721a-124">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="a721a-124">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="a721a-125">No hay memoria suficiente para procesar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a721a-125">There is insufficient memory to process the request.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="a721a-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a721a-126">Remarks</span></span>

<span data-ttu-id="a721a-127">El motor de base de datos asignará una matriz de estructuras [JET_INSTANCE_INFO](./jet-instance-info-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="a721a-127">The database engine will allocate an array of [JET_INSTANCE_INFO](./jet-instance-info-structure.md) structures.</span></span> <span data-ttu-id="a721a-128">El autor de la llamada es responsable de liberar esta memoria con [JetFreeBuffer](./jetfreebuffer-function.md).</span><span class="sxs-lookup"><span data-stu-id="a721a-128">The caller is responsible for freeing this memory with [JetFreeBuffer](./jetfreebuffer-function.md).</span></span>

<span data-ttu-id="a721a-129">Si no hay ninguna instancia activa, **JetGetInstanceInfo** devolverá JET_errSuccess y *pcInstanceInfo* recibirá un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="a721a-129">If there are no active instances, **JetGetInstanceInfo** will return JET_errSuccess, and *pcInstanceInfo* will receive a value of 0.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a721a-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a721a-130">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a721a-131"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="a721a-131"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a721a-132">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a721a-132">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a721a-133"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a721a-133"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a721a-134">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a721a-134">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a721a-135"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="a721a-135"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a721a-136">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="a721a-136">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a721a-137"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="a721a-137"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a721a-138">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a721a-138">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a721a-139"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a721a-139"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a721a-140">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a721a-140">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a721a-141"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="a721a-141"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="a721a-142">Se implementa como <strong>JetGetInstanceInfoW</strong> (Unicode) y <strong>JetGetInstanceInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="a721a-142">Implemented as <strong>JetGetInstanceInfoW</strong> (Unicode) and <strong>JetGetInstanceInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a721a-143">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a721a-143">See Also</span></span>

[<span data-ttu-id="a721a-144">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a721a-144">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a721a-145">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="a721a-145">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="a721a-146">JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="a721a-146">JET_INSTANCE_INFO</span></span>](./jet-instance-info-structure.md)  
[<span data-ttu-id="a721a-147">JetFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="a721a-147">JetFreeBuffer</span></span>](./jetfreebuffer-function.md)
