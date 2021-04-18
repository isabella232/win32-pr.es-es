---
description: El método copy copia un ejemplo multimedia.
ms.assetid: 3fbc6925-6e9c-4419-ab0d-0bbdbdf9bb8e
title: Método CTransInPlaceFilter. Copy (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Copy
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3063427611cd3a5aae74fecf6be273c07fdb917c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681104"
---
# <a name="ctransinplacefiltercopy-method"></a><span data-ttu-id="2f529-103">CTransInPlaceFilter. Copy (método)</span><span class="sxs-lookup"><span data-stu-id="2f529-103">CTransInPlaceFilter.Copy method</span></span>

<span data-ttu-id="2f529-104">El `Copy` método copia un ejemplo multimedia.</span><span class="sxs-lookup"><span data-stu-id="2f529-104">The `Copy` method copies a media sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f529-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f529-105">Syntax</span></span>


```C++
IMediaSample* Copy(
   IMediaSample *pSource
);
```



## <a name="parameters"></a><span data-ttu-id="2f529-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f529-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f529-107">*pSource*</span><span class="sxs-lookup"><span data-stu-id="2f529-107">*pSource*</span></span> 
</dt> <dd>

<span data-ttu-id="2f529-108">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="2f529-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f529-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f529-109">Return value</span></span>

<span data-ttu-id="2f529-110">Devuelve un puntero a la interfaz **IMediaSample** en el nuevo ejemplo.</span><span class="sxs-lookup"><span data-stu-id="2f529-110">Returns a pointer to the **IMediaSample** interface on the new sample.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f529-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f529-111">Remarks</span></span>

<span data-ttu-id="2f529-112">Este método recupera un búfer vacío del asignador de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="2f529-112">This method retrieves an empty buffer from the downstream allocator.</span></span> <span data-ttu-id="2f529-113">Copia todas las propiedades de ejemplo de *pSource* en el nuevo ejemplo, junto con los datos reales en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="2f529-113">It copies all of the sample properties from *pSource* into the new sample, along with the actual data in the sample.</span></span> <span data-ttu-id="2f529-114">Si el filtro usa dos asignadores, llama a este método para copiar datos entre búferes.</span><span class="sxs-lookup"><span data-stu-id="2f529-114">If the filter is using two allocators, it calls this method to copy data across buffers.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f529-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f529-115">Requirements</span></span>



| <span data-ttu-id="2f529-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f529-116">Requirement</span></span> | <span data-ttu-id="2f529-117">Value</span><span class="sxs-lookup"><span data-stu-id="2f529-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f529-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f529-118">Header</span></span><br/>  | <dl> <span data-ttu-id="2f529-119"><dt>TRANSip. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f529-119"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2f529-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2f529-120">Library</span></span><br/> | <dl> <span data-ttu-id="2f529-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2f529-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f529-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f529-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f529-123">**Clase CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="2f529-123">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




