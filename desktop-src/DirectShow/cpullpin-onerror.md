---
description: Se llama al método OnError si se produce un error durante el streaming. La clase derivada debe implementar este método.
ms.assetid: 0f135cab-611c-4464-9605-360a30de7eb3
title: Método CPullPin. OnError (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.OnError
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2dc8bf7f307ab56609b5f90f6955a1f666854270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671382"
---
# <a name="cpullpinonerror-method"></a><span data-ttu-id="c0eb1-104">CPullPin. OnError (método)</span><span class="sxs-lookup"><span data-stu-id="c0eb1-104">CPullPin.OnError method</span></span>

<span data-ttu-id="c0eb1-105">`OnError`Se llama al método si se produce un error durante el streaming.</span><span class="sxs-lookup"><span data-stu-id="c0eb1-105">The `OnError` method is called if an error occurs during streaming.</span></span> <span data-ttu-id="c0eb1-106">La clase derivada debe implementar este método.</span><span class="sxs-lookup"><span data-stu-id="c0eb1-106">The derived class must implement this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0eb1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c0eb1-107">Syntax</span></span>


```C++
virtual void OnError(
   HRESULT hr
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="c0eb1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c0eb1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0eb1-109">*h*</span><span class="sxs-lookup"><span data-stu-id="c0eb1-109">*hr*</span></span> 
</dt> <dd>

<span data-ttu-id="c0eb1-110">Especifica el valor **HRESULT** devuelto por el método en el que se produjo el error.</span><span class="sxs-lookup"><span data-stu-id="c0eb1-110">Specifies the **HRESULT** value returned by the method that failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0eb1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c0eb1-111">Return value</span></span>

<span data-ttu-id="c0eb1-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c0eb1-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0eb1-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c0eb1-113">Remarks</span></span>

<span data-ttu-id="c0eb1-114">El objeto llama a este método siempre que se produce un error que detiene el subproceso de extracción de datos.</span><span class="sxs-lookup"><span data-stu-id="c0eb1-114">The object calls this method whenever an error occurs that halts the data-pulling thread.</span></span> <span data-ttu-id="c0eb1-115">El filtro puede utilizar este método para recuperar los errores de transmisión por secuencias correctamente.</span><span class="sxs-lookup"><span data-stu-id="c0eb1-115">The filter can use this method to recover from streaming errors gracefully.</span></span> <span data-ttu-id="c0eb1-116">En la mayoría de los casos, el error se devuelve desde el filtro de nivel superior, por lo que el filtro de nivel superior es responsable de notificarlo al administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="c0eb1-116">In most cases, the error is returned from the upstream filter, so the upstream filter is responsible for reporting it to the Filter Graph Manager.</span></span> <span data-ttu-id="c0eb1-117">Si el error se produce en el método [**CPullPin:: Receive**](cpullpin-receive.md) , el filtro debe enviar un evento [**\_ ERRORABORT de EC**](ec-errorabort.md) .</span><span class="sxs-lookup"><span data-stu-id="c0eb1-117">If the error occurs inside the [**CPullPin::Receive**](cpullpin-receive.md) method, your filter should send an [**EC\_ERRORABORT**](ec-errorabort.md) event.</span></span> <span data-ttu-id="c0eb1-118">(Vea [**IMediaEventSink:: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify)).</span><span class="sxs-lookup"><span data-stu-id="c0eb1-118">(See [**IMediaEventSink::Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify).)</span></span>

## <a name="requirements"></a><span data-ttu-id="c0eb1-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0eb1-119">Requirements</span></span>



| <span data-ttu-id="c0eb1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0eb1-120">Requirement</span></span> | <span data-ttu-id="c0eb1-121">Value</span><span class="sxs-lookup"><span data-stu-id="c0eb1-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0eb1-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c0eb1-122">Header</span></span><br/>  | <dl> <span data-ttu-id="c0eb1-123"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0eb1-123"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="c0eb1-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c0eb1-124">Library</span></span><br/> | <dl> <span data-ttu-id="c0eb1-125"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c0eb1-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0eb1-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="c0eb1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0eb1-127">**Clase CPullPin**</span><span class="sxs-lookup"><span data-stu-id="c0eb1-127">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




