---
description: El método MatchesPartial determina si este tipo de medio coincide con un tipo de medio especificado parcialmente.
ms.assetid: 62d531f3-5aa2-4af2-b951-584a49a849fc
title: Método CMediaType. MatchesPartial (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.MatchesPartial
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f4d2d4232b64857ca209e6b43cd7081a42495fee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671311"
---
# <a name="cmediatypematchespartial-method"></a><span data-ttu-id="04055-103">CMediaType. MatchesPartial, método</span><span class="sxs-lookup"><span data-stu-id="04055-103">CMediaType.MatchesPartial method</span></span>

<span data-ttu-id="04055-104">El `MatchesPartial` método determina si este tipo de medio coincide con un tipo de medio especificado parcialmente.</span><span class="sxs-lookup"><span data-stu-id="04055-104">The `MatchesPartial` method determines if this media type matches a partially specified media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="04055-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="04055-105">Syntax</span></span>


```C++
BOOL MatchesPartial(
   const CMediaType *ppartial
) const;
```



## <a name="parameters"></a><span data-ttu-id="04055-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="04055-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04055-107">*ppartial*</span><span class="sxs-lookup"><span data-stu-id="04055-107">*ppartial*</span></span> 
</dt> <dd>

<span data-ttu-id="04055-108">Puntero al tipo de medio que debe coincidir.</span><span class="sxs-lookup"><span data-stu-id="04055-108">Pointer to the media type to match.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04055-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="04055-109">Return value</span></span>

<span data-ttu-id="04055-110">Devuelve **true** si los tipos de medios coinciden.</span><span class="sxs-lookup"><span data-stu-id="04055-110">Returns **TRUE** if the media types match.</span></span> <span data-ttu-id="04055-111">De lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="04055-111">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="04055-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="04055-112">Remarks</span></span>

<span data-ttu-id="04055-113">El tipo de medio especificado por *ppartial* puede tener un valor de GUID \_ null para el tipo principal, el subtipo o el tipo de formato.</span><span class="sxs-lookup"><span data-stu-id="04055-113">The media type specified by *ppartial* can have a value of GUID\_NULL for the major type, subtype, or format type.</span></span> <span data-ttu-id="04055-114">\_No se prueba ningún miembro con valores NULL de GUID.</span><span class="sxs-lookup"><span data-stu-id="04055-114">Any members with GUID\_NULL values are not tested.</span></span> <span data-ttu-id="04055-115">(En efecto, GUID \_ ) NULL actúa como comodín). Los miembros con valores distintos \_ del GUID null deben coincidir para que el tipo de medio coincida.</span><span class="sxs-lookup"><span data-stu-id="04055-115">(In effect, GUID\_NULL acts as a wildcard.) Members with values other than GUID\_NULL must match for the media type to match.</span></span>

## <a name="requirements"></a><span data-ttu-id="04055-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04055-116">Requirements</span></span>



| <span data-ttu-id="04055-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="04055-117">Requirement</span></span> | <span data-ttu-id="04055-118">Value</span><span class="sxs-lookup"><span data-stu-id="04055-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04055-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="04055-119">Header</span></span><br/>  | <dl> <span data-ttu-id="04055-120"><dt>Mtype. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="04055-120"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="04055-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="04055-121">Library</span></span><br/> | <dl> <span data-ttu-id="04055-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="04055-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04055-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="04055-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04055-124">**Clase CMediaType**</span><span class="sxs-lookup"><span data-stu-id="04055-124">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




