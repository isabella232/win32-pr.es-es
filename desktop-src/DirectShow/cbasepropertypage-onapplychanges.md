---
description: Se llama al método OnApplyChanges cuando el usuario aplica los cambios a la página de propiedades.
ms.assetid: 15a55644-b7bf-4c72-8e26-18fc4fb714b9
title: Método CBasePropertyPage. OnApplyChanges (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnApplyChanges
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cbcea308a8daaa8b9fdf15be765dc5d3a0df182c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671613"
---
# <a name="cbasepropertypageonapplychanges-method"></a><span data-ttu-id="21b64-103">CBasePropertyPage. OnApplyChanges, método</span><span class="sxs-lookup"><span data-stu-id="21b64-103">CBasePropertyPage.OnApplyChanges method</span></span>

<span data-ttu-id="21b64-104">`OnApplyChanges`Se llama al método cuando el usuario aplica los cambios a la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="21b64-104">The `OnApplyChanges` method is called when the user applies changes to the property page.</span></span>

## <a name="syntax"></a><span data-ttu-id="21b64-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="21b64-105">Syntax</span></span>


```C++
virtual HRESULT OnApplyChanges();
```



## <a name="parameters"></a><span data-ttu-id="21b64-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="21b64-106">Parameters</span></span>

<span data-ttu-id="21b64-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="21b64-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="21b64-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="21b64-108">Return value</span></span>

<span data-ttu-id="21b64-109">La implementación de la clase base devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="21b64-109">The base-class implementation returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="21b64-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="21b64-110">Remarks</span></span>

<span data-ttu-id="21b64-111">El método [**CBasePropertyPage:: Apply**](cbasepropertypage-apply.md) llama a `OnApplyChanges` si la marca [**\_ bDirty CBasePropertyPage:: m**](cbasepropertypage-m-bdirty.md) es **true**.</span><span class="sxs-lookup"><span data-stu-id="21b64-111">The [**CBasePropertyPage::Apply**](cbasepropertypage-apply.md) method calls `OnApplyChanges` if the [**CBasePropertyPage::m\_bDirty**](cbasepropertypage-m-bdirty.md) flag is **TRUE**.</span></span> <span data-ttu-id="21b64-112">Invalide `OnApplyChanges` para procesar los cambios y restablecer **m \_ bDirty** en **false**.</span><span class="sxs-lookup"><span data-stu-id="21b64-112">Override `OnApplyChanges` to process the changes and reset **m\_bDirty** to **FALSE**.</span></span>

## <a name="examples"></a><span data-ttu-id="21b64-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="21b64-113">Examples</span></span>


```C++
HRESULT CMyProp::OnApplyChanges(void)
{
    ASSERT(m_pOwningFilter != NULL);
    return m_pOwningFilter->SetSomeProperty(&m_lNewVal);
}
```



## <a name="requirements"></a><span data-ttu-id="21b64-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21b64-114">Requirements</span></span>



| <span data-ttu-id="21b64-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="21b64-115">Requirement</span></span> | <span data-ttu-id="21b64-116">Value</span><span class="sxs-lookup"><span data-stu-id="21b64-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21b64-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="21b64-117">Header</span></span><br/>  | <dl> <span data-ttu-id="21b64-118"><dt>Cprop. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="21b64-118"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="21b64-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="21b64-119">Library</span></span><br/> | <dl> <span data-ttu-id="21b64-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="21b64-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21b64-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="21b64-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21b64-122">**Clase CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="21b64-122">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




