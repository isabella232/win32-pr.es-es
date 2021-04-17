---
description: Se llama al método OnDisconnect cuando la página de propiedades debe liberar el objeto asociado.
ms.assetid: 55bab0ca-587e-405c-9025-f391cf08a620
title: Método CBasePropertyPage. OnDisconnection (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnDisconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abd251d20ca82ad0374a613d9ee73f0eaee21d31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670510"
---
# <a name="cbasepropertypageondisconnect-method"></a><span data-ttu-id="1f89f-103">CBasePropertyPage. OnDisconnection (método)</span><span class="sxs-lookup"><span data-stu-id="1f89f-103">CBasePropertyPage.OnDisconnect method</span></span>

<span data-ttu-id="1f89f-104">`OnDisconnect`Se llama al método cuando la página de propiedades debe liberar el objeto asociado.</span><span class="sxs-lookup"><span data-stu-id="1f89f-104">The `OnDisconnect` method is called when the property page should release the associated object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f89f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1f89f-105">Syntax</span></span>


```C++
virtual HRESULT OnDisconnect();
```



## <a name="parameters"></a><span data-ttu-id="1f89f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1f89f-106">Parameters</span></span>

<span data-ttu-id="1f89f-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="1f89f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1f89f-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1f89f-108">Return value</span></span>

<span data-ttu-id="1f89f-109">La implementación de la clase base devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="1f89f-109">The base-class implementation returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f89f-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1f89f-110">Remarks</span></span>

<span data-ttu-id="1f89f-111">El método [**CBasePropertyPage:: SetObjects**](cbasepropertypage-setobjects.md) llama al `OnDisconnect` método.</span><span class="sxs-lookup"><span data-stu-id="1f89f-111">The [**CBasePropertyPage::SetObjects**](cbasepropertypage-setobjects.md) method calls the `OnDisconnect` method.</span></span> <span data-ttu-id="1f89f-112">Invalide `OnDisconnect` para liberar los punteros que se obtuvieron en el método [**CBasePropertyPage:: alconnect**](cbasepropertypage-onconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="1f89f-112">Override `OnDisconnect` to release any pointers that were obtained in the [**CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="1f89f-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1f89f-113">Examples</span></span>


```C++
HRESULT CMyProp::OnDisconnect(void)
{
    if (m_pOwningFilter)
    {
        m_pOwningFilter->Release();
        m_pOwningFilter = NULL;
    }
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="1f89f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f89f-114">Requirements</span></span>



| <span data-ttu-id="1f89f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f89f-115">Requirement</span></span> | <span data-ttu-id="1f89f-116">Value</span><span class="sxs-lookup"><span data-stu-id="1f89f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f89f-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1f89f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1f89f-118"><dt>Cprop. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1f89f-118"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="1f89f-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1f89f-119">Library</span></span><br/> | <dl> <span data-ttu-id="1f89f-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1f89f-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f89f-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="1f89f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f89f-122">**Clase CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="1f89f-122">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




