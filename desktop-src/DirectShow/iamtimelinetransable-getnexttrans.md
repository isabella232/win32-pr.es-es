---
description: El método GetNextTrans recupera la primera transición que aparece en el momento especificado o posterior.
ms.assetid: 40598d8d-ce74-4a6f-83d0-ea409b0a858c
title: 'IAMTimelineTransable:: GetNextTrans (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetNextTrans
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cc8f7c88dab2b8c0dfece6f2799b6648c0b9da2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689931"
---
# <a name="iamtimelinetransablegetnexttrans-method"></a><span data-ttu-id="f5d30-103">IAMTimelineTransable:: GetNextTrans (método)</span><span class="sxs-lookup"><span data-stu-id="f5d30-103">IAMTimelineTransable::GetNextTrans method</span></span>

> [!Note]  
> <span data-ttu-id="f5d30-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="f5d30-104">\[Deprecated.</span></span> <span data-ttu-id="f5d30-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f5d30-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f5d30-106">El `GetNextTrans` método recupera la primera transición que aparece en el momento especificado o posterior.</span><span class="sxs-lookup"><span data-stu-id="f5d30-106">The `GetNextTrans` method retrieves the first transition that appears at the specified time or later.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5d30-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f5d30-107">Syntax</span></span>


```C++
HRESULT GetNextTrans(
  [out] IAMTimelineObj **ppTrans,
        REFERENCE_TIME *pInOut
);
```



## <a name="parameters"></a><span data-ttu-id="f5d30-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f5d30-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5d30-109">*ppTrans* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f5d30-109">*ppTrans* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5d30-110">Recibe un puntero a la interfaz [**IAMTimelineObj**](iamtimelineobj.md) del objeto de transición.</span><span class="sxs-lookup"><span data-stu-id="f5d30-110">Receives a pointer to the transition object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="f5d30-111">*Patilla*</span><span class="sxs-lookup"><span data-stu-id="f5d30-111">*pInOut*</span></span> 
</dt> <dd>

<span data-ttu-id="f5d30-112">Puntero a una variable que especifica el tiempo en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="f5d30-112">Pointer to a variable that specifies the time in 100-nanosecond units.</span></span> <span data-ttu-id="f5d30-113">En la entrada, este valor especifica la hora a partir de la que se va a buscar la transición.</span><span class="sxs-lookup"><span data-stu-id="f5d30-113">On input, this value specifies the time from which to find the transition.</span></span> <span data-ttu-id="f5d30-114">En la salida, si se recupera una transición, este valor se establece en la hora de detención de la transición.</span><span class="sxs-lookup"><span data-stu-id="f5d30-114">On output, if a transition is retrieved, this value is set to the stop time of the transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5d30-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f5d30-115">Return value</span></span>

<span data-ttu-id="f5d30-116">Devuelve S \_ OK si el método recupera una transición o es \_ false si no encuentra una transición.</span><span class="sxs-lookup"><span data-stu-id="f5d30-116">Returns S\_OK if the method retrieves a transition, or S\_FALSE if it does not find a transition.</span></span> <span data-ttu-id="f5d30-117">De lo contrario, devuelve un valor **HRESULT** que indica la causa del error.</span><span class="sxs-lookup"><span data-stu-id="f5d30-117">Otherwise, returns an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5d30-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f5d30-118">Remarks</span></span>

<span data-ttu-id="f5d30-119">La hora de inicio de la transición puede ser menor que el tiempo que se especifica en el *pines*, si la transición abarca la hora especificada.</span><span class="sxs-lookup"><span data-stu-id="f5d30-119">The start time of the transition might be less than the time that you specify in *pInOut*, if the transition spans the specified time.</span></span>

<span data-ttu-id="f5d30-120">Si el método devuelve S \_ correcto, la interfaz [**IAMTimelineObj**](iamtimelineobj.md) que devuelve tiene un recuento de referencias pendiente.</span><span class="sxs-lookup"><span data-stu-id="f5d30-120">If the method returns S\_OK, the [**IAMTimelineObj**](iamtimelineobj.md) interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="f5d30-121">Asegúrese de liberar la interfaz cuando termine de usarla.</span><span class="sxs-lookup"><span data-stu-id="f5d30-121">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="f5d30-122">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="f5d30-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f5d30-123">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f5d30-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f5d30-124">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f5d30-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f5d30-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5d30-125">Requirements</span></span>



| <span data-ttu-id="f5d30-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5d30-126">Requirement</span></span> | <span data-ttu-id="f5d30-127">Value</span><span class="sxs-lookup"><span data-stu-id="f5d30-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5d30-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f5d30-128">Header</span></span><br/>  | <dl> <span data-ttu-id="f5d30-129"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5d30-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f5d30-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f5d30-130">Library</span></span><br/> | <dl> <span data-ttu-id="f5d30-131"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5d30-131"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5d30-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5d30-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5d30-133">**Interfaz IAMTimelineTransable**</span><span class="sxs-lookup"><span data-stu-id="f5d30-133">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="f5d30-134">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="f5d30-134">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




