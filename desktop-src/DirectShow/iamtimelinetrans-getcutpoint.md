---
description: El método GetCutPoint recupera el punto de corte.
ms.assetid: f54ef17e-3407-4164-911d-3dc7fad656ed
title: 'IAMTimelineTrans:: GetCutPoint (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutPoint
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e89cc2e7bc6d18842212a58bc5c00b6424947b66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691027"
---
# <a name="iamtimelinetransgetcutpoint-method"></a><span data-ttu-id="05341-103">IAMTimelineTrans:: GetCutPoint (método)</span><span class="sxs-lookup"><span data-stu-id="05341-103">IAMTimelineTrans::GetCutPoint method</span></span>

> [!Note]  
> <span data-ttu-id="05341-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="05341-104">\[Deprecated.</span></span> <span data-ttu-id="05341-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="05341-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="05341-106">El `GetCutPoint` método recupera el punto de corte.</span><span class="sxs-lookup"><span data-stu-id="05341-106">The `GetCutPoint` method retrieves the cut point.</span></span> <span data-ttu-id="05341-107">Si representa una transición como un corte, el punto de corte es el momento en que la transición corta de un origen al siguiente.</span><span class="sxs-lookup"><span data-stu-id="05341-107">If you render a transition as a cut, the cut point is the time when the transition cuts from one source to the next.</span></span> <span data-ttu-id="05341-108">De forma predeterminada, este valor es el medio de la transición.</span><span class="sxs-lookup"><span data-stu-id="05341-108">By default, this value is the middle of the transition.</span></span> <span data-ttu-id="05341-109">Por ejemplo, en una transición que abarca un segundo, el punto de corte predeterminado es de 0,5 segundos en la transición.</span><span class="sxs-lookup"><span data-stu-id="05341-109">For example, in a transition that spans one second, the default cut point is 0.5 seconds into the transition.</span></span>

## <a name="syntax"></a><span data-ttu-id="05341-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="05341-110">Syntax</span></span>


```C++
HRESULT GetCutPoint(
   REFERENCE_TIME *pTLTime
);
```



## <a name="parameters"></a><span data-ttu-id="05341-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="05341-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05341-112">*pTLTime*</span><span class="sxs-lookup"><span data-stu-id="05341-112">*pTLTime*</span></span> 
</dt> <dd>

<span data-ttu-id="05341-113">Recibe el punto de corte, relativo a la hora de inicio de la transición, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="05341-113">Receives the cut point, relative to the start time of the transition, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05341-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="05341-114">Return value</span></span>

<span data-ttu-id="05341-115">Devuelve uno de los siguientes valores **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="05341-115">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="05341-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="05341-116">Return code</span></span>                                                                               | <span data-ttu-id="05341-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="05341-117">Description</span></span>                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="05341-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="05341-118"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="05341-119">No se estableció el punto de corte.</span><span class="sxs-lookup"><span data-stu-id="05341-119">The cut point was not set.</span></span> <span data-ttu-id="05341-120">El valor devuelto es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="05341-120">The value returned is the default value.</span></span><br/> |
| <dl> <span data-ttu-id="05341-121"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="05341-121"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="05341-122">El punto de corte se estableció en un valor distinto del predeterminado.</span><span class="sxs-lookup"><span data-stu-id="05341-122">The cut point was set to a value other than the default.</span></span><br/>            |
| <dl> <span data-ttu-id="05341-123"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="05341-123"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="05341-124">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="05341-124">**NULL** pointer argument.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="05341-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="05341-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="05341-126">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="05341-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="05341-127">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="05341-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="05341-128">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="05341-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="05341-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05341-129">Requirements</span></span>



| <span data-ttu-id="05341-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="05341-130">Requirement</span></span> | <span data-ttu-id="05341-131">Value</span><span class="sxs-lookup"><span data-stu-id="05341-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="05341-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="05341-132">Header</span></span><br/>  | <dl> <span data-ttu-id="05341-133"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="05341-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="05341-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="05341-134">Library</span></span><br/> | <dl> <span data-ttu-id="05341-135"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="05341-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05341-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="05341-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05341-137">**Interfaz IAMTimelineTrans**</span><span class="sxs-lookup"><span data-stu-id="05341-137">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="05341-138">**IAMTimelineTrans::SetCutPoint**</span><span class="sxs-lookup"><span data-stu-id="05341-138">**IAMTimelineTrans::SetCutPoint**</span></span>](iamtimelinetrans-setcutpoint.md)
</dt> <dt>

[<span data-ttu-id="05341-139">**IAMTimelineTrans::GetCutsOnly**</span><span class="sxs-lookup"><span data-stu-id="05341-139">**IAMTimelineTrans::GetCutsOnly**</span></span>](iamtimelinetrans-getcutsonly.md)
</dt> <dt>

[<span data-ttu-id="05341-140">**IAMTimeline::TransitionsEnabled**</span><span class="sxs-lookup"><span data-stu-id="05341-140">**IAMTimeline::TransitionsEnabled**</span></span>](iamtimeline-transitionsenabled.md)
</dt> <dt>

[<span data-ttu-id="05341-141">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="05341-141">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




