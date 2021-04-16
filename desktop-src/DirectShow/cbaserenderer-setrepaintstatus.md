---
description: El método SetRepaintStatus habilita o deshabilita los eventos Repaint.
ms.assetid: 94ae4935-459e-4009-9f64-c7c5b14504ae
title: Método CBaseRenderer. SetRepaintStatus (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetRepaintStatus
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39822b535680a699654e969abc316c10c54ba51b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671673"
---
# <a name="cbaserenderersetrepaintstatus-method"></a><span data-ttu-id="55638-103">CBaseRenderer. SetRepaintStatus, método</span><span class="sxs-lookup"><span data-stu-id="55638-103">CBaseRenderer.SetRepaintStatus method</span></span>

<span data-ttu-id="55638-104">El `SetRepaintStatus` método habilita o deshabilita los eventos Repaint.</span><span class="sxs-lookup"><span data-stu-id="55638-104">The `SetRepaintStatus` method enables or disables repaint events.</span></span>

## <a name="syntax"></a><span data-ttu-id="55638-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="55638-105">Syntax</span></span>


```C++
void SetRepaintStatus(
   BOOL bRepaint
);
```



## <a name="parameters"></a><span data-ttu-id="55638-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="55638-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55638-107">*bRepaint*</span><span class="sxs-lookup"><span data-stu-id="55638-107">*bRepaint*</span></span> 
</dt> <dd>

<span data-ttu-id="55638-108">Valor booleano que indica si están habilitados los eventos Repaint.</span><span class="sxs-lookup"><span data-stu-id="55638-108">Boolean value indicating whether repaint events are enabled.</span></span> <span data-ttu-id="55638-109">Si **es true**, el filtro enviará los eventos de [**EC \_ Repaint**](ec-repaint.md) al administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="55638-109">If **TRUE**, the filter will sent [**EC\_REPAINT**](ec-repaint.md) events to the filter graph manager.</span></span> <span data-ttu-id="55638-110">De lo contrario, no enviará \_ eventos de Repaint de EC.</span><span class="sxs-lookup"><span data-stu-id="55638-110">Otherwise, it will not send EC\_REPAINT events.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55638-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="55638-111">Return value</span></span>

<span data-ttu-id="55638-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="55638-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="55638-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="55638-113">Remarks</span></span>

<span data-ttu-id="55638-114">Este método garantiza que el administrador de gráficos de filtro no se inunda con eventos de Repaint de EC redundantes \_ .</span><span class="sxs-lookup"><span data-stu-id="55638-114">This method ensures that the filter graph manager is not flooded with redundant EC\_REPAINT events.</span></span> <span data-ttu-id="55638-115">Una vez que el filtro envía un evento [**re \_ Repaint**](ec-repaint.md) , llama a este método con el valor **true**.</span><span class="sxs-lookup"><span data-stu-id="55638-115">After the filter sends an [**EC\_REPAINT**](ec-repaint.md) event, it calls this method with the value **TRUE**.</span></span> <span data-ttu-id="55638-116">El filtro no envía más eventos de \_ Repaint de EC hasta que reciba más datos.</span><span class="sxs-lookup"><span data-stu-id="55638-116">The filter does not send more EC\_REPAINT events until it receives more data.</span></span>

## <a name="requirements"></a><span data-ttu-id="55638-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55638-117">Requirements</span></span>



| <span data-ttu-id="55638-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="55638-118">Requirement</span></span> | <span data-ttu-id="55638-119">Value</span><span class="sxs-lookup"><span data-stu-id="55638-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55638-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="55638-120">Header</span></span><br/>  | <dl> <span data-ttu-id="55638-121"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="55638-121"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="55638-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="55638-122">Library</span></span><br/> | <dl> <span data-ttu-id="55638-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="55638-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55638-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="55638-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55638-125">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="55638-125">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




