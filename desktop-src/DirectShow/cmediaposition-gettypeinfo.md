---
description: 'Método CMediaPosition.GetTypeInfo: el método GetTypeInfo recupera la información de tipo del objeto , que luego se puede usar para obtener la información de tipo de una interfaz.'
ms.assetid: 0a04c43d-8b4b-4780-b02f-04053c405c77
title: Método CMediaPosition.GetTypeInfo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f7827a3599f05061b5760084bed46cd2554b45f9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099143"
---
# <a name="cmediapositiongettypeinfo-method"></a><span data-ttu-id="be6e2-103">Método CMediaPosition.GetTypeInfo</span><span class="sxs-lookup"><span data-stu-id="be6e2-103">CMediaPosition.GetTypeInfo method</span></span>

<span data-ttu-id="be6e2-104">El método recupera la información de tipo del objeto , que luego se puede usar `GetTypeInfo` para obtener la información de tipo de una interfaz.</span><span class="sxs-lookup"><span data-stu-id="be6e2-104">The `GetTypeInfo` method retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="be6e2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="be6e2-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="be6e2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="be6e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be6e2-107">*itinfo*</span><span class="sxs-lookup"><span data-stu-id="be6e2-107">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="be6e2-108">Escriba la información que se devolverá.</span><span class="sxs-lookup"><span data-stu-id="be6e2-108">Type information to return.</span></span> <span data-ttu-id="be6e2-109">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="be6e2-109">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="be6e2-110">*lcid*</span><span class="sxs-lookup"><span data-stu-id="be6e2-110">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="be6e2-111">Identificador de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="be6e2-111">Locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="be6e2-112">*pptinfo*</span><span class="sxs-lookup"><span data-stu-id="be6e2-112">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="be6e2-113">Dirección de una variable que recibe un **puntero ITypeInfo.**</span><span class="sxs-lookup"><span data-stu-id="be6e2-113">Address of a variable that receives an **ITypeInfo** pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be6e2-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="be6e2-114">Return value</span></span>

<span data-ttu-id="be6e2-115">Devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="be6e2-115">Returns an **HRESULT** value.</span></span> <span data-ttu-id="be6e2-116">Estos son algunos de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="be6e2-116">Possible values include the following.</span></span>



| <span data-ttu-id="be6e2-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="be6e2-117">Return code</span></span>                                                                                             | <span data-ttu-id="be6e2-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="be6e2-118">Description</span></span>                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="be6e2-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="be6e2-119"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="be6e2-120">Correcto.</span><span class="sxs-lookup"><span data-stu-id="be6e2-120">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="be6e2-121"><dt>**PUNTERO \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="be6e2-121"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="be6e2-122">**Argumento de** puntero NULL.</span><span class="sxs-lookup"><span data-stu-id="be6e2-122">**NULL** pointer argument.</span></span><br/>          |
| <dl> <span data-ttu-id="be6e2-123"><dt>**TYPE \_ E \_ ELEMENTNOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="be6e2-123"><dt>**TYPE\_E\_ELEMENTNOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="be6e2-124">El *parámetro itinfo* no es cero.</span><span class="sxs-lookup"><span data-stu-id="be6e2-124">The *itinfo* parameter is not zero.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="be6e2-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be6e2-125">Requirements</span></span>



| <span data-ttu-id="be6e2-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="be6e2-126">Requirement</span></span> | <span data-ttu-id="be6e2-127">Value</span><span class="sxs-lookup"><span data-stu-id="be6e2-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be6e2-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="be6e2-128">Header</span></span><br/>  | <dl> <span data-ttu-id="be6e2-129"><dt>Ctlutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="be6e2-129"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="be6e2-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="be6e2-130">Library</span></span><br/> | <dl> <span data-ttu-id="be6e2-131"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="be6e2-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be6e2-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="be6e2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be6e2-133">**CMediaPosition (clase)**</span><span class="sxs-lookup"><span data-stu-id="be6e2-133">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




