---
description: Recupera un objeto de información de tipo, que puede recuperar la información de tipo de una interfaz.
ms.assetid: d54042d5-e9d3-415c-b90d-1fe7d38164f5
title: Método CMediaEvent. GetTypeInfo (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e351d3b8b06bea4f6f9a1a160802972a8fa50f82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671558"
---
# <a name="cmediaeventgettypeinfo-method"></a><span data-ttu-id="550a9-103">CMediaEvent. GetTypeInfo, método</span><span class="sxs-lookup"><span data-stu-id="550a9-103">CMediaEvent.GetTypeInfo method</span></span>

<span data-ttu-id="550a9-104">Recupera un objeto de información de tipo, que puede recuperar la información de tipo de una interfaz.</span><span class="sxs-lookup"><span data-stu-id="550a9-104">Retrieves a type-information object, which can retrieve the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="550a9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="550a9-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="550a9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="550a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="550a9-107">*itinfo*</span><span class="sxs-lookup"><span data-stu-id="550a9-107">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="550a9-108">Información de tipo que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="550a9-108">Type information to return.</span></span> <span data-ttu-id="550a9-109">Pase cero para recuperar la información de tipo de la implementación de **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="550a9-109">Pass zero to retrieve type information for the **IDispatch** implementation.</span></span>

</dd> <dt>

<span data-ttu-id="550a9-110">*lcid*</span><span class="sxs-lookup"><span data-stu-id="550a9-110">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="550a9-111">IDENTIFICADOR de configuración regional de la información de tipo.</span><span class="sxs-lookup"><span data-stu-id="550a9-111">Locale ID for the type information.</span></span> <span data-ttu-id="550a9-112">En el caso de las clases que admiten nombres de miembro localizados, es posible que un objeto pueda devolver información de tipo diferente para distintos idiomas.</span><span class="sxs-lookup"><span data-stu-id="550a9-112">For classes that support localized member names, an object might be able to return different type information for different languages.</span></span> <span data-ttu-id="550a9-113">En el caso de las clases que no admiten nombres de miembro localizados, este parámetro se puede omitir.</span><span class="sxs-lookup"><span data-stu-id="550a9-113">For classes that do not support localized member names, this parameter can be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="550a9-114">*pptinfo*</span><span class="sxs-lookup"><span data-stu-id="550a9-114">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="550a9-115">Dirección de un puntero al objeto de información de tipo solicitado.</span><span class="sxs-lookup"><span data-stu-id="550a9-115">Address of a pointer to the type-information object requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="550a9-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="550a9-116">Return value</span></span>

<span data-ttu-id="550a9-117">Devuelve un \_ puntero E si *pptinfo* no es válido.</span><span class="sxs-lookup"><span data-stu-id="550a9-117">Returns an E\_POINTER if *pptinfo* is invalid.</span></span> <span data-ttu-id="550a9-118">Devuelve el tipo \_ E \_ ELEMENTNOTFOUND si *itinfo* no es cero.</span><span class="sxs-lookup"><span data-stu-id="550a9-118">Returns TYPE\_E\_ELEMENTNOTFOUND if *itinfo* is not zero.</span></span> <span data-ttu-id="550a9-119">Devuelve S \_ correcto si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="550a9-119">Returns S\_OK if is successful.</span></span> <span data-ttu-id="550a9-120">De lo contrario, devuelve un **valor HRESULT** de una de las llamadas para recuperar el tipo.</span><span class="sxs-lookup"><span data-stu-id="550a9-120">Otherwise, returns an **HRESULT** from one of the calls to retrieve the type.</span></span>

## <a name="requirements"></a><span data-ttu-id="550a9-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="550a9-121">Requirements</span></span>



| <span data-ttu-id="550a9-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="550a9-122">Requirement</span></span> | <span data-ttu-id="550a9-123">Value</span><span class="sxs-lookup"><span data-stu-id="550a9-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="550a9-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="550a9-124">Header</span></span><br/>  | <dl> <span data-ttu-id="550a9-125"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="550a9-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="550a9-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="550a9-126">Library</span></span><br/> | <dl> <span data-ttu-id="550a9-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="550a9-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="550a9-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="550a9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="550a9-129">**Clase CMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="550a9-129">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 




