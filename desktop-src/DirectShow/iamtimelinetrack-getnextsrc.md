---
description: El método GetNextSrc busca en la pista el siguiente origen que aparece en el momento especificado o en una versión posterior.
ms.assetid: e87d8978-7b45-41a3-a74d-b5dd231d1d85
title: 'IAMTimelineTrack:: GetNextSrc (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrc
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd8ca25b2d5a551d803e79e69cf8d1095ee47511
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679052"
---
# <a name="iamtimelinetrackgetnextsrc-method"></a><span data-ttu-id="92dc6-103">IAMTimelineTrack:: GetNextSrc (método)</span><span class="sxs-lookup"><span data-stu-id="92dc6-103">IAMTimelineTrack::GetNextSrc method</span></span>

> [!Note]  
> <span data-ttu-id="92dc6-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="92dc6-104">\[Deprecated.</span></span> <span data-ttu-id="92dc6-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="92dc6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="92dc6-106">El `GetNextSrc` método busca en la pista el siguiente origen que aparece en el momento especificado o en una versión posterior.</span><span class="sxs-lookup"><span data-stu-id="92dc6-106">The `GetNextSrc` method searches the track for the next source that appears at the specified time or later.</span></span>

## <a name="syntax"></a><span data-ttu-id="92dc6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92dc6-107">Syntax</span></span>


```C++
HRESULT GetNextSrc(
  [out] IAMTimelineObj **ppSrc,
        REFERENCE_TIME *pInOut
);
```



## <a name="parameters"></a><span data-ttu-id="92dc6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="92dc6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92dc6-109">*ppSrc* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="92dc6-109">*ppSrc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92dc6-110">Recibe un puntero a la interfaz [**IAMTimelineObj**](iamtimelineobj.md) del objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="92dc6-110">Receives a pointer to the source object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="92dc6-111">*Patilla*</span><span class="sxs-lookup"><span data-stu-id="92dc6-111">*pInOut*</span></span> 
</dt> <dd>

<span data-ttu-id="92dc6-112">Puntero a una variable que contiene la hora de inicio de la búsqueda, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="92dc6-112">Pointer to a variable that contains the start time for the search, in 100-nanosecond units.</span></span> <span data-ttu-id="92dc6-113">Si el método recupera un origen, establece el valor en la hora de detención del origen.</span><span class="sxs-lookup"><span data-stu-id="92dc6-113">If the method retrieves a source, it sets the value to the stop time of the source.</span></span> <span data-ttu-id="92dc6-114">Si el método no recupera un origen, el valor deja de ser válido y la aplicación no debe usarlo.</span><span class="sxs-lookup"><span data-stu-id="92dc6-114">If the method does not retrieve a source, the value becomes invalid and the application should not use it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92dc6-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="92dc6-115">Return value</span></span>

<span data-ttu-id="92dc6-116">Devuelve S \_ OK si el método recupera un origen o s \_ false en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="92dc6-116">Returns S\_OK if the method retrieves a source, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="92dc6-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="92dc6-117">Remarks</span></span>

<span data-ttu-id="92dc6-118">Si la hora especificada por el número de *conexiones* se encuentra entre las horas de inicio y de detención de un origen, el método recupera ese origen.</span><span class="sxs-lookup"><span data-stu-id="92dc6-118">If the time specified by *pInOut* falls between the start and stop times of a source, the method retrieves that source.</span></span>

<span data-ttu-id="92dc6-119">Si el método devuelve S \_ correcto, la interfaz **IAMTimelineObj** que devuelve tiene un recuento de referencias pendiente.</span><span class="sxs-lookup"><span data-stu-id="92dc6-119">If the method returns S\_OK, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="92dc6-120">Asegúrese de liberar la interfaz cuando termine de usarla.</span><span class="sxs-lookup"><span data-stu-id="92dc6-120">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="92dc6-121">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="92dc6-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="92dc6-122">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="92dc6-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="92dc6-123">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="92dc6-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="92dc6-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92dc6-124">Requirements</span></span>



| <span data-ttu-id="92dc6-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="92dc6-125">Requirement</span></span> | <span data-ttu-id="92dc6-126">Value</span><span class="sxs-lookup"><span data-stu-id="92dc6-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="92dc6-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="92dc6-127">Header</span></span><br/>  | <dl> <span data-ttu-id="92dc6-128"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="92dc6-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="92dc6-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="92dc6-129">Library</span></span><br/> | <dl> <span data-ttu-id="92dc6-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="92dc6-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92dc6-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="92dc6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92dc6-132">**Interfaz IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="92dc6-132">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="92dc6-133">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="92dc6-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




