---
description: 'El método SetPageSite inicializa la página de propiedades y proporciona un puntero a la interfaz IPropertyPageSite del marco de propiedad. Este método implementa el método IPropertyPage:: SetPageSite.'
ms.assetid: 16c4633f-2f91-4b1b-a47c-4ef945c3af00
title: Método CBasePropertyPage. SetPageSite (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.SetPageSite
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a165ff60971cef3d2373e0f07b2abee554308279
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660248"
---
# <a name="cbasepropertypagesetpagesite-method"></a><span data-ttu-id="1e925-104">CBasePropertyPage. SetPageSite, método</span><span class="sxs-lookup"><span data-stu-id="1e925-104">CBasePropertyPage.SetPageSite method</span></span>

<span data-ttu-id="1e925-105">El `SetPageSite` método inicializa la página de propiedades y proporciona un puntero a la interfaz **IPropertyPageSite** del marco de propiedad.</span><span class="sxs-lookup"><span data-stu-id="1e925-105">The `SetPageSite` method initializes the property page and provides a pointer to the property frame's **IPropertyPageSite** interface.</span></span> <span data-ttu-id="1e925-106">Este método implementa el método **IPropertyPage:: SetPageSite** .</span><span class="sxs-lookup"><span data-stu-id="1e925-106">This method implements the **IPropertyPage::SetPageSite** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e925-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e925-107">Syntax</span></span>


```C++
HRESULT SetPageSite(
   IPropertyPageSite *pPageSite
);
```



## <a name="parameters"></a><span data-ttu-id="1e925-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1e925-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e925-109">*pPageSite*</span><span class="sxs-lookup"><span data-stu-id="1e925-109">*pPageSite*</span></span> 
</dt> <dd>

<span data-ttu-id="1e925-110">Puntero a la interfaz **IPropertyPageSite** .</span><span class="sxs-lookup"><span data-stu-id="1e925-110">Pointer to the **IPropertyPageSite** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e925-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1e925-111">Return value</span></span>

<span data-ttu-id="1e925-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1e925-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="1e925-113">Estos son algunos de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="1e925-113">Possible values include the following.</span></span>



| <span data-ttu-id="1e925-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1e925-114">Return code</span></span>                                                                                  | <span data-ttu-id="1e925-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e925-115">Description</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="1e925-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="1e925-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="1e925-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="1e925-117">Success.</span></span><br/>            |
| <dl> <span data-ttu-id="1e925-118"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="1e925-118"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="1e925-119">Error inesperado.</span><span class="sxs-lookup"><span data-stu-id="1e925-119">Unexpected failure.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1e925-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1e925-120">Remarks</span></span>

<span data-ttu-id="1e925-121">El método almacena el puntero *pPageSite* en la variable miembro [**CBasePropertyPage:: m \_ pPageSite**](cbasepropertypage-m-ppagesite.md) .</span><span class="sxs-lookup"><span data-stu-id="1e925-121">The method stores the *pPageSite* pointer in the [**CBasePropertyPage::m\_pPageSite**](cbasepropertypage-m-ppagesite.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e925-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e925-122">Requirements</span></span>



| <span data-ttu-id="1e925-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e925-123">Requirement</span></span> | <span data-ttu-id="1e925-124">Value</span><span class="sxs-lookup"><span data-stu-id="1e925-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e925-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1e925-125">Header</span></span><br/>  | <dl> <span data-ttu-id="1e925-126"><dt>Cprop. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1e925-126"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="1e925-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1e925-127">Library</span></span><br/> | <dl> <span data-ttu-id="1e925-128"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1e925-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e925-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e925-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e925-130">**Clase CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="1e925-130">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




