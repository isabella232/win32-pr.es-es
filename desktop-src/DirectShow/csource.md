---
description: La clase CSource es una clase base para la implementación de filtros de origen. Un filtro derivado de CSource contiene uno o varios PIN de salida derivados de la clase CSourceStream. Cada pin de salida crea un subproceso de trabajo que envía muestras de multimedia de bajada.
ms.assetid: 25bd0334-4ad1-48ed-93f9-b36c13a280a3
title: Clase CSource (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4fcecbd1973c54e30c9bf1251bed174aa4a469f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690532"
---
# <a name="csource-class"></a><span data-ttu-id="2a97b-105">Clase CSource</span><span class="sxs-lookup"><span data-stu-id="2a97b-105">CSource class</span></span>

![jerarquía de clases csource](images/source01.png)

<span data-ttu-id="2a97b-107">La clase **CSource** es una clase base para la implementación de filtros de origen.</span><span class="sxs-lookup"><span data-stu-id="2a97b-107">The **CSource** class is a base class for implementing source filters.</span></span> <span data-ttu-id="2a97b-108">Un filtro derivado de **CSource** contiene uno o varios PIN de salida derivados de la clase [**CSourceStream**](csourcestream.md) .</span><span class="sxs-lookup"><span data-stu-id="2a97b-108">A filter derived from **CSource** contains one or more output pins derived from the [**CSourceStream**](csourcestream.md) class.</span></span> <span data-ttu-id="2a97b-109">Cada pin de salida crea un subproceso de trabajo que envía muestras de multimedia de bajada.</span><span class="sxs-lookup"><span data-stu-id="2a97b-109">Each output pin creates a worker thread that pushes media samples downstream.</span></span>

> [!Note]  
> <span data-ttu-id="2a97b-110">La clase **CSource** está diseñada para admitir el modelo de entrada para el flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="2a97b-110">The **CSource** class is designed to support the push model for data flow.</span></span> <span data-ttu-id="2a97b-111">Esta clase no se recomienda para crear filtros de lector de archivos.</span><span class="sxs-lookup"><span data-stu-id="2a97b-111">This class is not recommended for creating file-reader filters.</span></span> <span data-ttu-id="2a97b-112">Los lectores de archivos deben admitir el modelo de extracción a través de la interfaz [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .</span><span class="sxs-lookup"><span data-stu-id="2a97b-112">File readers should support the pull model, through the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span> <span data-ttu-id="2a97b-113">Para obtener más información, vea [flujo de datos para desarrolladores de filtros](data-flow-for-filter-developers.md).</span><span class="sxs-lookup"><span data-stu-id="2a97b-113">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

 



| <span data-ttu-id="2a97b-114">Variables de miembro protegidas</span><span class="sxs-lookup"><span data-stu-id="2a97b-114">Protected Member Variables</span></span>                     | <span data-ttu-id="2a97b-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a97b-115">Description</span></span>                                                  |
|------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="2a97b-116">**m \_ iPins**</span><span class="sxs-lookup"><span data-stu-id="2a97b-116">**m\_iPins**</span></span>](csource-m-ipins.md)            | <span data-ttu-id="2a97b-117">Número de clavijas en el filtro.</span><span class="sxs-lookup"><span data-stu-id="2a97b-117">Number of pins on the filter.</span></span>                                |
| [<span data-ttu-id="2a97b-118">**m en las \_ secuencias**</span><span class="sxs-lookup"><span data-stu-id="2a97b-118">**m\_paStreams**</span></span>](csource-m-pastreams.md)    | <span data-ttu-id="2a97b-119">Matriz de clavijas.</span><span class="sxs-lookup"><span data-stu-id="2a97b-119">Array of pins.</span></span>                                               |
| [<span data-ttu-id="2a97b-120">**m \_ cStateLock**</span><span class="sxs-lookup"><span data-stu-id="2a97b-120">**m\_cStateLock**</span></span>](csource-m-cstatelock.md)  | <span data-ttu-id="2a97b-121">Objeto de sección crítica que protege el estado del filtro.</span><span class="sxs-lookup"><span data-stu-id="2a97b-121">Critical section object that protects the filter state.</span></span>      |
| <span data-ttu-id="2a97b-122">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="2a97b-122">Public Methods</span></span>                                 | <span data-ttu-id="2a97b-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a97b-123">Description</span></span>                                                  |
| [<span data-ttu-id="2a97b-124">**CSource**</span><span class="sxs-lookup"><span data-stu-id="2a97b-124">**CSource**</span></span>](csource-csource.md)             | <span data-ttu-id="2a97b-125">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="2a97b-125">Constructor method.</span></span>                                          |
| [<span data-ttu-id="2a97b-126">**~ CSource**</span><span class="sxs-lookup"><span data-stu-id="2a97b-126">**~CSource**</span></span>](csource--csource.md)           | <span data-ttu-id="2a97b-127">Método de destructor.</span><span class="sxs-lookup"><span data-stu-id="2a97b-127">Destructor method.</span></span>                                           |
| [<span data-ttu-id="2a97b-128">**GetPinCount**</span><span class="sxs-lookup"><span data-stu-id="2a97b-128">**GetPinCount**</span></span>](csource-getpincount.md)     | <span data-ttu-id="2a97b-129">Recupera el número de clavijas del filtro.</span><span class="sxs-lookup"><span data-stu-id="2a97b-129">Retrieves the number of pins on the filter.</span></span>                  |
| [<span data-ttu-id="2a97b-130">**GetPin**</span><span class="sxs-lookup"><span data-stu-id="2a97b-130">**GetPin**</span></span>](csource-getpin.md)               | <span data-ttu-id="2a97b-131">Recupera un código PIN.</span><span class="sxs-lookup"><span data-stu-id="2a97b-131">Retrieves a pin.</span></span>                                             |
| [<span data-ttu-id="2a97b-132">**pStateLock**</span><span class="sxs-lookup"><span data-stu-id="2a97b-132">**pStateLock**</span></span>](csource--pstatelock.md)      | <span data-ttu-id="2a97b-133">Recupera un puntero al objeto de sección crítica del filtro.</span><span class="sxs-lookup"><span data-stu-id="2a97b-133">Retrieves a pointer to the filter's critical section object.</span></span> |
| [<span data-ttu-id="2a97b-134">**AddPin**</span><span class="sxs-lookup"><span data-stu-id="2a97b-134">**AddPin**</span></span>](csource-addpin.md)               | <span data-ttu-id="2a97b-135">Agrega un nuevo PIN de salida al filtro.</span><span class="sxs-lookup"><span data-stu-id="2a97b-135">Adds a new output pin to the filter.</span></span>                         |
| [<span data-ttu-id="2a97b-136">**RemovePin**</span><span class="sxs-lookup"><span data-stu-id="2a97b-136">**RemovePin**</span></span>](csource-removepin.md)         | <span data-ttu-id="2a97b-137">Quita un punto de conexión especificado del filtro.</span><span class="sxs-lookup"><span data-stu-id="2a97b-137">Removes a specified pin from the filter.</span></span>                     |
| [<span data-ttu-id="2a97b-138">**FindPinNumber**</span><span class="sxs-lookup"><span data-stu-id="2a97b-138">**FindPinNumber**</span></span>](csource-findpinnumber.md) | <span data-ttu-id="2a97b-139">Recupera el número de un PIN especificado en el filtro.</span><span class="sxs-lookup"><span data-stu-id="2a97b-139">Retrieves the number of a specified pin on the filter.</span></span>       |
| <span data-ttu-id="2a97b-140">Métodos IBaseFilter</span><span class="sxs-lookup"><span data-stu-id="2a97b-140">IBaseFilter Methods</span></span>                            | <span data-ttu-id="2a97b-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a97b-141">Description</span></span>                                                  |
| [<span data-ttu-id="2a97b-142">**FindPin**</span><span class="sxs-lookup"><span data-stu-id="2a97b-142">**FindPin**</span></span>](csource-findpin.md)             | <span data-ttu-id="2a97b-143">Recupera el pin con el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="2a97b-143">Retrieves the pin with the specified identifier.</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="2a97b-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2a97b-144">Remarks</span></span>

<span data-ttu-id="2a97b-145">Para implementar un PIN de salida, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2a97b-145">To implement an output pin, do the following:</span></span>

-   <span data-ttu-id="2a97b-146">Derive una clase de [**CSourceStream**](csourcestream.md).</span><span class="sxs-lookup"><span data-stu-id="2a97b-146">Derive a class from [**CSourceStream**](csourcestream.md).</span></span>
-   <span data-ttu-id="2a97b-147">Invalide el método [**CSourceStream:: GetMediaType**](csourcestream-getmediatype.md) y, posiblemente, el método [**CSourceStream:: CheckMediaType**](csourcestream-checkmediatype.md) , que valida los tipos de medios para el PIN.</span><span class="sxs-lookup"><span data-stu-id="2a97b-147">Override the [**CSourceStream::GetMediaType**](csourcestream-getmediatype.md) method and possibly the [**CSourceStream::CheckMediaType**](csourcestream-checkmediatype.md) method, which validate media types for the pin.</span></span>
-   <span data-ttu-id="2a97b-148">Implemente el método [**CBaseOutputPin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) , que devuelve los requisitos de búfer del PIN.</span><span class="sxs-lookup"><span data-stu-id="2a97b-148">Implement the [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md) method, which returns the pin's buffer requirements.</span></span>
-   <span data-ttu-id="2a97b-149">Implemente el método [**CSourceStream:: FillBuffer**](csourcestream-fillbuffer.md) , que rellena un búfer de ejemplo multimedia con datos.</span><span class="sxs-lookup"><span data-stu-id="2a97b-149">Implement the [**CSourceStream::FillBuffer**](csourcestream-fillbuffer.md) method, which fills a media sample buffer with data.</span></span>

<span data-ttu-id="2a97b-150">Para implementar el filtro, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2a97b-150">To implement the filter, do the following:</span></span>

-   <span data-ttu-id="2a97b-151">Derive una clase de **CSource**.</span><span class="sxs-lookup"><span data-stu-id="2a97b-151">Derive a class from **CSource**.</span></span>
-   <span data-ttu-id="2a97b-152">En el constructor, cree uno o varios PIN de salida derivados de [**CSourceStream**](csourcestream.md).</span><span class="sxs-lookup"><span data-stu-id="2a97b-152">In the constructor, create one or more output pins derived from [**CSourceStream**](csourcestream.md).</span></span> <span data-ttu-id="2a97b-153">Los PIN se agregan automáticamente al filtro en sus métodos de constructor y se quitan a sí mismos en sus métodos de destructor.</span><span class="sxs-lookup"><span data-stu-id="2a97b-153">The pins automatically add themselves to the filter in their constructor methods, and remove themselves in their destructor methods.</span></span>

<span data-ttu-id="2a97b-154">Para sincronizar el estado del filtro entre varios subprocesos, llame al método [**CSource::P statelock**](csource--pstatelock.md) .</span><span class="sxs-lookup"><span data-stu-id="2a97b-154">To synchronize the filter state among multiple threads, call the [**CSource::pStateLock**](csource--pstatelock.md) method.</span></span> <span data-ttu-id="2a97b-155">Este método devuelve un puntero a la sección crítica de estado de filtro.</span><span class="sxs-lookup"><span data-stu-id="2a97b-155">This method returns a pointer to the filter-state critical section.</span></span> <span data-ttu-id="2a97b-156">Use la clase [**CAutoLock**](cautolock.md) para almacenar la sección crítica.</span><span class="sxs-lookup"><span data-stu-id="2a97b-156">Use the [**CAutoLock**](cautolock.md) class to hold the critical section.</span></span> <span data-ttu-id="2a97b-157">Desde un PIN, puede acceder a **pStateLock** desde la variable miembro [**CBasePin:: m \_ pFilter**](cbasepin-m-pfilter.md) del PIN, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="2a97b-157">From a pin, you can access **pStateLock** from the pin's [**CBasePin::m\_pFilter**](cbasepin-m-pfilter.md) member variable, as follows:</span></span>


```
CAutoLock lock(m_pFilter->pStateLock());
```



## <a name="requirements"></a><span data-ttu-id="2a97b-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a97b-158">Requirements</span></span>



| <span data-ttu-id="2a97b-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a97b-159">Requirement</span></span> | <span data-ttu-id="2a97b-160">Value</span><span class="sxs-lookup"><span data-stu-id="2a97b-160">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a97b-161">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2a97b-161">Header</span></span><br/>  | <dl> <span data-ttu-id="2a97b-162"><dt>Source. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2a97b-162"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="2a97b-163">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2a97b-163">Library</span></span><br/> | <dl> <span data-ttu-id="2a97b-164"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2a97b-164"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a97b-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a97b-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a97b-166">Escribir filtros de origen</span><span class="sxs-lookup"><span data-stu-id="2a97b-166">Writing Source Filters</span></span>](writing-source-filters.md)
</dt> </dl>

 

 




