---
description: 'El método SetStartStop2 establece las horas de inicio y detención del objeto, en relación con el elemento primario del objeto. Este método es equivalente a IAMTimelineObj:: SetStartStop, pero toma valores REFTIME.'
ms.assetid: 0fc79c82-d8e1-4b87-9e59-6d9e6ca614f3
title: 'IAMTimelineObj:: SetStartStop2 (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetStartStop2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 190e47d2ccee00d202dc16e20704b545447d844f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690720"
---
# <a name="iamtimelineobjsetstartstop2-method"></a><span data-ttu-id="e175f-104">IAMTimelineObj:: SetStartStop2 (método)</span><span class="sxs-lookup"><span data-stu-id="e175f-104">IAMTimelineObj::SetStartStop2 method</span></span>

> [!Note]  
> <span data-ttu-id="e175f-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="e175f-105">\[Deprecated.</span></span> <span data-ttu-id="e175f-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e175f-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e175f-107">El `SetStartStop2` método establece las horas de inicio y detención del objeto, en relación con el elemento primario del objeto.</span><span class="sxs-lookup"><span data-stu-id="e175f-107">The `SetStartStop2` method sets the object's start and stop times, relative to the object's parent.</span></span> <span data-ttu-id="e175f-108">Este método es equivalente a [**IAMTimelineObj:: SetStartStop**](iamtimelineobj-setstartstop.md), pero toma valores [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="e175f-108">This method is equivalent to [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="e175f-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e175f-109">Syntax</span></span>


```C++
HRESULT SetStartStop2(
   REFTIME Start,
   REFTIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="e175f-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e175f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e175f-111">*Iniciar*</span><span class="sxs-lookup"><span data-stu-id="e175f-111">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="e175f-112">Nueva hora de inicio, en segundos, o – 1 para mantener la hora de inicio existente.</span><span class="sxs-lookup"><span data-stu-id="e175f-112">New start time, in seconds, or –1 to keep the existing start time.</span></span>

</dd> <dt>

<span data-ttu-id="e175f-113">*Detención*</span><span class="sxs-lookup"><span data-stu-id="e175f-113">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="e175f-114">Nueva hora de detención, en segundos, o – 1 para mantener la hora de detención existente.</span><span class="sxs-lookup"><span data-stu-id="e175f-114">New stop time, in seconds, or –1 to keep the existing stop time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e175f-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e175f-115">Return value</span></span>

<span data-ttu-id="e175f-116">Devuelve uno de los siguientes valores **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="e175f-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="e175f-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e175f-117">Return code</span></span>                                                                                  | <span data-ttu-id="e175f-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="e175f-118">Description</span></span>                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="e175f-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="e175f-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="e175f-120">Correcto.</span><span class="sxs-lookup"><span data-stu-id="e175f-120">Success.</span></span><br/>          |
| <dl> <span data-ttu-id="e175f-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e175f-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="e175f-122">Argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="e175f-122">Invalid argument.</span></span><br/> |
| <dl> <span data-ttu-id="e175f-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="e175f-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>    | <span data-ttu-id="e175f-124">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="e175f-124">Not implemented.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="e175f-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e175f-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e175f-126">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="e175f-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e175f-127">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e175f-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e175f-128">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e175f-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e175f-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e175f-129">Requirements</span></span>



| <span data-ttu-id="e175f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e175f-130">Requirement</span></span> | <span data-ttu-id="e175f-131">Value</span><span class="sxs-lookup"><span data-stu-id="e175f-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e175f-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e175f-132">Header</span></span><br/>  | <dl> <span data-ttu-id="e175f-133"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="e175f-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e175f-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e175f-134">Library</span></span><br/> | <dl> <span data-ttu-id="e175f-135"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e175f-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e175f-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="e175f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e175f-137">**Interfaz IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="e175f-137">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="e175f-138">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="e175f-138">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




