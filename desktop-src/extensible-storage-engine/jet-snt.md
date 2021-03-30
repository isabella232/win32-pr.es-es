---
description: 'Más información acerca de: JET_SNT'
title: JET_SNT
TOCTitle: JET_SNT
ms:assetid: 74ac5142-8102-4dd3-8f2a-786a7a2ac78f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269294(v=EXCHG.10)
ms:contentKeyID: 32765586
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
ms.openlocfilehash: 5d1d4fa75c8a41528e9868bc94fa638042d01cff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275195"
---
# <a name="jet_snt"></a><span data-ttu-id="36440-103">JET_SNT</span><span class="sxs-lookup"><span data-stu-id="36440-103">JET_SNT</span></span>


<span data-ttu-id="36440-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="36440-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_snt"></a><span data-ttu-id="36440-105">JET_SNT</span><span class="sxs-lookup"><span data-stu-id="36440-105">JET_SNT</span></span>

<span data-ttu-id="36440-106">El [JET_SNT]() grupo de constantes describe los puntos del progreso de una operación sobre qué información se solicita en una llamada a la función de devolución de llamada [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) .</span><span class="sxs-lookup"><span data-stu-id="36440-106">The [JET_SNT]() group of constants describe the points of the progress of an operation about which information is requested in a call to the [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) callback function.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="36440-107">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="36440-107">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="36440-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="36440-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="36440-109">JET_sntBegin</span><span class="sxs-lookup"><span data-stu-id="36440-109">JET_sntBegin</span></span><br />
<span data-ttu-id="36440-110">5</span><span class="sxs-lookup"><span data-stu-id="36440-110">5</span></span></p></td>
<td><p><span data-ttu-id="36440-111">Inicio de una operación</span><span class="sxs-lookup"><span data-stu-id="36440-111">The beginning of an operation</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36440-112">JET_sntRequirements</span><span class="sxs-lookup"><span data-stu-id="36440-112">JET_sntRequirements</span></span><br />
<span data-ttu-id="36440-113">7</span><span class="sxs-lookup"><span data-stu-id="36440-113">7</span></span></p></td>
<td><p><span data-ttu-id="36440-114">No se admite.</span><span class="sxs-lookup"><span data-stu-id="36440-114">Not supported.</span></span></p>
<p><span data-ttu-id="36440-115"><strong>Windows 2000 Server:</strong>  La operación se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="36440-115"><strong>Windows 2000 Server:</strong>  The operation is started.</span></span> <span data-ttu-id="36440-116">En este caso, el último parámetro de la función de devolución de llamada debe ser un puntero válido a una estructura de <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> que indique el número total de unidades que se van a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="36440-116">In this case, the last parameter of the callback function should be a valid pointer to a <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> structure indicating the total number of units to be executed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36440-117">JET_sntProgress</span><span class="sxs-lookup"><span data-stu-id="36440-117">JET_sntProgress</span></span><br />
<span data-ttu-id="36440-118">0</span><span class="sxs-lookup"><span data-stu-id="36440-118">0</span></span></p></td>
<td><p><span data-ttu-id="36440-119">El número de unidades completadas y el número de unidades que se deben realizar todavía.</span><span class="sxs-lookup"><span data-stu-id="36440-119">The number of units completed and number of units yet to be done.</span></span> <span data-ttu-id="36440-120">Esta información se devuelve en los miembros de una estructura de <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> .</span><span class="sxs-lookup"><span data-stu-id="36440-120">This information is returned in the members of a <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36440-121">JET_sntComplete</span><span class="sxs-lookup"><span data-stu-id="36440-121">JET_sntComplete</span></span><br />
<span data-ttu-id="36440-122">6</span><span class="sxs-lookup"><span data-stu-id="36440-122">6</span></span></p></td>
<td><p><span data-ttu-id="36440-123">Finalización de una operación.</span><span class="sxs-lookup"><span data-stu-id="36440-123">The completion of an operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36440-124">JET_sntFail</span><span class="sxs-lookup"><span data-stu-id="36440-124">JET_sntFail</span></span><br />
<span data-ttu-id="36440-125">3</span><span class="sxs-lookup"><span data-stu-id="36440-125">3</span></span></p></td>
<td><p><span data-ttu-id="36440-126">Error de una operación.</span><span class="sxs-lookup"><span data-stu-id="36440-126">The failure of an operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36440-127">JET_sntRecoveryStep</span><span class="sxs-lookup"><span data-stu-id="36440-127">JET_sntRecoveryStep</span></span><br />
<span data-ttu-id="36440-128">8</span><span class="sxs-lookup"><span data-stu-id="36440-128">8</span></span></p></td>
<td><p><span data-ttu-id="36440-129">Control de recuperación de una operación.</span><span class="sxs-lookup"><span data-stu-id="36440-129">The recovery control of an operation.</span></span></p>
<div class="alert">

> [!NOTE]
> <P><span data-ttu-id="36440-130">Este valor no es aplicable a las versiones del sistema operativo Windows a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="36440-130">This value is not applicable to versions of the Windows operating system starting with Windows 8.</span></span></P>


</div></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="36440-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36440-131">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="36440-132"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="36440-132"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="36440-133">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="36440-133">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36440-134"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="36440-134"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="36440-135">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="36440-135">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36440-136"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="36440-136"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="36440-137">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="36440-137">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="36440-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="36440-138">See Also</span></span>

[<span data-ttu-id="36440-139">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="36440-139">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="36440-140">JET_SNP</span><span class="sxs-lookup"><span data-stu-id="36440-140">JET_SNP</span></span>](./jet-snp.md)  
[<span data-ttu-id="36440-141">JET_SNPROG</span><span class="sxs-lookup"><span data-stu-id="36440-141">JET_SNPROG</span></span>](./jet-snprog-structure.md)
