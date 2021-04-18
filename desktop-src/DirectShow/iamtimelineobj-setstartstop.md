---
description: El método SetStartStop establece las horas de inicio y detención del objeto, en relación con el elemento primario del objeto.
ms.assetid: 6275a36b-f963-4916-bf60-ea68008ad153
title: 'IAMTimelineObj:: SetStartStop (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetStartStop
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e7839417a0406fc2702fb0fbd593edc92fa80437
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690721"
---
# <a name="iamtimelineobjsetstartstop-method"></a><span data-ttu-id="3216c-103">IAMTimelineObj:: SetStartStop (método)</span><span class="sxs-lookup"><span data-stu-id="3216c-103">IAMTimelineObj::SetStartStop method</span></span>

> [!Note]  
> <span data-ttu-id="3216c-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="3216c-104">\[Deprecated.</span></span> <span data-ttu-id="3216c-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3216c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3216c-106">El `SetStartStop` método establece las horas de inicio y detención del objeto, en relación con el elemento primario del objeto.</span><span class="sxs-lookup"><span data-stu-id="3216c-106">The `SetStartStop` method sets the object's start and stop times, relative to the object's parent.</span></span>

## <a name="syntax"></a><span data-ttu-id="3216c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3216c-107">Syntax</span></span>


```C++
HRESULT SetStartStop(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="3216c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3216c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3216c-109">*Iniciar*</span><span class="sxs-lookup"><span data-stu-id="3216c-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="3216c-110">Nueva hora de inicio, en unidades de 100-nanosegundos, o – 1 para mantener la hora de inicio existente.</span><span class="sxs-lookup"><span data-stu-id="3216c-110">New start time, in 100-nanosecond units, or –1 to keep the existing start time.</span></span>

</dd> <dt>

<span data-ttu-id="3216c-111">*Detención*</span><span class="sxs-lookup"><span data-stu-id="3216c-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="3216c-112">Nueva hora de detención, en unidades de 100-nanosegundos, o – 1 para mantener la hora de detención existente.</span><span class="sxs-lookup"><span data-stu-id="3216c-112">New stop time, in 100-nanosecond units, or –1 to keep the existing stop time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3216c-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3216c-113">Return value</span></span>

<span data-ttu-id="3216c-114">Devuelve uno de los siguientes valores **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="3216c-114">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="3216c-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3216c-115">Return code</span></span>                                                                                  | <span data-ttu-id="3216c-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="3216c-116">Description</span></span>                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="3216c-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="3216c-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="3216c-118">Correcto.</span><span class="sxs-lookup"><span data-stu-id="3216c-118">Success.</span></span><br/>          |
| <dl> <span data-ttu-id="3216c-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3216c-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="3216c-120">Argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="3216c-120">Invalid argument.</span></span><br/> |
| <dl> <span data-ttu-id="3216c-121"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="3216c-121"><dt>**E\_NOTIMPL**</dt></span></span> </dl>    | <span data-ttu-id="3216c-122">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="3216c-122">Not implemented.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="3216c-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3216c-123">Remarks</span></span>

<span data-ttu-id="3216c-124">Las pistas, las composiciones y los grupos no implementan este método.</span><span class="sxs-lookup"><span data-stu-id="3216c-124">Tracks, compositions, and groups do not implement this method.</span></span> <span data-ttu-id="3216c-125">Para estos objetos, la hora de inicio siempre es cero y la hora de detención es el tiempo de detención máximo de los objetos que contienen.</span><span class="sxs-lookup"><span data-stu-id="3216c-125">For these objects, the start time is always zero, and the stop time is the maximum stop time of the objects they contain.</span></span>

<span data-ttu-id="3216c-126">No establezca tiempos de superposición en objetos de origen dentro de la misma pista. Si lo hace, pueden producirse comportamientos indefinidos.</span><span class="sxs-lookup"><span data-stu-id="3216c-126">Do not set overlapping times on source objects within the same track. Doing so can cause undefined behaviors.</span></span>

<span data-ttu-id="3216c-127">En el caso de los objetos de origen, los tiempos de inicio y detención son independientes de los tiempos de inicio y detención del medio.</span><span class="sxs-lookup"><span data-stu-id="3216c-127">For source objects, the start and stop times are independent of the media start and media stop times.</span></span> <span data-ttu-id="3216c-128">Al cambiar un par de valores, no se cambia el otro.</span><span class="sxs-lookup"><span data-stu-id="3216c-128">Changing one pair of values does not change the other.</span></span> <span data-ttu-id="3216c-129">Para establecer las horas de inicio y detención del medio, llame al método [**IAMTimelineSrc:: SetMediaTimes**](iamtimelinesrc-setmediatimes.md) .</span><span class="sxs-lookup"><span data-stu-id="3216c-129">To set the media start and stop times, call the [**IAMTimelineSrc::SetMediaTimes**](iamtimelinesrc-setmediatimes.md) method.</span></span> <span data-ttu-id="3216c-130">Para obtener más información, vea [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="3216c-130">For more information, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

<span data-ttu-id="3216c-131">Para obtener cortes y transiciones con precisión de fotogramas, establezca los parámetros de *Inicio* y *detención* en los límites del marco.</span><span class="sxs-lookup"><span data-stu-id="3216c-131">To get frame-accurate cuts and transitions, set the *Start* and *Stop* parameters to frame boundaries.</span></span> <span data-ttu-id="3216c-132">Puede usar el método [**IAMTimelineObj:: FixTimes**](iamtimelineobj-fixtimes.md) para convertir un valor de hora en el límite de fotograma más cercano, o bien usar la función siguiente para convertir de número de fotograma a hora de referencia:</span><span class="sxs-lookup"><span data-stu-id="3216c-132">You can use the [**IAMTimelineObj::FixTimes**](iamtimelineobj-fixtimes.md) method to convert a time value into the nearest frame boundary, or use the following function to convert from frame number to reference time:</span></span>


```C++
REFERENCE_TIME inline FrameNumToTime(LONGLONG frame, double fps)
{
    double dt = (frame * 10000000 / fps);
    if (frame >= 0) 
    {
        dt += 0.5;    }
    else
    {
        dt -= 0.5;
    }
    return (REFERENCE_TIME)dt;
}
```



> [!Note]  
> <span data-ttu-id="3216c-133">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="3216c-133">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3216c-134">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3216c-134">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3216c-135">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="3216c-135">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3216c-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3216c-136">Requirements</span></span>



| <span data-ttu-id="3216c-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="3216c-137">Requirement</span></span> | <span data-ttu-id="3216c-138">Value</span><span class="sxs-lookup"><span data-stu-id="3216c-138">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3216c-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3216c-139">Header</span></span><br/>  | <dl> <span data-ttu-id="3216c-140"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="3216c-140"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3216c-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3216c-141">Library</span></span><br/> | <dl> <span data-ttu-id="3216c-142"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3216c-142"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3216c-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="3216c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3216c-144">**Interfaz IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="3216c-144">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="3216c-145">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="3216c-145">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




