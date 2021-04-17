---
description: Método de constructor.
ms.assetid: 35198320-d028-42d4-823f-4f8346d8f977
title: Constructor CMediaType. CMediaType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 776d59550d09396cc248937be611f2b4ec3699df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689938"
---
# <a name="cmediatypecmediatype-constructor-mtypeh"></a><span data-ttu-id="3470e-103">Constructor CMediaType. CMediaType (mtype. h)</span><span class="sxs-lookup"><span data-stu-id="3470e-103">CMediaType.CMediaType constructor (Mtype.h)</span></span>

<span data-ttu-id="3470e-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="3470e-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3470e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3470e-105">Syntax</span></span>


```C++
CMediaType(
  [ref] const CMediaType &cmtype,
              HRESULT    *phr = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="3470e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3470e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3470e-107">*cmtype* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="3470e-107">*cmtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="3470e-108">Referencia a un `CMediaType` objeto.</span><span class="sxs-lookup"><span data-stu-id="3470e-108">Reference to a `CMediaType` object.</span></span> <span data-ttu-id="3470e-109">El constructor copia el tipo de archivo multimedia en el nuevo objeto, incluido el bloque de formato, si existe.</span><span class="sxs-lookup"><span data-stu-id="3470e-109">The constructor copies the media type to the new object, including the format block, if any.</span></span>

</dd> <dt>

<span data-ttu-id="3470e-110">*phr*</span><span class="sxs-lookup"><span data-stu-id="3470e-110">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="3470e-111">Puntero a una variable que recibe un valor HRESULT.</span><span class="sxs-lookup"><span data-stu-id="3470e-111">Pointer to a variable that receives an HRESULT value.</span></span> <span data-ttu-id="3470e-112">Este parámetro puede ser un puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="3470e-112">This parameter can be a **NULL** pointer.</span></span> <span data-ttu-id="3470e-113">De lo contrario, el autor de la llamada debe establecer el valor en es \_ correcto antes de llamar al constructor.</span><span class="sxs-lookup"><span data-stu-id="3470e-113">Otherwise, the caller must set the value to S\_OK before calling the constructor.</span></span> <span data-ttu-id="3470e-114">Si se produce un error en el constructor, establece el valor en un código de error.</span><span class="sxs-lookup"><span data-stu-id="3470e-114">If the constructor fails, it sets the value to a failure code.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3470e-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3470e-115">Remarks</span></span>

<span data-ttu-id="3470e-116">El constructor llama al método [**CMediaType:: InitMediaType**](cmediatype-initmediatype.md) para inicializar el tipo de archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="3470e-116">The constructor calls the [**CMediaType::InitMediaType**](cmediatype-initmediatype.md) method to initialize the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="3470e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3470e-117">Requirements</span></span>



| <span data-ttu-id="3470e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3470e-118">Requirement</span></span> | <span data-ttu-id="3470e-119">Value</span><span class="sxs-lookup"><span data-stu-id="3470e-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3470e-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3470e-120">Header</span></span><br/>  | <dl> <span data-ttu-id="3470e-121"><dt>Mtype. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3470e-121"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="3470e-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3470e-122">Library</span></span><br/> | <dl> <span data-ttu-id="3470e-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="3470e-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3470e-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="3470e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3470e-125">**Clase CMediaType**</span><span class="sxs-lookup"><span data-stu-id="3470e-125">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




