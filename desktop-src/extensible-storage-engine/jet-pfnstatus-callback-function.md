---
description: 'Más información acerca de: JET_PFNSTATUS función de devolución de llamada'
title: JET_PFNSTATUS función de devolución de llamada
TOCTitle: JET_PFNSTATUS Callback Function
ms:assetid: 8b0cf5bf-a4ee-4d8f-8dd7-556c35cd269d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269326(v=EXCHG.10)
ms:contentKeyID: 32765616
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
ms.openlocfilehash: c5f3eb374580dc6bed752900434706b66c6623b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277863"
---
# <a name="jet_pfnstatus-callback-function"></a><span data-ttu-id="5dc76-103">JET_PFNSTATUS función de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="5dc76-103">JET_PFNSTATUS Callback Function</span></span>


<span data-ttu-id="5dc76-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5dc76-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_pfnstatus-callback-function"></a><span data-ttu-id="5dc76-105">JET_PFNSTATUS función de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="5dc76-105">JET_PFNSTATUS Callback Function</span></span>

<span data-ttu-id="5dc76-106">La función de devolución de llamada **JET_PFNSTATUS** recibe información sobre el progreso de las operaciones de ejecución prolongada, como la desfragmentación, la copia de seguridad o las operaciones de restauración.</span><span class="sxs-lookup"><span data-stu-id="5dc76-106">The **JET_PFNSTATUS** callback function receives information about the progress of long-running operations, such as defragmentation, backup, or restore operations.</span></span> <span data-ttu-id="5dc76-107">Durante estas operaciones, el motor de base de datos llama a esta función de devolución de llamada para proporcionar una actualización en el progreso de la operación.</span><span class="sxs-lookup"><span data-stu-id="5dc76-107">During such operations, the database engine calls this callback function to give an update on the progress of the operation.</span></span>

```cpp
    JET_ERR JET_API JET_PFNSTATUS(
                           JET_SESID  sesid,
                           JET_SNP snp,
                           JET_SNT snt,
                           void* pv
    );
```

### <a name="parameters"></a><span data-ttu-id="5dc76-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5dc76-108">Parameters</span></span>

<span data-ttu-id="5dc76-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="5dc76-109">*sesid*</span></span>

<span data-ttu-id="5dc76-110">Sesión de tipo [JET_SESID](./jet-sesid.md) con la que se llamó a la función de ejecución prolongada.</span><span class="sxs-lookup"><span data-stu-id="5dc76-110">The session of type [JET_SESID](./jet-sesid.md) with which the long-running function was called.</span></span>

<span data-ttu-id="5dc76-111">*SNP*</span><span class="sxs-lookup"><span data-stu-id="5dc76-111">*snp*</span></span>

<span data-ttu-id="5dc76-112">El tipo de operación tal y como se especifica en [JET_SNP](./jet-snp.md).</span><span class="sxs-lookup"><span data-stu-id="5dc76-112">The type of operation as specified in [JET_SNP](./jet-snp.md).</span></span> <span data-ttu-id="5dc76-113">Entre los tipos de operaciones se incluyen reparación, compactación, restauración, copia de seguridad, actualización, limpieza y actualización del formato de registro.</span><span class="sxs-lookup"><span data-stu-id="5dc76-113">Types of operations include repair, compact, restore, backup, update, scrub, and update the record format.</span></span>

<span data-ttu-id="5dc76-114">*SNT*</span><span class="sxs-lookup"><span data-stu-id="5dc76-114">*snt*</span></span>

<span data-ttu-id="5dc76-115">Estado de una operación.</span><span class="sxs-lookup"><span data-stu-id="5dc76-115">The status of an operation.</span></span> <span data-ttu-id="5dc76-116">Los tipos de estado incluyen Inicio, en curso, finalización o error.</span><span class="sxs-lookup"><span data-stu-id="5dc76-116">Status types include beginning, in progress, completion, or failure.</span></span> <span data-ttu-id="5dc76-117">El estado se especificará con el tercer parámetro de tipo [JET_SNT](./jet-snt.md).</span><span class="sxs-lookup"><span data-stu-id="5dc76-117">The status will be specified with the third parameter of type [JET_SNT](./jet-snt.md).</span></span>

