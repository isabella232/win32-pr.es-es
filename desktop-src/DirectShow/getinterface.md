---
description: La función GetInterface recupera un puntero de interfaz.
ms.assetid: 75fe8849-c779-4d47-a5ff-5a23308c8a21
title: GetInterface (función) (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetInterface
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 317f08af2a4ff0e9410c61da8b19d14735a14f6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680767"
---
# <a name="getinterface-function"></a><span data-ttu-id="88dbd-103">GetInterface (función)</span><span class="sxs-lookup"><span data-stu-id="88dbd-103">GetInterface function</span></span>

<span data-ttu-id="88dbd-104">La `GetInterface` función recupera un puntero de interfaz.</span><span class="sxs-lookup"><span data-stu-id="88dbd-104">The `GetInterface` function retrieves an interface pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="88dbd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="88dbd-105">Syntax</span></span>


```C++
HRESULT GetInterface(
   LPUNKNOWN pUnk,
   void      **ppv
);
```



## <a name="parameters"></a><span data-ttu-id="88dbd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="88dbd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88dbd-107">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="88dbd-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="88dbd-108">Puntero a la interfaz **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="88dbd-108">Pointer to the **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="88dbd-109">*PPV*</span><span class="sxs-lookup"><span data-stu-id="88dbd-109">*ppv*</span></span> 
</dt> <dd>

<span data-ttu-id="88dbd-110">Dirección de un puntero a la interfaz recuperada.</span><span class="sxs-lookup"><span data-stu-id="88dbd-110">Address of a pointer to the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88dbd-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="88dbd-111">Return value</span></span>

<span data-ttu-id="88dbd-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="88dbd-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="88dbd-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="88dbd-113">Remarks</span></span>

<span data-ttu-id="88dbd-114">Esta función miembro realiza un incremento seguro para subprocesos del recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="88dbd-114">This member function performs a thread-safe increment of the reference count.</span></span> <span data-ttu-id="88dbd-115">Para recuperar la interfaz y agregar una referencia, llame a esta función desde su implementación de reemplazo del método **INonDelegatingUnknown:: NonDelegatingQueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="88dbd-115">To retrieve the interface and add a reference, call this function from your overriding implementation of the **INonDelegatingUnknown::NonDelegatingQueryInterface** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="88dbd-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88dbd-116">Requirements</span></span>



| <span data-ttu-id="88dbd-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="88dbd-117">Requirement</span></span> | <span data-ttu-id="88dbd-118">Value</span><span class="sxs-lookup"><span data-stu-id="88dbd-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88dbd-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="88dbd-119">Header</span></span><br/>  | <dl> <span data-ttu-id="88dbd-120"><dt>ComBase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="88dbd-120"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="88dbd-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="88dbd-121">Library</span></span><br/> | <dl> <span data-ttu-id="88dbd-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="88dbd-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88dbd-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="88dbd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88dbd-124">**Funciones auxiliares de COM**</span><span class="sxs-lookup"><span data-stu-id="88dbd-124">**COM Helper Functions**</span></span>](com-helper-functions.md)
</dt> <dt>

[<span data-ttu-id="88dbd-125">**INonDelegatingUnknown**</span><span class="sxs-lookup"><span data-stu-id="88dbd-125">**INonDelegatingUnknown**</span></span>](inondelegatingunknown.md)
</dt> </dl>

 

 




