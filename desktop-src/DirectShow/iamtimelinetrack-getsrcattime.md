---
description: El método GetSrcAtTime recupera el objeto de origen más cercano a la hora especificada, de acuerdo con las condiciones de límite especificadas.
ms.assetid: 0469c0c2-13df-49f7-95b2-15d3069c5b1c
title: 'IAMTimelineTrack:: GetSrcAtTime (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetSrcAtTime
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4b726d26efd0550df364200a27d536d60d38274a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690121"
---
# <a name="iamtimelinetrackgetsrcattime-method"></a><span data-ttu-id="3161c-103">IAMTimelineTrack:: GetSrcAtTime (método)</span><span class="sxs-lookup"><span data-stu-id="3161c-103">IAMTimelineTrack::GetSrcAtTime method</span></span>

> [!Note]  
> <span data-ttu-id="3161c-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="3161c-104">\[Deprecated.</span></span> <span data-ttu-id="3161c-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3161c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3161c-106">El `GetSrcAtTime` método recupera el objeto de origen más cercano a la hora especificada, de acuerdo con las condiciones de límite especificadas.</span><span class="sxs-lookup"><span data-stu-id="3161c-106">The `GetSrcAtTime` method retrieves the source object nearest to the specified time, according to the specified boundary conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="3161c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3161c-107">Syntax</span></span>


```C++
HRESULT GetSrcAtTime(
  [out] IAMTimelineObj **ppSrc,
        REFERENCE_TIME Time,
        long           SearchDirection
);
```



## <a name="parameters"></a><span data-ttu-id="3161c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3161c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3161c-109">*ppSrc* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3161c-109">*ppSrc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3161c-110">Recibe un puntero a la interfaz [**IAMTimelineObj**](iamtimelineobj.md) del objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="3161c-110">Receives a pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the source object.</span></span>

</dd> <dt>

<span data-ttu-id="3161c-111">*Time*</span><span class="sxs-lookup"><span data-stu-id="3161c-111">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="3161c-112">Hora de inicio de la búsqueda, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="3161c-112">Start time for the search, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="3161c-113">*SearchDirection*</span><span class="sxs-lookup"><span data-stu-id="3161c-113">*SearchDirection*</span></span> 
</dt> <dd>

<span data-ttu-id="3161c-114">Miembro del tipo enumerado de [**\_ marcas de \_ búsqueda \_ de DEXTERF Track**](dexterf-track-search-flags.md) que especifica las condiciones de límite de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="3161c-114">Member of the [**DEXTERF\_TRACK\_SEARCH\_FLAGS**](dexterf-track-search-flags.md) enumerated type that specifies the boundary conditions for the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3161c-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3161c-115">Return value</span></span>

<span data-ttu-id="3161c-116">Devuelve uno de los siguientes valores **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="3161c-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="3161c-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3161c-117">Return code</span></span>                                                                                  | <span data-ttu-id="3161c-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="3161c-118">Description</span></span>                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="3161c-119"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="3161c-119"><dt>**S\_FALSE**</dt></span></span> </dl>      | <span data-ttu-id="3161c-120">No se encontró un objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="3161c-120">Did not locate a source object.</span></span><br/> |
| <dl> <span data-ttu-id="3161c-121"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="3161c-121"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="3161c-122">Encontró un objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="3161c-122">Located a source object.</span></span><br/>        |
| <dl> <span data-ttu-id="3161c-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3161c-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="3161c-124">Argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="3161c-124">Invalid argument.</span></span><br/>               |
| <dl> <span data-ttu-id="3161c-125"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="3161c-125"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="3161c-126">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="3161c-126">**NULL** pointer argument.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="3161c-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3161c-127">Remarks</span></span>

<span data-ttu-id="3161c-128">Si el método devuelve S \_ correcto, la interfaz **IAMTimelineObj** que devuelve tiene un recuento de referencias pendiente.</span><span class="sxs-lookup"><span data-stu-id="3161c-128">If the method returns S\_OK, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="3161c-129">Asegúrese de liberar la interfaz cuando termine de usarla.</span><span class="sxs-lookup"><span data-stu-id="3161c-129">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="3161c-130">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="3161c-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3161c-131">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3161c-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3161c-132">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="3161c-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3161c-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3161c-133">Requirements</span></span>



| <span data-ttu-id="3161c-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="3161c-134">Requirement</span></span> | <span data-ttu-id="3161c-135">Value</span><span class="sxs-lookup"><span data-stu-id="3161c-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3161c-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3161c-136">Header</span></span><br/>  | <dl> <span data-ttu-id="3161c-137"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="3161c-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3161c-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3161c-138">Library</span></span><br/> | <dl> <span data-ttu-id="3161c-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3161c-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3161c-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="3161c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3161c-141">**Interfaz IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="3161c-141">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="3161c-142">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="3161c-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




