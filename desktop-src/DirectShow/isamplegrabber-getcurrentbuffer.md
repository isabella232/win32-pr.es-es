---
description: El método GetCurrentBuffer recupera una copia del búfer asociado al ejemplo más reciente.
ms.assetid: 08550c82-4711-4725-9cd0-19b43cf4c92e
title: 'ISampleGrabber:: GetCurrentBuffer (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.GetCurrentBuffer
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d4df4c825761b42533590f10432bf62e5e4e0298
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680643"
---
# <a name="isamplegrabbergetcurrentbuffer-method"></a><span data-ttu-id="9e75c-103">ISampleGrabber:: GetCurrentBuffer (método)</span><span class="sxs-lookup"><span data-stu-id="9e75c-103">ISampleGrabber::GetCurrentBuffer method</span></span>

> [!Note]  
> <span data-ttu-id="9e75c-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="9e75c-104">\[Deprecated.</span></span> <span data-ttu-id="9e75c-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9e75c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9e75c-106">El método **GetCurrentBuffer** recupera una copia del búfer asociado al ejemplo más reciente.</span><span class="sxs-lookup"><span data-stu-id="9e75c-106">The **GetCurrentBuffer** method retrieves a copy of the buffer associated with the most recent sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e75c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9e75c-107">Syntax</span></span>


