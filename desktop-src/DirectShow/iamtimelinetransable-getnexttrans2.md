---
description: 'El método GetNextTrans2 recupera la primera transición que aparece en el momento especificado o posterior. Este método es equivalente a IAMTimelineTransable:: GetNextTrans, pero toma un valor REFTIME.'
ms.assetid: e6910e94-f289-4a5d-9976-1e8f7373c882
title: 'IAMTimelineTransable:: GetNextTrans2 (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetNextTrans2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2c5f79ff20507247fbcac3badceaf2c3e28f0303
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690997"
---
# <a name="iamtimelinetransablegetnexttrans2-method"></a><span data-ttu-id="488de-104">IAMTimelineTransable:: GetNextTrans2 (método)</span><span class="sxs-lookup"><span data-stu-id="488de-104">IAMTimelineTransable::GetNextTrans2 method</span></span>

> [!Note]  
> <span data-ttu-id="488de-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="488de-105">\[Deprecated.</span></span> <span data-ttu-id="488de-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="488de-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="488de-107">El `GetNextTrans2` método recupera la primera transición que aparece en el momento especificado o posterior.</span><span class="sxs-lookup"><span data-stu-id="488de-107">The `GetNextTrans2` method retrieves the first transition that appears at the specified time or later.</span></span> <span data-ttu-id="488de-108">Este método es equivalente a [**IAMTimelineTransable:: GetNextTrans**](iamtimelinetransable-getnexttrans.md), pero toma un valor [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="488de-108">This method is equivalent to [**IAMTimelineTransable::GetNextTrans**](iamtimelinetransable-getnexttrans.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="488de-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="488de-109">Syntax</span></span>


```C++
HRESULT GetNextTrans2(
  [out] IAMTimelineObj **ppTrans,
        REFTIME        *pInOut
);
```



## <a name="parameters"></a><span data-ttu-id="488de-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="488de-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="488de-111">*ppTrans* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="488de-111">*ppTrans* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="488de-112">Recibe un puntero a la interfaz [**IAMTimelineObj**](iamtimelineobj.md) del objeto de transición.</span><span class="sxs-lookup"><span data-stu-id="488de-112">Receives a pointer to the transition object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="488de-113">*Patilla*</span><span class="sxs-lookup"><span data-stu-id="488de-113">*pInOut*</span></span> 
</dt> <dd>

<span data-ttu-id="488de-114">Puntero a una variable que especifica el tiempo en segundos.</span><span class="sxs-lookup"><span data-stu-id="488de-114">Pointer to a variable that specifies the time in seconds.</span></span> <span data-ttu-id="488de-115">En la entrada, este valor especifica la hora a partir de la que se va a buscar la transición.</span><span class="sxs-lookup"><span data-stu-id="488de-115">On input, this value specifies the time from which to find the transition.</span></span> <span data-ttu-id="488de-116">En la salida, si se recupera una transición, este valor se establece en la hora de detención de la transición.</span><span class="sxs-lookup"><span data-stu-id="488de-116">On output, if a transition is retrieved, this value is set to the stop time of the transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="488de-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="488de-117">Return value</span></span>

<span data-ttu-id="488de-118">Devuelve S \_ OK si el método recupera una transición o es \_ false si no encuentra una transición.</span><span class="sxs-lookup"><span data-stu-id="488de-118">Returns S\_OK if the method retrieves a transition, or S\_FALSE if it does not find a transition.</span></span> <span data-ttu-id="488de-119">De lo contrario, devuelve un valor **HRESULT** que indica la causa del error.</span><span class="sxs-lookup"><span data-stu-id="488de-119">Otherwise, returns an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="488de-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="488de-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="488de-121">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="488de-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="488de-122">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="488de-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="488de-123">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="488de-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="488de-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="488de-124">Requirements</span></span>



| <span data-ttu-id="488de-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="488de-125">Requirement</span></span> | <span data-ttu-id="488de-126">Value</span><span class="sxs-lookup"><span data-stu-id="488de-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="488de-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="488de-127">Header</span></span><br/>  | <dl> <span data-ttu-id="488de-128"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="488de-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="488de-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="488de-129">Library</span></span><br/> | <dl> <span data-ttu-id="488de-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="488de-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="488de-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="488de-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="488de-132">**Interfaz IAMTimelineTransable**</span><span class="sxs-lookup"><span data-stu-id="488de-132">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="488de-133">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="488de-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




