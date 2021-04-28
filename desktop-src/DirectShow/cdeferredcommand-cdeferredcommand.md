---
description: 'Constructor CDeferredCommand.CDeferredCommand: método constructor.'
ms.assetid: 0b372fa2-78a9-4e38-813c-f18123716c6d
title: Constructor CDeferredCommand.CDeferredCommand (Ctlutil.h)
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
ms.openlocfilehash: 9a10d8bba48902ed2d6fd66da8483cea1ba9aacc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119793"
---
# <a name="cdeferredcommandcdeferredcommand-constructor"></a><span data-ttu-id="de1e8-103">Constructor CDeferredCommand.CDeferredCommand</span><span class="sxs-lookup"><span data-stu-id="de1e8-103">CDeferredCommand.CDeferredCommand constructor</span></span>

<span data-ttu-id="de1e8-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="de1e8-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="de1e8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="de1e8-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="de1e8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="de1e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de1e8-107">*Pq*</span><span class="sxs-lookup"><span data-stu-id="de1e8-107">*pQ*</span></span> 
</dt> <dd>

<span data-ttu-id="de1e8-108">Puntero a un objeto que expone la [**interfaz IQueueCommand.**](/windows/desktop/api/Control/nn-control-iqueuecommand)</span><span class="sxs-lookup"><span data-stu-id="de1e8-108">Pointer to an object that exposes the [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) interface.</span></span>

</dd> <dt>

<span data-ttu-id="de1e8-109">*Punk*</span><span class="sxs-lookup"><span data-stu-id="de1e8-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="de1e8-110">Puntero a la interfaz **IUnknown externa** para la agregación.</span><span class="sxs-lookup"><span data-stu-id="de1e8-110">Pointer to the outer **IUnknown** interface for aggregation.</span></span>

</dd> <dt>

<span data-ttu-id="de1e8-111">*Phr*</span><span class="sxs-lookup"><span data-stu-id="de1e8-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="de1e8-112">Puntero a un valor **HRESULT** devuelto.</span><span class="sxs-lookup"><span data-stu-id="de1e8-112">Pointer to a returned **HRESULT** value.</span></span>

</dd> <dt>

<span data-ttu-id="de1e8-113">*pUnkExecutor*</span><span class="sxs-lookup"><span data-stu-id="de1e8-113">*pUnkExecutor*</span></span> 
</dt> <dd>

<span data-ttu-id="de1e8-114">Puntero al objeto que llevará a cabo este comando.</span><span class="sxs-lookup"><span data-stu-id="de1e8-114">Pointer to the object that will carry out this command.</span></span>

</dd> <dt>

<span data-ttu-id="de1e8-115">*time*</span><span class="sxs-lookup"><span data-stu-id="de1e8-115">*time*</span></span> 
</dt> <dd>

<span data-ttu-id="de1e8-116">Hora a la que se ejecutará el comando.</span><span class="sxs-lookup"><span data-stu-id="de1e8-116">Time at which the command will be run.</span></span>

</dd> <dt>

<span data-ttu-id="de1e8-117">*Iid*</span><span class="sxs-lookup"><span data-stu-id="de1e8-117">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="de1e8-118">Puntero al identificador único global **(GUID)** de la interfaz que contiene el método .</span><span class="sxs-lookup"><span data-stu-id="de1e8-118">Pointer to the globally unique identifier (**GUID**) of the interface that contains the method.</span></span>

</dd> <dt>

<span data-ttu-id="de1e8-119">*dispidMethod*</span><span class="sxs-lookup"><span data-stu-id="de1e8-119">*dispidMethod*</span></span> 
</dt> <dd>

<span data-ttu-id="de1e8-120">Método en la interfaz a la que se llamará.</span><span class="sxs-lookup"><span data-stu-id="de1e8-120">Method on the interface to call.</span></span>

</dd> <dt>

<span data-ttu-id="de1e8-121">*wFlags*</span><span class="sxs-lookup"><span data-stu-id="de1e8-121">*wFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="de1e8-122">Contexto de la invocación.</span><span class="sxs-lookup"><span data-stu-id="de1e8-122">Context of the invocation.</span></span>

</dd> <dt>

<span data-ttu-id="de1e8-123">*cArgs*</span><span class="sxs-lookup"><span data-stu-id="de1e8-123">*cArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="de1e8-124">Número de argumentos pasados.</span><span class="sxs-lookup"><span data-stu-id="de1e8-124">Number of arguments passed.</span></span>

</dd> <dt>

<span data-ttu-id="de1e8-125">*pDispParams*</span><span class="sxs-lookup"><span data-stu-id="de1e8-125">*pDispParams*</span></span> 
</dt> <dd>

<span data-ttu-id="de1e8-126">Puntero a una lista de tipos de variante de argumento.</span><span class="sxs-lookup"><span data-stu-id="de1e8-126">Pointer to a list of argument variant types.</span></span>

</dd> <dt>

<span data-ttu-id="de1e8-127">*pvarResult*</span><span class="sxs-lookup"><span data-stu-id="de1e8-127">*pvarResult*</span></span> 
</dt> <dd>

<span data-ttu-id="de1e8-128">Puntero a una lista de tipo variante devuelta, si la hay.</span><span class="sxs-lookup"><span data-stu-id="de1e8-128">Pointer to a returned variant type list, if any.</span></span>

</dd> <dt>

<span data-ttu-id="de1e8-129">*puArgErr*</span><span class="sxs-lookup"><span data-stu-id="de1e8-129">*puArgErr*</span></span> 
</dt> <dd>

<span data-ttu-id="de1e8-130">Puntero al último argumento de la lista *de parámetros pDispParams* con un error.</span><span class="sxs-lookup"><span data-stu-id="de1e8-130">Pointer to the last argument in the *pDispParams* parameter list with an error.</span></span>

</dd> <dt>

<span data-ttu-id="de1e8-131">*bStream*</span><span class="sxs-lookup"><span data-stu-id="de1e8-131">*bStream*</span></span> 
</dt> <dd>

<span data-ttu-id="de1e8-132">Valor que indica si el tiempo de comando diferido está en tiempo de secuencia (**TRUE**) o tiempo de presentación (**FALSE**).</span><span class="sxs-lookup"><span data-stu-id="de1e8-132">Value indicating whether the deferred command time is in stream time (**TRUE**) or presentation time (**FALSE**).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="de1e8-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de1e8-133">Requirements</span></span>



| <span data-ttu-id="de1e8-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="de1e8-134">Requirement</span></span> | <span data-ttu-id="de1e8-135">Value</span><span class="sxs-lookup"><span data-stu-id="de1e8-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de1e8-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="de1e8-136">Header</span></span><br/>  | <dl> <span data-ttu-id="de1e8-137"><dt>Ctlutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="de1e8-137"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="de1e8-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="de1e8-138">Library</span></span><br/> | <dl> <span data-ttu-id="de1e8-139"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="de1e8-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de1e8-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="de1e8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de1e8-141">**CDeferredCommand (clase)**</span><span class="sxs-lookup"><span data-stu-id="de1e8-141">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




