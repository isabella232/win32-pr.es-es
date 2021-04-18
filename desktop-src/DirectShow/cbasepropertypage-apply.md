---
description: 'El método Apply aplica los valores de la página de propiedades actual al objeto asociado a la página de propiedades. Este método implementa el método IPropertyPage:: Apply.'
ms.assetid: 9fe759d1-2b46-4489-b7b8-b5a35330091d
title: Método CBasePropertyPage. Apply (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Apply
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21d1208979cca167b059cb720c492ac51c362c39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660768"
---
# <a name="cbasepropertypageapply-method"></a><span data-ttu-id="1c614-104">CBasePropertyPage. Apply (método)</span><span class="sxs-lookup"><span data-stu-id="1c614-104">CBasePropertyPage.Apply method</span></span>

<span data-ttu-id="1c614-105">El `Apply` método aplica los valores actuales de la página de propiedades al objeto asociado a la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="1c614-105">The `Apply` method applies the current property page values to the object associated with the property page.</span></span> <span data-ttu-id="1c614-106">Este método implementa el método **IPropertyPage:: Apply** .</span><span class="sxs-lookup"><span data-stu-id="1c614-106">This method implements the **IPropertyPage::Apply** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c614-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1c614-107">Syntax</span></span>


```C++
HRESULT Apply();
```



## <a name="parameters"></a><span data-ttu-id="1c614-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1c614-108">Parameters</span></span>

<span data-ttu-id="1c614-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="1c614-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1c614-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1c614-110">Return value</span></span>

<span data-ttu-id="1c614-111">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1c614-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="1c614-112">Estos son algunos de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="1c614-112">Possible values include the following.</span></span>



| <span data-ttu-id="1c614-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1c614-113">Return code</span></span>                                                                                  | <span data-ttu-id="1c614-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c614-114">Description</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="1c614-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="1c614-115"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="1c614-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="1c614-116">Success.</span></span><br/>            |
| <dl> <span data-ttu-id="1c614-117"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="1c614-117"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="1c614-118">Error inesperado.</span><span class="sxs-lookup"><span data-stu-id="1c614-118">Unexpected failure.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1c614-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1c614-119">Remarks</span></span>

<span data-ttu-id="1c614-120">Si la marca [**CBasePropertyPage:: m \_ BDirty**](cbasepropertypage-m-bdirty.md) es **true**, este método llama al método [**CBasePropertyPage:: OnApplyChanges**](cbasepropertypage-onapplychanges.md) .</span><span class="sxs-lookup"><span data-stu-id="1c614-120">If the [**CBasePropertyPage::m\_bDirty**](cbasepropertypage-m-bdirty.md) flag is **TRUE**, this method calls the [**CBasePropertyPage::OnApplyChanges**](cbasepropertypage-onapplychanges.md) method.</span></span> <span data-ttu-id="1c614-121">Invalide **OnApplyChanges** para aplicar los cambios al objeto.</span><span class="sxs-lookup"><span data-stu-id="1c614-121">Override **OnApplyChanges** to apply the changes to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c614-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c614-122">Requirements</span></span>



| <span data-ttu-id="1c614-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c614-123">Requirement</span></span> | <span data-ttu-id="1c614-124">Value</span><span class="sxs-lookup"><span data-stu-id="1c614-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c614-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1c614-125">Header</span></span><br/>  | <dl> <span data-ttu-id="1c614-126"><dt>Cprop. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1c614-126"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="1c614-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1c614-127">Library</span></span><br/> | <dl> <span data-ttu-id="1c614-128"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1c614-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c614-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="1c614-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c614-130">**Clase CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="1c614-130">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




