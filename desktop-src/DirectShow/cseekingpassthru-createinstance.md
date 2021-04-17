---
description: El método CreateInstance crea una instancia del objeto. Este método admite la creación del objeto a través de un generador de clases. Para obtener más información, vea CFactoryTemplate.
ms.assetid: 88dfa933-6fa1-4b57-8b0d-579233fa960c
title: Método CSeekingPassThru. CreateInstance (Seekpt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3640cbd6a0a3e582899e7f5cd349ca48498f3532
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660550"
---
# <a name="cseekingpassthrucreateinstance-method"></a><span data-ttu-id="ab1ec-105">CSeekingPassThru. CreateInstance (método)</span><span class="sxs-lookup"><span data-stu-id="ab1ec-105">CSeekingPassThru.CreateInstance method</span></span>

<span data-ttu-id="ab1ec-106">El `CreateInstance` método crea una instancia del objeto.</span><span class="sxs-lookup"><span data-stu-id="ab1ec-106">The `CreateInstance` method creates an instance of the object.</span></span> <span data-ttu-id="ab1ec-107">Este método admite la creación del objeto a través de un generador de clases.</span><span class="sxs-lookup"><span data-stu-id="ab1ec-107">This method supports creation of the object through a class factory.</span></span> <span data-ttu-id="ab1ec-108">Para obtener más información, vea [**CFactoryTemplate**](cfactorytemplate.md).</span><span class="sxs-lookup"><span data-stu-id="ab1ec-108">For more information, see [**CFactoryTemplate**](cfactorytemplate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ab1ec-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab1ec-109">Syntax</span></span>


```C++
static CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="ab1ec-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ab1ec-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab1ec-111">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="ab1ec-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="ab1ec-112">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="ab1ec-112">Pointer to the owner of this object.</span></span> <span data-ttu-id="ab1ec-113">Si se agrega el objeto, pase un puntero a la interfaz **IUnknown** del objeto de agregación.</span><span class="sxs-lookup"><span data-stu-id="ab1ec-113">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="ab1ec-114">De lo contrario, establezca este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="ab1ec-114">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ab1ec-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="ab1ec-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="ab1ec-116">Puntero a un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ab1ec-116">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="ab1ec-117">ignorado.</span><span class="sxs-lookup"><span data-stu-id="ab1ec-117">Ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab1ec-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ab1ec-118">Return value</span></span>

<span data-ttu-id="ab1ec-119">Devuelve un puntero a un nuevo objeto **CSeekingPassThru** .</span><span class="sxs-lookup"><span data-stu-id="ab1ec-119">Returns a pointer to a new **CSeekingPassThru** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab1ec-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab1ec-120">Requirements</span></span>



| <span data-ttu-id="ab1ec-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab1ec-121">Requirement</span></span> | <span data-ttu-id="ab1ec-122">Value</span><span class="sxs-lookup"><span data-stu-id="ab1ec-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab1ec-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ab1ec-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ab1ec-124"><dt>Seekpt. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab1ec-124"><dt>Seekpt.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ab1ec-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ab1ec-125">Library</span></span><br/> | <dl> <span data-ttu-id="ab1ec-126"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ab1ec-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab1ec-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab1ec-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab1ec-128">**Clase CSeekingPassThru**</span><span class="sxs-lookup"><span data-stu-id="ab1ec-128">**CSeekingPassThru Class**</span></span>](cseekingpassthru.md)
</dt> </dl>

 

 




