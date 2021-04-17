---
description: 'El método ModifyStopTime2 establece la hora de detención. Este método es equivalente a IAMTimelineSrc:: ModifyStopTime, pero toma un valor REFTIME.'
ms.assetid: 8bebda47-3e52-42a2-870c-acc14561fa25
title: 'IAMTimelineSrc:: ModifyStopTime2 (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.ModifyStopTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 42ca3c9c1f8fa47abc7a9c21a44458540007939f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690938"
---
# <a name="iamtimelinesrcmodifystoptime2-method"></a><span data-ttu-id="65c54-104">IAMTimelineSrc:: ModifyStopTime2 (método)</span><span class="sxs-lookup"><span data-stu-id="65c54-104">IAMTimelineSrc::ModifyStopTime2 method</span></span>

> [!Note]  
> <span data-ttu-id="65c54-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="65c54-105">\[Deprecated.</span></span> <span data-ttu-id="65c54-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="65c54-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="65c54-107">El `ModifyStopTime2` método establece la hora de detención.</span><span class="sxs-lookup"><span data-stu-id="65c54-107">The `ModifyStopTime2` method sets the stop time.</span></span> <span data-ttu-id="65c54-108">Este método es equivalente a [**IAMTimelineSrc:: ModifyStopTime**](iamtimelinesrc-modifystoptime.md), pero toma un valor [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="65c54-108">This method is equivalent to [**IAMTimelineSrc::ModifyStopTime**](iamtimelinesrc-modifystoptime.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="65c54-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65c54-109">Syntax</span></span>


```C++
HRESULT ModifyStopTime2(
   REFTIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="65c54-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="65c54-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65c54-111">*Detención*</span><span class="sxs-lookup"><span data-stu-id="65c54-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="65c54-112">Nuevo tiempo de detención, en segundos.</span><span class="sxs-lookup"><span data-stu-id="65c54-112">New stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65c54-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="65c54-113">Return value</span></span>

<span data-ttu-id="65c54-114">Devuelve \_ si es correcto, o E \_ INVALIDARG si la hora especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="65c54-114">Returns S\_OK if successful, or E\_INVALIDARG if the specified time is not valid.</span></span>

## <a name="remarks"></a><span data-ttu-id="65c54-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="65c54-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="65c54-116">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="65c54-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="65c54-117">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="65c54-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="65c54-118">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="65c54-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="65c54-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65c54-119">Requirements</span></span>



| <span data-ttu-id="65c54-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="65c54-120">Requirement</span></span> | <span data-ttu-id="65c54-121">Value</span><span class="sxs-lookup"><span data-stu-id="65c54-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65c54-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="65c54-122">Header</span></span><br/>  | <dl> <span data-ttu-id="65c54-123"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="65c54-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="65c54-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="65c54-124">Library</span></span><br/> | <dl> <span data-ttu-id="65c54-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="65c54-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65c54-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="65c54-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65c54-127">**Interfaz IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="65c54-127">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="65c54-128">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="65c54-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




