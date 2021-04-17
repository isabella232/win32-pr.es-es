---
description: El método GetTypeInfo recupera la información de tipo para el objeto, que se puede usar para obtener la información de tipo de una interfaz.
ms.assetid: aa06b97c-541b-44fc-bdef-97fd1f014e85
title: Método CBaseDispatch. GetTypeInfo (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f63d79327d2f2bf2a60f06e0290aa34891e78ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660583"
---
# <a name="cbasedispatchgettypeinfo-method"></a><span data-ttu-id="9a046-103">CBaseDispatch. GetTypeInfo, método</span><span class="sxs-lookup"><span data-stu-id="9a046-103">CBaseDispatch.GetTypeInfo method</span></span>

<span data-ttu-id="9a046-104">El `GetTypeInfo` método recupera la información de tipo para el objeto, que se puede usar para obtener la información de tipo de una interfaz.</span><span class="sxs-lookup"><span data-stu-id="9a046-104">The `GetTypeInfo` method retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a046-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9a046-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   REFIID    riid,
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="9a046-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9a046-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a046-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="9a046-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="9a046-108">Referencia a un identificador de interfaz (IID) que especifica la interfaz.</span><span class="sxs-lookup"><span data-stu-id="9a046-108">Reference to an interface identifier (IID) that specifies the interface.</span></span>

</dd> <dt>

<span data-ttu-id="9a046-109">*itinfo*</span><span class="sxs-lookup"><span data-stu-id="9a046-109">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="9a046-110">Información de tipo que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="9a046-110">Type information to return.</span></span> <span data-ttu-id="9a046-111">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="9a046-111">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9a046-112">*lcid*</span><span class="sxs-lookup"><span data-stu-id="9a046-112">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="9a046-113">Identificador de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="9a046-113">Locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="9a046-114">*pptinfo*</span><span class="sxs-lookup"><span data-stu-id="9a046-114">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="9a046-115">Dirección de una variable que recibe un puntero **ITypeInfo** .</span><span class="sxs-lookup"><span data-stu-id="9a046-115">Address of a variable that receives an **ITypeInfo** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a046-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9a046-116">Return value</span></span>

<span data-ttu-id="9a046-117">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9a046-117">Returns an **HRESULT** value.</span></span> <span data-ttu-id="9a046-118">Estos son algunos de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="9a046-118">Possible values include the following.</span></span>



| <span data-ttu-id="9a046-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9a046-119">Return code</span></span>                                                                                             | <span data-ttu-id="9a046-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a046-120">Description</span></span>                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="9a046-121"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="9a046-121"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="9a046-122">Correcto.</span><span class="sxs-lookup"><span data-stu-id="9a046-122">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="9a046-123"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="9a046-123"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="9a046-124">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="9a046-124">**NULL** pointer argument.</span></span><br/>          |
| <dl> <span data-ttu-id="9a046-125"><dt>**Escriba \_ E \_ ELEMENTNOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="9a046-125"><dt>**TYPE\_E\_ELEMENTNOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="9a046-126">El parámetro *itinfo* no es cero.</span><span class="sxs-lookup"><span data-stu-id="9a046-126">The *itinfo* parameter is not zero.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9a046-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9a046-127">Remarks</span></span>

<span data-ttu-id="9a046-128">Este método se comporta como el método **IDispatch:: GetTypeInfo** .</span><span class="sxs-lookup"><span data-stu-id="9a046-128">This method behaves like the **IDispatch::GetTypeInfo** method.</span></span> <span data-ttu-id="9a046-129">Sin embargo, incluye un parámetro adicional, *riid*, que especifica la interfaz cuya información de tipo se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="9a046-129">However, it includes an additional parameter, *riid*, which specifies the interface for which to retrieve type information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a046-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a046-130">Requirements</span></span>



| <span data-ttu-id="9a046-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a046-131">Requirement</span></span> | <span data-ttu-id="9a046-132">Value</span><span class="sxs-lookup"><span data-stu-id="9a046-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a046-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9a046-133">Header</span></span><br/>  | <dl> <span data-ttu-id="9a046-134"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9a046-134"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9a046-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9a046-135">Library</span></span><br/> | <dl> <span data-ttu-id="9a046-136"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="9a046-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a046-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="9a046-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a046-138">**Clase CBaseDispatch**</span><span class="sxs-lookup"><span data-stu-id="9a046-138">**CBaseDispatch Class**</span></span>](cbasedispatch.md)
</dt> </dl>

 

 