<span data-ttu-id="5dc76-118">*FV*</span><span class="sxs-lookup"><span data-stu-id="5dc76-118">*pv*</span></span>

<span data-ttu-id="5dc76-119">Puntero opcional a una estructura de tipo [JET_SNPROG](./jet-snprog-structure.md).</span><span class="sxs-lookup"><span data-stu-id="5dc76-119">An optional pointer to a structure of type [JET_SNPROG](./jet-snprog-structure.md).</span></span>

### <a name="return-value"></a><span data-ttu-id="5dc76-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5dc76-120">Return Value</span></span>

<span data-ttu-id="5dc76-121">Esta función devuelve el tipo de información [JET_ERR](./jet-err.md) con uno de los [códigos de error del motor de almacenamiento extensible](./extensible-storage-engine-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5dc76-121">This function returns the [JET_ERR](./jet-err.md) datatype with one of the [Extensible Storage Engine error codes](./extensible-storage-engine-error-codes.md).</span></span> <span data-ttu-id="5dc76-122">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="5dc76-122">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<span data-ttu-id="5dc76-123">Si se ejecuta correctamente, la operación que emitió la devolución de llamada puede continuar con normalidad.</span><span class="sxs-lookup"><span data-stu-id="5dc76-123">On success, the operation that issued the callback can proceed normally.</span></span> <span data-ttu-id="5dc76-124">En algunos casos, la devolución de llamada podría devolver una advertencia que influye en esa operación.</span><span class="sxs-lookup"><span data-stu-id="5dc76-124">In some cases, the callback might return a warning that influences that operation.</span></span>

<span data-ttu-id="5dc76-125">En caso de error, la operación que emitió la devolución de llamada podría continuar normalmente o producir un error.</span><span class="sxs-lookup"><span data-stu-id="5dc76-125">On failure, the operation that issued the callback might proceed normally or might fail.</span></span>

### <a name="remarks"></a><span data-ttu-id="5dc76-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5dc76-126">Remarks</span></span>

<span data-ttu-id="5dc76-127">Esta función de devolución de llamada se usará en una notificación de progreso en la que la estructura indicará el estado actual del progreso.</span><span class="sxs-lookup"><span data-stu-id="5dc76-127">This callback function will be used in a progress notification in which the structure will indicate the current state of the progress.</span></span> <span data-ttu-id="5dc76-128">Tenga en cuenta que es posible que se llame varias veces a la función de devolución de llamada para el progreso de la operación.</span><span class="sxs-lookup"><span data-stu-id="5dc76-128">Note that the callback function might be called multiple times for the progress of the operation.</span></span>

### <a name="requirements"></a><span data-ttu-id="5dc76-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5dc76-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5dc76-130"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="5dc76-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5dc76-131">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="5dc76-131">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dc76-132"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="5dc76-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5dc76-133">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="5dc76-133">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dc76-134"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="5dc76-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5dc76-135">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="5dc76-135">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="5dc76-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5dc76-136">See Also</span></span>

[<span data-ttu-id="5dc76-137">Códigos de error del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="5dc76-137">Extensible Storage Engine error codes</span></span>](./extensible-storage-engine-error-codes.md)  
[<span data-ttu-id="5dc76-138">Errores del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="5dc76-138">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="5dc76-139">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="5dc76-139">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="5dc76-140">JET_SNP</span><span class="sxs-lookup"><span data-stu-id="5dc76-140">JET_SNP</span></span>](./jet-snp.md)  
[<span data-ttu-id="5dc76-141">JET_SNPROG</span><span class="sxs-lookup"><span data-stu-id="5dc76-141">JET_SNPROG</span></span>](./jet-snprog-structure.md)  
[<span data-ttu-id="5dc76-142">JET_SNT</span><span class="sxs-lookup"><span data-stu-id="5dc76-142">JET_SNT</span></span>](./jet-snt.md)
