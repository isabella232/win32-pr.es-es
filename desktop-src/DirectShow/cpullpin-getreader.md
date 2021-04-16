---
description: El método GetReader devuelve un puntero a la interfaz IAsyncReader del terminal de salida.
ms.assetid: bb7ed3f2-a5bc-496c-8a52-f9915a75105e
title: Método CPullPin. GetReader (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.GetReader
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a20bbb689c4ee5e3ac12c510098163d9fbb224e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671385"
---
# <a name="cpullpingetreader-method"></a><span data-ttu-id="89576-103">CPullPin. GetReader, método</span><span class="sxs-lookup"><span data-stu-id="89576-103">CPullPin.GetReader method</span></span>

<span data-ttu-id="89576-104">El `GetReader` método devuelve un puntero a la interfaz [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) del terminal de salida.</span><span class="sxs-lookup"><span data-stu-id="89576-104">The `GetReader` method returns a pointer to the output pin's [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="89576-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="89576-105">Syntax</span></span>


```C++
IAsyncReader* GetReader();
```



## <a name="parameters"></a><span data-ttu-id="89576-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="89576-106">Parameters</span></span>

<span data-ttu-id="89576-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="89576-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="89576-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="89576-108">Return value</span></span>

<span data-ttu-id="89576-109">Devuelve un puntero a la interfaz [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .</span><span class="sxs-lookup"><span data-stu-id="89576-109">Returns a pointer to the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="89576-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="89576-110">Remarks</span></span>

<span data-ttu-id="89576-111">La interfaz devuelta tiene un recuento de referencias pendiente.</span><span class="sxs-lookup"><span data-stu-id="89576-111">The returned interface has an outstanding reference count.</span></span> <span data-ttu-id="89576-112">El llamador debe liberar la interfaz.</span><span class="sxs-lookup"><span data-stu-id="89576-112">The caller must release the interface.</span></span>

<span data-ttu-id="89576-113">El método no comprueba el valor del puntero de interfaz antes de llamar a **AddRef**, por lo que no debe llamarlo hasta que se haya llamado correctamente al método [**CPullPin:: Connect**](cpullpin-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="89576-113">The method does not check the value of the interface pointer before calling **AddRef**, so do not call this until you have successfully called the [**CPullPin::Connect**](cpullpin-connect.md) method.</span></span> <span data-ttu-id="89576-114">De lo contrario, el puntero de interfaz podría ser **null** y llamar a **AddRef** producirá una excepción.</span><span class="sxs-lookup"><span data-stu-id="89576-114">Otherwise, the interface pointer might be **NULL** and calling **AddRef** will throw an exception.</span></span>

## <a name="requirements"></a><span data-ttu-id="89576-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89576-115">Requirements</span></span>



| <span data-ttu-id="89576-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="89576-116">Requirement</span></span> | <span data-ttu-id="89576-117">Value</span><span class="sxs-lookup"><span data-stu-id="89576-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89576-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="89576-118">Header</span></span><br/>  | <dl> <span data-ttu-id="89576-119"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="89576-119"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="89576-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="89576-120">Library</span></span><br/> | <dl> <span data-ttu-id="89576-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="89576-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89576-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="89576-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89576-123">**Clase CPullPin**</span><span class="sxs-lookup"><span data-stu-id="89576-123">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




