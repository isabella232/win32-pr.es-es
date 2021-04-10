---
description: Especifica el tamaño del segmento en unidades de megabytes (MB), bits o una fila de MB.
ms.assetid: 42E7DB19-9FB9-4226-B0B5-97AD6B9C0E12
title: Propiedad CODECAPI_AVEncSliceControlSize (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e4c3e58fa34922941ea564d42e449cefd798ad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153676"
---
# <a name="codecapi_avencslicecontrolsize-property"></a><span data-ttu-id="d5098-103">\_Propiedad AVEncSliceControlSize de CODECAPI</span><span class="sxs-lookup"><span data-stu-id="d5098-103">CODECAPI\_AVEncSliceControlSize property</span></span>

<span data-ttu-id="d5098-104">Especifica el tamaño del segmento en unidades de megabytes (MB), bits o una fila de MB.</span><span class="sxs-lookup"><span data-stu-id="d5098-104">Specifies the size of the slice in units of megabyte (MB), bits, or MB row.</span></span>

## <a name="data-type"></a><span data-ttu-id="d5098-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d5098-105">Data type</span></span>

<span data-ttu-id="d5098-106">**ULong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="d5098-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="d5098-107">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="d5098-107">Property GUID</span></span>

<span data-ttu-id="d5098-108">**CODECAPI \_ AVEncSliceControlSize**</span><span class="sxs-lookup"><span data-stu-id="d5098-108">**CODECAPI\_AVEncSliceControlSize**</span></span>

## <a name="remarks"></a><span data-ttu-id="d5098-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5098-109">Remarks</span></span>

<span data-ttu-id="d5098-110">**Codificadores H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="d5098-110">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="d5098-111">El significado del valor de CODECAPI \_ AVEncSliceControlSize se controla mediante la propiedad [CODECAPI \_ AVEncSliceControlMode](codecapi-avencslicecontrolmode.md) .</span><span class="sxs-lookup"><span data-stu-id="d5098-111">The meaning of the value of CODECAPI\_AVEncSliceControlSize is controlled by the [CODECAPI\_AVEncSliceControlMode](codecapi-avencslicecontrolmode.md) property.</span></span> <span data-ttu-id="d5098-112">En la tabla siguiente se muestra cómo las \_ propiedades CODECAPI AVEncSliceControlSize y CODECAPI \_ AVEncSliceControlMode controlan el tamaño y el número de segmentos de un marco.</span><span class="sxs-lookup"><span data-stu-id="d5098-112">The following table illustrates how the CODECAPI\_AVEncSliceControlSize and CODECAPI\_AVEncSliceControlMode properties control the size and number of slices in a frame.</span></span>



| <span data-ttu-id="d5098-113">Configuración de CODECAPI \_ AVEncSliceControlMode</span><span class="sxs-lookup"><span data-stu-id="d5098-113">CODECAPI\_AVEncSliceControlMode setting</span></span> | <span data-ttu-id="d5098-114">Significado del valor</span><span class="sxs-lookup"><span data-stu-id="d5098-114">Meaning of value</span></span>                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5098-115">0</span><span class="sxs-lookup"><span data-stu-id="d5098-115">0</span></span>                                       | <span data-ttu-id="d5098-116">Es un entero que indica el tamaño de cada sector del marco en unidades de macrobloques.</span><span class="sxs-lookup"><span data-stu-id="d5098-116">This is an integer that indicates the size of each slice in the frame in units of macroblocks.</span></span> <br/> <span data-ttu-id="d5098-117">El codificador debe rechazar la configuración cuando el valor es mayor que el número de macrobloques en el marco.</span><span class="sxs-lookup"><span data-stu-id="d5098-117">The encoder should reject the setting when the value is greater than the number of macroblocks in the frame.</span></span><br/>                                                                                                                                                                         |
| <span data-ttu-id="d5098-118">1</span><span class="sxs-lookup"><span data-stu-id="d5098-118">1</span></span>                                       | <span data-ttu-id="d5098-119">Es un entero que indica el tamaño de cada sector del marco en unidades de bits.</span><span class="sxs-lookup"><span data-stu-id="d5098-119">This is an integer that indicates the size of each slice in the frame in units of bits.</span></span> <br/> <span data-ttu-id="d5098-120">El codificador debe iniciar un nuevo segmento en el adaptativo macrobloque que hace que el número de bits del segmento supere este valor (por lo que el tamaño de cada segmento siempre será menor o igual que este valor).</span><span class="sxs-lookup"><span data-stu-id="d5098-120">The encoder should start a new slice at the macroblock that causes the number of bits in the slice to exceed this value (so the size of each slice will always be less than or equal than this value).</span></span> <span data-ttu-id="d5098-121">Esto significa que el tamaño del último segmento podría ser significativamente menor que este valor.</span><span class="sxs-lookup"><span data-stu-id="d5098-121">This means that the last slice size could be significantly smaller than this value.</span></span> <br/> |
| <span data-ttu-id="d5098-122">2</span><span class="sxs-lookup"><span data-stu-id="d5098-122">2</span></span>                                       | <span data-ttu-id="d5098-123">Es un entero que indica el tamaño de cada sector del marco en unidades de filas de adaptativo macrobloque.</span><span class="sxs-lookup"><span data-stu-id="d5098-123">This is an integer that indicates the size of each slice in the frame in units of macroblock rows.</span></span> <br/> <span data-ttu-id="d5098-124">El codificador debe rechazar la configuración cuando el valor es mayor que el número de filas de adaptativo macrobloque en el marco.</span><span class="sxs-lookup"><span data-stu-id="d5098-124">The encoder should reject the setting when the value is greater than the number of macroblock rows in the frame.</span></span><br/>                                                                                                                                                                 |



 

<span data-ttu-id="d5098-125">Si la aplicación no establece un valor para [CODECAPI \_ AVEncSliceControlMode](codecapi-avencslicecontrolmode.md), el codificador debe devolver un error.</span><span class="sxs-lookup"><span data-stu-id="d5098-125">If the application does not set a value for [CODECAPI\_AVEncSliceControlMode](codecapi-avencslicecontrolmode.md), the encoder should return an error.</span></span>

<span data-ttu-id="d5098-126">El valor predeterminado recomendado es tener un solo segmento para todo el marco.</span><span class="sxs-lookup"><span data-stu-id="d5098-126">The recommended default is to have a single slice for whole frame.</span></span>

<span data-ttu-id="d5098-127">Algunos codificadores pueden codificar segmentos en paralelo y, por tanto, el rendimiento podría verse afectado en función de la configuración del control del segmento.</span><span class="sxs-lookup"><span data-stu-id="d5098-127">Some encoders might encode slices in parallel and so performance could be affected depending on the slice control settings.</span></span> <span data-ttu-id="d5098-128">Por ejemplo, la codificación de un fotograma como un solo segmento podría ser más lenta que si el marco se codificara como varios segmentos.</span><span class="sxs-lookup"><span data-stu-id="d5098-128">For example, encoding a frame as a single slice might be slower than if the frame was encoded as multiple slices.</span></span>

<span data-ttu-id="d5098-129">La configuración del control de segmento es dinámica y se puede cambiar durante la sesión de codificación.</span><span class="sxs-lookup"><span data-stu-id="d5098-129">The slice control settings are dynamic and can be changed during the encoding session.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5098-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5098-130">Requirements</span></span>



| <span data-ttu-id="d5098-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5098-131">Requirement</span></span> | <span data-ttu-id="d5098-132">Value</span><span class="sxs-lookup"><span data-stu-id="d5098-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5098-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5098-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d5098-134">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="d5098-134">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="d5098-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5098-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d5098-136">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="d5098-136">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="d5098-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5098-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5098-138"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5098-138"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5098-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5098-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5098-140">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d5098-140">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




