---
description: El método Connect completa una conexión con el terminal de salida.
ms.assetid: fb20ef5d-e00a-4154-a6da-25bef663c0e7
title: Método CPullPin. Connect (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Connect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 97e3b0b676e02dee0e3ebd82de9def56edc2ea28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680838"
---
# <a name="cpullpinconnect-method"></a><span data-ttu-id="0d202-103">CPullPin. Connect (método)</span><span class="sxs-lookup"><span data-stu-id="0d202-103">CPullPin.Connect method</span></span>

<span data-ttu-id="0d202-104">El `Connect` método completa una conexión con el PIN de salida.</span><span class="sxs-lookup"><span data-stu-id="0d202-104">The `Connect` method completes a connection to the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d202-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0d202-105">Syntax</span></span>


```C++
HRESULT Connect(
   IUnknown      *pUnk,
   IMemAllocator *pAlloc,
   BOOL          bSync
);
```



## <a name="parameters"></a><span data-ttu-id="0d202-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0d202-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d202-107">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="0d202-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="0d202-108">Puntero a la interfaz **IUnknown** del PIN de salida.</span><span class="sxs-lookup"><span data-stu-id="0d202-108">Pointer to the **IUnknown** interface of the output pin.</span></span>

</dd> <dt>

<span data-ttu-id="0d202-109">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="0d202-109">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="0d202-110">Puntero a la interfaz [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) del asignador preferido del PIN de entrada o **null**.</span><span class="sxs-lookup"><span data-stu-id="0d202-110">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface of the input pin's preferred allocator, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0d202-111">*bSync*</span><span class="sxs-lookup"><span data-stu-id="0d202-111">*bSync*</span></span> 
</dt> <dd>

<span data-ttu-id="0d202-112">Valor booleano que especifica si se van a utilizar lecturas sincrónicas.</span><span class="sxs-lookup"><span data-stu-id="0d202-112">Boolean value that specifies whether to use synchronous reads.</span></span> <span data-ttu-id="0d202-113">Si **es true**, el PIN realiza operaciones de lectura sincrónicas en el PIN de salida.</span><span class="sxs-lookup"><span data-stu-id="0d202-113">If **TRUE**, the pin performs synchronous read operations on the output pin.</span></span> <span data-ttu-id="0d202-114">Si **es false**, el PIN realiza solicitudes de lectura asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="0d202-114">If **FALSE**, the pin makes asynchronous read requests.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d202-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0d202-115">Return value</span></span>

<span data-ttu-id="0d202-116">Devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="0d202-116">Returns an **HRESULT**.</span></span> <span data-ttu-id="0d202-117">Estos son algunos de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="0d202-117">Possible values include the following.</span></span>



| <span data-ttu-id="0d202-118">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0d202-118">Return code</span></span>                                                                                               | <span data-ttu-id="0d202-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d202-119">Description</span></span>                                                                     |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0d202-120"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="0d202-120"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="0d202-121">Correcto.</span><span class="sxs-lookup"><span data-stu-id="0d202-121">Success.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="0d202-122"><dt>**VFW \_ E \_ ya \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="0d202-122"><dt>**VFW\_E\_ALREADY\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="0d202-123">El PIN de entrada ya está conectado.</span><span class="sxs-lookup"><span data-stu-id="0d202-123">The input pin is already connected.</span></span><br/>                                  |
| <dl> <span data-ttu-id="0d202-124"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="0d202-124"><dt>**E\_NOINTERFACE**</dt></span></span> </dl>             | <span data-ttu-id="0d202-125">El PIN de salida no expone [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader).</span><span class="sxs-lookup"><span data-stu-id="0d202-125">The output pin does not expose [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0d202-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0d202-126">Remarks</span></span>

<span data-ttu-id="0d202-127">Llame a este método durante el proceso de conexión del terminal de entrada.</span><span class="sxs-lookup"><span data-stu-id="0d202-127">Call this method during the input pin's connection process.</span></span> <span data-ttu-id="0d202-128">Si se produce un error en el método, el PIN debe producir un error en la conexión.</span><span class="sxs-lookup"><span data-stu-id="0d202-128">If the method fails, the pin should fail the connection.</span></span>

<span data-ttu-id="0d202-129">Este método consulta el PIN de salida de la interfaz **IAsyncReader** .</span><span class="sxs-lookup"><span data-stu-id="0d202-129">This method queries the output pin for the **IAsyncReader** interface.</span></span> <span data-ttu-id="0d202-130">Si se realiza correctamente, llama a [**CPullPin::D ecideallocator**](cpullpin-decideallocator.md) para negociar el asignador de la conexión.</span><span class="sxs-lookup"><span data-stu-id="0d202-130">If successful, it calls [**CPullPin::DecideAllocator**](cpullpin-decideallocator.md) to negotiate the allocator for the connection.</span></span> <span data-ttu-id="0d202-131">Si el PIN de entrada tiene un asignador preferido, especifíquelo en el parámetro *pAlloc* . el método **DecideAllocator** pasa este puntero al método [**IAsyncReader:: RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) del terminal de salida.</span><span class="sxs-lookup"><span data-stu-id="0d202-131">If your input pin has a preferred allocator, specify it in the *pAlloc* parameter; the **DecideAllocator** method passes this pointer to the output pin's [**IAsyncReader::RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) method.</span></span> <span data-ttu-id="0d202-132">En caso contrario, establezca *pAlloc* en **null**.</span><span class="sxs-lookup"><span data-stu-id="0d202-132">Otherwise, set *pAlloc* to **NULL**.</span></span>

<span data-ttu-id="0d202-133">Si el valor de *bSync* es **true**, el objeto **CPullPin** realiza solicitudes sincrónicas de lectura, llamando a [**IAsyncReader:: SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned)del terminal de salida.</span><span class="sxs-lookup"><span data-stu-id="0d202-133">If the value of *bSync* is **TRUE**, the **CPullPin** object makes synchronous read requests, by calling the output pin's [**IAsyncReader::SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned).</span></span> <span data-ttu-id="0d202-134">De lo contrario, llama al método [**IAsyncReader:: Request**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request) para realizar solicitudes de lectura superpuestas.</span><span class="sxs-lookup"><span data-stu-id="0d202-134">Otherwise, it calls the [**IAsyncReader::Request**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request) method to make overlapping read requests.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d202-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d202-135">Requirements</span></span>



| <span data-ttu-id="0d202-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d202-136">Requirement</span></span> | <span data-ttu-id="0d202-137">Value</span><span class="sxs-lookup"><span data-stu-id="0d202-137">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d202-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0d202-138">Header</span></span><br/>  | <dl> <span data-ttu-id="0d202-139"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d202-139"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="0d202-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0d202-140">Library</span></span><br/> | <dl> <span data-ttu-id="0d202-141"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0d202-141"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d202-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d202-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d202-143">**Clase CPullPin**</span><span class="sxs-lookup"><span data-stu-id="0d202-143">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




