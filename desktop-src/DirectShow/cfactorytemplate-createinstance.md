---
description: El método CreateInstance llama a la función de creación de objetos para la clase.
ms.assetid: 8a7d5c56-867d-432d-a0c2-97b8e3cf8a69
title: Método CFactoryTemplate. CreateInstance (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0f67ba528943bc2a468419fc84db44359745d4a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660855"
---
# <a name="cfactorytemplatecreateinstance-method"></a><span data-ttu-id="640fb-103">CFactoryTemplate. CreateInstance (método)</span><span class="sxs-lookup"><span data-stu-id="640fb-103">CFactoryTemplate.CreateInstance method</span></span>

<span data-ttu-id="640fb-104">El `CreateInstance` método llama a la función de creación de objetos para la clase.</span><span class="sxs-lookup"><span data-stu-id="640fb-104">The `CreateInstance` method calls the object-creation function for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="640fb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="640fb-105">Syntax</span></span>


```C++
CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="640fb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="640fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="640fb-107">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="640fb-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="640fb-108">Puntero a la interfaz **IUnknown** de agregación.</span><span class="sxs-lookup"><span data-stu-id="640fb-108">Pointer to the aggregating **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="640fb-109">*phr*</span><span class="sxs-lookup"><span data-stu-id="640fb-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="640fb-110">Puntero a una variable que recibe un valor **HRESULT** que indica si el método se ha ejecutado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="640fb-110">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="640fb-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="640fb-111">Return value</span></span>

<span data-ttu-id="640fb-112">Devuelve una instancia del objeto de clase.</span><span class="sxs-lookup"><span data-stu-id="640fb-112">Returns an instance of the class object.</span></span>

## <a name="remarks"></a><span data-ttu-id="640fb-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="640fb-113">Remarks</span></span>

<span data-ttu-id="640fb-114">El método **IClassFactory:: CreateInstance** llama a este método de clase.</span><span class="sxs-lookup"><span data-stu-id="640fb-114">The **IClassFactory::CreateInstance** method calls this class method.</span></span> <span data-ttu-id="640fb-115">Este método llama a la función a la que apunta la variable miembro [**CFactoryTemplate:: m \_ lpfnNew**](cfactorytemplate-m-lpfnnew.md) .</span><span class="sxs-lookup"><span data-stu-id="640fb-115">This method calls the function pointed to by the [**CFactoryTemplate::m\_lpfnNew**](cfactorytemplate-m-lpfnnew.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="640fb-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="640fb-116">Requirements</span></span>



| <span data-ttu-id="640fb-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="640fb-117">Requirement</span></span> | <span data-ttu-id="640fb-118">Value</span><span class="sxs-lookup"><span data-stu-id="640fb-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="640fb-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="640fb-119">Header</span></span><br/>  | <dl> <span data-ttu-id="640fb-120"><dt>ComBase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="640fb-120"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="640fb-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="640fb-121">Library</span></span><br/> | <dl> <span data-ttu-id="640fb-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="640fb-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="640fb-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="640fb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="640fb-124">**Clase CFactoryTemplate**</span><span class="sxs-lookup"><span data-stu-id="640fb-124">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




