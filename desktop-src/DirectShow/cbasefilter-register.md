---
description: El método Register agrega el filtro al registro.
ms.assetid: 934e421a-25a6-40fa-a48b-6d7331f34b78
title: Método CBaseFilter. Register (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Register
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1bd7ba5a57d670ef28ffda022c95c7dc5b12df77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661102"
---
# <a name="cbasefilterregister-method"></a><span data-ttu-id="703c7-103">CBaseFilter. Register (método)</span><span class="sxs-lookup"><span data-stu-id="703c7-103">CBaseFilter.Register method</span></span>

<span data-ttu-id="703c7-104">El `Register` método agrega el filtro al registro.</span><span class="sxs-lookup"><span data-stu-id="703c7-104">The `Register` method adds the filter to the registry.</span></span>

> [!Note]  
> <span data-ttu-id="703c7-105">Este método está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="703c7-105">This method is obsolete.</span></span> <span data-ttu-id="703c7-106">Los nuevos filtros deben registrarse con la función [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) .</span><span class="sxs-lookup"><span data-stu-id="703c7-106">New filters should be registered using the [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) function.</span></span> <span data-ttu-id="703c7-107">Para obtener más información, consulte [Cómo registrar filtros de DirectShow](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="703c7-107">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="703c7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="703c7-108">Syntax</span></span>


```C++
HRESULT Register();
```



## <a name="parameters"></a><span data-ttu-id="703c7-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="703c7-109">Parameters</span></span>

<span data-ttu-id="703c7-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="703c7-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="703c7-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="703c7-111">Return value</span></span>

<span data-ttu-id="703c7-112">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="703c7-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="703c7-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="703c7-113">Return code</span></span>                                                                             | <span data-ttu-id="703c7-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="703c7-114">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="703c7-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="703c7-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="703c7-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="703c7-116">Success.</span></span><br/>                                  |
| <dl> <span data-ttu-id="703c7-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="703c7-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="703c7-118">No hay información de registro disponible.</span><span class="sxs-lookup"><span data-stu-id="703c7-118">No registration information is available.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="703c7-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="703c7-119">Requirements</span></span>



| <span data-ttu-id="703c7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="703c7-120">Requirement</span></span> | <span data-ttu-id="703c7-121">Value</span><span class="sxs-lookup"><span data-stu-id="703c7-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="703c7-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="703c7-122">Header</span></span><br/>  | <dl> <span data-ttu-id="703c7-123"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="703c7-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="703c7-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="703c7-124">Library</span></span><br/> | <dl> <span data-ttu-id="703c7-125"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="703c7-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="703c7-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="703c7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="703c7-127">**Clase CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="703c7-127">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




