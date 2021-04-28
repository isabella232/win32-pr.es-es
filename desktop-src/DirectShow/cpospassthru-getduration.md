---
description: 'Método CPosPassThru.GetDuration: el método GetDuration recupera la duración de la secuencia. Este método implementa el método IMediaSeeking::GetDuration.'
ms.assetid: 0552e7bb-4d7e-40a8-a8ad-89ae6fff8ccb
title: Método CPosPassThru.GetDuration (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetDuration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0b0af7bfaca405ed52a4e3c5a63c18b4bc087ba3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085583"
---
# <a name="cpospassthrugetduration-method"></a><span data-ttu-id="40daf-104">Método CPosPassThru.GetDuration</span><span class="sxs-lookup"><span data-stu-id="40daf-104">CPosPassThru.GetDuration method</span></span>

<span data-ttu-id="40daf-105">El `GetDuration` método recupera la duración de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="40daf-105">The `GetDuration` method retrieves the duration of the stream.</span></span> <span data-ttu-id="40daf-106">Este método implementa el [**método IMediaSeeking::GetDuration.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration)</span><span class="sxs-lookup"><span data-stu-id="40daf-106">This method implements the [**IMediaSeeking::GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="40daf-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="40daf-107">Syntax</span></span>


```C++
HRESULT GetDuration(
   LONGLONG *pDuration
);
```



## <a name="parameters"></a><span data-ttu-id="40daf-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="40daf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40daf-109">*pDuration*</span><span class="sxs-lookup"><span data-stu-id="40daf-109">*pDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="40daf-110">Puntero a una variable que recibe la duración, en unidades del formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="40daf-110">Pointer to a variable that receives the duration, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40daf-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="40daf-111">Return value</span></span>

<span data-ttu-id="40daf-112">Devuelve el **valor HRESULT** del pin conectado.</span><span class="sxs-lookup"><span data-stu-id="40daf-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="40daf-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40daf-113">Requirements</span></span>



| <span data-ttu-id="40daf-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="40daf-114">Requirement</span></span> | <span data-ttu-id="40daf-115">Value</span><span class="sxs-lookup"><span data-stu-id="40daf-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40daf-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="40daf-116">Header</span></span><br/>  | <dl> <span data-ttu-id="40daf-117"><dt>Ctlutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="40daf-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="40daf-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="40daf-118">Library</span></span><br/> | <dl> <span data-ttu-id="40daf-119"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="40daf-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40daf-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="40daf-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40daf-121">**CPosPassThru (clase)**</span><span class="sxs-lookup"><span data-stu-id="40daf-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




