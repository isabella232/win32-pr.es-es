---
description: Método de constructor.
ms.assetid: 0b372fa2-78a9-4e38-813c-f18123716c6d
title: Constructor CDeferredCommand. CDeferredCommand (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.CDeferredCommand
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e92a2ffc5129ee38fc5061b28ea7ffef49da0f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681197"
---
# <a name="cdeferredcommandcdeferredcommand-constructor"></a><span data-ttu-id="a8ddc-103">Constructor CDeferredCommand. CDeferredCommand</span><span class="sxs-lookup"><span data-stu-id="a8ddc-103">CDeferredCommand.CDeferredCommand constructor</span></span>

<span data-ttu-id="a8ddc-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="a8ddc-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8ddc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a8ddc-105">Syntax</span></span>


```C++
CDeferredCommand(
   CCmdQueue *pQ,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   LPUNKNOWN pUnkExecutor,
   REFTIME   time,
   GUID      *iid,
   long      dispidMethod,
   short     wFlags,
   long      cArgs,
   VARIANT   *pDispParams,
   VARIANT   *pvarResult,
   short     *puArgErr,
   BOOL      bStream
);
```



## <a name="parameters"></a><span data-ttu-id="a8ddc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8ddc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8ddc-107">*pQ*</span><span class="sxs-lookup"><span data-stu-id="a8ddc-107">*pQ*</span></span> 
</dt> <dd>

<span data-ttu-id="a8ddc-108">Puntero a un objeto que expone la interfaz [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) .</span><span class="sxs-lookup"><span data-stu-id="a8ddc-108">Pointer to an object that exposes the [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) interface.</span></span>

</dd> <dt>

<span data-ttu-id="a8ddc-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="a8ddc-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="a8ddc-110">Puntero a la interfaz **IUnknown** externa para la agregación.</span><span class="sxs-lookup"><span data-stu-id="a8ddc-110">Pointer to the outer **IUnknown** interface for aggregation.</span></span>

</dd> <dt>

<span data-ttu-id="a8ddc-111">*phr*</span><span class="sxs-lookup"><span data-stu-id="a8ddc-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="a8ddc-112">Puntero a un valor **HRESULT** devuelto.</span><span class="sxs-lookup"><span data-stu-id="a8ddc-112">Pointer to a returned **HRESULT** value.</span></span>

</dd> <dt>

<span data-ttu-id="a8ddc-113">*pUnkExecutor*</span><span class="sxs-lookup"><span data-stu-id="a8ddc-113">*pUnkExecutor*</span></span> 
</dt> <dd>

<span data-ttu-id="a8ddc-114">Puntero al objeto que llevará a cabo este comando.</span><span class="sxs-lookup"><span data-stu-id="a8ddc-114">Pointer to the object that will carry out this command.</span></span>

</dd> <dt>

<span data-ttu-id="a8ddc-115">*time*</span><span class="sxs-lookup"><span data-stu-id="a8ddc-115">*time*</span></span> 
</dt> <dd>

<span data-ttu-id="a8ddc-116">Hora a la que se ejecutará el comando.</span><span class="sxs-lookup"><span data-stu-id="a8ddc-116">Time at which the command will be run.</span></span>

</dd> <dt>

<span data-ttu-id="a8ddc-117">*suscripto*</span><span class="sxs-lookup"><span data-stu-id="a8ddc-117">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="a8ddc-118">Puntero al identificador único global (**GUID**) de la interfaz que contiene el método.</span><span class="sxs-lookup"><span data-stu-id="a8ddc-118">Pointer to the globally unique identifier (**GUID**) of the interface that contains the method.</span></span>

</dd> <dt>

<span data-ttu-id="a8ddc-119">*dispidMethod*</span><span class="sxs-lookup"><span data-stu-id="a8ddc-119">*dispidMethod*</span></span> 
</dt> <dd>

<span data-ttu-id="a8ddc-120">Método de la interfaz que se va a llamar.</span><span class="sxs-lookup"><span data-stu-id="a8ddc-120">Method on the interface to call.</span></span>

</dd> <dt>

<span data-ttu-id="a8ddc-121">*wFlags*</span><span class="sxs-lookup"><span data-stu-id="a8ddc-121">*wFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="a8ddc-122">Contexto de la invocación.</span><span class="sxs-lookup"><span data-stu-id="a8ddc-122">Context of the invocation.</span></span>

</dd> <dt>

<span data-ttu-id="a8ddc-123">*cArgs*</span><span class="sxs-lookup"><span data-stu-id="a8ddc-123">*cArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="a8ddc-124">Número de argumentos pasados.</span><span class="sxs-lookup"><span data-stu-id="a8ddc-124">Number of arguments passed.</span></span>

</dd> <dt>

<span data-ttu-id="a8ddc-125">*pDispParams*</span><span class="sxs-lookup"><span data-stu-id="a8ddc-125">*pDispParams*</span></span> 
</dt> <dd>

<span data-ttu-id="a8ddc-126">Puntero a una lista de tipos de variante de argumento.</span><span class="sxs-lookup"><span data-stu-id="a8ddc-126">Pointer to a list of argument variant types.</span></span>

</dd> <dt>

<span data-ttu-id="a8ddc-127">*pvarResult*</span><span class="sxs-lookup"><span data-stu-id="a8ddc-127">*pvarResult*</span></span> 
</dt> <dd>

<span data-ttu-id="a8ddc-128">Puntero a una lista de tipos Variant devuelta, si existe.</span><span class="sxs-lookup"><span data-stu-id="a8ddc-128">Pointer to a returned variant type list, if any.</span></span>

</dd> <dt>

<span data-ttu-id="a8ddc-129">*puArgErr*</span><span class="sxs-lookup"><span data-stu-id="a8ddc-129">*puArgErr*</span></span> 
</dt> <dd>

<span data-ttu-id="a8ddc-130">Puntero al último argumento de la lista de parámetros *pDispParams* con un error.</span><span class="sxs-lookup"><span data-stu-id="a8ddc-130">Pointer to the last argument in the *pDispParams* parameter list with an error.</span></span>

</dd> <dt>

<span data-ttu-id="a8ddc-131">*bStream*</span><span class="sxs-lookup"><span data-stu-id="a8ddc-131">*bStream*</span></span> 
</dt> <dd>

<span data-ttu-id="a8ddc-132">Valor que indica si el tiempo de comando aplazado está en tiempo de secuencia (**true**) o en tiempo de presentación (**false**).</span><span class="sxs-lookup"><span data-stu-id="a8ddc-132">Value indicating whether the deferred command time is in stream time (**TRUE**) or presentation time (**FALSE**).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a8ddc-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8ddc-133">Requirements</span></span>



| <span data-ttu-id="a8ddc-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8ddc-134">Requirement</span></span> | <span data-ttu-id="a8ddc-135">Value</span><span class="sxs-lookup"><span data-stu-id="a8ddc-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8ddc-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8ddc-136">Header</span></span><br/>  | <dl> <span data-ttu-id="a8ddc-137"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a8ddc-137"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a8ddc-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a8ddc-138">Library</span></span><br/> | <dl> <span data-ttu-id="a8ddc-139"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a8ddc-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8ddc-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8ddc-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8ddc-141">**Clase CDeferredCommand**</span><span class="sxs-lookup"><span data-stu-id="a8ddc-141">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




