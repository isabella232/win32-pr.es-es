---
description: Método virtual puro que invalidan las clases derivadas.
ms.assetid: 05c73f6b-27f4-4930-b4d5-1688b6bf1791
title: Método CBaseControlVideo. GetStaticImage (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetStaticImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 13b0515e20202373954050b6fa18f10a20a76a6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660715"
---
# <a name="cbasecontrolvideogetstaticimage-method"></a><span data-ttu-id="81b42-103">CBaseControlVideo. GetStaticImage, método</span><span class="sxs-lookup"><span data-stu-id="81b42-103">CBaseControlVideo.GetStaticImage method</span></span>

<span data-ttu-id="81b42-104">Método virtual puro que invalidan las clases derivadas.</span><span class="sxs-lookup"><span data-stu-id="81b42-104">Pure virtual method that derived classes override.</span></span>

## <a name="syntax"></a><span data-ttu-id="81b42-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81b42-105">Syntax</span></span>


```C++
virtual HRESULT GetStaticImage(
   long *pBufferSize,
   long *pDIBImage
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="81b42-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="81b42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81b42-107">*pBufferSize*</span><span class="sxs-lookup"><span data-stu-id="81b42-107">*pBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="81b42-108">Puntero al tamaño del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="81b42-108">Pointer to the size of the output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="81b42-109">*pDIBImage*</span><span class="sxs-lookup"><span data-stu-id="81b42-109">*pDIBImage*</span></span> 
</dt> <dd>

<span data-ttu-id="81b42-110">Puntero al búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="81b42-110">Pointer to the output buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81b42-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="81b42-111">Return value</span></span>

<span data-ttu-id="81b42-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="81b42-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="81b42-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="81b42-113">Remarks</span></span>

<span data-ttu-id="81b42-114">A través de la interfaz [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) , una aplicación puede solicitar que se le proporcione una copia de la imagen actual en un búfer de memoria (algunos representadores pueden devolver E \_ NOTIMPL si no lo admiten).</span><span class="sxs-lookup"><span data-stu-id="81b42-114">Through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface, an application can request that it be given a copy of the current image in a memory buffer (some renderers can return E\_NOTIMPL to this if they do not support it).</span></span> <span data-ttu-id="81b42-115">La clase derivada determina cómo recuperar la imagen.</span><span class="sxs-lookup"><span data-stu-id="81b42-115">The derived class determines how to retrieve the image.</span></span> <span data-ttu-id="81b42-116">Cuando la aplicación llama a **CBaseControlVideo:: GetStaticImage**, llama a este método virtual puro que la clase derivada debe reemplazar para implementarlo.</span><span class="sxs-lookup"><span data-stu-id="81b42-116">When the application calls **CBaseControlVideo::GetStaticImage**, it calls this pure virtual method that the derived class should override to implement it.</span></span> <span data-ttu-id="81b42-117">También se llama mediante la función miembro [**CBaseControlVideo:: GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md) .</span><span class="sxs-lookup"><span data-stu-id="81b42-117">This is also called by the [**CBaseControlVideo::GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md) member function.</span></span>

<span data-ttu-id="81b42-118">La clase proporciona una función miembro auxiliar, [**CBaseControlVideo:: CopyImage**](cbasecontrolvideo-copyimage.md), a la que se puede dar un ejemplo que contiene una imagen, y la función miembro copiará la sección correspondiente de ella (según el rectángulo de origen actual) en el búfer de salida proporcionado por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="81b42-118">The class provides a helper member function, [**CBaseControlVideo::CopyImage**](cbasecontrolvideo-copyimage.md), that can be given a sample that contains an image, and the member function will copy the relevant section of it (based on the current source rectangle) into the output buffer supplied by the application.</span></span>

<span data-ttu-id="81b42-119">En el ejemplo siguiente se muestra una implementación de esta función miembro en una clase derivada.</span><span class="sxs-lookup"><span data-stu-id="81b42-119">The following example demonstrates an implementation of this member function in a derived class.</span></span> <span data-ttu-id="81b42-120">En este ejemplo, m \_ pRenderer contiene un objeto de una clase derivada de [**CBaseVideoRenderer**](cbasevideorenderer.md).</span><span class="sxs-lookup"><span data-stu-id="81b42-120">In this example, m\_pRenderer holds an object of a class derived from [**CBaseVideoRenderer**](cbasevideorenderer.md).</span></span>


```C++
// Return a copy of the current image in the video renderer
HRESULT CVideoText::GetStaticImage(long *pBufferSize,long *pDIBImage)
{
    // Get any sample the renderer may be holding.

    IMediaSample *pMediaSample = m_pRenderer->GetCurrentSample();
    if (pMediaSample == NULL) {
        return E_UNEXPECTED;
    }

    // Call the base class helper method to do the work.

    HRESULT hr = CopyImage(pMediaSample,       // Buffer containing image
                      &m_pRenderer->m_mtIn,    // Type representing bitmap
                      pBufferSize,             // Size of buffer for DIB
                     (BYTE*) pDIBImage);       // Data buffer for output

    pMediaSample->Release();
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="81b42-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81b42-121">Requirements</span></span>



| <span data-ttu-id="81b42-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="81b42-122">Requirement</span></span> | <span data-ttu-id="81b42-123">Value</span><span class="sxs-lookup"><span data-stu-id="81b42-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81b42-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="81b42-124">Header</span></span><br/>  | <dl> <span data-ttu-id="81b42-125"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="81b42-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="81b42-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="81b42-126">Library</span></span><br/> | <dl> <span data-ttu-id="81b42-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="81b42-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81b42-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="81b42-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81b42-129">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="81b42-129">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




