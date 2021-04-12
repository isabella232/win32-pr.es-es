---
description: 'Más información acerca de: JET_PFNREALLOC función de devolución de llamada'
title: JET_PFNREALLOC función de devolución de llamada
TOCTitle: JET_PFNREALLOC Callback Function
ms:assetid: 443d0b7e-1c3b-4584-9bc3-938724527313
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269237(v=EXCHG.10)
ms:contentKeyID: 32765539
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
ms.openlocfilehash: 032c1edcfd18166b79f4c8b2868d53d0b84434d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279400"
---
# <a name="jet_pfnrealloc-callback-function"></a><span data-ttu-id="22b77-103">JET_PFNREALLOC función de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="22b77-103">JET_PFNREALLOC Callback Function</span></span>


<span data-ttu-id="22b77-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="22b77-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_pfnrealloc-callback-function"></a><span data-ttu-id="22b77-105">JET_PFNREALLOC función de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="22b77-105">JET_PFNREALLOC Callback Function</span></span>

<span data-ttu-id="22b77-106">La función JET_PFNREALLOC es una devolución de llamada compatible con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) usada por [JetEnumerateColumns](./jetenumeratecolumns-function.md) para asignar memoria para sus búferes de salida.</span><span class="sxs-lookup"><span data-stu-id="22b77-106">The JET_PFNREALLOC function is a [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback used by [JetEnumerateColumns](./jetenumeratecolumns-function.md) to allocate memory for its output buffers.</span></span>

```cpp
    void * JET_API JET_PFNREALLOC(
      [in]                 void* pvContext,
      [in]                 void* pv,
      [in]                 unsigned long cb
    );
```

### <a name="parameters"></a><span data-ttu-id="22b77-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="22b77-107">Parameters</span></span>

<span data-ttu-id="22b77-108">*pvContext*</span><span class="sxs-lookup"><span data-stu-id="22b77-108">*pvContext*</span></span>

<span data-ttu-id="22b77-109">El puntero de contexto dado a [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="22b77-109">The context pointer given to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span> <span data-ttu-id="22b77-110">Este puntero de contexto se puede usar para transmitir el estado del llamador de [JetEnumerateColumns](./jetenumeratecolumns-function.md) a la implementación de esta devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="22b77-110">This context pointer can be used to convey state from the caller of [JetEnumerateColumns](./jetenumeratecolumns-function.md) to the implementation of this callback.</span></span>

<span data-ttu-id="22b77-111">*FV*</span><span class="sxs-lookup"><span data-stu-id="22b77-111">*pv*</span></span>

<span data-ttu-id="22b77-112">Si no es NULL, especifica un puntero a un bloque de memoria asignado previamente por esta devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="22b77-112">If non-NULL, specifies a pointer to a memory block previously allocated by this callback.</span></span> <span data-ttu-id="22b77-113">Si es NULL, se asignará un nuevo bloque de memoria del tamaño solicitado.</span><span class="sxs-lookup"><span data-stu-id="22b77-113">If NULL, a new memory block of the requested size will be allocated.</span></span>

<span data-ttu-id="22b77-114">*CB*</span><span class="sxs-lookup"><span data-stu-id="22b77-114">*cb*</span></span>

<span data-ttu-id="22b77-115">Nuevo tamaño del bloque de memoria en bytes.</span><span class="sxs-lookup"><span data-stu-id="22b77-115">The new size of the memory block in bytes.</span></span> <span data-ttu-id="22b77-116">Si este parámetro es 0 (cero) y se especifica un bloque de memoria, el bloque de memoria se liberará.</span><span class="sxs-lookup"><span data-stu-id="22b77-116">If this parameter is 0 (zero) and a memory block is specified, that memory block will be freed.</span></span>

### <a name="return-value"></a><span data-ttu-id="22b77-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="22b77-117">Return Value</span></span>

<span data-ttu-id="22b77-118">El sistema puede generar códigos de éxito o error como resultado de una llamada a esta función.</span><span class="sxs-lookup"><span data-stu-id="22b77-118">The system may generate success or failure codes as a result of a call to this function.</span></span> <span data-ttu-id="22b77-119">Para obtener información sobre cómo devolver estos códigos como valores HRESULT, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md).</span><span class="sxs-lookup"><span data-stu-id="22b77-119">For information about how to return these codes as HRESULTs, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="22b77-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="22b77-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="22b77-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="22b77-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="22b77-122">Correcto</span><span class="sxs-lookup"><span data-stu-id="22b77-122">Success</span></span></p></td>
<td><p><span data-ttu-id="22b77-123">Si se especificó un bloque de memoria asignado previamente y se especificó un nuevo tamaño de cero, se liberará ese bloque y se devolverá NULL.</span><span class="sxs-lookup"><span data-stu-id="22b77-123">If a previously allocated memory block was specified and a new size of zero was specified then that block is freed and NULL will be returned.</span></span> <span data-ttu-id="22b77-124">Si se especificó un bloque de memoria asignado previamente y se especificó un nuevo tamaño distinto de cero, se devuelve el bloque de memoria reasignado.</span><span class="sxs-lookup"><span data-stu-id="22b77-124">If a previously allocated memory block was specified and a non-zero new size was specified then the reallocated memory block is returned.</span></span> <span data-ttu-id="22b77-125">Si no se especificó ningún bloque de memoria, se devuelve un bloque de memoria recién asignado del tamaño especificado.</span><span class="sxs-lookup"><span data-stu-id="22b77-125">If no memory block was specified then a newly allocated memory block of the specified size is returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22b77-126">Error</span><span class="sxs-lookup"><span data-stu-id="22b77-126">Failure</span></span></p></td>
<td><p><span data-ttu-id="22b77-127">Se devolverá NULL.</span><span class="sxs-lookup"><span data-stu-id="22b77-127">NULL will be returned.</span></span> <span data-ttu-id="22b77-128">Si se proporcionó un bloque de memoria asignado previamente, ese bloque permanecerá asignado.</span><span class="sxs-lookup"><span data-stu-id="22b77-128">If a previously allocated memory block was provided then that block will remain allocated.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="22b77-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22b77-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="22b77-130"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="22b77-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="22b77-131">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="22b77-131">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22b77-132"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="22b77-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="22b77-133">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="22b77-133">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22b77-134"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="22b77-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="22b77-135">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="22b77-135">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="22b77-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="22b77-136">See Also</span></span>

[<span data-ttu-id="22b77-137">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="22b77-137">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)
