---
description: El método GetIDsOfNames asigna un conjunto de nombres a un conjunto correspondiente de DispId.
ms.assetid: 0c0a2726-e89a-4eaf-aab0-e7e9e82e3c34
title: Método CBaseDispatch. GetIDsOfNames (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf11e4aa298f924b69c299c2f411dde88e28e5b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660193"
---
# <a name="cbasedispatchgetidsofnames-method"></a><span data-ttu-id="1d912-103">CBaseDispatch. GetIDsOfNames (método)</span><span class="sxs-lookup"><span data-stu-id="1d912-103">CBaseDispatch.GetIDsOfNames method</span></span>

<span data-ttu-id="1d912-104">El `GetIDsOfNames` método asigna un conjunto de nombres a un conjunto correspondiente de DispId.</span><span class="sxs-lookup"><span data-stu-id="1d912-104">The `GetIDsOfNames` method maps a set of names to a corresponding set of DISPIDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d912-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d912-105">Syntax</span></span>


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a><span data-ttu-id="1d912-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1d912-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d912-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="1d912-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="1d912-108">Referencia a un identificador de interfaz (IID) que especifica la interfaz.</span><span class="sxs-lookup"><span data-stu-id="1d912-108">Reference to an interface identifier (IID) that specifies the interface.</span></span>

</dd> <dt>

<span data-ttu-id="1d912-109">*rgszNames*</span><span class="sxs-lookup"><span data-stu-id="1d912-109">*rgszNames*</span></span> 
</dt> <dd>

<span data-ttu-id="1d912-110">Dirección de una matriz de cadenas de caracteres anchos que contienen los nombres que se van a asignar.</span><span class="sxs-lookup"><span data-stu-id="1d912-110">Address of an array of wide-character strings that contain the names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="1d912-111">*CNAME*</span><span class="sxs-lookup"><span data-stu-id="1d912-111">*cNames*</span></span> 
</dt> <dd>

<span data-ttu-id="1d912-112">Tamaño de la matriz proporcionado por el parámetro *rgszNames* .</span><span class="sxs-lookup"><span data-stu-id="1d912-112">Size of the array given by the *rgszNames* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1d912-113">*lcid*</span><span class="sxs-lookup"><span data-stu-id="1d912-113">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="1d912-114">Contexto de configuración regional en el que se van a interpretar los nombres.</span><span class="sxs-lookup"><span data-stu-id="1d912-114">Locale context in which to interpret the names.</span></span> <span data-ttu-id="1d912-115">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="1d912-115">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1d912-116">*rgdispid*</span><span class="sxs-lookup"><span data-stu-id="1d912-116">*rgdispid*</span></span> 
</dt> <dd>

<span data-ttu-id="1d912-117">Puntero a una matriz que recibe los DispId.</span><span class="sxs-lookup"><span data-stu-id="1d912-117">Pointer to an array that receives the DISPIDs.</span></span> <span data-ttu-id="1d912-118">Cada elemento de recibe un identificador que corresponde a uno de los nombres pasados en el parámetro *rgszNames* .</span><span class="sxs-lookup"><span data-stu-id="1d912-118">Each element of receives an identifier that corresponds to one of the names passed in the *rgszNames* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d912-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1d912-119">Return value</span></span>

<span data-ttu-id="1d912-120">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1d912-120">Returns an **HRESULT** value.</span></span> <span data-ttu-id="1d912-121">Estos son algunos de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="1d912-121">Possible values include the following.</span></span>



| <span data-ttu-id="1d912-122">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1d912-122">Return code</span></span>                                                                                         | <span data-ttu-id="1d912-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="1d912-123">Description</span></span>                                         |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="1d912-124"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="1d912-124"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="1d912-125">Correcto.</span><span class="sxs-lookup"><span data-stu-id="1d912-125">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="1d912-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1d912-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="1d912-127">Memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="1d912-127">Insufficient memory.</span></span><br/>                     |
| <dl> <span data-ttu-id="1d912-128"><dt>**DISP \_ E \_ UNKNOWNNAME**</dt></span><span class="sxs-lookup"><span data-stu-id="1d912-128"><dt>**DISP\_E\_UNKNOWNNAME**</dt></span></span> </dl> | <span data-ttu-id="1d912-129">No se conocían uno o varios de los nombres.</span><span class="sxs-lookup"><span data-stu-id="1d912-129">One or more of the names were not known.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1d912-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1d912-130">Remarks</span></span>

<span data-ttu-id="1d912-131">Este método se comporta como el método **IDispatch:: GetIDsOfNames** , pero el parámetro *riid* especifica la interfaz en la que se van a recuperar los DispId.</span><span class="sxs-lookup"><span data-stu-id="1d912-131">This method behaves like the **IDispatch::GetIDsOfNames** method, but the *riid* parameter specifies the interface on which to retrieve DISPIDs.</span></span> <span data-ttu-id="1d912-132">(En la versión **IDispatch** , el parámetro *riid* está reservado).</span><span class="sxs-lookup"><span data-stu-id="1d912-132">(In the **IDispatch** version, the *riid* parameter is reserved.)</span></span>

<span data-ttu-id="1d912-133">Si el método devuelve DISP \_ E \_ UNKNOWNNAME, los DISPID devueltos contienen DISPID \_ Unknown para cada entrada que corresponde a un nombre desconocido.</span><span class="sxs-lookup"><span data-stu-id="1d912-133">If the method returns DISP\_E\_UNKNOWNNAME, the returned DISPIDs contain DISPID\_UNKNOWN for each entry that corresponds to an unknown name.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d912-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d912-134">Requirements</span></span>



| <span data-ttu-id="1d912-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d912-135">Requirement</span></span> | <span data-ttu-id="1d912-136">Value</span><span class="sxs-lookup"><span data-stu-id="1d912-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d912-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1d912-137">Header</span></span><br/>  | <dl> <span data-ttu-id="1d912-138"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1d912-138"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1d912-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1d912-139">Library</span></span><br/> | <dl> <span data-ttu-id="1d912-140"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1d912-140"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d912-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d912-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d912-142">**Clase CBaseDispatch**</span><span class="sxs-lookup"><span data-stu-id="1d912-142">**CBaseDispatch Class**</span></span>](cbasedispatch.md)
</dt> </dl>

 

 




