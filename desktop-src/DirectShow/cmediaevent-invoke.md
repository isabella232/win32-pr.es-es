---
description: 'Método CMediaEvent.Invoke: proporciona acceso a propiedades y métodos expuestos por un objeto .'
ms.assetid: 2b091b57-0855-489a-9a33-cfc75f63ad07
title: Método CMediaEvent.Invoke (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ea812d0c7629b98d90f3f7e535d229c707452b23
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095543"
---
# <a name="cmediaeventinvoke-method"></a><span data-ttu-id="9d0e0-103">Método CMediaEvent.Invoke</span><span class="sxs-lookup"><span data-stu-id="9d0e0-103">CMediaEvent.Invoke method</span></span>

<span data-ttu-id="9d0e0-104">Proporciona acceso a las propiedades y los métodos expuestos por un objeto.</span><span class="sxs-lookup"><span data-stu-id="9d0e0-104">Provides access to properties and methods exposed by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d0e0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9d0e0-105">Syntax</span></span>


```C++
HRESULT Invoke(
   DISPID     dispidMember,
   REFIID     riid,
   LCID       lcid,
   WORD       wFlags,
   DISPPARAMS *pdispparams,
   VARIANT    *pvarResult,
   EXCEPINFO  *pexcepinfo,
   UINT       *puArgErr
);
```



## <a name="parameters"></a><span data-ttu-id="9d0e0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9d0e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d0e0-107">*dispidMember*</span><span class="sxs-lookup"><span data-stu-id="9d0e0-107">*dispidMember*</span></span> 
</dt> <dd>

<span data-ttu-id="9d0e0-108">Identificador del miembro.</span><span class="sxs-lookup"><span data-stu-id="9d0e0-108">Identifier of the member.</span></span> <span data-ttu-id="9d0e0-109">Use [**CMediaEvent::GetIDsOfNames**](cmediaevent-getidsofnames.md) o la documentación del objeto para obtener el identificador de envío.</span><span class="sxs-lookup"><span data-stu-id="9d0e0-109">Use [**CMediaEvent::GetIDsOfNames**](cmediaevent-getidsofnames.md) or the object's documentation to obtain the dispatch identifier.</span></span>

</dd> <dt>

<span data-ttu-id="9d0e0-110">*riid*</span><span class="sxs-lookup"><span data-stu-id="9d0e0-110">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="9d0e0-111">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="9d0e0-111">Reserved for future use.</span></span> <span data-ttu-id="9d0e0-112">Debe ser IID \_ NULL.</span><span class="sxs-lookup"><span data-stu-id="9d0e0-112">Must be IID\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="9d0e0-113">*lcid*</span><span class="sxs-lookup"><span data-stu-id="9d0e0-113">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="9d0e0-114">Contexto de configuración regional en el que se interpretarán los argumentos.</span><span class="sxs-lookup"><span data-stu-id="9d0e0-114">Locale context in which to interpret arguments.</span></span>

</dd> <dt>

<span data-ttu-id="9d0e0-115">*wFlags*</span><span class="sxs-lookup"><span data-stu-id="9d0e0-115">*wFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="9d0e0-116">Marcas que describen el contexto de la `CMediaEvent::Invoke` llamada.</span><span class="sxs-lookup"><span data-stu-id="9d0e0-116">Flags describing the context of the `CMediaEvent::Invoke` call.</span></span>

</dd> <dt>

<span data-ttu-id="9d0e0-117">*pdispparams*</span><span class="sxs-lookup"><span data-stu-id="9d0e0-117">*pdispparams*</span></span> 
</dt> <dd>

<span data-ttu-id="9d0e0-118">Puntero a una estructura que contiene una matriz de argumentos, una matriz de los ID de distribución de argumentos para argumentos con nombre y cuenta el número de elementos de las matrices.</span><span class="sxs-lookup"><span data-stu-id="9d0e0-118">Pointer to a structure containing an array of arguments, an array of argument dispatch IDs for named arguments, and counts for the number of elements in the arrays.</span></span>

</dd> <dt>

<span data-ttu-id="9d0e0-119">*pvarResult*</span><span class="sxs-lookup"><span data-stu-id="9d0e0-119">*pvarResult*</span></span> 
</dt> <dd>

<span data-ttu-id="9d0e0-120">Puntero a donde se almacenará el resultado o **NULL** si el autor de la llamada no espera ningún resultado.</span><span class="sxs-lookup"><span data-stu-id="9d0e0-120">Pointer to where the result is to be stored, or **NULL** if the caller expects no result.</span></span>

</dd> <dt>

<span data-ttu-id="9d0e0-121">*pexcepinfo*</span><span class="sxs-lookup"><span data-stu-id="9d0e0-121">*pexcepinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="9d0e0-122">Puntero a una estructura que contiene información de excepción.</span><span class="sxs-lookup"><span data-stu-id="9d0e0-122">Pointer to a structure containing exception information.</span></span>

</dd> <dt>

<span data-ttu-id="9d0e0-123">*puArgErr*</span><span class="sxs-lookup"><span data-stu-id="9d0e0-123">*puArgErr*</span></span> 
</dt> <dd>

<span data-ttu-id="9d0e0-124">Puntero al índice del primer argumento, dentro de la matriz **rgvarg** de la estructura **DIS DISLIGRAMS,** que tiene un error.</span><span class="sxs-lookup"><span data-stu-id="9d0e0-124">Pointer to the index of the first argument, within the **DISPPARAMS** structure's **rgvarg** array, that has an error.</span></span> <span data-ttu-id="9d0e0-125">Para obtener más información **sobre DIS DISRAMS,** consulte el SDK de plataforma.</span><span class="sxs-lookup"><span data-stu-id="9d0e0-125">For more information on **DISPPARAMS**, see the Platform SDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d0e0-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9d0e0-126">Return value</span></span>

<span data-ttu-id="9d0e0-127">Devuelve DISP \_ E \_ UNKNOWNINTERFACE si *riid* no es IID \_ NULL.</span><span class="sxs-lookup"><span data-stu-id="9d0e0-127">Returns DISP\_E\_UNKNOWNINTERFACE if *riid* is not IID\_NULL.</span></span> <span data-ttu-id="9d0e0-128">Devuelve uno de los códigos de error de [**CMediaEvent::GetTypeInfo**](cmediaevent-gettypeinfo.md) si se produce un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="9d0e0-128">Returns one of the error codes from [**CMediaEvent::GetTypeInfo**](cmediaevent-gettypeinfo.md) if the call fails.</span></span> <span data-ttu-id="9d0e0-129">De lo contrario, **devuelve el valor HRESULT** de la llamada a **IDispatch::Invoke**.</span><span class="sxs-lookup"><span data-stu-id="9d0e0-129">Otherwise, returns the **HRESULT** from the call to **IDispatch::Invoke**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d0e0-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d0e0-130">Requirements</span></span>



| <span data-ttu-id="9d0e0-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d0e0-131">Requirement</span></span> | <span data-ttu-id="9d0e0-132">Value</span><span class="sxs-lookup"><span data-stu-id="9d0e0-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d0e0-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9d0e0-133">Header</span></span><br/>  | <dl> <span data-ttu-id="9d0e0-134"><dt>Ctlutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="9d0e0-134"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9d0e0-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9d0e0-135">Library</span></span><br/> | <dl> <span data-ttu-id="9d0e0-136"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="9d0e0-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d0e0-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9d0e0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d0e0-138">**CMediaEvent (clase)**</span><span class="sxs-lookup"><span data-stu-id="9d0e0-138">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 




