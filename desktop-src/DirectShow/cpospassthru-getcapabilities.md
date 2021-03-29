---
description: 'El método GetCapabilities recupera todas las funciones de búsqueda de la secuencia. Este método implementa el método IMediaSeeking:: GetCapabilities.'
ms.assetid: c60c4f47-48de-47d0-9b87-589b84df842c
title: Método CPosPassThru. GetCapabilities (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f896adbc1015cb34e6f9063cb5ebf73e5cdb441c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660506"
---
# <a name="cpospassthrugetcapabilities-method"></a><span data-ttu-id="e0fb9-104">CPosPassThru. GetCapabilities, método</span><span class="sxs-lookup"><span data-stu-id="e0fb9-104">CPosPassThru.GetCapabilities method</span></span>

<span data-ttu-id="e0fb9-105">El método **GetCapabilities** recupera todas las funciones de búsqueda de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="e0fb9-105">The **GetCapabilities** method retrieves all the seeking capabilities of the stream.</span></span> <span data-ttu-id="e0fb9-106">Este método implementa el método [**IMediaSeeking:: GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="e0fb9-106">This method implements the [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0fb9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e0fb9-107">Syntax</span></span>


```C++
HRESULT GetCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="e0fb9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e0fb9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0fb9-109">*pCapabilities*</span><span class="sxs-lookup"><span data-stu-id="e0fb9-109">*pCapabilities*</span></span> 
</dt> <dd>

<span data-ttu-id="e0fb9-110">Puntero a una variable que recibe una combinación bit a bit de los marcadores de búsqueda de [**\_ \_ \_ funciones de búsqueda**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) .</span><span class="sxs-lookup"><span data-stu-id="e0fb9-110">Pointer to a variable that receives a bitwise combination of [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) flags.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0fb9-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e0fb9-111">Return value</span></span>

<span data-ttu-id="e0fb9-112">Devuelve el valor **HRESULT** del PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="e0fb9-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0fb9-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0fb9-113">Requirements</span></span>



| <span data-ttu-id="e0fb9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0fb9-114">Requirement</span></span> | <span data-ttu-id="e0fb9-115">Value</span><span class="sxs-lookup"><span data-stu-id="e0fb9-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0fb9-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e0fb9-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e0fb9-117"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e0fb9-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e0fb9-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e0fb9-118">Library</span></span><br/> | <dl> <span data-ttu-id="e0fb9-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e0fb9-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0fb9-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0fb9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0fb9-121">**Clase CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="e0fb9-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




