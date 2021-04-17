---
description: 'Más información acerca de: JetFreeBuffer (función)'
title: JetFreeBuffer función)
TOCTitle: JetFreeBuffer Function
ms:assetid: f37d35f6-4bea-46ba-a334-7b8ad7a1568c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294134(v=EXCHG.10)
ms:contentKeyID: 32765748
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetFreeBuffer
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fe638e2aab1d37324a6fd6bf477a578f02b9ac58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707021"
---
# <a name="jetfreebuffer-function"></a><span data-ttu-id="cd775-103">JetFreeBuffer función)</span><span class="sxs-lookup"><span data-stu-id="cd775-103">JetFreeBuffer Function</span></span>


<span data-ttu-id="cd775-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="cd775-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetfreebuffer-function"></a><span data-ttu-id="cd775-105">JetFreeBuffer función)</span><span class="sxs-lookup"><span data-stu-id="cd775-105">JetFreeBuffer Function</span></span>

<span data-ttu-id="cd775-106">La función **JetFreeBuffer** libera memoria asignada por una llamada del motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="cd775-106">The **JetFreeBuffer** function frees memory that was allocated by a database engine call.</span></span>

<span data-ttu-id="cd775-107">**Windows XP: JetFreeBuffer** se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cd775-107">**Windows XP:  JetFreeBuffer** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetFreeBuffer(
      __in          char* pbBuf
    );
```

### <a name="parameters"></a><span data-ttu-id="cd775-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd775-108">Parameters</span></span>

<span data-ttu-id="cd775-109">*pbBuf*</span><span class="sxs-lookup"><span data-stu-id="cd775-109">*pbBuf*</span></span>

<span data-ttu-id="cd775-110">Puntero a una región de memoria que se asignó previamente mediante una llamada al motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="cd775-110">Pointer to a region of memory that was previously allocated by a call to the database engine.</span></span> <span data-ttu-id="cd775-111">**Null** es aceptable y se omitirá.</span><span class="sxs-lookup"><span data-stu-id="cd775-111">**NULL** is acceptable, and will be ignored.</span></span>

### <a name="return-value"></a><span data-ttu-id="cd775-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd775-112">Return Value</span></span>

<span data-ttu-id="cd775-113">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="cd775-113">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="cd775-114">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="cd775-114">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cd775-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="cd775-115">Return code</span></span></p></th>
<th><p><span data-ttu-id="cd775-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd775-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd775-117">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="cd775-117">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="cd775-118">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="cd775-118">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="cd775-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd775-119">Remarks</span></span>

<span data-ttu-id="cd775-120">Es un comportamiento indefinido para pasar memoria que no fue asignada por el motor de base de datos de a *pbBuf*.</span><span class="sxs-lookup"><span data-stu-id="cd775-120">It is undefined behavior to pass memory that was not allocated by the database engine in to *pbBuf*.</span></span>

#### <a name="requirements"></a><span data-ttu-id="cd775-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd775-121">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd775-122"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="cd775-122"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="cd775-123">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cd775-123">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd775-124"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="cd775-124"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="cd775-125">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="cd775-125">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd775-126"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="cd775-126"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="cd775-127">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="cd775-127">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd775-128"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="cd775-128"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="cd775-129">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="cd775-129">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd775-130"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="cd775-130"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="cd775-131">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="cd775-131">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="cd775-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="cd775-132">See Also</span></span>

[<span data-ttu-id="cd775-133">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="cd775-133">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="cd775-134">JetGetInstanceInfo</span><span class="sxs-lookup"><span data-stu-id="cd775-134">JetGetInstanceInfo</span></span>](./jetgetinstanceinfo-function.md)
