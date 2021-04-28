---
description: 'Método CMediaControl.GetTypeInfo: recupera un objeto type-information, que puede recuperar la información de tipo de una interfaz.'
ms.assetid: 2014485f-d937-415d-a2fc-0c69269b5237
title: Método CMediaControl.GetTypeInfo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 857dbdeee9a2add9ab77cae0ff97d69699d2dd2e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099133"
---
# <a name="cmediacontrolgettypeinfo-method"></a><span data-ttu-id="6c4b5-103">Método CMediaControl.GetTypeInfo</span><span class="sxs-lookup"><span data-stu-id="6c4b5-103">CMediaControl.GetTypeInfo method</span></span>

<span data-ttu-id="6c4b5-104">Recupera un objeto de información de tipo, que puede recuperar la información de tipo de una interfaz.</span><span class="sxs-lookup"><span data-stu-id="6c4b5-104">Retrieves a type-information object, which can retrieve the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c4b5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6c4b5-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="6c4b5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6c4b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c4b5-107">*itinfo*</span><span class="sxs-lookup"><span data-stu-id="6c4b5-107">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="6c4b5-108">Escriba la información que se devolverá.</span><span class="sxs-lookup"><span data-stu-id="6c4b5-108">Type information to return.</span></span> <span data-ttu-id="6c4b5-109">Pase cero para recuperar información de tipo para **la implementación de IDispatch.**</span><span class="sxs-lookup"><span data-stu-id="6c4b5-109">Pass zero to retrieve type information for the **IDispatch** implementation.</span></span>

</dd> <dt>

<span data-ttu-id="6c4b5-110">*lcid*</span><span class="sxs-lookup"><span data-stu-id="6c4b5-110">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="6c4b5-111">Identificador de configuración regional para la información de tipo.</span><span class="sxs-lookup"><span data-stu-id="6c4b5-111">Locale ID for the type information.</span></span> <span data-ttu-id="6c4b5-112">Para las clases que admiten nombres de miembros localizados, un objeto podría devolver información de tipo diferente para distintos idiomas.</span><span class="sxs-lookup"><span data-stu-id="6c4b5-112">For classes that support localized member names, an object might be able to return different type information for different languages.</span></span> <span data-ttu-id="6c4b5-113">Para las clases que no admiten nombres de miembros localizados, este parámetro se puede omitir.</span><span class="sxs-lookup"><span data-stu-id="6c4b5-113">For classes that do not support localized member names, this parameter can be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="6c4b5-114">*pptinfo*</span><span class="sxs-lookup"><span data-stu-id="6c4b5-114">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="6c4b5-115">Dirección de un puntero al objeto de información de tipo solicitado.</span><span class="sxs-lookup"><span data-stu-id="6c4b5-115">Address of a pointer to the type-information object requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c4b5-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6c4b5-116">Return value</span></span>

<span data-ttu-id="6c4b5-117">Devuelve un puntero E \_ si *pptinfo* no es válido.</span><span class="sxs-lookup"><span data-stu-id="6c4b5-117">Returns an E\_POINTER if *pptinfo* is invalid.</span></span> <span data-ttu-id="6c4b5-118">Devuelve TYPE \_ E \_ ELEMENTNOTFOUND si *itinfo* no es cero.</span><span class="sxs-lookup"><span data-stu-id="6c4b5-118">Returns TYPE\_E\_ELEMENTNOTFOUND if *itinfo* is not zero.</span></span> <span data-ttu-id="6c4b5-119">Devuelve S \_ OK si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="6c4b5-119">Returns S\_OK if is successful.</span></span> <span data-ttu-id="6c4b5-120">De lo contrario, **devuelve un HRESULT** de una de las llamadas para recuperar el tipo.</span><span class="sxs-lookup"><span data-stu-id="6c4b5-120">Otherwise, returns an **HRESULT** from one of the calls to retrieve the type.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c4b5-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c4b5-121">Requirements</span></span>



| <span data-ttu-id="6c4b5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c4b5-122">Requirement</span></span> | <span data-ttu-id="6c4b5-123">Value</span><span class="sxs-lookup"><span data-stu-id="6c4b5-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c4b5-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c4b5-124">Header</span></span><br/>  | <dl> <span data-ttu-id="6c4b5-125"><dt>Ctlutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="6c4b5-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6c4b5-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6c4b5-126">Library</span></span><br/> | <dl> <span data-ttu-id="6c4b5-127"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="6c4b5-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c4b5-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6c4b5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c4b5-129">**CMediaControl (clase)**</span><span class="sxs-lookup"><span data-stu-id="6c4b5-129">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 




