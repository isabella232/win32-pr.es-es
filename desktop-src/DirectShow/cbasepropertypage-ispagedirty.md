---
description: 'El método IsPageDirty indica si la página de propiedades ha cambiado desde que se activó o desde la llamada más reciente a IPropertyPage:: Apply. Este método implementa el método IPropertyPage:: IsPageDirty.'
ms.assetid: 95eeec26-7dbb-4add-a827-6505b40afe48
title: Método CBasePropertyPage. IsPageDirty (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.IsPageDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c69c2e7d480f63542e146c73e56b9e692693f665
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660992"
---
# <a name="cbasepropertypageispagedirty-method"></a><span data-ttu-id="abebc-104">CBasePropertyPage. IsPageDirty, método</span><span class="sxs-lookup"><span data-stu-id="abebc-104">CBasePropertyPage.IsPageDirty method</span></span>

<span data-ttu-id="abebc-105">El `IsPageDirty` método indica si la página de propiedades ha cambiado desde que se activó o desde la llamada más reciente a **IPropertyPage:: Apply**.</span><span class="sxs-lookup"><span data-stu-id="abebc-105">The `IsPageDirty` method indicates whether the property page has changed since it was activated or since the most recent call to **IPropertyPage::Apply**.</span></span> <span data-ttu-id="abebc-106">Este método implementa el método **IPropertyPage:: IsPageDirty** .</span><span class="sxs-lookup"><span data-stu-id="abebc-106">This method implements the **IPropertyPage::IsPageDirty** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="abebc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="abebc-107">Syntax</span></span>


```C++
HRESULT IsPageDirty();
```



## <a name="parameters"></a><span data-ttu-id="abebc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="abebc-108">Parameters</span></span>

<span data-ttu-id="abebc-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="abebc-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="abebc-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="abebc-110">Return value</span></span>

<span data-ttu-id="abebc-111">Devuelve S \_ OK si [**CBasePropertyPage:: m \_ bDirty**](cbasepropertypage-m-bdirty.md) es **true** o S \_ false en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="abebc-111">Returns S\_OK if [**CBasePropertyPage::m\_bDirty**](cbasepropertypage-m-bdirty.md) is **TRUE**, or S\_FALSE otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="abebc-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abebc-112">Requirements</span></span>



| <span data-ttu-id="abebc-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="abebc-113">Requirement</span></span> | <span data-ttu-id="abebc-114">Value</span><span class="sxs-lookup"><span data-stu-id="abebc-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abebc-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="abebc-115">Header</span></span><br/>  | <dl> <span data-ttu-id="abebc-116"><dt>Cprop. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="abebc-116"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="abebc-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="abebc-117">Library</span></span><br/> | <dl> <span data-ttu-id="abebc-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="abebc-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abebc-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="abebc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abebc-120">**Clase CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="abebc-120">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




