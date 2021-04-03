---
description: 'Más información acerca de: JetGetInstanceMiscInfo (función)'
title: JetGetInstanceMiscInfo función)
TOCTitle: JetGetInstanceMiscInfo Function
ms:assetid: 0bfe36fe-4ddd-442b-b934-57a7bfb28e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269183(v=EXCHG.10)
ms:contentKeyID: 32765486
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceMiscInfo
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ed63c6a5c6d3b2488f7226da0a1f23e1adb39e09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083042"
---
# <a name="jetgetinstancemiscinfo-function"></a><span data-ttu-id="2e998-103">JetGetInstanceMiscInfo función)</span><span class="sxs-lookup"><span data-stu-id="2e998-103">JetGetInstanceMiscInfo Function</span></span>


<span data-ttu-id="2e998-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="2e998-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetinstancemiscinfo-function"></a><span data-ttu-id="2e998-105">JetGetInstanceMiscInfo función)</span><span class="sxs-lookup"><span data-stu-id="2e998-105">JetGetInstanceMiscInfo Function</span></span>

<span data-ttu-id="2e998-106">La función **JetGetInstanceMiscInfo** recupera información sobre la instancia, mientras que la instancia está en línea.</span><span class="sxs-lookup"><span data-stu-id="2e998-106">The **JetGetInstanceMiscInfo** function retrieves information about the instance, while the instance is online.</span></span>

<span data-ttu-id="2e998-107">**Windows Vista: JetGetInstanceMiscInfo** se presentó en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2e998-107">**Windows Vista:  JetGetInstanceMiscInfo** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetGetInstanceMiscInfo(
      __in          JET_INSTANCE instance,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="2e998-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e998-108">Parameters</span></span>

<span data-ttu-id="2e998-109">*repetición*</span><span class="sxs-lookup"><span data-stu-id="2e998-109">*instance*</span></span>

<span data-ttu-id="2e998-110">Identifica la instancia de base de datos que se utilizará para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="2e998-110">Identifies the database instance that will be used for the API call.</span></span>

<span data-ttu-id="2e998-111">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="2e998-111">*pvResult*</span></span>

<span data-ttu-id="2e998-112">Puntero a un búfer que recibirá la información.</span><span class="sxs-lookup"><span data-stu-id="2e998-112">Pointer to a buffer that will receive the information.</span></span> <span data-ttu-id="2e998-113">El tipo de búfer depende de *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="2e998-113">The type of the buffer is dependent on *InfoLevel*.</span></span> <span data-ttu-id="2e998-114">El autor de la llamada es responsable de alinear el búfer adecuadamente.</span><span class="sxs-lookup"><span data-stu-id="2e998-114">The caller is responsible for aligning the buffer appropriately.</span></span>

<span data-ttu-id="2e998-115">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="2e998-115">*cbMax*</span></span>

<span data-ttu-id="2e998-116">Tamaño, en bytes, del búfer pasado en *pvResult*.</span><span class="sxs-lookup"><span data-stu-id="2e998-116">The size, in bytes, of the buffer passed in *pvResult*.</span></span>

<span data-ttu-id="2e998-117">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="2e998-117">*InfoLevel*</span></span>

<span data-ttu-id="2e998-118">Determina qué tipo de información se recuperará para la instancia especificada por la *instancia* de.</span><span class="sxs-lookup"><span data-stu-id="2e998-118">Determines what type of information will be retrieved for the instance specified by *instance*.</span></span> <span data-ttu-id="2e998-119">El formato de los datos almacenados en *pvResult* depende de *InfoLevel*.</span><span class="sxs-lookup"><span data-stu-id="2e998-119">The format of the data stored in *pvResult* is dependent on *InfoLevel*.</span></span>

<span data-ttu-id="2e998-120">Las siguientes opciones están disponibles para su uso con este parámetro.</span><span class="sxs-lookup"><span data-stu-id="2e998-120">The following options are available for use with this parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2e998-121">Value</span><span class="sxs-lookup"><span data-stu-id="2e998-121">Value</span></span></p></th>
<th><p><span data-ttu-id="2e998-122">Significado</span><span class="sxs-lookup"><span data-stu-id="2e998-122">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2e998-123">JET_InstanceMiscInfoLogSignature</span><span class="sxs-lookup"><span data-stu-id="2e998-123">JET_InstanceMiscInfoLogSignature</span></span></p></td>
<td><p><span data-ttu-id="2e998-124"><em>pvResult</em> se interpreta como una estructura <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a> de la secuencia de registro de transacciones asociada a esta instancia.</span><span class="sxs-lookup"><span data-stu-id="2e998-124"><em>pvResult</em> is interpreted as a <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a> structure of the transaction log sequence associated with this instance.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="2e998-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2e998-125">Return Value</span></span>

<span data-ttu-id="2e998-126">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="2e998-126">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="2e998-127">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="2e998-127">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2e998-128">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2e998-128">Return code</span></span></p></th>
<th><p><span data-ttu-id="2e998-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e998-129">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2e998-130">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="2e998-130">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="2e998-131">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="2e998-131">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e998-132">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="2e998-132">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="2e998-133">El búfer era demasiado pequeño.</span><span class="sxs-lookup"><span data-stu-id="2e998-133">The buffer was too small.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e998-134">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="2e998-134">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="2e998-135">Se especificó una <a href="gg294048(v=exchg.10).md">JET_INSTANCE</a> no válida o un <em>InfoLevel</em> no válido.</span><span class="sxs-lookup"><span data-stu-id="2e998-135">Either an invalid <a href="gg294048(v=exchg.10).md">JET_INSTANCE</a> or an invalid <em>InfoLevel</em> was specified.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="2e998-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e998-136">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2e998-137"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="2e998-137"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2e998-138">Requiere Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2e998-138">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e998-139"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="2e998-139"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2e998-140">Requiere Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="2e998-140">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e998-141"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="2e998-141"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2e998-142">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="2e998-142">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e998-143"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="2e998-143"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="2e998-144">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="2e998-144">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e998-145"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="2e998-145"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="2e998-146">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="2e998-146">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="2e998-147">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2e998-147">See Also</span></span>

[<span data-ttu-id="2e998-148">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="2e998-148">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="2e998-149">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="2e998-149">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="2e998-150">JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="2e998-150">JET_SIGNATURE</span></span>](./jet-signature-structure.md)
