---
description: El método FixTimes redondea las horas de inicio y detención especificadas a los límites del marco más cercano, según se define en la configuración de velocidad de fotogramas del grupo primario.
ms.assetid: 033ac221-7616-4c62-937e-c5585bc73a16
title: 'IAMTimelineObj:: FixTimes (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.FixTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3442d45328b10437111219ad36fc114a9aa15ad6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691061"
---
# <a name="iamtimelineobjfixtimes-method"></a><span data-ttu-id="a0a42-103">IAMTimelineObj:: FixTimes (método)</span><span class="sxs-lookup"><span data-stu-id="a0a42-103">IAMTimelineObj::FixTimes method</span></span>

> [!Note]  
> <span data-ttu-id="a0a42-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="a0a42-104">\[Deprecated.</span></span> <span data-ttu-id="a0a42-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a0a42-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a0a42-106">El `FixTimes` método redondea las horas de inicio y detención especificadas a los límites del marco más cercano, según se define en la configuración de velocidad de fotogramas del grupo primario.</span><span class="sxs-lookup"><span data-stu-id="a0a42-106">The `FixTimes` method rounds the specified start and stop times to the nearest frame boundaries, as defined by the parent group's frame rate setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0a42-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a0a42-107">Syntax</span></span>


```C++
HRESULT FixTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="a0a42-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a0a42-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0a42-109">*pStart*</span><span class="sxs-lookup"><span data-stu-id="a0a42-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="a0a42-110">Puntero a una variable que contiene la hora de inicio, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="a0a42-110">Pointer to a variable that contains the start time, in 100-nanosecond units.</span></span> <span data-ttu-id="a0a42-111">Si la llamada se realiza correctamente, esta variable se establece en el tiempo redondeado.</span><span class="sxs-lookup"><span data-stu-id="a0a42-111">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> <dt>

<span data-ttu-id="a0a42-112">*pStop*</span><span class="sxs-lookup"><span data-stu-id="a0a42-112">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="a0a42-113">Puntero a una variable que contiene la hora de detención, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="a0a42-113">Pointer to a variable that contains the stop time, in 100-nanosecond units.</span></span> <span data-ttu-id="a0a42-114">Si la llamada se realiza correctamente, esta variable se establece en el tiempo redondeado.</span><span class="sxs-lookup"><span data-stu-id="a0a42-114">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0a42-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a0a42-115">Return value</span></span>

<span data-ttu-id="a0a42-116">Devuelve \_ si es correcto, o E \_ NOTINTREE si el objeto no forma parte de un grupo.</span><span class="sxs-lookup"><span data-stu-id="a0a42-116">Returns S\_OK if successful, or E\_NOTINTREE if the object is not part of a group.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0a42-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a0a42-117">Remarks</span></span>

<span data-ttu-id="a0a42-118">Durante la representación, DES redondea las horas de inicio y detención del objeto al límite de fotogramas más cercano.</span><span class="sxs-lookup"><span data-stu-id="a0a42-118">During rendering, DES rounds the object's start and stop times to the nearest frame boundary.</span></span> <span data-ttu-id="a0a42-119">Sin embargo, DES no sobrescribe las horas del objeto.</span><span class="sxs-lookup"><span data-stu-id="a0a42-119">However, DES does not overwrite the object's times.</span></span> <span data-ttu-id="a0a42-120">Si cambia la velocidad de fotogramas de grupo, los tiempos redondeados siempre se calculan a partir de las horas originales.</span><span class="sxs-lookup"><span data-stu-id="a0a42-120">If you change the group frame rate, the rounded times are always calculated from the original times.</span></span> <span data-ttu-id="a0a42-121">Para obtener más información, vea [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="a0a42-121">For more information, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

<span data-ttu-id="a0a42-122">Use este método para determinar los tiempos de inicio y detención precisos en el proyecto representado.</span><span class="sxs-lookup"><span data-stu-id="a0a42-122">Use this method to determine accurate start and stop times in the rendered project.</span></span> <span data-ttu-id="a0a42-123">Por ejemplo, debe buscar las horas redondeadas, en lugar de las horas de inicio y detención originales del objeto.</span><span class="sxs-lookup"><span data-stu-id="a0a42-123">For example, you should seek to the rounded times, rather than the object's original start and stop times.</span></span> <span data-ttu-id="a0a42-124">Llame a [**IAMTimelineObj:: GetStartStop**](iamtimelineobj-getstartstop.md) para obtener las horas originales y pase esos valores a `FixTimes` .</span><span class="sxs-lookup"><span data-stu-id="a0a42-124">Call [**IAMTimelineObj::GetStartStop**](iamtimelineobj-getstartstop.md) to obtain the original times, and pass those values to `FixTimes`.</span></span>

> [!Note]  
> <span data-ttu-id="a0a42-125">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="a0a42-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a0a42-126">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a0a42-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a0a42-127">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a0a42-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a0a42-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0a42-128">Requirements</span></span>



| <span data-ttu-id="a0a42-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0a42-129">Requirement</span></span> | <span data-ttu-id="a0a42-130">Value</span><span class="sxs-lookup"><span data-stu-id="a0a42-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0a42-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a0a42-131">Header</span></span><br/>  | <dl> <span data-ttu-id="a0a42-132"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0a42-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a0a42-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a0a42-133">Library</span></span><br/> | <dl> <span data-ttu-id="a0a42-134"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0a42-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0a42-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="a0a42-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0a42-136">**Interfaz IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="a0a42-136">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="a0a42-137">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="a0a42-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




