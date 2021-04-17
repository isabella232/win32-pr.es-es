---
description: Puntero a una función que crea una instancia del objeto.
ms.assetid: 86859bf9-e16a-4494-bf1b-1d8ddbc1c805
title: 'Miembro CFactoryTemplate:: m_lpfnNew (ComBase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lpfnNew
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2299f7a87f348ac8a5fa6c6d83b6a17fbf97ca28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671149"
---
# <a name="cfactorytemplatem_lpfnnew-member"></a><span data-ttu-id="3860f-103">Miembro lpfnNew CFactoryTemplate:: m \_</span><span class="sxs-lookup"><span data-stu-id="3860f-103">CFactoryTemplate::m\_lpfnNew member</span></span>

<span data-ttu-id="3860f-104">Puntero a una función que crea una instancia del objeto.</span><span class="sxs-lookup"><span data-stu-id="3860f-104">Pointer to a function that creates an instance of the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3860f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3860f-105">Syntax</span></span>


```C++
LPFNNewCOMObject m_lpfnNew;
```



## <a name="remarks"></a><span data-ttu-id="3860f-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3860f-106">Remarks</span></span>

<span data-ttu-id="3860f-107">En el archivo DLL, declare una función estática que devuelva un puntero a una nueva instancia del objeto.</span><span class="sxs-lookup"><span data-stu-id="3860f-107">In your DLL, declare a static function that returns a pointer to a new instance of the object.</span></span> <span data-ttu-id="3860f-108">En la plantilla de generador, establezca la variable de miembro **m \_ lpfnNew** en la dirección de esta función estática.</span><span class="sxs-lookup"><span data-stu-id="3860f-108">In the factory template, set the **m\_lpfnNew** member variable to the address of this static function.</span></span>

<span data-ttu-id="3860f-109">El tipo de puntero de función es [**LPFNNewCOMObject**](lpfnnewcomobject.md).</span><span class="sxs-lookup"><span data-stu-id="3860f-109">The function pointer type is [**LPFNNewCOMObject**](lpfnnewcomobject.md).</span></span>

<span data-ttu-id="3860f-110">En el ejemplo siguiente se muestra una función típica para **m \_ lpfnNew**:</span><span class="sxs-lookup"><span data-stu-id="3860f-110">The following example shows a typical function for **m\_lpfnNew**:</span></span>


```C++
CUnknown * WINAPI CMyComponent::CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr) 
{
    CMyComponent *pNewObject = 
        new CMyComponent(NAME("My Component"), pUnk, pHr );

    if (pNewObject == NULL)  
    {
        *phr = E_OUTOFMEMORY;
    }
    return pNewObject;
}
```



## <a name="requirements"></a><span data-ttu-id="3860f-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3860f-111">Requirements</span></span>



| <span data-ttu-id="3860f-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="3860f-112">Requirement</span></span> | <span data-ttu-id="3860f-113">Value</span><span class="sxs-lookup"><span data-stu-id="3860f-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3860f-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3860f-114">Header</span></span><br/>  | <dl> <span data-ttu-id="3860f-115"><dt>ComBase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3860f-115"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3860f-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3860f-116">Library</span></span><br/> | <dl> <span data-ttu-id="3860f-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="3860f-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3860f-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="3860f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3860f-119">**Clase CFactoryTemplate**</span><span class="sxs-lookup"><span data-stu-id="3860f-119">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




