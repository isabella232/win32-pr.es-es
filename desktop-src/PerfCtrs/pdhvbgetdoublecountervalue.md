---
description: La función PdhVbGetDoubleCounterValue devuelve el valor actual del contador especificado como un valor de punto flotante de precisión doble.
ms.assetid: a2ee63dd-da39-4104-921d-371172bcb45c
title: PdhVbGetDoubleCounterValue función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetDoubleCounterValue
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 67f0372a26649fbe781cf4d9bd25794b82d6346e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360701"
---
# <a name="pdhvbgetdoublecountervalue-function"></a><span data-ttu-id="adc52-103">PdhVbGetDoubleCounterValue función)</span><span class="sxs-lookup"><span data-stu-id="adc52-103">PdhVbGetDoubleCounterValue function</span></span>

<span data-ttu-id="adc52-104">La función **PdhVbGetDoubleCounterValue** devuelve el valor actual del contador especificado como un valor de punto flotante de precisión doble.</span><span class="sxs-lookup"><span data-stu-id="adc52-104">The **PdhVbGetDoubleCounterValue** function returns the current value of the specified counter as a double-precision floating point value.</span></span> <span data-ttu-id="adc52-105">Debe comprobar la *contracondición* antes de usar el número devuelto, ya que es posible que el contador no sea válido cuando se lea.</span><span class="sxs-lookup"><span data-stu-id="adc52-105">You should check *CounterStatus* before using the returned number, because the counter may not be valid when it is read.</span></span> <span data-ttu-id="adc52-106">Para comprobar el estado del contador, llame a la función [**PdhVbIsGoodStatus**](pdhvbisgoodstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="adc52-106">To check the counter status, call the [**PdhVbIsGoodStatus**](pdhvbisgoodstatus.md) function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="adc52-107">La función que se describe en este tema puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="adc52-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="adc52-108">En su lugar, Microsoft recomienda que use las funciones descritas en [funciones de contadores de rendimiento](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="adc52-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="adc52-109">Función PdhVbGetDoubleCounterValue ( \_ ByVal Contrahandle as Long, \_ ByVal perstatus as Long \_ ) as Double</span><span class="sxs-lookup"><span data-stu-id="adc52-109">Function PdhVbGetDoubleCounterValue( \_ ByVal CounterHandle As Long, \_ ByVal CounterStatus As Long \_ ) As Double</span></span>

## <a name="parameters"></a><span data-ttu-id="adc52-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="adc52-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adc52-111">*Control de contracargo*</span><span class="sxs-lookup"><span data-stu-id="adc52-111">*CounterHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="adc52-112">IDENTIFICADOR del contador cuyo valor actual se va a leer.</span><span class="sxs-lookup"><span data-stu-id="adc52-112">ID of the counter whose current value is to be read.</span></span>

</dd> <dt>

<span data-ttu-id="adc52-113">*ContraEstado*</span><span class="sxs-lookup"><span data-stu-id="adc52-113">*CounterStatus*</span></span> 
</dt> <dd>

<span data-ttu-id="adc52-114">Variable en la que el estado actual del valor del contador se devuelve al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="adc52-114">Variable in which the current status of the counter value is returned to the caller.</span></span> <span data-ttu-id="adc52-115">El valor de los datos devueltos es válido si y solo si el valor devuelto en el estado de los datos es PDH \_ CSTATUS válido o los datos de \_ \_ PDH \_ CSTATUS \_ nuevos \_ (vea códigos de error de PDH).</span><span class="sxs-lookup"><span data-stu-id="adc52-115">The returned data value is valid if and only if the value returned in CounterStatus is PDH\_CSTATUS\_VALID\_DATA or PDH\_CSTATUS\_NEW\_DATA (see PDH error codes).</span></span> <span data-ttu-id="adc52-116">Si el valor devuelto en contrastatus es cualquier otro valor, no use los datos.</span><span class="sxs-lookup"><span data-stu-id="adc52-116">If the value returned in CounterStatus is any other value, do not use the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adc52-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="adc52-117">Return value</span></span>

<span data-ttu-id="adc52-118">La función devuelve el valor de punto flotante de precisión doble del contador actual, calculado y con formato tal y como se define en el tipo de contador.</span><span class="sxs-lookup"><span data-stu-id="adc52-118">The function returns the double-precision floating point value of the current counter, computed and formatted as defined by the counter type.</span></span>

## <a name="requirements"></a><span data-ttu-id="adc52-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="adc52-119">Requirements</span></span>



| <span data-ttu-id="adc52-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="adc52-120">Requirement</span></span> | <span data-ttu-id="adc52-121">Value</span><span class="sxs-lookup"><span data-stu-id="adc52-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="adc52-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="adc52-122">Minimum supported client</span></span><br/> | <span data-ttu-id="adc52-123">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="adc52-123">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="adc52-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="adc52-124">Minimum supported server</span></span><br/> | <span data-ttu-id="adc52-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="adc52-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="adc52-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="adc52-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="adc52-127"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="adc52-127"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="adc52-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="adc52-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="adc52-129"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="adc52-129"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adc52-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="adc52-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adc52-131">**PdhVbIsGoodStatus**</span><span class="sxs-lookup"><span data-stu-id="adc52-131">**PdhVbIsGoodStatus**</span></span>](pdhvbisgoodstatus.md)
</dt> </dl>

 

 




