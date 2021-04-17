---
description: 'El método GetSrcAtTime2 recupera el objeto de origen más cercano a la hora especificada, de acuerdo con las condiciones de límite especificadas. Este método es equivalente a IAMTimelineTrack:: GetSrcAtTime, pero toma un valor REFTIME.'
ms.assetid: 11f6545b-478b-4ffd-8344-2bf8585db2a5
title: 'IAMTimelineTrack:: GetSrcAtTime2 (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetSrcAtTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7140644f64c66b204d6a50cb8e88cb5beca41dae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679159"
---
# <a name="iamtimelinetrackgetsrcattime2-method"></a><span data-ttu-id="86517-104">IAMTimelineTrack:: GetSrcAtTime2 (método)</span><span class="sxs-lookup"><span data-stu-id="86517-104">IAMTimelineTrack::GetSrcAtTime2 method</span></span>

> [!Note]  
> <span data-ttu-id="86517-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="86517-105">\[Deprecated.</span></span> <span data-ttu-id="86517-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="86517-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="86517-107">El `GetSrcAtTime2` método recupera el objeto de origen más cercano a la hora especificada, de acuerdo con las condiciones de límite especificadas.</span><span class="sxs-lookup"><span data-stu-id="86517-107">The `GetSrcAtTime2` method retrieves the source object nearest to the specified time, according to the specified boundary conditions.</span></span> <span data-ttu-id="86517-108">Este método es equivalente a [**IAMTimelineTrack:: GetSrcAtTime**](iamtimelinetrack-getsrcattime.md), pero toma un valor [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="86517-108">This method is equivalent to [**IAMTimelineTrack::GetSrcAtTime**](iamtimelinetrack-getsrcattime.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="86517-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="86517-109">Syntax</span></span>


```C++
HRESULT GetSrcAtTime2(
  [out] IAMTimelineObj **ppSrc,
        REFTIME        Time,
        long           SearchDirection
);
```



## <a name="parameters"></a><span data-ttu-id="86517-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="86517-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86517-111">*ppSrc* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="86517-111">*ppSrc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86517-112">Recibe un puntero a la interfaz [**IAMTimelineObj**](iamtimelineobj.md) del objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="86517-112">Receives a pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the source object.</span></span>

</dd> <dt>

<span data-ttu-id="86517-113">*Time*</span><span class="sxs-lookup"><span data-stu-id="86517-113">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="86517-114">Hora de inicio de la búsqueda, en segundos.</span><span class="sxs-lookup"><span data-stu-id="86517-114">Start time for the search, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="86517-115">*SearchDirection*</span><span class="sxs-lookup"><span data-stu-id="86517-115">*SearchDirection*</span></span> 
</dt> <dd>

<span data-ttu-id="86517-116">Miembro del tipo enumerado de [**\_ marcas de \_ búsqueda \_ de DEXTERF Track**](dexterf-track-search-flags.md) que especifica las condiciones de límite de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="86517-116">Member of the [**DEXTERF\_TRACK\_SEARCH\_FLAGS**](dexterf-track-search-flags.md) enumerated type that specifies the boundary conditions for the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86517-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="86517-117">Return value</span></span>

<span data-ttu-id="86517-118">Devuelve uno de los siguientes valores **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="86517-118">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="86517-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="86517-119">Return code</span></span>                                                                                  | <span data-ttu-id="86517-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="86517-120">Description</span></span>                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="86517-121"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="86517-121"><dt>**S\_FALSE**</dt></span></span> </dl>      | <span data-ttu-id="86517-122">No se encontró un objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="86517-122">Did not locate a source object.</span></span><br/> |
| <dl> <span data-ttu-id="86517-123"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="86517-123"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="86517-124">Encontró un objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="86517-124">Located a source object.</span></span><br/>        |
| <dl> <span data-ttu-id="86517-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="86517-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="86517-126">Argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="86517-126">Invalid argument.</span></span><br/>               |
| <dl> <span data-ttu-id="86517-127"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="86517-127"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="86517-128">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="86517-128">**NULL** pointer argument.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="86517-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="86517-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="86517-130">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="86517-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="86517-131">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="86517-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="86517-132">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="86517-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="86517-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86517-133">Requirements</span></span>



| <span data-ttu-id="86517-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="86517-134">Requirement</span></span> | <span data-ttu-id="86517-135">Value</span><span class="sxs-lookup"><span data-stu-id="86517-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86517-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="86517-136">Header</span></span><br/>  | <dl> <span data-ttu-id="86517-137"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="86517-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="86517-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="86517-138">Library</span></span><br/> | <dl> <span data-ttu-id="86517-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86517-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86517-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="86517-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86517-141">**Interfaz IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="86517-141">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="86517-142">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="86517-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




