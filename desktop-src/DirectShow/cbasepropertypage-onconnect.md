---
description: El método alconnect proporciona un puntero IUnknown al objeto asociado a la página de propiedades.
ms.assetid: 74cae8e1-5347-4e3d-ba5f-6a4efec2ddae
title: Método CBasePropertyPage. alconnect (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 38f83a7c491f1591cece8d5d85eb4525a1059d2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661240"
---
# <a name="cbasepropertypageonconnect-method"></a><span data-ttu-id="06486-103">CBasePropertyPage. alconnect (método)</span><span class="sxs-lookup"><span data-stu-id="06486-103">CBasePropertyPage.OnConnect method</span></span>

<span data-ttu-id="06486-104">El `OnConnect` método proporciona un puntero **IUnknown** al objeto asociado a la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="06486-104">The `OnConnect` method provides an **IUnknown** pointer to the object associated with the property page.</span></span>

## <a name="syntax"></a><span data-ttu-id="06486-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="06486-105">Syntax</span></span>


```C++
virtual HRESULT OnConnect(
   IUnknown *pUnknown
);
```



## <a name="parameters"></a><span data-ttu-id="06486-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="06486-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06486-107">*pUnknown*</span><span class="sxs-lookup"><span data-stu-id="06486-107">*pUnknown*</span></span> 
</dt> <dd>

<span data-ttu-id="06486-108">Puntero a la interfaz **IUnknown** del objeto.</span><span class="sxs-lookup"><span data-stu-id="06486-108">Pointer to the **IUnknown** interface of the object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06486-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="06486-109">Return value</span></span>

<span data-ttu-id="06486-110">La implementación de la clase base devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="06486-110">The base-class implementation returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="06486-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="06486-111">Remarks</span></span>

<span data-ttu-id="06486-112">El método [**CBasePropertyPage:: SetObjects**](cbasepropertypage-setobjects.md) llama al `OnConnect` método.</span><span class="sxs-lookup"><span data-stu-id="06486-112">The [**CBasePropertyPage::SetObjects**](cbasepropertypage-setobjects.md) method calls the `OnConnect` method.</span></span> <span data-ttu-id="06486-113">Invalide este método para almacenar un puntero al objeto especificado por *pUnknown*.</span><span class="sxs-lookup"><span data-stu-id="06486-113">Override this method to store a pointer to the object specified by *pUnknown*.</span></span> <span data-ttu-id="06486-114">Puede almacenar el puntero *pUnknown* en sí o consultar ese puntero para otras interfaces.</span><span class="sxs-lookup"><span data-stu-id="06486-114">You can either store the *pUnknown* pointer itself, or query that pointer for other interfaces.</span></span> <span data-ttu-id="06486-115">Si almacena el puntero *pUnknown* , llame a **AddRef** antes de que `OnConnect` devuelva.</span><span class="sxs-lookup"><span data-stu-id="06486-115">If you store the *pUnknown* pointer, call **AddRef** before `OnConnect` returns.</span></span>

<span data-ttu-id="06486-116">En el método [**CBasePropertyPage:: OnActivate**](cbasepropertypage-onactivate.md) , use el puntero almacenado (o los punteros) para recuperar los valores iniciales de las propiedades del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="06486-116">In the [**CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md) method, use the stored pointer (or pointers) to retrieve initial values for the dialog properties.</span></span> <span data-ttu-id="06486-117">En el método [**CBasePropertyPage:: OnApplyChanges**](cbasepropertypage-onapplychanges.md) , aplique los cambios de nuevo al objeto.</span><span class="sxs-lookup"><span data-stu-id="06486-117">In the [**CBasePropertyPage::OnApplyChanges**](cbasepropertypage-onapplychanges.md) method, apply any changes back to the object.</span></span> <span data-ttu-id="06486-118">Libera todos los punteros en el método [**CBasePropertyPage:: OnDisconnection**](cbasepropertypage-ondisconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="06486-118">Release all pointers in the [**CBasePropertyPage::OnDisconnect**](cbasepropertypage-ondisconnect.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="06486-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="06486-119">Examples</span></span>


```C++
HRESULT CMyProp::OnConnect(IUnknown *pUnk)
{
    ASSERT(m_pOwningFilter == NULL);
    HRESULT hr;
    // Query pUnk for the filter's custom interface.
    hr = pUnk->QueryInterface(IID_ISomeCustomInterface,
             reinterpret_cast<void**>(&m_pOwningFilter));
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="06486-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06486-120">Requirements</span></span>



| <span data-ttu-id="06486-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="06486-121">Requirement</span></span> | <span data-ttu-id="06486-122">Value</span><span class="sxs-lookup"><span data-stu-id="06486-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06486-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="06486-123">Header</span></span><br/>  | <dl> <span data-ttu-id="06486-124"><dt>Cprop. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="06486-124"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="06486-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="06486-125">Library</span></span><br/> | <dl> <span data-ttu-id="06486-126"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="06486-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06486-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="06486-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06486-128">**Clase CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="06486-128">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




