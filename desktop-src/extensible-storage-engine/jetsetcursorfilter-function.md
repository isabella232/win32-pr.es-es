---
description: 'Más información acerca de: JetSetCursorFilter (función)'
title: JetSetCursorFilter función)
TOCTitle: JetSetCursorFilter Function
ms:assetid: 3cea5beb-2cf8-4053-8e7f-7b8645580ef0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835040(v=EXCHG.10)
ms:contentKeyID: 49894662
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetSetCursorFilter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad589fecb190ad0f0676325b78adc7c96028a3fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154004"
---
# <a name="jetsetcursorfilter-function"></a><span data-ttu-id="dc8e2-103">JetSetCursorFilter función)</span><span class="sxs-lookup"><span data-stu-id="dc8e2-103">JetSetCursorFilter Function</span></span>


<span data-ttu-id="dc8e2-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="dc8e2-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="dc8e2-105">La función **JetSetCursorFilter** establece una matriz de filtros simples para la función [JetMove](./jetmove-function.md) .</span><span class="sxs-lookup"><span data-stu-id="dc8e2-105">The **JetSetCursorFilter** function sets an array of simple filters for the [JetMove](./jetmove-function.md) function.</span></span>

<span data-ttu-id="dc8e2-106">La función **JetSetCursorFilter** se presentó en el sistema operativo Windows 8.</span><span class="sxs-lookup"><span data-stu-id="dc8e2-106">The **JetSetCursorFilter** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetSetCursorFilter(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in_ecount(cFilters)  JET_INDEX_COLUMN* rgFilters,
  __in          DWORD cFilters,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="dc8e2-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dc8e2-107">Parameters</span></span>

<span data-ttu-id="dc8e2-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="dc8e2-108">*sesid*</span></span>

<span data-ttu-id="dc8e2-109">Contexto de sesión de base de datos que se va a usar para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="dc8e2-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="dc8e2-110">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="dc8e2-110">*tableid*</span></span>

<span data-ttu-id="dc8e2-111">Cursor que se va a colocar.</span><span class="sxs-lookup"><span data-stu-id="dc8e2-111">The cursor to position.</span></span>

<span data-ttu-id="dc8e2-112">*rgFilters*</span><span class="sxs-lookup"><span data-stu-id="dc8e2-112">*rgFilters*</span></span>

<span data-ttu-id="dc8e2-113">Filtros de registro simples.</span><span class="sxs-lookup"><span data-stu-id="dc8e2-113">The simple record filters.</span></span>

<span data-ttu-id="dc8e2-114">*cFilters*</span><span class="sxs-lookup"><span data-stu-id="dc8e2-114">*cFilters*</span></span>

<span data-ttu-id="dc8e2-115">Número de filtros.</span><span class="sxs-lookup"><span data-stu-id="dc8e2-115">The number of filters.</span></span>

<span data-ttu-id="dc8e2-116">*grbit*</span><span class="sxs-lookup"><span data-stu-id="dc8e2-116">*grbit*</span></span>

<span data-ttu-id="dc8e2-117">Grupo de bits que especifica cero o más de las opciones de movimiento que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="dc8e2-117">A group of bits that specifies zero or more of the move options listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dc8e2-118">Value</span><span class="sxs-lookup"><span data-stu-id="dc8e2-118">Value</span></span></p></th>
<th><p><span data-ttu-id="dc8e2-119">Significado</span><span class="sxs-lookup"><span data-stu-id="dc8e2-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc8e2-120">Ninguno</span><span class="sxs-lookup"><span data-stu-id="dc8e2-120">None</span></span></p></td>
<td><p><span data-ttu-id="dc8e2-121">Opciones predeterminadas</span><span class="sxs-lookup"><span data-stu-id="dc8e2-121">Default option.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="dc8e2-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dc8e2-122">Return value</span></span>

<span data-ttu-id="dc8e2-123">Esta función devuelve el tipo de datos [JET_ERR](./jet-err.md) con uno de los códigos de retorno que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="dc8e2-123">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="dc8e2-124">Para obtener más información sobre los posibles errores del motor de almacenamiento extensible (ESE), vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="dc8e2-124">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dc8e2-125">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="dc8e2-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="dc8e2-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc8e2-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc8e2-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="dc8e2-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="dc8e2-128">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="dc8e2-128">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="dc8e2-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc8e2-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc8e2-130"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="dc8e2-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="dc8e2-131">Requiere Windows 8.</span><span class="sxs-lookup"><span data-stu-id="dc8e2-131">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc8e2-132"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="dc8e2-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="dc8e2-133">Requiere Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="dc8e2-133">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc8e2-134"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="dc8e2-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="dc8e2-135">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="dc8e2-135">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc8e2-136"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="dc8e2-136"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="dc8e2-137">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="dc8e2-137">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc8e2-138"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="dc8e2-138"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="dc8e2-139">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="dc8e2-139">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="dc8e2-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc8e2-140">See also</span></span>

[<span data-ttu-id="dc8e2-141">JetMove</span><span class="sxs-lookup"><span data-stu-id="dc8e2-141">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="dc8e2-142">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="dc8e2-142">JET_ERR</span></span>](./jet-err.md)
