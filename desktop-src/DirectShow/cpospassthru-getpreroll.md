---
description: 'El método GetPreroll recupera la cantidad de datos que se pondrán en cola antes de la posición de inicio. Este método implementa el método IMediaSeeking:: GetPreroll.'
ms.assetid: b00de2fa-ba3c-4a16-ad67-adf3df52ef9a
title: Método CPosPassThru. GetPreroll (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e72d7c83c8cdb0fa08a4b395fd65c80edbe3fb05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680509"
---
# <a name="cpospassthrugetpreroll-method"></a><span data-ttu-id="56897-104">CPosPassThru. GetPreroll, método</span><span class="sxs-lookup"><span data-stu-id="56897-104">CPosPassThru.GetPreroll method</span></span>

<span data-ttu-id="56897-105">El `GetPreroll` método recupera la cantidad de datos que se pondrán en cola antes de la posición de inicio.</span><span class="sxs-lookup"><span data-stu-id="56897-105">The `GetPreroll` method retrieves the amount of data that will be queued before the start position.</span></span> <span data-ttu-id="56897-106">Este método implementa el método [**IMediaSeeking:: GetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) .</span><span class="sxs-lookup"><span data-stu-id="56897-106">This method implements the [**IMediaSeeking::GetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="56897-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="56897-107">Syntax</span></span>


```C++
HRESULT GetPreroll(
   LONGLONG *pllPreroll
);
```



## <a name="parameters"></a><span data-ttu-id="56897-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="56897-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56897-109">*pllPreroll*</span><span class="sxs-lookup"><span data-stu-id="56897-109">*pllPreroll*</span></span> 
</dt> <dd>

<span data-ttu-id="56897-110">Puntero a una variable que recibe el tiempo de prelanzamiento, en unidades del formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="56897-110">Pointer to a variable that receives the preroll time, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56897-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="56897-111">Return value</span></span>

<span data-ttu-id="56897-112">Devuelve el valor **HRESULT** del PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="56897-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="56897-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56897-113">Requirements</span></span>



| <span data-ttu-id="56897-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="56897-114">Requirement</span></span> | <span data-ttu-id="56897-115">Value</span><span class="sxs-lookup"><span data-stu-id="56897-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56897-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="56897-116">Header</span></span><br/>  | <dl> <span data-ttu-id="56897-117"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="56897-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="56897-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="56897-118">Library</span></span><br/> | <dl> <span data-ttu-id="56897-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="56897-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56897-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="56897-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56897-121">**Clase CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="56897-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




