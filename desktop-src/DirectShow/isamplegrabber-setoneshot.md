---
description: El método SetOneShot especifica si el filtro de enganche de ejemplo se detiene después de que el filtro reciba un ejemplo.
ms.assetid: 7e3a3e8c-1834-425b-9657-279ab4451a2b
title: 'ISampleGrabber:: SetOneShot (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetOneShot
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 72a6e0e1798bcb8e19807619e982f487b0f04e6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679507"
---
# <a name="isamplegrabbersetoneshot-method"></a><span data-ttu-id="277f8-103">ISampleGrabber:: SetOneShot (método)</span><span class="sxs-lookup"><span data-stu-id="277f8-103">ISampleGrabber::SetOneShot method</span></span>

> [!Note]  
> <span data-ttu-id="277f8-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="277f8-104">\[Deprecated.</span></span> <span data-ttu-id="277f8-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="277f8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="277f8-106">El método **SetOneShot** especifica si el filtro de [**enganche de ejemplo**](sample-grabber-filter.md) se detiene después de que el filtro reciba un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="277f8-106">The **SetOneShot** method specifies whether the [**Sample Grabber**](sample-grabber-filter.md) filter halts after the filter receives a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="277f8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="277f8-107">Syntax</span></span>


```C++
HRESULT SetOneShot(
   BOOL OneShot
);
```



## <a name="parameters"></a><span data-ttu-id="277f8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="277f8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="277f8-109">*OneShot*</span><span class="sxs-lookup"><span data-stu-id="277f8-109">*OneShot*</span></span> 
</dt> <dd>

<span data-ttu-id="277f8-110">Valor booleano que especifica si el filtro de enganche de ejemplo se detiene tras recibir un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="277f8-110">A Boolean value that specifies whether the Sample Grabber filter halts after receiving a sample.</span></span>



| <span data-ttu-id="277f8-111">Value</span><span class="sxs-lookup"><span data-stu-id="277f8-111">Value</span></span>                                                                                                                                    | <span data-ttu-id="277f8-112">Significado</span><span class="sxs-lookup"><span data-stu-id="277f8-112">Meaning</span></span>                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="277f8-113"><dt>TRUE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="277f8-113"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>    | <span data-ttu-id="277f8-114">El enganche de ejemplo se detiene después del primer ejemplo.</span><span class="sxs-lookup"><span data-stu-id="277f8-114">The Sample Grabber halts after the first sample.</span></span> <br/>                                                      |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="277f8-115"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="277f8-115"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="277f8-116">Después del primer ejemplo, el enganche de ejemplo continúa procesando ejemplos.</span><span class="sxs-lookup"><span data-stu-id="277f8-116">After the first sample, the Sample Grabber continues to process samples.</span></span> <span data-ttu-id="277f8-117">Este es el comportamiento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="277f8-117">This is the default behavior.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="277f8-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="277f8-118">Return value</span></span>

<span data-ttu-id="277f8-119">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="277f8-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="277f8-120">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="277f8-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="277f8-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="277f8-121">Remarks</span></span>

<span data-ttu-id="277f8-122">Use este método para obtener una muestra única de la secuencia, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="277f8-122">Use this method to get a single sample from the stream, as follows:</span></span>

1.  <span data-ttu-id="277f8-123">Llame a **SetOneShot** con el valor **true**.</span><span class="sxs-lookup"><span data-stu-id="277f8-123">Call **SetOneShot** with the value **TRUE**.</span></span>
2.  <span data-ttu-id="277f8-124">Opcionalmente, use la interfaz [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) para buscar una posición en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="277f8-124">Optionally, use the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface to seek to a position in the stream.</span></span>
3.  <span data-ttu-id="277f8-125">Llame a [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) para ejecutar el gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="277f8-125">Call [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) to run the filter graph.</span></span>
4.  <span data-ttu-id="277f8-126">Llame a [**IMediaEvent:: WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) para esperar a que el gráfico se detenga.</span><span class="sxs-lookup"><span data-stu-id="277f8-126">Call [**IMediaEvent::WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) to wait for the graph to halt.</span></span> <span data-ttu-id="277f8-127">Como alternativa, llame a [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) para obtener eventos de gráfico, hasta que reciba el evento de [**\_ finalización de EC**](ec-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="277f8-127">Alternatively, call [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) to get graph events, until you receive the [**EC\_COMPLETE**](ec-complete.md) event.</span></span>

<span data-ttu-id="277f8-128">Una vez que se detiene el enganche de ejemplo, el gráfico de filtro sigue en estado en ejecución.</span><span class="sxs-lookup"><span data-stu-id="277f8-128">After the Sample Grabber halts, the filter graph is still in a running state.</span></span> <span data-ttu-id="277f8-129">Puede buscar o pausar el gráfico para obtener otro ejemplo.</span><span class="sxs-lookup"><span data-stu-id="277f8-129">You can seek or pause the graph to get another sample.</span></span>

> [!Note]  
> <span data-ttu-id="277f8-130">Una versión anterior de la documentación indicó que el gráfico de filtro se detiene una vez recibido el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="277f8-130">An earlier version of the documentation stated that the filter graph stops after the sample is received.</span></span> <span data-ttu-id="277f8-131">Eso no es preciso.</span><span class="sxs-lookup"><span data-stu-id="277f8-131">That is not accurate.</span></span> <span data-ttu-id="277f8-132">La secuencia finaliza, pero el gráfico permanece en el estado en ejecución.</span><span class="sxs-lookup"><span data-stu-id="277f8-132">The stream ends, but the graph remains in the running state.</span></span>

 

<span data-ttu-id="277f8-133">El enganche de ejemplo implementa el modo de una sola toma llamando a [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) en el filtro de nivel inferior y devuelve S \_ false desde el método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) .</span><span class="sxs-lookup"><span data-stu-id="277f8-133">The Sample Grabber implements one-shot mode by calling [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) on the downstream filter and returning S\_FALSE from the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method of it.</span></span>

> [!Note]  
> <span data-ttu-id="277f8-134">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="277f8-134">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="277f8-135">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="277f8-135">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="277f8-136">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="277f8-136">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="277f8-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="277f8-137">Requirements</span></span>



| <span data-ttu-id="277f8-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="277f8-138">Requirement</span></span> | <span data-ttu-id="277f8-139">Value</span><span class="sxs-lookup"><span data-stu-id="277f8-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="277f8-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="277f8-140">Header</span></span><br/>  | <dl> <span data-ttu-id="277f8-141"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="277f8-141"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="277f8-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="277f8-142">Library</span></span><br/> | <dl> <span data-ttu-id="277f8-143"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="277f8-143"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="277f8-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="277f8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="277f8-145">Usar el enganche de ejemplo</span><span class="sxs-lookup"><span data-stu-id="277f8-145">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="277f8-146">**Interfaz ISampleGrabber**</span><span class="sxs-lookup"><span data-stu-id="277f8-146">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




