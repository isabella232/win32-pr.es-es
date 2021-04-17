---
description: El método IsValid determina si se ha asignado un tipo principal a este objeto.
ms.assetid: 22d28019-f360-4b93-972c-d1dfe83938f0
title: Método CMediaType. IsValid (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.IsValid
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d8e1731060021b61eb5037e1baeeda95021e8f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680696"
---
# <a name="cmediatypeisvalid-method"></a><span data-ttu-id="b5c63-103">Método CMediaType. IsValid</span><span class="sxs-lookup"><span data-stu-id="b5c63-103">CMediaType.IsValid method</span></span>

<span data-ttu-id="b5c63-104">El `IsValid` método determina si se ha asignado un tipo principal a este objeto.</span><span class="sxs-lookup"><span data-stu-id="b5c63-104">The `IsValid` method determines whether a major type has been assigned to this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5c63-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b5c63-105">Syntax</span></span>


```C++
BOOL IsValid() const;
```



## <a name="parameters"></a><span data-ttu-id="b5c63-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5c63-106">Parameters</span></span>

<span data-ttu-id="b5c63-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="b5c63-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b5c63-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b5c63-108">Return value</span></span>

<span data-ttu-id="b5c63-109">Devuelve **true** si se ha asignado un tipo principal a este objeto.</span><span class="sxs-lookup"><span data-stu-id="b5c63-109">Returns **TRUE** if a major type has been assigned to this object.</span></span> <span data-ttu-id="b5c63-110">De lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="b5c63-110">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5c63-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b5c63-111">Remarks</span></span>

<span data-ttu-id="b5c63-112">De forma predeterminada, los objetos [**CMediaType**](cmediatype.md) se inicializan con un tipo principal de GUID \_ null.</span><span class="sxs-lookup"><span data-stu-id="b5c63-112">By default, [**CMediaType**](cmediatype.md) objects are initialized with a major type of GUID\_NULL.</span></span> <span data-ttu-id="b5c63-113">Llame a este método para determinar si el objeto se ha inicializado correctamente.</span><span class="sxs-lookup"><span data-stu-id="b5c63-113">Call this method to determine whether the object has been correctly initialized.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5c63-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5c63-114">Requirements</span></span>



| <span data-ttu-id="b5c63-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5c63-115">Requirement</span></span> | <span data-ttu-id="b5c63-116">Value</span><span class="sxs-lookup"><span data-stu-id="b5c63-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5c63-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b5c63-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b5c63-118"><dt>Mtype. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b5c63-118"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="b5c63-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b5c63-119">Library</span></span><br/> | <dl> <span data-ttu-id="b5c63-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b5c63-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5c63-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5c63-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5c63-122">**Clase CMediaType**</span><span class="sxs-lookup"><span data-stu-id="b5c63-122">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




