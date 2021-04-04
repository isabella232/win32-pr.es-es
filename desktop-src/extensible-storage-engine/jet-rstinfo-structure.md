---
description: 'Más información acerca de: estructura de JET_RSTINFO'
title: Estructura de JET_RSTINFO
TOCTitle: JET_RSTINFO Structure
ms:assetid: 2f144d68-dcd9-4d0d-9d9e-a7d2a5c350fe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269216(v=EXCHG.10)
ms:contentKeyID: 32765519
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
ms.openlocfilehash: 3a776c84d89dfc97272c65bb0c0684faba814fdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154020"
---
# <a name="jet_rstinfo-structure"></a><span data-ttu-id="5a87d-103">Estructura de JET_RSTINFO</span><span class="sxs-lookup"><span data-stu-id="5a87d-103">JET_RSTINFO Structure</span></span>


<span data-ttu-id="5a87d-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5a87d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_rstinfo-structure"></a><span data-ttu-id="5a87d-105">Estructura de JET_RSTINFO</span><span class="sxs-lookup"><span data-stu-id="5a87d-105">JET_RSTINFO Structure</span></span>

<span data-ttu-id="5a87d-106">La estructura **JET_RSTINFO** contiene información sobre el control del proceso de recuperación, como la información de reubicación de la base de datos y la capacidad de controlar la detención de la recuperación.</span><span class="sxs-lookup"><span data-stu-id="5a87d-106">The **JET_RSTINFO** structure contains control information for the recovery process like database relocation information and ability to control stopping recovery.</span></span>

<span data-ttu-id="5a87d-107">**Windows Vista:** La estructura de **JET_RSTINFO** se introduce en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5a87d-107">**Windows Vista:** The **JET_RSTINFO** structure is introduced in Windows Vista.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_RSTMAP* rgrstmap;
      long crstmap;
      JET_LGPOS lgposStop;
      JET_LOGTIME logtimeStop;
      JET_PFNSTATUS pfnStatus;
    } JET_RSTINFO;
```

### <a name="members"></a><span data-ttu-id="5a87d-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="5a87d-108">Members</span></span>

<span data-ttu-id="5a87d-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="5a87d-109">**cbStruct**</span></span>

<span data-ttu-id="5a87d-110">Tamaño de la estructura.</span><span class="sxs-lookup"><span data-stu-id="5a87d-110">The size of the structure.</span></span>

<span data-ttu-id="5a87d-111">**rgrstmap**</span><span class="sxs-lookup"><span data-stu-id="5a87d-111">**rgrstmap**</span></span>

<span data-ttu-id="5a87d-112">La estructura que describe la ruta de acceso antigua y nueva de una base de datos restaurada.</span><span class="sxs-lookup"><span data-stu-id="5a87d-112">The structure that describes the old and new path of a restored database.</span></span>

<span data-ttu-id="5a87d-113">**crstmap**</span><span class="sxs-lookup"><span data-stu-id="5a87d-113">**crstmap**</span></span>

<span data-ttu-id="5a87d-114">Recuento de entradas de matriz en rgrstmap.</span><span class="sxs-lookup"><span data-stu-id="5a87d-114">Count of array entries in the rgrstmap.</span></span>

<span data-ttu-id="5a87d-115">**lgposStop**</span><span class="sxs-lookup"><span data-stu-id="5a87d-115">**lgposStop**</span></span>

<span data-ttu-id="5a87d-116">La posición del registro en la que detener la recuperación.</span><span class="sxs-lookup"><span data-stu-id="5a87d-116">The log position to stop recovery at.</span></span> <span data-ttu-id="5a87d-117">No se realizará la operación de deshacer.</span><span class="sxs-lookup"><span data-stu-id="5a87d-117">No undo will be done.</span></span>

<span data-ttu-id="5a87d-118">**logtimeStop**</span><span class="sxs-lookup"><span data-stu-id="5a87d-118">**logtimeStop**</span></span>

<span data-ttu-id="5a87d-119">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="5a87d-119">Reserved for future use.</span></span>

<span data-ttu-id="5a87d-120">**pfnStatus**</span><span class="sxs-lookup"><span data-stu-id="5a87d-120">**pfnStatus**</span></span>

<span data-ttu-id="5a87d-121">Función de estado para notificar el estado de recuperación.</span><span class="sxs-lookup"><span data-stu-id="5a87d-121">A status function for reporting status of recovery.</span></span>

### <a name="requirements"></a><span data-ttu-id="5a87d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a87d-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5a87d-123"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="5a87d-123"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5a87d-124">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="5a87d-124">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a87d-125"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="5a87d-125"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5a87d-126">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="5a87d-126">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5a87d-127"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="5a87d-127"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5a87d-128">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="5a87d-128">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5a87d-129"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="5a87d-129"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="5a87d-130">Se implementa como <strong>JET_RSTINFO_W</strong> (Unicode) y <strong>JET_RSTINFO_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="5a87d-130">Implemented as <strong>JET_RSTINFO_W</strong> (Unicode) and <strong>JET_RSTINFO_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="5a87d-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5a87d-131">See Also</span></span>

[<span data-ttu-id="5a87d-132">JetInit3</span><span class="sxs-lookup"><span data-stu-id="5a87d-132">JetInit3</span></span>](./jetinit3-function.md)
