---
description: El método ModifyStopTime establece la hora de detención, relativa a la escala de tiempo.
ms.assetid: 0d9b6cf7-d029-4c35-9045-82cbeff1e3ae
title: 'IAMTimelineSrc:: ModifyStopTime (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.ModifyStopTime
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5e0f3ac58df4e74926d2163705261ffad4551e69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681072"
---
# <a name="iamtimelinesrcmodifystoptime-method"></a><span data-ttu-id="20dec-103">IAMTimelineSrc:: ModifyStopTime (método)</span><span class="sxs-lookup"><span data-stu-id="20dec-103">IAMTimelineSrc::ModifyStopTime method</span></span>

> [!Note]  
> <span data-ttu-id="20dec-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="20dec-104">\[Deprecated.</span></span> <span data-ttu-id="20dec-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="20dec-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="20dec-106">El `ModifyStopTime` método establece la hora de detención, relativa a la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="20dec-106">The `ModifyStopTime` method sets the stop time, relative to the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="20dec-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="20dec-107">Syntax</span></span>


```C++
HRESULT ModifyStopTime(
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="20dec-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="20dec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20dec-109">*Detención*</span><span class="sxs-lookup"><span data-stu-id="20dec-109">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="20dec-110">Nueva hora de detención, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="20dec-110">New stop time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20dec-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="20dec-111">Return value</span></span>

<span data-ttu-id="20dec-112">Devuelve S \_ OK o E \_ INVALIDARG si la hora especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="20dec-112">Returns S\_OK, or E\_INVALIDARG if the specified time is not valid.</span></span>

## <a name="remarks"></a><span data-ttu-id="20dec-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="20dec-113">Remarks</span></span>

<span data-ttu-id="20dec-114">Este método equivale a llamar a [**IAMTimelineObj:: SetStartStop**](iamtimelineobj-setstartstop.md) con la hora de inicio original y una nueva hora de detención.</span><span class="sxs-lookup"><span data-stu-id="20dec-114">This method is equivalent to calling [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md) with the original start time and a new stop time.</span></span>

> [!Note]  
> <span data-ttu-id="20dec-115">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="20dec-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="20dec-116">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="20dec-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="20dec-117">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="20dec-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="20dec-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20dec-118">Requirements</span></span>



| <span data-ttu-id="20dec-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="20dec-119">Requirement</span></span> | <span data-ttu-id="20dec-120">Value</span><span class="sxs-lookup"><span data-stu-id="20dec-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20dec-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="20dec-121">Header</span></span><br/>  | <dl> <span data-ttu-id="20dec-122"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="20dec-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="20dec-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="20dec-123">Library</span></span><br/> | <dl> <span data-ttu-id="20dec-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20dec-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20dec-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="20dec-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20dec-126">**Interfaz IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="20dec-126">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="20dec-127">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="20dec-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