```C++
HRESULT GetCurrentBuffer(
  [in, out] long *pBufferSize,
  [out]     long *pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="9e75c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9e75c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e75c-109">*pBufferSize* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="9e75c-109">*pBufferSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e75c-110">Puntero al tamaño del búfer.</span><span class="sxs-lookup"><span data-stu-id="9e75c-110">Pointer to the size of the buffer.</span></span> <span data-ttu-id="9e75c-111">Si *pBuffer* es **null**, este parámetro recibe el tamaño de búfer necesario, en bytes.</span><span class="sxs-lookup"><span data-stu-id="9e75c-111">If *pBuffer* is **NULL**, this parameter receives the required buffer size, in bytes.</span></span> <span data-ttu-id="9e75c-112">Si *pBuffer* no es **null**, establezca este parámetro igual al tamaño del búfer, en bytes.</span><span class="sxs-lookup"><span data-stu-id="9e75c-112">If *pBuffer* is not **NULL**, set this parameter equal to the size of the buffer, in bytes.</span></span> <span data-ttu-id="9e75c-113">En la salida, el parámetro recibe el número de bytes que se copiaron en el búfer.</span><span class="sxs-lookup"><span data-stu-id="9e75c-113">On output, the parameter receives the number of bytes that were copied into the buffer.</span></span> <span data-ttu-id="9e75c-114">Este valor puede ser menor que el tamaño del búfer.</span><span class="sxs-lookup"><span data-stu-id="9e75c-114">This value might be smaller than the size of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="9e75c-115">*pBuffer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9e75c-115">*pBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e75c-116">Puntero a una matriz de bytes de tamaño *pBufferSize* o **null**.</span><span class="sxs-lookup"><span data-stu-id="9e75c-116">Pointer to an array of bytes of size *pBufferSize*, or **NULL**.</span></span> <span data-ttu-id="9e75c-117">Si este parámetro no es **null**, el búfer actual se copia en la matriz.</span><span class="sxs-lookup"><span data-stu-id="9e75c-117">If this parameter is not **NULL**, the current buffer is copied into the array.</span></span> <span data-ttu-id="9e75c-118">Si este parámetro es **null**, el parámetro *pBufferSize* recibe el tamaño de búfer necesario.</span><span class="sxs-lookup"><span data-stu-id="9e75c-118">If this parameter is **NULL**, the *pBufferSize* parameter receives the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e75c-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9e75c-119">Return value</span></span>

<span data-ttu-id="9e75c-120">Devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="9e75c-120">Returns one of the following values.</span></span>



| <span data-ttu-id="9e75c-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9e75c-121">Return code</span></span>                                                                                           | <span data-ttu-id="9e75c-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="9e75c-122">Description</span></span>                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9e75c-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9e75c-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="9e75c-124">Los ejemplos no se almacenan en búfer.</span><span class="sxs-lookup"><span data-stu-id="9e75c-124">Samples are not being buffered.</span></span> <span data-ttu-id="9e75c-125">Llame a [**ISampleGrabber:: SetBufferSamples**](isamplegrabber-setbuffersamples.md).</span><span class="sxs-lookup"><span data-stu-id="9e75c-125">Call [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md).</span></span><br/> |
| <dl> <span data-ttu-id="9e75c-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="9e75c-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>         | <span data-ttu-id="9e75c-127">El búfer especificado no es suficientemente grande.</span><span class="sxs-lookup"><span data-stu-id="9e75c-127">The specified buffer is not large enough.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="9e75c-128"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="9e75c-128"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="9e75c-129">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="9e75c-129">**NULL** pointer argument.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="9e75c-130"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="9e75c-130"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="9e75c-131">Correcto.</span><span class="sxs-lookup"><span data-stu-id="9e75c-131">Success.</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="9e75c-132"><dt>**VFW \_ E \_ no \_ conectada**</dt></span><span class="sxs-lookup"><span data-stu-id="9e75c-132"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="9e75c-133">El filtro no está conectado.</span><span class="sxs-lookup"><span data-stu-id="9e75c-133">The filter is not connected.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="9e75c-134"><dt>**Estado de VFW \_ E \_ incorrecto \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9e75c-134"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>   | <span data-ttu-id="9e75c-135">El filtro no ha recibido todavía ningún ejemplo.</span><span class="sxs-lookup"><span data-stu-id="9e75c-135">The filter has not received any samples yet.</span></span> <span data-ttu-id="9e75c-136">Para ofrecer un ejemplo, ejecute o Pause el gráfico.</span><span class="sxs-lookup"><span data-stu-id="9e75c-136">To deliver a sample, run or pause the graph.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="9e75c-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9e75c-137">Remarks</span></span>

<span data-ttu-id="9e75c-138">Para activar el almacenamiento en búfer, llame a [**ISampleGrabber:: SetBufferSamples**](isamplegrabber-setbuffersamples.md) con un valor de **true**.</span><span class="sxs-lookup"><span data-stu-id="9e75c-138">To activate buffering, call [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) with a value of **TRUE**.</span></span>

<span data-ttu-id="9e75c-139">Llame a este método dos veces.</span><span class="sxs-lookup"><span data-stu-id="9e75c-139">Call this method twice.</span></span> <span data-ttu-id="9e75c-140">En la primera llamada, establezca *pBuffer* en **null**.</span><span class="sxs-lookup"><span data-stu-id="9e75c-140">On the first call, set *pBuffer* to **NULL**.</span></span> <span data-ttu-id="9e75c-141">El tamaño del búfer se devuelve en *pBufferSize*.</span><span class="sxs-lookup"><span data-stu-id="9e75c-141">The size of the buffer is returned in *pBufferSize*.</span></span> <span data-ttu-id="9e75c-142">A continuación, asigne una matriz y llame de nuevo al método.</span><span class="sxs-lookup"><span data-stu-id="9e75c-142">Then allocate an array and call the method again.</span></span> <span data-ttu-id="9e75c-143">En la segunda llamada, se pasa el tamaño de la matriz en *pBufferSize* y se pasa la dirección de la matriz en *pBuffer*.</span><span class="sxs-lookup"><span data-stu-id="9e75c-143">On the second call, pass the size of the array in *pBufferSize*, and pass the address of the array in *pBuffer*.</span></span> <span data-ttu-id="9e75c-144">Si la matriz no es suficientemente grande, el método devuelve E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="9e75c-144">If the array is not large enough, the method returns E\_OUTOFMEMORY.</span></span>

<span data-ttu-id="9e75c-145">El parámetro *pBuffer* se escribe como un puntero **largo** , pero el contenido del búfer depende del formato de los datos.</span><span class="sxs-lookup"><span data-stu-id="9e75c-145">The *pBuffer* parameter is typed as a **long** pointer, but the contents of the buffer depend on the format of the data.</span></span> <span data-ttu-id="9e75c-146">Llame a [**ISampleGrabber:: GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) para obtener el tipo de medio del formato.</span><span class="sxs-lookup"><span data-stu-id="9e75c-146">Call [**ISampleGrabber::GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) to get the media type of the format.</span></span>

<span data-ttu-id="9e75c-147">No llame a este método mientras se está ejecutando el gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="9e75c-147">Do not call this method while the filter graph is running.</span></span> <span data-ttu-id="9e75c-148">Mientras se ejecuta el gráfico de filtros, el filtro de enganche de ejemplo sobrescribe el contenido del búfer cada vez que recibe un nuevo ejemplo.</span><span class="sxs-lookup"><span data-stu-id="9e75c-148">While the filter graph is running, the Sample Grabber filter overwrites the contents of the buffer whenever it receives a new sample.</span></span> <span data-ttu-id="9e75c-149">La mejor manera de utilizar este método es usar el "modo de una sola vacuna", que detiene el gráfico después de recibir el primer ejemplo.</span><span class="sxs-lookup"><span data-stu-id="9e75c-149">The best way to use this method is to use "one-shot mode," which stops the graph after receiving the first sample.</span></span> <span data-ttu-id="9e75c-150">Para establecer el modo de una sola toma, llame a [**ISampleGrabber:: SetOneShot**](isamplegrabber-setoneshot.md).</span><span class="sxs-lookup"><span data-stu-id="9e75c-150">To set one-shot mode, call [**ISampleGrabber::SetOneShot**](isamplegrabber-setoneshot.md).</span></span>

<span data-ttu-id="9e75c-151">El filtro no almacena en búfer ejemplos de prefijo, o muestras en las que el miembro **dwStreamId** de la estructura de [**\_ \_ propiedades AM SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) es distinto de los \_ medios de secuencia AM \_ .</span><span class="sxs-lookup"><span data-stu-id="9e75c-151">The filter does not buffer preroll samples, or samples in which the **dwStreamId** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure is anything other than AM\_STREAM\_MEDIA.</span></span>

> [!Note]  
> <span data-ttu-id="9e75c-152">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="9e75c-152">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9e75c-153">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9e75c-153">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9e75c-154">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="9e75c-154">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9e75c-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e75c-155">Requirements</span></span>



| <span data-ttu-id="9e75c-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e75c-156">Requirement</span></span> | <span data-ttu-id="9e75c-157">Value</span><span class="sxs-lookup"><span data-stu-id="9e75c-157">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e75c-158">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9e75c-158">Header</span></span><br/>  | <dl> <span data-ttu-id="9e75c-159"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e75c-159"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9e75c-160">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9e75c-160">Library</span></span><br/> | <dl> <span data-ttu-id="9e75c-161"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e75c-161"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e75c-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e75c-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e75c-163">Usar el enganche de ejemplo</span><span class="sxs-lookup"><span data-stu-id="9e75c-163">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="9e75c-164">**Interfaz ISampleGrabber**</span><span class="sxs-lookup"><span data-stu-id="9e75c-164">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




