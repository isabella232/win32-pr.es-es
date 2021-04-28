---
description: 'Método CRendererPosPassThru.GetMediaTime: el método GetMediaTime recupera las marcas de tiempo del ejemplo actual.'
ms.assetid: 13710373-04fd-4c1d-ba97-78be5cf27e7d
title: Método CRendererPosPassThru.GetMediaTime (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 588c92faec6b68cfa51392d4df00567c4e881460
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085373"
---
# <a name="crendererpospassthrugetmediatime-method"></a><span data-ttu-id="0c8ef-103">Método CRendererPosPassThru.GetMediaTime</span><span class="sxs-lookup"><span data-stu-id="0c8ef-103">CRendererPosPassThru.GetMediaTime method</span></span>

<span data-ttu-id="0c8ef-104">El `GetMediaTime` método recupera las marcas de tiempo en el ejemplo actual.</span><span class="sxs-lookup"><span data-stu-id="0c8ef-104">The `GetMediaTime` method retrieves the time stamps on the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c8ef-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0c8ef-105">Syntax</span></span>


```C++
HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="0c8ef-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0c8ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c8ef-107">*pStartTime*</span><span class="sxs-lookup"><span data-stu-id="0c8ef-107">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="0c8ef-108">Puntero a una variable que recibe la hora de inicio, en unidades del formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="0c8ef-108">Pointer to a variable that receives the start time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="0c8ef-109">*pEndTime*</span><span class="sxs-lookup"><span data-stu-id="0c8ef-109">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="0c8ef-110">Puntero a una variable que recibe la hora de finalización, en unidades del formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="0c8ef-110">Pointer to a variable that receives the end time, in units of the current time format.</span></span> <span data-ttu-id="0c8ef-111">Puede ser **NULL.**</span><span class="sxs-lookup"><span data-stu-id="0c8ef-111">Can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c8ef-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0c8ef-112">Return value</span></span>

<span data-ttu-id="0c8ef-113">Devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="0c8ef-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0c8ef-114">Los valores posibles incluyen los enumerados en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="0c8ef-114">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="0c8ef-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0c8ef-115">Return code</span></span>                                                                                  | <span data-ttu-id="0c8ef-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c8ef-116">Description</span></span>                                            |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="0c8ef-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0c8ef-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="0c8ef-118">Correcto.</span><span class="sxs-lookup"><span data-stu-id="0c8ef-118">Success.</span></span><br/>                                    |
| <dl> <span data-ttu-id="0c8ef-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0c8ef-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="0c8ef-120">No se admite la conversión a este formato.</span><span class="sxs-lookup"><span data-stu-id="0c8ef-120">Conversion to this format is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="0c8ef-121"><dt>**PUNTERO \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="0c8ef-121"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="0c8ef-122">**Argumento de** puntero NULL.</span><span class="sxs-lookup"><span data-stu-id="0c8ef-122">**NULL** pointer argument.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="0c8ef-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0c8ef-123">Remarks</span></span>

<span data-ttu-id="0c8ef-124">Este método invalida el [**método CPosPassThru::GetMediaTime.**](cpospassthru-getmediatime.md)</span><span class="sxs-lookup"><span data-stu-id="0c8ef-124">This method overrides the [**CPosPassThru::GetMediaTime**](cpospassthru-getmediatime.md) method.</span></span> <span data-ttu-id="0c8ef-125">Los valores de marca de tiempo se convierten al formato de hora actual llamando al método [**CPosPassThru::ConvertTimeFormat.**](cpospassthru-converttimeformat.md)</span><span class="sxs-lookup"><span data-stu-id="0c8ef-125">The time-stamp values are converted to the current time format by calling the [**CPosPassThru::ConvertTimeFormat**](cpospassthru-converttimeformat.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c8ef-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c8ef-126">Requirements</span></span>



| <span data-ttu-id="0c8ef-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c8ef-127">Requirement</span></span> | <span data-ttu-id="0c8ef-128">Value</span><span class="sxs-lookup"><span data-stu-id="0c8ef-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c8ef-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0c8ef-129">Header</span></span><br/>  | <dl> <span data-ttu-id="0c8ef-130"><dt>Ctlutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="0c8ef-130"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0c8ef-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0c8ef-131">Library</span></span><br/> | <dl> <span data-ttu-id="0c8ef-132"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0c8ef-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




