---
description: El método SetMediaTimes establece las horas de detención e inicio del medio.
ms.assetid: 9fa7938c-8128-4c26-a738-771d57b315b5
title: 'IAMTimelineSrc:: SetMediaTimes (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd8255c7744a155ff8328682005e2aacafaf2d13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680568"
---
# <a name="iamtimelinesrcsetmediatimes-method"></a><span data-ttu-id="6de37-103">IAMTimelineSrc:: SetMediaTimes (método)</span><span class="sxs-lookup"><span data-stu-id="6de37-103">IAMTimelineSrc::SetMediaTimes method</span></span>

> [!Note]  
> <span data-ttu-id="6de37-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="6de37-104">\[Deprecated.</span></span> <span data-ttu-id="6de37-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6de37-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6de37-106">El `SetMediaTimes` método establece las horas de detención e inicio del medio.</span><span class="sxs-lookup"><span data-stu-id="6de37-106">The `SetMediaTimes` method sets the media stop and start times.</span></span>

## <a name="syntax"></a><span data-ttu-id="6de37-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6de37-107">Syntax</span></span>


```C++
HRESULT SetMediaTimes(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="6de37-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6de37-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6de37-109">*Iniciar*</span><span class="sxs-lookup"><span data-stu-id="6de37-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="6de37-110">Hora de inicio del medio, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="6de37-110">Media start time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="6de37-111">*Detención*</span><span class="sxs-lookup"><span data-stu-id="6de37-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="6de37-112">Tiempo de detención del medio, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="6de37-112">Media stop time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6de37-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6de37-113">Return value</span></span>

<span data-ttu-id="6de37-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="6de37-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6de37-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6de37-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6de37-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6de37-116">Remarks</span></span>

<span data-ttu-id="6de37-117">Las horas de los medios son las horas de detención e inicio relativas al archivo multimedia original.</span><span class="sxs-lookup"><span data-stu-id="6de37-117">The media times are the stop and start times relative to the original media file.</span></span> <span data-ttu-id="6de37-118">Establezca siempre las horas del medio al agregar un origen de vídeo o de audio a la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="6de37-118">Always set the media times when you add a video or audio source to the timeline.</span></span> <span data-ttu-id="6de37-119">De lo contrario, podrían producirse problemas de representación.</span><span class="sxs-lookup"><span data-stu-id="6de37-119">Otherwise, rendering problems might occur.</span></span> <span data-ttu-id="6de37-120">La hora de detención debe ser mayor que la hora de inicio.</span><span class="sxs-lookup"><span data-stu-id="6de37-120">The stop time must be greater than the start time.</span></span>

<span data-ttu-id="6de37-121">Para usar un fotograma fijo de un origen de vídeo, establezca la hora de detención en una cantidad fraccionaria superior a la hora de inicio, por ejemplo, 100 nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="6de37-121">To use a still frame from a video source, set the stop time to a fractional amount more than the start time, such as 100 nanoseconds.</span></span> <span data-ttu-id="6de37-122">Si se establecen en el mismo valor, se produce un error de representación.</span><span class="sxs-lookup"><span data-stu-id="6de37-122">Setting them to the same value causes a rendering error.</span></span>

<span data-ttu-id="6de37-123">Si la duración de la escala de tiempo no coincide con la duración del medio, el origen se expande o se reduce en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="6de37-123">If the timeline duration does not match the media duration, the source stretches or shrinks accordingly.</span></span> <span data-ttu-id="6de37-124">Esto hace que el clip se reproduzca más lentamente o más rápido que la tarifa creada.</span><span class="sxs-lookup"><span data-stu-id="6de37-124">This causes the clip to play slower or faster than the authored rate.</span></span> <span data-ttu-id="6de37-125">(El cambio de tono se producirá en un origen de audio). Para obtener más información, vea [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="6de37-125">(Pitch shifting will occur in an audio source.) For more information, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

<span data-ttu-id="6de37-126">Puede especificar la duración del archivo de código fuente llamando al método [**SetMediaLength**](iamtimelinesrc-setmedialength.md) .</span><span class="sxs-lookup"><span data-stu-id="6de37-126">You can specify the duration of the source file by calling the [**SetMediaLength**](iamtimelinesrc-setmedialength.md) method.</span></span> <span data-ttu-id="6de37-127">Si establece una hora de detención de medios que supera la duración, DES trunca la hora de detención.</span><span class="sxs-lookup"><span data-stu-id="6de37-127">If you set a media stop time that exceeds the duration, DES truncates the stop time.</span></span>

> [!Note]  
> <span data-ttu-id="6de37-128">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="6de37-128">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6de37-129">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6de37-129">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6de37-130">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="6de37-130">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6de37-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6de37-131">Requirements</span></span>



| <span data-ttu-id="6de37-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="6de37-132">Requirement</span></span> | <span data-ttu-id="6de37-133">Value</span><span class="sxs-lookup"><span data-stu-id="6de37-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6de37-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6de37-134">Header</span></span><br/>  | <dl> <span data-ttu-id="6de37-135"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="6de37-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6de37-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6de37-136">Library</span></span><br/> | <dl> <span data-ttu-id="6de37-137"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6de37-137"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6de37-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="6de37-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6de37-139">**Interfaz IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="6de37-139">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="6de37-140">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="6de37-140">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




