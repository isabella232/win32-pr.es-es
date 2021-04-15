---
description: 'El método GetNextSrc2 busca en la pista el siguiente origen que aparece en el momento especificado o en una versión posterior. Este método es equivalente a IAMTimelineTrack:: GetNextSrc, pero toma un valor REFTIME.'
ms.assetid: f3f7b000-ec73-4ae9-802b-a9bc6f1840b3
title: 'IAMTimelineTrack:: GetNextSrc2 (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrc2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c934cfd6c4f58c5fca59e78e120fee89af3f73a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690126"
---
# <a name="iamtimelinetrackgetnextsrc2-method"></a><span data-ttu-id="1d0dc-104">IAMTimelineTrack:: GetNextSrc2 (método)</span><span class="sxs-lookup"><span data-stu-id="1d0dc-104">IAMTimelineTrack::GetNextSrc2 method</span></span>

> [!Note]  
> <span data-ttu-id="1d0dc-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="1d0dc-105">\[Deprecated.</span></span> <span data-ttu-id="1d0dc-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1d0dc-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1d0dc-107">El `GetNextSrc2` método busca en la pista el siguiente origen que aparece en el momento especificado o en una versión posterior.</span><span class="sxs-lookup"><span data-stu-id="1d0dc-107">The `GetNextSrc2` method searches the track for the next source that appears at the specified time or later.</span></span> <span data-ttu-id="1d0dc-108">Este método es equivalente a [**IAMTimelineTrack:: GetNextSrc**](iamtimelinetrack-getnextsrc.md), pero toma un valor [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="1d0dc-108">This method is equivalent to [**IAMTimelineTrack::GetNextSrc**](iamtimelinetrack-getnextsrc.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d0dc-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d0dc-109">Syntax</span></span>


```C++
HRESULT GetNextSrc2(
  [out] IAMTimelineObj **ppSrc,
        REFTIME        *pInOut
);
```



## <a name="parameters"></a><span data-ttu-id="1d0dc-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1d0dc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d0dc-111">*ppSrc* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1d0dc-111">*ppSrc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d0dc-112">Recibe un puntero a la interfaz [**IAMTimelineObj**](iamtimelineobj.md) del objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="1d0dc-112">Receives a pointer to the source object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="1d0dc-113">*Patilla*</span><span class="sxs-lookup"><span data-stu-id="1d0dc-113">*pInOut*</span></span> 
</dt> <dd>

<span data-ttu-id="1d0dc-114">En la entrada, contiene la hora de inicio de la búsqueda, en segundos.</span><span class="sxs-lookup"><span data-stu-id="1d0dc-114">On input, contains the start time for the search, in seconds.</span></span> <span data-ttu-id="1d0dc-115">Si el método recupera un origen, establece el valor en la hora de detención del origen.</span><span class="sxs-lookup"><span data-stu-id="1d0dc-115">If the method retrieves a source, it sets the value to the stop time of the source.</span></span> <span data-ttu-id="1d0dc-116">Si el método no recupera un origen, el valor deja de ser válido y la aplicación no debe usarlo.</span><span class="sxs-lookup"><span data-stu-id="1d0dc-116">If the method does not retrieve a source, the value becomes invalid and the application should not use it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d0dc-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1d0dc-117">Return value</span></span>

<span data-ttu-id="1d0dc-118">Devuelve S \_ OK si el método recupera un origen o s \_ false en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="1d0dc-118">Returns S\_OK if the method retrieves a source, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d0dc-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1d0dc-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1d0dc-120">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="1d0dc-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1d0dc-121">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1d0dc-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1d0dc-122">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="1d0dc-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1d0dc-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d0dc-123">Requirements</span></span>



| <span data-ttu-id="1d0dc-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d0dc-124">Requirement</span></span> | <span data-ttu-id="1d0dc-125">Value</span><span class="sxs-lookup"><span data-stu-id="1d0dc-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d0dc-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1d0dc-126">Header</span></span><br/>  | <dl> <span data-ttu-id="1d0dc-127"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d0dc-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1d0dc-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1d0dc-128">Library</span></span><br/> | <dl> <span data-ttu-id="1d0dc-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d0dc-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d0dc-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d0dc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d0dc-131">**Interfaz IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="1d0dc-131">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="1d0dc-132">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="1d0dc-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




