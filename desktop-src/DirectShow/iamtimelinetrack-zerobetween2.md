---
description: 'El método ZeroBetween2 quita todo de la pista entre las horas especificadas. Este método es equivalente a IAMTimelineTrack:: ZeroBetween, pero toma valores REFTIME.'
ms.assetid: 56b9be30-cc3f-4843-bf35-910498242d71
title: 'IAMTimelineTrack:: ZeroBetween2 (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.ZeroBetween2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 27e3ab5cc2a631cb54c926824c2f3410413cd981
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690110"
---
# <a name="iamtimelinetrackzerobetween2-method"></a><span data-ttu-id="4a29c-104">IAMTimelineTrack:: ZeroBetween2 (método)</span><span class="sxs-lookup"><span data-stu-id="4a29c-104">IAMTimelineTrack::ZeroBetween2 method</span></span>

> [!Note]  
> <span data-ttu-id="4a29c-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="4a29c-105">\[Deprecated.</span></span> <span data-ttu-id="4a29c-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4a29c-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4a29c-107">El `ZeroBetween2` método quita todo de la pista entre las horas especificadas.</span><span class="sxs-lookup"><span data-stu-id="4a29c-107">The `ZeroBetween2` method removes everything from the track between the specified times.</span></span> <span data-ttu-id="4a29c-108">Este método es equivalente a [**IAMTimelineTrack:: ZeroBetween**](iamtimelinetrack-zerobetween.md), pero toma valores [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="4a29c-108">This method is equivalent to [**IAMTimelineTrack::ZeroBetween**](iamtimelinetrack-zerobetween.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a29c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4a29c-109">Syntax</span></span>


```C++
HRESULT ZeroBetween2(
   REFTIME rtStart,
   REFTIME rtEnd
);
```



## <a name="parameters"></a><span data-ttu-id="4a29c-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4a29c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a29c-111">*rtStart*</span><span class="sxs-lookup"><span data-stu-id="4a29c-111">*rtStart*</span></span> 
</dt> <dd>

<span data-ttu-id="4a29c-112">Comienzo del intervalo que se va a borrar, en segundos.</span><span class="sxs-lookup"><span data-stu-id="4a29c-112">Beginning of the range to clear, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="4a29c-113">*rtEnd*</span><span class="sxs-lookup"><span data-stu-id="4a29c-113">*rtEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="4a29c-114">Final del intervalo que se va a borrar, en segundos.</span><span class="sxs-lookup"><span data-stu-id="4a29c-114">End of the range to clear, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a29c-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4a29c-115">Return value</span></span>

<span data-ttu-id="4a29c-116">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4a29c-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="4a29c-117">Estos son algunos de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="4a29c-117">Possible values include the following.</span></span>



| <span data-ttu-id="4a29c-118">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="4a29c-118">Return code</span></span>                                                                             | <span data-ttu-id="4a29c-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a29c-119">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="4a29c-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="4a29c-120"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="4a29c-121">El intervalo de tiempo está por encima de todo en la pista.</span><span class="sxs-lookup"><span data-stu-id="4a29c-121">The time range falls beyond everything in the track.</span></span><br/> |
| <dl> <span data-ttu-id="4a29c-122"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="4a29c-122"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="4a29c-123">Correcto.</span><span class="sxs-lookup"><span data-stu-id="4a29c-123">Success.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="4a29c-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4a29c-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4a29c-125">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="4a29c-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4a29c-126">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4a29c-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4a29c-127">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4a29c-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4a29c-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a29c-128">Requirements</span></span>



| <span data-ttu-id="4a29c-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a29c-129">Requirement</span></span> | <span data-ttu-id="4a29c-130">Value</span><span class="sxs-lookup"><span data-stu-id="4a29c-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a29c-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4a29c-131">Header</span></span><br/>  | <dl> <span data-ttu-id="4a29c-132"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a29c-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4a29c-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4a29c-133">Library</span></span><br/> | <dl> <span data-ttu-id="4a29c-134"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a29c-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a29c-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a29c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a29c-136">**Interfaz IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="4a29c-136">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="4a29c-137">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="4a29c-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




