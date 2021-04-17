---
description: El método BreakConnect libera el PIN de entrada de una conexión.
ms.assetid: e295cec1-8c8f-471c-8832-075ac7708cb1
title: Método CBaseRenderer. BreakConnect (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98c1e01c15740616541706ca4d9da3ab5e66538c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671080"
---
# <a name="cbaserendererbreakconnect-method"></a><span data-ttu-id="2fb03-103">CBaseRenderer. BreakConnect, método</span><span class="sxs-lookup"><span data-stu-id="2fb03-103">CBaseRenderer.BreakConnect method</span></span>

<span data-ttu-id="2fb03-104">El `BreakConnect` método libera el PIN de entrada de una conexión.</span><span class="sxs-lookup"><span data-stu-id="2fb03-104">The `BreakConnect` method releases the input pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fb03-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2fb03-105">Syntax</span></span>


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="2fb03-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2fb03-106">Parameters</span></span>

<span data-ttu-id="2fb03-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="2fb03-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2fb03-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2fb03-108">Return value</span></span>

<span data-ttu-id="2fb03-109">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="2fb03-109">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="2fb03-110">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2fb03-110">Return code</span></span>                                                                                         | <span data-ttu-id="2fb03-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="2fb03-111">Description</span></span>                            |
|-----------------------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="2fb03-112"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="2fb03-112"><dt>**S\_FALSE**</dt></span></span> </dl>             | <span data-ttu-id="2fb03-113">El PIN no estaba conectado.</span><span class="sxs-lookup"><span data-stu-id="2fb03-113">The pin was not connected.</span></span><br/>  |
| <dl> <span data-ttu-id="2fb03-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="2fb03-114"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="2fb03-115">Correcto.</span><span class="sxs-lookup"><span data-stu-id="2fb03-115">Success.</span></span><br/>                    |
| <dl> <span data-ttu-id="2fb03-116"><dt>**VFW \_ E \_ no \_ detenido**</dt></span><span class="sxs-lookup"><span data-stu-id="2fb03-116"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl> | <span data-ttu-id="2fb03-117">El filtro todavía está activo.</span><span class="sxs-lookup"><span data-stu-id="2fb03-117">The filter is still active.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2fb03-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2fb03-118">Remarks</span></span>

<span data-ttu-id="2fb03-119">El PIN de entrada del filtro llama a este método desde dentro de su propio `BreakConnect` método.</span><span class="sxs-lookup"><span data-stu-id="2fb03-119">The filter's input pin calls this method from inside its own `BreakConnect` method.</span></span> <span data-ttu-id="2fb03-120">(Para obtener más información, vea [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md)). El filtro realiza una contabilidad interna, como el restablecimiento de la marca de fin de secuencia.</span><span class="sxs-lookup"><span data-stu-id="2fb03-120">(For more information, see [**CBasePin::BreakConnect**](cbasepin-breakconnect.md).) The filter performs some internal bookkeeping, such as resetting the end-of-stream flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fb03-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2fb03-121">Requirements</span></span>



| <span data-ttu-id="2fb03-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fb03-122">Requirement</span></span> | <span data-ttu-id="2fb03-123">Value</span><span class="sxs-lookup"><span data-stu-id="2fb03-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fb03-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2fb03-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2fb03-125"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2fb03-125"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2fb03-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2fb03-126">Library</span></span><br/> | <dl> <span data-ttu-id="2fb03-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2fb03-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fb03-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="2fb03-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fb03-129">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="2fb03-129">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




