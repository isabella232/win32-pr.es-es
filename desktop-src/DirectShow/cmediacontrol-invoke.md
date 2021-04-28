---
description: 'Método CMediaControl.Invoke: proporciona acceso a propiedades y métodos expuestos por un objeto .'
ms.assetid: 05006f1e-24ff-4ed2-8291-2ba48495fec0
title: Método CMediaControl.Invoke (Ctlutil.h)
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
ms.openlocfilehash: fe077b2c69f603eef8737cbf7ea8c514e9b90c85
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085643"
---
# <a name="cmediacontrolinvoke-method"></a><span data-ttu-id="ee252-103">Método CMediaControl.Invoke</span><span class="sxs-lookup"><span data-stu-id="ee252-103">CMediaControl.Invoke method</span></span>

<span data-ttu-id="ee252-104">Proporciona acceso a las propiedades y los métodos expuestos por un objeto.</span><span class="sxs-lookup"><span data-stu-id="ee252-104">Provides access to properties and methods exposed by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee252-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ee252-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="ee252-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ee252-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee252-107">*dispidMember*</span><span class="sxs-lookup"><span data-stu-id="ee252-107">*dispidMember*</span></span> 
</dt> <dd>

<span data-ttu-id="ee252-108">Identificador del miembro.</span><span class="sxs-lookup"><span data-stu-id="ee252-108">Identifier of the member.</span></span> <span data-ttu-id="ee252-109">Use [**CMediaControl::GetIDsOfNames**](cmediacontrol-getidsofnames.md) o la documentación del objeto para obtener el identificador de envío.</span><span class="sxs-lookup"><span data-stu-id="ee252-109">Use [**CMediaControl::GetIDsOfNames**](cmediacontrol-getidsofnames.md) or the object's documentation to obtain the dispatch identifier.</span></span>

</dd> <dt>

<span data-ttu-id="ee252-110">*riid*</span><span class="sxs-lookup"><span data-stu-id="ee252-110">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="ee252-111">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="ee252-111">Reserved for future use.</span></span> <span data-ttu-id="ee252-112">Debe ser IID \_ NULL.</span><span class="sxs-lookup"><span data-stu-id="ee252-112">Must be IID\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="ee252-113">*lcid*</span><span class="sxs-lookup"><span data-stu-id="ee252-113">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="ee252-114">Contexto de configuración regional en el que se interpretarán los argumentos.</span><span class="sxs-lookup"><span data-stu-id="ee252-114">Locale context in which to interpret arguments.</span></span>

</dd> <dt>

<span data-ttu-id="ee252-115">*wFlags*</span><span class="sxs-lookup"><span data-stu-id="ee252-115">*wFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="ee252-116">Marcas que describen el contexto de la `CMediaControl::Invoke` llamada.</span><span class="sxs-lookup"><span data-stu-id="ee252-116">Flags describing the context of the `CMediaControl::Invoke` call.</span></span>

</dd> <dt>

<span data-ttu-id="ee252-117">*pdispparams*</span><span class="sxs-lookup"><span data-stu-id="ee252-117">*pdispparams*</span></span> 
</dt> <dd>

<span data-ttu-id="ee252-118">Puntero a una estructura que contiene una matriz de argumentos, una matriz de los ID de distribución de argumentos para argumentos con nombre y cuenta el número de elementos de las matrices.</span><span class="sxs-lookup"><span data-stu-id="ee252-118">Pointer to a structure containing an array of arguments, an array of argument dispatch IDs for named arguments, and counts for number of elements in the arrays.</span></span>

</dd> <dt>

<span data-ttu-id="ee252-119">*pvarResult*</span><span class="sxs-lookup"><span data-stu-id="ee252-119">*pvarResult*</span></span> 
</dt> <dd>

<span data-ttu-id="ee252-120">Puntero a donde se almacenará el resultado o **NULL** si el autor de la llamada no espera ningún resultado.</span><span class="sxs-lookup"><span data-stu-id="ee252-120">Pointer to where the result is to be stored, or **NULL** if the caller expects no result.</span></span>

</dd> <dt>

<span data-ttu-id="ee252-121">*pexcepinfo*</span><span class="sxs-lookup"><span data-stu-id="ee252-121">*pexcepinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="ee252-122">Puntero a una estructura que contiene información de excepción.</span><span class="sxs-lookup"><span data-stu-id="ee252-122">Pointer to a structure containing exception information.</span></span>

</dd> <dt>

<span data-ttu-id="ee252-123">*puArgErr*</span><span class="sxs-lookup"><span data-stu-id="ee252-123">*puArgErr*</span></span> 
</dt> <dd>

<span data-ttu-id="ee252-124">Puntero al índice del primer argumento, dentro de la matriz **rgvarg** de la estructura **DIS DISLIGRAMS,** que tiene un error.</span><span class="sxs-lookup"><span data-stu-id="ee252-124">Pointer to the index of the first argument, within the **DISPPARAMS** structure's **rgvarg** array, that has an error.</span></span> <span data-ttu-id="ee252-125">Para obtener más información **sobre DIS DISRAMS,** consulte el SDK de plataforma.</span><span class="sxs-lookup"><span data-stu-id="ee252-125">For more information on **DISPPARAMS**, see the Platform SDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee252-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ee252-126">Return value</span></span>

<span data-ttu-id="ee252-127">Devuelve DISP \_ E \_ UNKNOWNINTERFACE si *riid* no es IID \_ NULL.</span><span class="sxs-lookup"><span data-stu-id="ee252-127">Returns DISP\_E\_UNKNOWNINTERFACE if *riid* is not IID\_NULL.</span></span> <span data-ttu-id="ee252-128">Devuelve uno de los códigos de error de [**CMediaControl::GetTypeInfo**](cmediacontrol-gettypeinfo.md) si se produce un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="ee252-128">Returns one of the error codes from [**CMediaControl::GetTypeInfo**](cmediacontrol-gettypeinfo.md) if the call fails.</span></span> <span data-ttu-id="ee252-129">De lo contrario, **devuelve el valor HRESULT** de la llamada a **IDispatch::Invoke**.</span><span class="sxs-lookup"><span data-stu-id="ee252-129">Otherwise, returns the **HRESULT** from the call to **IDispatch::Invoke**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee252-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee252-130">Requirements</span></span>



| <span data-ttu-id="ee252-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee252-131">Requirement</span></span> | <span data-ttu-id="ee252-132">Value</span><span class="sxs-lookup"><span data-stu-id="ee252-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee252-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ee252-133">Header</span></span><br/>  | <dl> <span data-ttu-id="ee252-134"><dt>Ctlutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee252-134"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ee252-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ee252-135">Library</span></span><br/> | <dl> <span data-ttu-id="ee252-136"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ee252-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee252-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ee252-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee252-138">**CMediaControl (clase)**</span><span class="sxs-lookup"><span data-stu-id="ee252-138">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 




