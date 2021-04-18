---
title: Función de devolución de llamada ICMProgressProcCallback
description: La función ICMProgressProcCallback es una función de devolución de llamada proporcionada por la aplicación que informa del progreso y permite que la aplicación cancele el procesamiento de color.
ms.assetid: 4e0bfa4c-f0eb-4776-98d6-90d9adf71bee
keywords:
- Función de devolución de llamada ICMProgressProcCallback sistema de color de Windows
topic_type:
- apiref
api_name:
- ICMProgressProcCallback
api_location:
- Icm.h
api_type:
- UserDefined
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8acf790a135a41e4eabb4a67c2498f1ed914c4c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721573"
---
# <a name="icmprogressproccallback-callback-function"></a><span data-ttu-id="b131f-104">Función de devolución de llamada ICMProgressProcCallback</span><span class="sxs-lookup"><span data-stu-id="b131f-104">ICMProgressProcCallback callback function</span></span>

<span data-ttu-id="b131f-105">La función **ICMProgressProcCallback** es una función de devolución de llamada proporcionada por la aplicación que informa del progreso y permite que la aplicación cancele el procesamiento de color.</span><span class="sxs-lookup"><span data-stu-id="b131f-105">The **ICMProgressProcCallback** function is an application-supplied callback function that reports progress and permits the application to cancel color processing.</span></span>

## <a name="syntax"></a><span data-ttu-id="b131f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b131f-106">Syntax</span></span>


```C++
BOOL WINAPI ICMProgressProcCallback(
   ULONG  ulMax,
   ULONG  ulCurrent,
   LPARAM ulCallbackData
);
```



## <a name="parameters"></a><span data-ttu-id="b131f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b131f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b131f-108">*ulMax*</span><span class="sxs-lookup"><span data-stu-id="b131f-108">*ulMax*</span></span> 
</dt> <dd>

<span data-ttu-id="b131f-109">Especifica el valor máximo del contador de progreso (que se usa para estimar la finalización del procesamiento de mapas de bits).</span><span class="sxs-lookup"><span data-stu-id="b131f-109">Specifies the maximum value of the progress counter (used to estimate completion of the bitmap processing).</span></span>

</dd> <dt>

<span data-ttu-id="b131f-110">*ulCurrent*</span><span class="sxs-lookup"><span data-stu-id="b131f-110">*ulCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="b131f-111">Especifica el valor actual del contador de progreso (cuando se divide por el valor máximo, proporciona una estimación aproximada del porcentaje de finalización).</span><span class="sxs-lookup"><span data-stu-id="b131f-111">Specifies the current value of the progress counter (when divided by the maximum value, provides a rough estimate of percentage of completion).</span></span>

</dd> <dt>

<span data-ttu-id="b131f-112">*ulCallbackData*</span><span class="sxs-lookup"><span data-stu-id="b131f-112">*ulCallbackData*</span></span> 
</dt> <dd>

<span data-ttu-id="b131f-113">Especifica los datos que pasa la aplicación a una función ICM2, que después lo pasa a la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="b131f-113">Specifies the data which is passed by the application to an ICM2 function, which then passes it on to the callback function.</span></span> <span data-ttu-id="b131f-114">Estos datos se pueden utilizar, por ejemplo, para identificar el mapa de bits y el proceso sobre el que se está informando del progreso.</span><span class="sxs-lookup"><span data-stu-id="b131f-114">Such data can be used, for example, to identify the bitmap and process about which progress is being reported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b131f-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b131f-115">Return value</span></span>

<span data-ttu-id="b131f-116">Esta función devuelve **true** para continuar el procesamiento de mapas de bits.</span><span class="sxs-lookup"><span data-stu-id="b131f-116">This function returns **TRUE** to continue bitmap processing.</span></span> <span data-ttu-id="b131f-117">El valor devuelto es **false** para cancelar el procesamiento.</span><span class="sxs-lookup"><span data-stu-id="b131f-117">The return value is **FALSE** to cancel processing.</span></span> <span data-ttu-id="b131f-118">Si se cancela el procesamiento, la función de llamada devuelve cero para indicar un error, aunque es posible que el búfer de salida se llene parcialmente.</span><span class="sxs-lookup"><span data-stu-id="b131f-118">If processing is canceled, the calling function returns zero to indicate failure, although its output buffer may be partially filled.</span></span>

## <a name="remarks"></a><span data-ttu-id="b131f-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b131f-119">Remarks</span></span>

<span data-ttu-id="b131f-120">La aplicación proporciona el nombre de esta función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="b131f-120">The name of this callback function is supplied by the application.</span></span> <span data-ttu-id="b131f-121">Un número de funciones WCS, incluidas [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits) y [**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits), llama a esta función periódicamente.</span><span class="sxs-lookup"><span data-stu-id="b131f-121">A number of WCS functions, including [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits) and [**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits), call this function periodically.</span></span>

## <a name="requirements"></a><span data-ttu-id="b131f-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b131f-122">Requirements</span></span>



| <span data-ttu-id="b131f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b131f-123">Requirement</span></span> | <span data-ttu-id="b131f-124">Value</span><span class="sxs-lookup"><span data-stu-id="b131f-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b131f-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b131f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b131f-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b131f-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b131f-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b131f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b131f-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b131f-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b131f-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b131f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b131f-130"><dt>ICM. h</dt></span><span class="sxs-lookup"><span data-stu-id="b131f-130"><dt>Icm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b131f-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="b131f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b131f-132">Conceptos básicos de la administración del color</span><span class="sxs-lookup"><span data-stu-id="b131f-132">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="b131f-133">Funciones</span><span class="sxs-lookup"><span data-stu-id="b131f-133">Functions</span></span>](functions.md)
</dt> <dt>

[<span data-ttu-id="b131f-134">**TranslateBitmapBits**</span><span class="sxs-lookup"><span data-stu-id="b131f-134">**TranslateBitmapBits**</span></span>](/windows/win32/api/icm/nf-icm-translatebitmapbits)
</dt> <dt>

[<span data-ttu-id="b131f-135">**CheckBitmapBits**</span><span class="sxs-lookup"><span data-stu-id="b131f-135">**CheckBitmapBits**</span></span>](/windows/win32/api/icm/nf-icm-checkbitmapbits)
</dt> </dl>
