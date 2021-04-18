---
description: 'El método GetTransAtTime2 recupera la transición más cercana a la hora especificada, de acuerdo con las condiciones de límite especificadas. Este método es equivalente a IAMTimelineTransable:: GetTransAtTime, pero toma un parámetro REFTIME.'
ms.assetid: b51b53ec-4b56-4900-98b5-427d752354b0
title: 'IAMTimelineTransable:: GetTransAtTime2 (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetTransAtTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6b3de498791a634ea651da46ba9c95557ca12b87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690993"
---
# <a name="iamtimelinetransablegettransattime2-method"></a><span data-ttu-id="2e623-104">IAMTimelineTransable:: GetTransAtTime2 (método)</span><span class="sxs-lookup"><span data-stu-id="2e623-104">IAMTimelineTransable::GetTransAtTime2 method</span></span>

> [!Note]  
> <span data-ttu-id="2e623-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="2e623-105">\[Deprecated.</span></span> <span data-ttu-id="2e623-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2e623-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2e623-107">El `GetTransAtTime2` método recupera la transición más cercana a la hora especificada, de acuerdo con las condiciones de límite especificadas.</span><span class="sxs-lookup"><span data-stu-id="2e623-107">The `GetTransAtTime2` method retrieves the transition nearest to the specified time, according to the specified boundary conditions.</span></span> <span data-ttu-id="2e623-108">Este método es equivalente a [**IAMTimelineTransable:: GetTransAtTime**](iamtimelinetransable-gettransattime.md), pero toma un parámetro [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="2e623-108">This method is equivalent to [**IAMTimelineTransable::GetTransAtTime**](iamtimelinetransable-gettransattime.md), but takes a [**REFTIME**](reftime.md) parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e623-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e623-109">Syntax</span></span>


```C++
HRESULT GetTransAtTime2(
  [out] IAMTimelineObj **ppObj,
        REFTIME        Time,
        long           SearchDirection
);
```



## <a name="parameters"></a><span data-ttu-id="2e623-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e623-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e623-111">*ppObj* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2e623-111">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e623-112">Recibe un puntero a la interfaz [**IAMTimelineObj**](iamtimelineobj.md) de la transición.</span><span class="sxs-lookup"><span data-stu-id="2e623-112">Receives a pointer to the transition's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="2e623-113">*Time*</span><span class="sxs-lookup"><span data-stu-id="2e623-113">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="2e623-114">Hora a partir de la que se va a comenzar la búsqueda, en segundos.</span><span class="sxs-lookup"><span data-stu-id="2e623-114">Time from which to begin the search, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="2e623-115">*SearchDirection*</span><span class="sxs-lookup"><span data-stu-id="2e623-115">*SearchDirection*</span></span> 
</dt> <dd>

<span data-ttu-id="2e623-116">Miembro del tipo enumerado de [**\_ marcas de \_ búsqueda \_ de DEXTERF Track**](dexterf-track-search-flags.md) que especifica las condiciones de límite de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="2e623-116">Member of the [**DEXTERF\_TRACK\_SEARCH\_FLAGS**](dexterf-track-search-flags.md) enumerated type that specifies the boundary conditions for the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e623-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2e623-117">Return value</span></span>

<span data-ttu-id="2e623-118">Devuelve uno de los siguientes valores **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="2e623-118">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="2e623-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2e623-119">Return code</span></span>                                                                                  | <span data-ttu-id="2e623-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e623-120">Description</span></span>                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="2e623-121"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="2e623-121"><dt>**S\_FALSE**</dt></span></span> </dl>      | <span data-ttu-id="2e623-122">No se encontró ninguna transición.</span><span class="sxs-lookup"><span data-stu-id="2e623-122">No transition was found.</span></span><br/>   |
| <dl> <span data-ttu-id="2e623-123"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="2e623-123"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="2e623-124">Se encontró la transición.</span><span class="sxs-lookup"><span data-stu-id="2e623-124">Transition was found.</span></span><br/>      |
| <dl> <span data-ttu-id="2e623-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2e623-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="2e623-126">Argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="2e623-126">Invalid argument.</span></span><br/>          |
| <dl> <span data-ttu-id="2e623-127"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="2e623-127"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="2e623-128">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="2e623-128">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2e623-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e623-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2e623-130">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="2e623-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2e623-131">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="2e623-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2e623-132">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="2e623-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2e623-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e623-133">Requirements</span></span>



| <span data-ttu-id="2e623-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e623-134">Requirement</span></span> | <span data-ttu-id="2e623-135">Value</span><span class="sxs-lookup"><span data-stu-id="2e623-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e623-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e623-136">Header</span></span><br/>  | <dl> <span data-ttu-id="2e623-137"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e623-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2e623-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2e623-138">Library</span></span><br/> | <dl> <span data-ttu-id="2e623-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e623-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e623-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e623-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e623-141">**Interfaz IAMTimelineTransable**</span><span class="sxs-lookup"><span data-stu-id="2e623-141">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="2e623-142">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="2e623-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




