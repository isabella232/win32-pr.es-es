---
description: La función PdhVbGetOneCounterPath muestra un cuadro de diálogo que permite al usuario examinar los contadores de rendimiento disponibles y seleccionar un contador.
ms.assetid: a42406ef-70e0-464d-90f8-fef9e1c3471d
title: PdhVbGetOneCounterPath función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetOneCounterPath
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 980665372d49f483e3fb59b7571ec38fa9c2851a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909730"
---
# <a name="pdhvbgetonecounterpath-function"></a><span data-ttu-id="58073-103">PdhVbGetOneCounterPath función)</span><span class="sxs-lookup"><span data-stu-id="58073-103">PdhVbGetOneCounterPath function</span></span>

<span data-ttu-id="58073-104">La función **PdhVbGetOneCounterPath** muestra un cuadro de diálogo que permite al usuario examinar los contadores de rendimiento disponibles y seleccionar un contador.</span><span class="sxs-lookup"><span data-stu-id="58073-104">The **PdhVbGetOneCounterPath** function displays a dialog box that lets the user browse the available performance counters and select one counter.</span></span> <span data-ttu-id="58073-105">El contador seleccionado se devuelve en la variable *PathString* .</span><span class="sxs-lookup"><span data-stu-id="58073-105">The counter selected is returned in the *PathString* variable.</span></span> <span data-ttu-id="58073-106">La variable *PathString* se debe dimensionar e inicializar antes de que se llame a esta función, y la variable *PathLength* debe indicar el tamaño de la dimensión.</span><span class="sxs-lookup"><span data-stu-id="58073-106">The *PathString* variable must be dimensioned and initialized before this function is called, and the dimensioned size must be indicated by the *PathLength* variable.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="58073-107">La función que se describe en este tema puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="58073-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="58073-108">En su lugar, Microsoft recomienda que use las funciones descritas en [funciones de contadores de rendimiento](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="58073-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="58073-109">Función PdhVbGetOneCounterPath ( \_ ByVal PathString As String, \_ ByVal PathLength as Long, \_ ByVal DetailLevel as Long, \_ ByVal CaptionString As String \_ ) as Long</span><span class="sxs-lookup"><span data-stu-id="58073-109">Function PdhVbGetOneCounterPath( \_ ByVal PathString As String, \_ ByVal PathLength As Long, \_ ByVal DetailLevel As Long, \_ ByVal CaptionString As String \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="58073-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="58073-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58073-111">*PathString*</span><span class="sxs-lookup"><span data-stu-id="58073-111">*PathString*</span></span> 
</dt> <dd>

<span data-ttu-id="58073-112">Variable de cadena inicializada utilizada para recibir la ruta de acceso del contador seleccionada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="58073-112">Initialized string variable used to receive the counter path selected by the user.</span></span>

</dd> <dt>

<span data-ttu-id="58073-113">*PathLength*</span><span class="sxs-lookup"><span data-stu-id="58073-113">*PathLength*</span></span> 
</dt> <dd>

<span data-ttu-id="58073-114">Longitud del PathString inicializado.</span><span class="sxs-lookup"><span data-stu-id="58073-114">Length of the initialized PathString.</span></span>

</dd> <dt>

<span data-ttu-id="58073-115">*DetailLevel*</span><span class="sxs-lookup"><span data-stu-id="58073-115">*DetailLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="58073-116">Tipos de contadores que se van a mostrar en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="58073-116">Types of counters to be displayed in the dialog box.</span></span> <span data-ttu-id="58073-117">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="58073-117">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="58073-118">Valor</span><span class="sxs-lookup"><span data-stu-id="58073-118">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="58073-119">Significado</span><span class="sxs-lookup"><span data-stu-id="58073-119">Meaning</span></span>                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PERF_DETAIL_ADVANCED"></span><span id="perf_detail_advanced"></span><dl> <span data-ttu-id="58073-120"><dt>**detalle de rendimiento \_ \_ avanzado**</dt></span><span class="sxs-lookup"><span data-stu-id="58073-120"><dt>**PERF\_DETAIL\_ADVANCED**</dt></span></span> </dl> | <span data-ttu-id="58073-121">Contadores que es probable que el usuario avanzado entienda, además de los contadores de usuario inexperto.</span><span class="sxs-lookup"><span data-stu-id="58073-121">Counters that the advanced user is likely to understand, in addition to the novice-user counters.</span></span><br/>                                            |
| <span id="PERF_DETAIL_EXPERT"></span><span id="perf_detail_expert"></span><dl> <span data-ttu-id="58073-122"><dt>**\_experto en detalles de rendimiento \_**</dt></span><span class="sxs-lookup"><span data-stu-id="58073-122"><dt>**PERF\_DETAIL\_EXPERT**</dt></span></span> </dl>       | <span data-ttu-id="58073-123">Los contadores que es probable que comprenda el desarrollador de software y el usuario experto, además de los contadores para los usuarios principiantes y avanzados.</span><span class="sxs-lookup"><span data-stu-id="58073-123">Counters that the expert user and software developer is likely to understand, in addition to the counters for the novice and advanced users.</span></span><br/> |
| <span id="PERF_DETAIL_NOVICE"></span><span id="perf_detail_novice"></span><dl> <span data-ttu-id="58073-124"><dt>**\_experto en detalles de rendimiento \_**</dt></span><span class="sxs-lookup"><span data-stu-id="58073-124"><dt>**PERF\_DETAIL\_NOVICE**</dt></span></span> </dl>       | <span data-ttu-id="58073-125">Solo los contadores que es probable que comprenda el usuario principiante.</span><span class="sxs-lookup"><span data-stu-id="58073-125">Only counters that the novice user is likely to understand.</span></span><br/>                                                                                  |
| <span id="PERF_DETAIL_WIZARD"></span><span id="perf_detail_wizard"></span><dl> <span data-ttu-id="58073-126"><dt>**\_Asistente para detalles de rendimiento \_**</dt></span><span class="sxs-lookup"><span data-stu-id="58073-126"><dt>**PERF\_DETAIL\_WIZARD**</dt></span></span> </dl>       | <span data-ttu-id="58073-127">Todos los contadores del sistema.</span><span class="sxs-lookup"><span data-stu-id="58073-127">All counters in the system.</span></span><br/>                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="58073-128">*CaptionString*</span><span class="sxs-lookup"><span data-stu-id="58073-128">*CaptionString*</span></span> 
</dt> <dd>

<span data-ttu-id="58073-129">Variable de cadena que contiene el texto que se mostrará en la barra de título del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="58073-129">String variable that contains the text that will be displayed in the caption bar of the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58073-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="58073-130">Return value</span></span>

<span data-ttu-id="58073-131">La función devuelve el número de caracteres que se escriben en el búfer de *PathString* .</span><span class="sxs-lookup"><span data-stu-id="58073-131">The function returns the number of characters written to the *PathString* buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="58073-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58073-132">Requirements</span></span>



| <span data-ttu-id="58073-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="58073-133">Requirement</span></span> | <span data-ttu-id="58073-134">Value</span><span class="sxs-lookup"><span data-stu-id="58073-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="58073-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="58073-135">Minimum supported client</span></span><br/> | <span data-ttu-id="58073-136">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="58073-136">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="58073-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="58073-137">Minimum supported server</span></span><br/> | <span data-ttu-id="58073-138">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="58073-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="58073-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="58073-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="58073-140"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="58073-140"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="58073-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="58073-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58073-142"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58073-142"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58073-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="58073-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58073-144">**PdhVbCreateCounterPathList**</span><span class="sxs-lookup"><span data-stu-id="58073-144">**PdhVbCreateCounterPathList**</span></span>](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[<span data-ttu-id="58073-145">**PdhVbGetCounterPathElements**</span><span class="sxs-lookup"><span data-stu-id="58073-145">**PdhVbGetCounterPathElements**</span></span>](pdhvbgetcounterpathelements.md)
</dt> <dt>

[<span data-ttu-id="58073-146">**PdhVbGetCounterPathFromList**</span><span class="sxs-lookup"><span data-stu-id="58073-146">**PdhVbGetCounterPathFromList**</span></span>](pdhvbgetcounterpathfromlist.md)
</dt> </dl>

 

 




