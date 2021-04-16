---
description: El método GetTypeInfo recupera la información de tipo para el objeto, que se puede usar para obtener la información de tipo de una interfaz.
ms.assetid: 0a04c43d-8b4b-4780-b02f-04053c405c77
title: Método CMediaPosition. GetTypeInfo (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6fa776ca71daff67185bf9fd2c1727f9535f8ac4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671556"
---
# <a name="cmediapositiongettypeinfo-method"></a><span data-ttu-id="81cfa-103">CMediaPosition. GetTypeInfo, método</span><span class="sxs-lookup"><span data-stu-id="81cfa-103">CMediaPosition.GetTypeInfo method</span></span>

<span data-ttu-id="81cfa-104">El `GetTypeInfo` método recupera la información de tipo para el objeto, que se puede usar para obtener la información de tipo de una interfaz.</span><span class="sxs-lookup"><span data-stu-id="81cfa-104">The `GetTypeInfo` method retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="81cfa-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81cfa-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="81cfa-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="81cfa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81cfa-107">*itinfo*</span><span class="sxs-lookup"><span data-stu-id="81cfa-107">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="81cfa-108">Información de tipo que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="81cfa-108">Type information to return.</span></span> <span data-ttu-id="81cfa-109">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="81cfa-109">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="81cfa-110">*lcid*</span><span class="sxs-lookup"><span data-stu-id="81cfa-110">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="81cfa-111">Identificador de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="81cfa-111">Locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="81cfa-112">*pptinfo*</span><span class="sxs-lookup"><span data-stu-id="81cfa-112">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="81cfa-113">Dirección de una variable que recibe un puntero **ITypeInfo** .</span><span class="sxs-lookup"><span data-stu-id="81cfa-113">Address of a variable that receives an **ITypeInfo** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81cfa-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="81cfa-114">Return value</span></span>

<span data-ttu-id="81cfa-115">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="81cfa-115">Returns an **HRESULT** value.</span></span> <span data-ttu-id="81cfa-116">Estos son algunos de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="81cfa-116">Possible values include the following.</span></span>



| <span data-ttu-id="81cfa-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="81cfa-117">Return code</span></span>                                                                                             | <span data-ttu-id="81cfa-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="81cfa-118">Description</span></span>                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="81cfa-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="81cfa-119"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="81cfa-120">Correcto.</span><span class="sxs-lookup"><span data-stu-id="81cfa-120">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="81cfa-121"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="81cfa-121"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="81cfa-122">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="81cfa-122">**NULL** pointer argument.</span></span><br/>          |
| <dl> <span data-ttu-id="81cfa-123"><dt>**Escriba \_ E \_ ELEMENTNOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="81cfa-123"><dt>**TYPE\_E\_ELEMENTNOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="81cfa-124">El parámetro *itinfo* no es cero.</span><span class="sxs-lookup"><span data-stu-id="81cfa-124">The *itinfo* parameter is not zero.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="81cfa-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81cfa-125">Requirements</span></span>



| <span data-ttu-id="81cfa-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="81cfa-126">Requirement</span></span> | <span data-ttu-id="81cfa-127">Value</span><span class="sxs-lookup"><span data-stu-id="81cfa-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81cfa-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="81cfa-128">Header</span></span><br/>  | <dl> <span data-ttu-id="81cfa-129"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="81cfa-129"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="81cfa-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="81cfa-130">Library</span></span><br/> | <dl> <span data-ttu-id="81cfa-131"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="81cfa-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81cfa-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="81cfa-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81cfa-133">**Clase CMediaPosition**</span><span class="sxs-lookup"><span data-stu-id="81cfa-133">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




