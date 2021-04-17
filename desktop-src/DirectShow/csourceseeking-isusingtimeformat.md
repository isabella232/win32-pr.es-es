---
description: El método IsUsingTimeFormat determina si un formato de hora especificado es el formato que se está usando actualmente.
ms.assetid: 86965bfc-fc9f-42d3-bcaa-2049195b98bd
title: Método CSourceSeeking. IsUsingTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.IsUsingTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8229387364a061febc7bd825e7bc76ee5d9b4a2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660776"
---
# <a name="csourceseekingisusingtimeformat-method"></a><span data-ttu-id="b4598-103">CSourceSeeking. IsUsingTimeFormat, método</span><span class="sxs-lookup"><span data-stu-id="b4598-103">CSourceSeeking.IsUsingTimeFormat method</span></span>

<span data-ttu-id="b4598-104">El `IsUsingTimeFormat` método determina si un formato de hora especificado es el formato que se está usando actualmente.</span><span class="sxs-lookup"><span data-stu-id="b4598-104">The `IsUsingTimeFormat` method determines whether a specified time format is the format currently in use.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4598-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b4598-105">Syntax</span></span>


```C++
HRESULT IsUsingTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="b4598-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b4598-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4598-107">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="b4598-107">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="b4598-108">Puntero a un GUID de formato de hora.</span><span class="sxs-lookup"><span data-stu-id="b4598-108">Pointer to a time format GUID.</span></span> <span data-ttu-id="b4598-109">Consulte [**GUID de formato de hora**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="b4598-109">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4598-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b4598-110">Return value</span></span>

<span data-ttu-id="b4598-111">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="b4598-111">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="b4598-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b4598-112">Return code</span></span>                                                                               | <span data-ttu-id="b4598-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4598-113">Description</span></span>                                                |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="b4598-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="b4598-114"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="b4598-115">El formato especificado no es el formato actual.</span><span class="sxs-lookup"><span data-stu-id="b4598-115">The specified format is not the current format.</span></span><br/> |
| <dl> <span data-ttu-id="b4598-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="b4598-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="b4598-117">El formato especificado es el formato actual.</span><span class="sxs-lookup"><span data-stu-id="b4598-117">The specified format is the current format.</span></span><br/>     |
| <dl> <span data-ttu-id="b4598-118"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="b4598-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="b4598-119">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="b4598-119">**NULL** pointer argument.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="b4598-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b4598-120">Remarks</span></span>

<span data-ttu-id="b4598-121">El único formato de hora admitido por la clase base es el \_ formato \_ de hora \_ tiempo medio (100-nanosegundos).</span><span class="sxs-lookup"><span data-stu-id="b4598-121">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="b4598-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4598-122">Requirements</span></span>



| <span data-ttu-id="b4598-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4598-123">Requirement</span></span> | <span data-ttu-id="b4598-124">Value</span><span class="sxs-lookup"><span data-stu-id="b4598-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4598-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b4598-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b4598-126"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b4598-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b4598-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b4598-127">Library</span></span><br/> | <dl> <span data-ttu-id="b4598-128"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b4598-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4598-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4598-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4598-130">**Clase CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="b4598-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




