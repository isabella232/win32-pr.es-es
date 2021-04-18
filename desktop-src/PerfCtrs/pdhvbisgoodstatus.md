---
description: La función PdhVbIsGoodStatus comprueba un valor de estado para determinar si es un código de error o correcto. Si el valor de estado es correcto, el valor devuelto será distinto de cero. Si se trata de un código de estado de error, el valor devuelto será cero.
ms.assetid: bdca8f64-5dcd-4ecb-ba95-72f7a56c0439
title: PdhVbIsGoodStatus función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbIsGoodStatus
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: d21686be0398a84a57a303ad816b8a25f50aa611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667307"
---
# <a name="pdhvbisgoodstatus-function"></a><span data-ttu-id="c8a5c-105">PdhVbIsGoodStatus función)</span><span class="sxs-lookup"><span data-stu-id="c8a5c-105">PdhVbIsGoodStatus function</span></span>

<span data-ttu-id="c8a5c-106">La función **PdhVbIsGoodStatus** comprueba un valor de estado para determinar si es un código de error o correcto.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-106">The **PdhVbIsGoodStatus** function tests a status value to determine if it is a success or failure code.</span></span> <span data-ttu-id="c8a5c-107">Si el valor de estado es correcto, el valor devuelto será distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-107">If the status value is a successful one, then the return value will be nonzero.</span></span> <span data-ttu-id="c8a5c-108">Si se trata de un código de estado de error, el valor devuelto será cero.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-108">If it is a failure status code, the return value will be zero.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c8a5c-109">La función que se describe en este tema puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-109">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="c8a5c-110">En su lugar, Microsoft recomienda que use las funciones descritas en [funciones de contadores de rendimiento](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="c8a5c-110">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="c8a5c-111">Función PdhVbIsGoodStatus ( \_ ByVal StatusValue as Long \_ ) as Long</span><span class="sxs-lookup"><span data-stu-id="c8a5c-111">Function PdhVbIsGoodStatus( \_ ByVal StatusValue As Long \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="c8a5c-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8a5c-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8a5c-113">*StatusValue*</span><span class="sxs-lookup"><span data-stu-id="c8a5c-113">*StatusValue*</span></span> 
</dt> <dd>

<span data-ttu-id="c8a5c-114">Valor de estado devuelto por otra función de PDH que se va a probar.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-114">Status value returned by another PDH function that is to be tested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8a5c-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8a5c-115">Return value</span></span>

<span data-ttu-id="c8a5c-116">La función devuelve cero si el código de estado es un código de estado de error.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-116">The function returns zero if the status code is a failure status code.</span></span> <span data-ttu-id="c8a5c-117">Devuelve un valor distinto de cero si el código de estado es un código de estado correcto.</span><span class="sxs-lookup"><span data-stu-id="c8a5c-117">It returns nonzero if the status code is a success status code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8a5c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8a5c-118">Requirements</span></span>



| <span data-ttu-id="c8a5c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8a5c-119">Requirement</span></span> | <span data-ttu-id="c8a5c-120">Value</span><span class="sxs-lookup"><span data-stu-id="c8a5c-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c8a5c-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8a5c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c8a5c-122">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="c8a5c-122">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c8a5c-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8a5c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c8a5c-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c8a5c-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c8a5c-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c8a5c-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="c8a5c-126"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8a5c-126"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="c8a5c-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c8a5c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8a5c-128"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8a5c-128"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8a5c-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8a5c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8a5c-130">**PdhVbGetDoubleCounterValue**</span><span class="sxs-lookup"><span data-stu-id="c8a5c-130">**PdhVbGetDoubleCounterValue**</span></span>](pdhvbgetdoublecountervalue.md)
</dt> </dl>

 

 




