---
description: El método SetCallback especifica un método de devolución de llamada al que llamar en los ejemplos de entrada.
ms.assetid: b84d3f52-b986-492a-a8b9-1d98618dcdd3
title: 'ISampleGrabber:: SetCallback (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetCallback
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 46e0565c314bab86967ee0d5dabee6ba449a87dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680641"
---
# <a name="isamplegrabbersetcallback-method"></a><span data-ttu-id="74984-103">ISampleGrabber:: SetCallback (método)</span><span class="sxs-lookup"><span data-stu-id="74984-103">ISampleGrabber::SetCallback method</span></span>

> [!Note]  
> <span data-ttu-id="74984-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="74984-104">\[Deprecated.</span></span> <span data-ttu-id="74984-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="74984-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="74984-106">El método **SetCallback** especifica un método de devolución de llamada al que llamar en los ejemplos de entrada.</span><span class="sxs-lookup"><span data-stu-id="74984-106">The **SetCallback** method specifies a callback method to call on incoming samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="74984-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="74984-107">Syntax</span></span>


```C++
HRESULT SetCallback(
   ISampleGrabberCB *pCallback,
   long             WhichMethodToCallback
);
```



## <a name="parameters"></a><span data-ttu-id="74984-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="74984-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74984-109">*pCallback*</span><span class="sxs-lookup"><span data-stu-id="74984-109">*pCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="74984-110">Puntero a una interfaz [**ISampleGrabberCB**](isamplegrabbercb.md) que contiene el método de devolución de llamada o **null** para cancelar la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="74984-110">Pointer to an [**ISampleGrabberCB**](isamplegrabbercb.md) interface containing the callback method, or **NULL** to cancel the callback.</span></span>

</dd> <dt>

<span data-ttu-id="74984-111">*WhichMethodToCallback*</span><span class="sxs-lookup"><span data-stu-id="74984-111">*WhichMethodToCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="74984-112">Índice que especifica el método de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="74984-112">Index specifying the callback method.</span></span> <span data-ttu-id="74984-113">Debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="74984-113">Must be one of the following values.</span></span>



| <span data-ttu-id="74984-114">Value</span><span class="sxs-lookup"><span data-stu-id="74984-114">Value</span></span> | <span data-ttu-id="74984-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="74984-115">Description</span></span>                                                                                                                                                                                     |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74984-116">0</span><span class="sxs-lookup"><span data-stu-id="74984-116">0</span></span>     | <span data-ttu-id="74984-117">El filtro de enganche de ejemplo llama al método [**ISampleGrabberCB:: SampleCB**](isamplegrabbercb-samplecb.md) .</span><span class="sxs-lookup"><span data-stu-id="74984-117">The Sample Grabber filter calls the [**ISampleGrabberCB::SampleCB**](isamplegrabbercb-samplecb.md) method.</span></span> <span data-ttu-id="74984-118">Este método recibe un puntero [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) .</span><span class="sxs-lookup"><span data-stu-id="74984-118">This method receives an [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) pointer.</span></span>               |
| <span data-ttu-id="74984-119">1</span><span class="sxs-lookup"><span data-stu-id="74984-119">1</span></span>     | <span data-ttu-id="74984-120">El filtro de enganche de ejemplo llama al método [**ISampleGrabberCB:: BufferCB**](isamplegrabbercb-buffercb.md) .</span><span class="sxs-lookup"><span data-stu-id="74984-120">The Sample Grabber filter calls the [**ISampleGrabberCB::BufferCB**](isamplegrabbercb-buffercb.md) method.</span></span> <span data-ttu-id="74984-121">Este método recibe un puntero al búfer incluido en el ejemplo multimedia.</span><span class="sxs-lookup"><span data-stu-id="74984-121">This method receives a pointer to the buffer that is contained in the media sample.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74984-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="74984-122">Return value</span></span>

<span data-ttu-id="74984-123">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="74984-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="74984-124">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="74984-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="74984-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="74984-125">Remarks</span></span>

<span data-ttu-id="74984-126">El subproceso de procesamiento de datos se bloquea hasta que se devuelve el método de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="74984-126">The data processing thread blocks until the callback method returns.</span></span> <span data-ttu-id="74984-127">Si la devolución de llamada no vuelve rápidamente, puede interferir con la reproducción.</span><span class="sxs-lookup"><span data-stu-id="74984-127">If the callback does not return quickly, it can interfere with playback.</span></span>

<span data-ttu-id="74984-128">El filtro no invoca la función de devolución de llamada para los ejemplos de prefijo o para los ejemplos en los que el miembro **dwStreamId** de la estructura de [**\_ \_ propiedades AM SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) es distinto de la \_ secuencia de multimedia AM \_ .</span><span class="sxs-lookup"><span data-stu-id="74984-128">The filter does not invoke the callback function for preroll samples, or for samples in which the **dwStreamId** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure is anything other than AM\_STREAM\_MEDIA.</span></span>

> [!Note]  
> <span data-ttu-id="74984-129">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="74984-129">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="74984-130">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="74984-130">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="74984-131">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="74984-131">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="74984-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74984-132">Requirements</span></span>



| <span data-ttu-id="74984-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="74984-133">Requirement</span></span> | <span data-ttu-id="74984-134">Value</span><span class="sxs-lookup"><span data-stu-id="74984-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74984-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="74984-135">Header</span></span><br/>  | <dl> <span data-ttu-id="74984-136"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="74984-136"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="74984-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="74984-137">Library</span></span><br/> | <dl> <span data-ttu-id="74984-138"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74984-138"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74984-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="74984-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74984-140">Usar el enganche de ejemplo</span><span class="sxs-lookup"><span data-stu-id="74984-140">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="74984-141">**Interfaz ISampleGrabber**</span><span class="sxs-lookup"><span data-stu-id="74984-141">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




