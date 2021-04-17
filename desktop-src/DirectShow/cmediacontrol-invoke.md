---
description: Proporciona acceso a las propiedades y los métodos expuestos por un objeto.
ms.assetid: 05006f1e-24ff-4ed2-8291-2ba48495fec0
title: Método CMediaControl. Invoke (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7b9a29d163180ffc609ca44f2bbbfb2870c5faef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680314"
---
# <a name="cmediacontrolinvoke-method"></a><span data-ttu-id="0ebf6-103">CMediaControl. Invoke (método)</span><span class="sxs-lookup"><span data-stu-id="0ebf6-103">CMediaControl.Invoke method</span></span>

<span data-ttu-id="0ebf6-104">Proporciona acceso a las propiedades y los métodos expuestos por un objeto.</span><span class="sxs-lookup"><span data-stu-id="0ebf6-104">Provides access to properties and methods exposed by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ebf6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0ebf6-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="0ebf6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0ebf6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ebf6-107">*dispidMember*</span><span class="sxs-lookup"><span data-stu-id="0ebf6-107">*dispidMember*</span></span> 
</dt> <dd>

<span data-ttu-id="0ebf6-108">Identificador del miembro.</span><span class="sxs-lookup"><span data-stu-id="0ebf6-108">Identifier of the member.</span></span> <span data-ttu-id="0ebf6-109">Use [**CMediaControl:: GetIDsOfNames**](cmediacontrol-getidsofnames.md) o la documentación del objeto para obtener el identificador de envío.</span><span class="sxs-lookup"><span data-stu-id="0ebf6-109">Use [**CMediaControl::GetIDsOfNames**](cmediacontrol-getidsofnames.md) or the object's documentation to obtain the dispatch identifier.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf6-110">*riid*</span><span class="sxs-lookup"><span data-stu-id="0ebf6-110">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="0ebf6-111">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="0ebf6-111">Reserved for future use.</span></span> <span data-ttu-id="0ebf6-112">Debe ser un IID \_ null.</span><span class="sxs-lookup"><span data-stu-id="0ebf6-112">Must be IID\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf6-113">*lcid*</span><span class="sxs-lookup"><span data-stu-id="0ebf6-113">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="0ebf6-114">Contexto de configuración regional en el que se interpretan los argumentos.</span><span class="sxs-lookup"><span data-stu-id="0ebf6-114">Locale context in which to interpret arguments.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf6-115">*wFlags*</span><span class="sxs-lookup"><span data-stu-id="0ebf6-115">*wFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="0ebf6-116">Marcas que describen el contexto de la `CMediaControl::Invoke` llamada.</span><span class="sxs-lookup"><span data-stu-id="0ebf6-116">Flags describing the context of the `CMediaControl::Invoke` call.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf6-117">*pdispparams*</span><span class="sxs-lookup"><span data-stu-id="0ebf6-117">*pdispparams*</span></span> 
</dt> <dd>

<span data-ttu-id="0ebf6-118">Puntero a una estructura que contiene una matriz de argumentos, una matriz de identificadores de envío de argumentos para argumentos con nombre y recuentos del número de elementos de las matrices.</span><span class="sxs-lookup"><span data-stu-id="0ebf6-118">Pointer to a structure containing an array of arguments, an array of argument dispatch IDs for named arguments, and counts for number of elements in the arrays.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf6-119">*pvarResult*</span><span class="sxs-lookup"><span data-stu-id="0ebf6-119">*pvarResult*</span></span> 
</dt> <dd>

<span data-ttu-id="0ebf6-120">Puntero al lugar donde se va a almacenar el resultado o **null** si el llamador no espera ningún resultado.</span><span class="sxs-lookup"><span data-stu-id="0ebf6-120">Pointer to where the result is to be stored, or **NULL** if the caller expects no result.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf6-121">*pexcepinfo*</span><span class="sxs-lookup"><span data-stu-id="0ebf6-121">*pexcepinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="0ebf6-122">Puntero a una estructura que contiene la información de la excepción.</span><span class="sxs-lookup"><span data-stu-id="0ebf6-122">Pointer to a structure containing exception information.</span></span>

</dd> <dt>

<span data-ttu-id="0ebf6-123">*puArgErr*</span><span class="sxs-lookup"><span data-stu-id="0ebf6-123">*puArgErr*</span></span> 
</dt> <dd>

<span data-ttu-id="0ebf6-124">Puntero al índice del primer argumento, dentro de la matriz **rgvarg** de la estructura **DISPPARAMS** , que tiene un error.</span><span class="sxs-lookup"><span data-stu-id="0ebf6-124">Pointer to the index of the first argument, within the **DISPPARAMS** structure's **rgvarg** array, that has an error.</span></span> <span data-ttu-id="0ebf6-125">Para obtener más información sobre **DISPPARAMS**, vea el SDK de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="0ebf6-125">For more information on **DISPPARAMS**, see the Platform SDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ebf6-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0ebf6-126">Return value</span></span>

<span data-ttu-id="0ebf6-127">Devuelve DISP \_ E \_ UNKNOWNINTERFACE si *riid* no es \_ null.</span><span class="sxs-lookup"><span data-stu-id="0ebf6-127">Returns DISP\_E\_UNKNOWNINTERFACE if *riid* is not IID\_NULL.</span></span> <span data-ttu-id="0ebf6-128">Devuelve uno de los códigos de error de [**CMediaControl:: GetTypeInfo**](cmediacontrol-gettypeinfo.md) si se produce un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="0ebf6-128">Returns one of the error codes from [**CMediaControl::GetTypeInfo**](cmediacontrol-gettypeinfo.md) if the call fails.</span></span> <span data-ttu-id="0ebf6-129">De lo contrario, devuelve el **HRESULT** de la llamada a **IDispatch:: Invoke**.</span><span class="sxs-lookup"><span data-stu-id="0ebf6-129">Otherwise, returns the **HRESULT** from the call to **IDispatch::Invoke**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ebf6-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ebf6-130">Requirements</span></span>



| <span data-ttu-id="0ebf6-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ebf6-131">Requirement</span></span> | <span data-ttu-id="0ebf6-132">Value</span><span class="sxs-lookup"><span data-stu-id="0ebf6-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ebf6-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0ebf6-133">Header</span></span><br/>  | <dl> <span data-ttu-id="0ebf6-134"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0ebf6-134"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0ebf6-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0ebf6-135">Library</span></span><br/> | <dl> <span data-ttu-id="0ebf6-136"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0ebf6-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ebf6-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ebf6-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ebf6-138">**Clase CMediaControl**</span><span class="sxs-lookup"><span data-stu-id="0ebf6-138">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 




