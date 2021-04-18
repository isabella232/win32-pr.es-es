---
description: La macro declare \_ IUNKNOWN declara los tres métodos de la interfaz base para una nueva interfaz.
ms.assetid: 3bf8e830-c923-4c31-8855-88fa08f80422
title: DECLARE_IUNKNOWN (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DECLARE_IUNKNOWN
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4823c1b4bd4832b1047a732bc503f04b4da65483
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660989"
---
# <a name="declare_iunknown"></a><span data-ttu-id="619ba-103">DECLARAR \_ IUNKNOWN</span><span class="sxs-lookup"><span data-stu-id="619ba-103">DECLARE\_IUNKNOWN</span></span>

<span data-ttu-id="619ba-104">La macro **declare \_ IUNKNOWN** declara los tres métodos de la interfaz base para una nueva interfaz.</span><span class="sxs-lookup"><span data-stu-id="619ba-104">The **DECLARE\_IUNKNOWN** macro declares the three methods of the base interface for a new interface.</span></span>

<span data-ttu-id="619ba-105">**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="619ba-105">**Syntax**</span></span>

``` syntax
#define DECLARE_IUNKNOWN                                        \
    STDMETHODIMP QueryInterface(REFIID riid, void **ppv) {      \
        return GetOwner()->QueryInterface(riid,ppv);            \
    };                                                          \
    STDMETHODIMP_(ULONG) AddRef() {                             \
        return GetOwner()->AddRef();                            \
    };                                                          \
    STDMETHODIMP_(ULONG) Release() {                            \
        return GetOwner()->Release();                           \
    };
```

## <a name="remarks"></a><span data-ttu-id="619ba-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="619ba-106">Remarks</span></span>

<span data-ttu-id="619ba-107">Al crear una nueva interfaz, debe derivar de **IUnknown**, que tiene tres métodos: **QueryInterface**, **AddRef** y **Release**.</span><span class="sxs-lookup"><span data-stu-id="619ba-107">When you create a new interface, it must derive from **IUnknown**, which has three methods: **QueryInterface**, **AddRef**, and **Release**.</span></span> <span data-ttu-id="619ba-108">Esta macro simplifica el proceso de declaración declarando cada uno de estos métodos para la nueva interfaz.</span><span class="sxs-lookup"><span data-stu-id="619ba-108">This macro simplifies the declaration process by declaring each of these methods for the new interface.</span></span>

<span data-ttu-id="619ba-109">Esta macro solo funciona con las clases que derivan directa o indirectamente de la clase [**CUnknown**](cunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="619ba-109">This macro works only with classes that derive, directly or indirectly, from the [**CUnknown**](cunknown.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="619ba-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="619ba-110">Requirements</span></span>



| <span data-ttu-id="619ba-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="619ba-111">Requirement</span></span> | <span data-ttu-id="619ba-112">Value</span><span class="sxs-lookup"><span data-stu-id="619ba-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="619ba-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="619ba-113">Header</span></span><br/>  | <dl> <span data-ttu-id="619ba-114"><dt>ComBase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="619ba-114"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="619ba-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="619ba-115">Library</span></span><br/> | <dl> <span data-ttu-id="619ba-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="619ba-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="619ba-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="619ba-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="619ba-118">**Funciones auxiliares de COM**</span><span class="sxs-lookup"><span data-stu-id="619ba-118">**COM Helper Functions**</span></span>](com-helper-functions.md)
</dt> <dt>

[<span data-ttu-id="619ba-119">**CUnknown:: GetOwner**</span><span class="sxs-lookup"><span data-stu-id="619ba-119">**CUnknown::GetOwner**</span></span>](cunknown-getowner.md)
</dt> <dt>

[<span data-ttu-id="619ba-120">Cómo implementar IUnknown</span><span class="sxs-lookup"><span data-stu-id="619ba-120">How to Implement IUnknown</span></span>](how-to-implement-iunknown.md)
</dt> </dl>

 

 




