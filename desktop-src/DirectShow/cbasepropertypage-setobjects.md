---
description: 'El método SetObjects proporciona punteros IUnknown para los objetos asociados a la página de propiedades. Este método implementa el método IPropertyPage:: SetObjects.'
ms.assetid: 11ca1e70-772c-414e-9647-7e4c4084c0d3
title: Método CBasePropertyPage. SetObjects (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.SetObjects
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 197c5eb82de76fb5a5f606d8a161e853b0c1e8f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671269"
---
# <a name="cbasepropertypagesetobjects-method"></a><span data-ttu-id="0969d-104">CBasePropertyPage. SetObjects, método</span><span class="sxs-lookup"><span data-stu-id="0969d-104">CBasePropertyPage.SetObjects method</span></span>

<span data-ttu-id="0969d-105">El `SetObjects` método proporciona punteros **IUnknown** para los objetos asociados a la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="0969d-105">The `SetObjects` method provides **IUnknown** pointers for the objects associated with the property page.</span></span> <span data-ttu-id="0969d-106">Este método implementa el método **IPropertyPage:: SetObjects** .</span><span class="sxs-lookup"><span data-stu-id="0969d-106">This method implements the **IPropertyPage::SetObjects** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0969d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0969d-107">Syntax</span></span>


```C++
HRESULT SetObjects(
   ULONG     cObjects,
   LPUNKNOWN *ppUnk
);
```



## <a name="parameters"></a><span data-ttu-id="0969d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0969d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0969d-109">*cObjects*</span><span class="sxs-lookup"><span data-stu-id="0969d-109">*cObjects*</span></span> 
</dt> <dd>

<span data-ttu-id="0969d-110">Especifica el número de punteros **IUnknown** en la matriz especificada por *ppUnk*.</span><span class="sxs-lookup"><span data-stu-id="0969d-110">Specifies the number of **IUnknown** pointers in the array specified by *ppUnk*.</span></span>

</dd> <dt>

<span data-ttu-id="0969d-111">*ppUnk*</span><span class="sxs-lookup"><span data-stu-id="0969d-111">*ppUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="0969d-112">Especifica una matriz de punteros **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="0969d-112">Specifies an array of **IUnknown** pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0969d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0969d-113">Return value</span></span>

<span data-ttu-id="0969d-114">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0969d-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0969d-115">Estos son algunos de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="0969d-115">Possible values include the following.</span></span>



| <span data-ttu-id="0969d-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0969d-116">Return code</span></span>                                                                                  | <span data-ttu-id="0969d-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="0969d-117">Description</span></span>                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="0969d-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="0969d-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="0969d-119">Correcto.</span><span class="sxs-lookup"><span data-stu-id="0969d-119">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="0969d-120"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="0969d-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="0969d-121">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="0969d-121">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="0969d-122"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="0969d-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="0969d-123">Error inesperado.</span><span class="sxs-lookup"><span data-stu-id="0969d-123">Unexpected failure.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="0969d-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0969d-124">Remarks</span></span>

<span data-ttu-id="0969d-125">Aunque *ppUnk* especifica una matriz de punteros **IUnknown** , la clase **CBasePropertyPage** está diseñada únicamente para admitir un objeto asociado.</span><span class="sxs-lookup"><span data-stu-id="0969d-125">Although *ppUnk* specifies an array of **IUnknown** pointers, the **CBasePropertyPage** class is designed only to support one associated object.</span></span> <span data-ttu-id="0969d-126">Si *cObjects* es mayor que 1, el método devuelve E \_ inesperado.</span><span class="sxs-lookup"><span data-stu-id="0969d-126">If *cObjects* is greater than 1, the method returns E\_UNEXPECTED.</span></span>

<span data-ttu-id="0969d-127">Si *cObjects* es igual a 1, este método llama al método [**CBasePropertyPage:: alconnect**](cbasepropertypage-onconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="0969d-127">If *cObjects* equals 1, this method calls the [**CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) method.</span></span> <span data-ttu-id="0969d-128">Si *cObjects* es igual a 0, este método llama al método [**CBasePropertyPage:: OnDisconnection**](cbasepropertypage-ondisconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="0969d-128">If *cObjects* equals 0, this method calls the [**CBasePropertyPage::OnDisconnect**](cbasepropertypage-ondisconnect.md) method.</span></span> <span data-ttu-id="0969d-129">La clase derivada debe reemplazar ambos métodos; para obtener más información, vea los comentarios de estos métodos.</span><span class="sxs-lookup"><span data-stu-id="0969d-129">The derived class should override both of those methods; for details, see the remarks for those methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="0969d-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0969d-130">Requirements</span></span>



| <span data-ttu-id="0969d-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="0969d-131">Requirement</span></span> | <span data-ttu-id="0969d-132">Value</span><span class="sxs-lookup"><span data-stu-id="0969d-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0969d-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0969d-133">Header</span></span><br/>  | <dl> <span data-ttu-id="0969d-134"><dt>Cprop. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0969d-134"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="0969d-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0969d-135">Library</span></span><br/> | <dl> <span data-ttu-id="0969d-136"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0969d-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0969d-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="0969d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0969d-138">**Clase CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="0969d-138">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




