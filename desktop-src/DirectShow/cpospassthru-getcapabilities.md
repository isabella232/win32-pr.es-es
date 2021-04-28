---
description: 'Método CPosPassThru.GetCapabilities: el método GetCapabilities recupera todas las funcionalidades de búsqueda de la secuencia. Este método implementa el método IMediaSeeking::GetCapabilities.'
ms.assetid: c60c4f47-48de-47d0-9b87-589b84df842c
title: Método CPosPassThru.GetCapabilities (Ctlutil.h)
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
ms.openlocfilehash: c21838d3df72d52255d0a2e35dd0b7d34ef55411
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085573"
---
# <a name="cpospassthrugetcapabilities-method"></a><span data-ttu-id="04185-104">Método CPosPassThru.GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="04185-104">CPosPassThru.GetCapabilities method</span></span>

<span data-ttu-id="04185-105">El **método GetCapabilities** recupera todas las funcionalidades de búsqueda de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="04185-105">The **GetCapabilities** method retrieves all the seeking capabilities of the stream.</span></span> <span data-ttu-id="04185-106">Este método implementa el [**método IMediaSeeking::GetCapabilities.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities)</span><span class="sxs-lookup"><span data-stu-id="04185-106">This method implements the [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="04185-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="04185-107">Syntax</span></span>


```C++
HRESULT GetCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="04185-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="04185-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04185-109">*pCapabilities*</span><span class="sxs-lookup"><span data-stu-id="04185-109">*pCapabilities*</span></span> 
</dt> <dd>

<span data-ttu-id="04185-110">Puntero a una variable que recibe una combinación bit a bit de marcas [**\_ AM SEEKING SEEKING \_ \_ CAPABILITIES.**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities)</span><span class="sxs-lookup"><span data-stu-id="04185-110">Pointer to a variable that receives a bitwise combination of [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) flags.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04185-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="04185-111">Return value</span></span>

<span data-ttu-id="04185-112">Devuelve el **valor HRESULT** del pin conectado.</span><span class="sxs-lookup"><span data-stu-id="04185-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="04185-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04185-113">Requirements</span></span>



| <span data-ttu-id="04185-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="04185-114">Requirement</span></span> | <span data-ttu-id="04185-115">Value</span><span class="sxs-lookup"><span data-stu-id="04185-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04185-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="04185-116">Header</span></span><br/>  | <dl> <span data-ttu-id="04185-117"><dt>Ctlutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="04185-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="04185-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="04185-118">Library</span></span><br/> | <dl> <span data-ttu-id="04185-119"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="04185-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04185-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="04185-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04185-121">**CPosPassThru (clase)**</span><span class="sxs-lookup"><span data-stu-id="04185-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




