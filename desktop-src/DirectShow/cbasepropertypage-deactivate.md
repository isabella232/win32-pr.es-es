---
description: El método Deactivate destruye la ventana del cuadro de diálogo. Este método implementa el método IPropertyPage::D eactivate.
ms.assetid: f2d2f15f-15f6-4902-bafc-f58a684ff193
title: Método CBasePropertyPage. Deactivate (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Deactivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63a843502fc735cc41ff3656e83ef3d6cb839a19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660767"
---
# <a name="cbasepropertypagedeactivate-method"></a><span data-ttu-id="a53b6-104">CBasePropertyPage. Deactivate (método)</span><span class="sxs-lookup"><span data-stu-id="a53b6-104">CBasePropertyPage.Deactivate method</span></span>

<span data-ttu-id="a53b6-105">El `Deactivate` método destruye la ventana del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a53b6-105">The `Deactivate` method destroys the dialog window.</span></span> <span data-ttu-id="a53b6-106">Este método implementa el método **IPropertyPage::D eactivate** .</span><span class="sxs-lookup"><span data-stu-id="a53b6-106">This method implements the **IPropertyPage::Deactivate** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a53b6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a53b6-107">Syntax</span></span>


```C++
HRESULT Deactivate();
```



## <a name="parameters"></a><span data-ttu-id="a53b6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a53b6-108">Parameters</span></span>

<span data-ttu-id="a53b6-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a53b6-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a53b6-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a53b6-110">Return value</span></span>

<span data-ttu-id="a53b6-111">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a53b6-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="a53b6-112">Estos son algunos de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="a53b6-112">Possible values include the following.</span></span>



| <span data-ttu-id="a53b6-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a53b6-113">Return code</span></span>                                                                                  | <span data-ttu-id="a53b6-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="a53b6-114">Description</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="a53b6-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="a53b6-115"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="a53b6-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="a53b6-116">Success.</span></span><br/>            |
| <dl> <span data-ttu-id="a53b6-117"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="a53b6-117"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="a53b6-118">Error inesperado.</span><span class="sxs-lookup"><span data-stu-id="a53b6-118">Unexpected failure.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a53b6-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a53b6-119">Requirements</span></span>



| <span data-ttu-id="a53b6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a53b6-120">Requirement</span></span> | <span data-ttu-id="a53b6-121">Value</span><span class="sxs-lookup"><span data-stu-id="a53b6-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a53b6-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a53b6-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a53b6-123"><dt>Cprop. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a53b6-123"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="a53b6-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a53b6-124">Library</span></span><br/> | <dl> <span data-ttu-id="a53b6-125"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a53b6-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a53b6-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="a53b6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a53b6-127">**Clase CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="a53b6-127">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> <dt>

[<span data-ttu-id="a53b6-128">**CBasePropertyPage:: OnDeactivate**</span><span class="sxs-lookup"><span data-stu-id="a53b6-128">**CBasePropertyPage::OnDeactivate**</span></span>](cbasepropertypage-ondeactivate.md)
</dt> </dl>

 

 




