---
description: El método IsPartiallySpecified determina si el tipo de medio se define parcialmente. Un tipo de medio es parcial si el tipo principal, el subtipo o el tipo de formato es el GUID \_ null.
ms.assetid: 26dd7a2b-b2f8-485f-a9af-31c3a9eb1def
title: Método CMediaType. IsPartiallySpecified (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.IsPartiallySpecified
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32c39942ab3f97d45ecf71ba841d56b7afd4be62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680697"
---
# <a name="cmediatypeispartiallyspecified-method"></a><span data-ttu-id="d855f-104">CMediaType. IsPartiallySpecified, método</span><span class="sxs-lookup"><span data-stu-id="d855f-104">CMediaType.IsPartiallySpecified method</span></span>

<span data-ttu-id="d855f-105">El `IsPartiallySpecified` método determina si el tipo de medio se define parcialmente.</span><span class="sxs-lookup"><span data-stu-id="d855f-105">The `IsPartiallySpecified` method determines if the media type is partially defined.</span></span> <span data-ttu-id="d855f-106">Un tipo de medio es *parcial* si el tipo principal, el subtipo o el tipo de formato es el GUID \_ null.</span><span class="sxs-lookup"><span data-stu-id="d855f-106">A media type is *partial* if the major type, subtype, or format type is GUID\_NULL.</span></span>

## <a name="syntax"></a><span data-ttu-id="d855f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d855f-107">Syntax</span></span>


```C++
BOOL IsPartiallySpecified() const;
```



## <a name="parameters"></a><span data-ttu-id="d855f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d855f-108">Parameters</span></span>

<span data-ttu-id="d855f-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="d855f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d855f-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d855f-110">Return value</span></span>

<span data-ttu-id="d855f-111">Devuelve **true** si el tipo de medio se especifica parcialmente.</span><span class="sxs-lookup"><span data-stu-id="d855f-111">Returns **TRUE** if the media type is partially specified.</span></span> <span data-ttu-id="d855f-112">De lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="d855f-112">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d855f-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d855f-113">Remarks</span></span>

<span data-ttu-id="d855f-114">El método [**IPin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) puede aceptar tipos de medios parciales.</span><span class="sxs-lookup"><span data-stu-id="d855f-114">The [**IPin::Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) method can accept partial media types.</span></span>

<span data-ttu-id="d855f-115">La implementación no prueba realmente el subtipo.</span><span class="sxs-lookup"><span data-stu-id="d855f-115">The implementation does not actually test the subtype.</span></span> <span data-ttu-id="d855f-116">Si hay un tipo de formato especificado, el tipo de medio no se considera parcial, incluso si el subtipo es GUID \_ null.</span><span class="sxs-lookup"><span data-stu-id="d855f-116">If there is a specified format type, the media type is not considered partial, even if the subtype is GUID\_NULL.</span></span>

## <a name="requirements"></a><span data-ttu-id="d855f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d855f-117">Requirements</span></span>



| <span data-ttu-id="d855f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d855f-118">Requirement</span></span> | <span data-ttu-id="d855f-119">Value</span><span class="sxs-lookup"><span data-stu-id="d855f-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d855f-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d855f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="d855f-121"><dt>Mtype. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d855f-121"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="d855f-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d855f-122">Library</span></span><br/> | <dl> <span data-ttu-id="d855f-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="d855f-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d855f-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d855f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d855f-125">**Clase CMediaType**</span><span class="sxs-lookup"><span data-stu-id="d855f-125">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




