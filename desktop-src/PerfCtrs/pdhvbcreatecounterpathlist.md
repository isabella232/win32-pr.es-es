---
description: La función PdhVbCreateCounterPathList muestra el cuadro de diálogo exploración de contadores de rendimiento, que permite al usuario seleccionar varios contadores de rendimiento. Cada ruta de acceso de contador seleccionada se debe leer mediante la función PdhVbGetCounterPathFromList.
ms.assetid: 8dda528f-2e06-4726-89a0-095781a2f80d
title: PdhVbCreateCounterPathList función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbCreateCounterPathList
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: bef484846507bf68d8ccfc0ad3ea10a250b83133
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909734"
---
# <a name="pdhvbcreatecounterpathlist-function"></a><span data-ttu-id="24229-104">PdhVbCreateCounterPathList función)</span><span class="sxs-lookup"><span data-stu-id="24229-104">PdhVbCreateCounterPathList function</span></span>

<span data-ttu-id="24229-105">La función **PdhVbCreateCounterPathList** muestra el cuadro de diálogo exploración de contadores de rendimiento, que permite al usuario seleccionar varios contadores de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="24229-105">The **PdhVbCreateCounterPathList** function displays the performance counter browsing dialog box, which lets the user select several performance counters.</span></span> <span data-ttu-id="24229-106">Cada ruta de acceso de contador seleccionada se debe leer mediante la función [**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md) .</span><span class="sxs-lookup"><span data-stu-id="24229-106">Each selected counter path must then be read using the [**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md) function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="24229-107">La función que se describe en este tema puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="24229-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="24229-108">En su lugar, Microsoft recomienda que use las funciones descritas en [funciones de contadores de rendimiento](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="24229-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="24229-109">La función PdhVbCreateCounterPathList ( \_ ByVal DetailLevel as Long, \_ ByVal CaptionString As String \_ ) as Long</span><span class="sxs-lookup"><span data-stu-id="24229-109">Function PdhVbCreateCounterPathList( \_ ByVal DetailLevel As Long, \_ ByVal CaptionString As String \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="24229-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="24229-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24229-111">*DetailLevel*</span><span class="sxs-lookup"><span data-stu-id="24229-111">*DetailLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="24229-112">Tipos de contadores que se van a mostrar en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="24229-112">Types of counters to be displayed in the dialog box.</span></span> <span data-ttu-id="24229-113">Use uno de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="24229-113">Use one of the following values.</span></span>



| <span data-ttu-id="24229-114">Value</span><span class="sxs-lookup"><span data-stu-id="24229-114">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="24229-115">Significado</span><span class="sxs-lookup"><span data-stu-id="24229-115">Meaning</span></span>                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PERF_DETAIL_ADVANCED"></span><span id="perf_detail_advanced"></span><dl> <span data-ttu-id="24229-116"><dt>**detalle de rendimiento \_ \_ avanzado**</dt></span><span class="sxs-lookup"><span data-stu-id="24229-116"><dt>**PERF\_DETAIL\_ADVANCED**</dt></span></span> </dl> | <span data-ttu-id="24229-117">Contadores que es probable que el usuario avanzado entienda, además de los contadores de usuario inexperto.</span><span class="sxs-lookup"><span data-stu-id="24229-117">Counters that the advanced user is likely to understand, in addition to the novice-user counters.</span></span><br/>                                            |
| <span id="PERF_DETAIL_EXPERT"></span><span id="perf_detail_expert"></span><dl> <span data-ttu-id="24229-118"><dt>**\_experto en detalles de rendimiento \_**</dt></span><span class="sxs-lookup"><span data-stu-id="24229-118"><dt>**PERF\_DETAIL\_EXPERT**</dt></span></span> </dl>       | <span data-ttu-id="24229-119">Los contadores que es probable que comprenda el desarrollador de software y el usuario experto, además de los contadores para los usuarios principiantes y avanzados.</span><span class="sxs-lookup"><span data-stu-id="24229-119">Counters that the expert user and software developer is likely to understand, in addition to the counters for the novice and advanced users.</span></span><br/> |
| <span id="PERF_DETAIL_NOVICE"></span><span id="perf_detail_novice"></span><dl> <span data-ttu-id="24229-120"><dt>**\_experto en detalles de rendimiento \_**</dt></span><span class="sxs-lookup"><span data-stu-id="24229-120"><dt>**PERF\_DETAIL\_NOVICE**</dt></span></span> </dl>       | <span data-ttu-id="24229-121">Solo los contadores que es probable que comprenda el usuario principiante.</span><span class="sxs-lookup"><span data-stu-id="24229-121">Only counters that the novice user is likely to understand.</span></span><br/>                                                                                  |
| <span id="PERF_DETAIL_WIZARD"></span><span id="perf_detail_wizard"></span><dl> <span data-ttu-id="24229-122"><dt>**\_Asistente para detalles de rendimiento \_**</dt></span><span class="sxs-lookup"><span data-stu-id="24229-122"><dt>**PERF\_DETAIL\_WIZARD**</dt></span></span> </dl>       | <span data-ttu-id="24229-123">Todos los contadores del sistema.</span><span class="sxs-lookup"><span data-stu-id="24229-123">All counters in the system.</span></span><br/>                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="24229-124">*CaptionString*</span><span class="sxs-lookup"><span data-stu-id="24229-124">*CaptionString*</span></span> 
</dt> <dd>

<span data-ttu-id="24229-125">Variable de cadena que contiene el texto que se mostrará en la barra de título del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="24229-125">String variable that contains the text that will be displayed in the caption bar of the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24229-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="24229-126">Return value</span></span>

<span data-ttu-id="24229-127">La función devuelve el número de rutas de acceso de contador que el usuario seleccionó.</span><span class="sxs-lookup"><span data-stu-id="24229-127">The function returns the number of counter paths that the user selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="24229-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24229-128">Requirements</span></span>



| <span data-ttu-id="24229-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="24229-129">Requirement</span></span> | <span data-ttu-id="24229-130">Value</span><span class="sxs-lookup"><span data-stu-id="24229-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="24229-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24229-131">Minimum supported client</span></span><br/> | <span data-ttu-id="24229-132">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="24229-132">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="24229-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24229-133">Minimum supported server</span></span><br/> | <span data-ttu-id="24229-134">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="24229-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="24229-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="24229-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="24229-136"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="24229-136"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="24229-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="24229-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24229-138"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24229-138"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24229-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="24229-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24229-140">**PdhVbGetCounterPathElements**</span><span class="sxs-lookup"><span data-stu-id="24229-140">**PdhVbGetCounterPathElements**</span></span>](pdhvbgetcounterpathelements.md)
</dt> <dt>

[<span data-ttu-id="24229-141">**PdhVbGetCounterPathFromList**</span><span class="sxs-lookup"><span data-stu-id="24229-141">**PdhVbGetCounterPathFromList**</span></span>](pdhvbgetcounterpathfromlist.md)
</dt> <dt>

[<span data-ttu-id="24229-142">**PdhVbGetOneCounterPath**</span><span class="sxs-lookup"><span data-stu-id="24229-142">**PdhVbGetOneCounterPath**</span></span>](pdhvbgetonecounterpath.md)
</dt> </dl>

 

 




