---
description: 'Constructor CMediaType.CMediaType (Mtype.h): método constructor.'
ms.assetid: 35198320-d028-42d4-823f-4f8346d8f977
title: 'Constructor CMediaType.CMediaType (Mtype.h): parámetros cmtype y phr'
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
ms.openlocfilehash: dd91252920c74d45e4218be3c3d03249a116bfcf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095423"
---
# <a name="cmediatypecmediatype-constructor-mtypeh"></a><span data-ttu-id="935bf-103">Constructor CMediaType.CMediaType (Mtype.h)</span><span class="sxs-lookup"><span data-stu-id="935bf-103">CMediaType.CMediaType constructor (Mtype.h)</span></span>

<span data-ttu-id="935bf-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="935bf-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="935bf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="935bf-105">Syntax</span></span>


```C++
CMediaType(
  [ref] const CMediaType &cmtype,
              HRESULT    *phr = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="935bf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="935bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="935bf-107">*cmtype* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="935bf-107">*cmtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="935bf-108">Referencia a un `CMediaType` objeto .</span><span class="sxs-lookup"><span data-stu-id="935bf-108">Reference to a `CMediaType` object.</span></span> <span data-ttu-id="935bf-109">El constructor copia el tipo de medio en el nuevo objeto, incluido el bloque de formato, si lo hubiera.</span><span class="sxs-lookup"><span data-stu-id="935bf-109">The constructor copies the media type to the new object, including the format block, if any.</span></span>

</dd> <dt>

<span data-ttu-id="935bf-110">*Phr*</span><span class="sxs-lookup"><span data-stu-id="935bf-110">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="935bf-111">Puntero a una variable que recibe un valor HRESULT.</span><span class="sxs-lookup"><span data-stu-id="935bf-111">Pointer to a variable that receives an HRESULT value.</span></span> <span data-ttu-id="935bf-112">Este parámetro puede ser un **puntero NULL.**</span><span class="sxs-lookup"><span data-stu-id="935bf-112">This parameter can be a **NULL** pointer.</span></span> <span data-ttu-id="935bf-113">De lo contrario, el autor de la llamada debe establecer el valor en S \_ OK antes de llamar al constructor.</span><span class="sxs-lookup"><span data-stu-id="935bf-113">Otherwise, the caller must set the value to S\_OK before calling the constructor.</span></span> <span data-ttu-id="935bf-114">Si se produce un error en el constructor, establece el valor en un código de error.</span><span class="sxs-lookup"><span data-stu-id="935bf-114">If the constructor fails, it sets the value to a failure code.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="935bf-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="935bf-115">Remarks</span></span>

<span data-ttu-id="935bf-116">El constructor llama al [**método CMediaType::InitMediaType**](cmediatype-initmediatype.md) para inicializar el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="935bf-116">The constructor calls the [**CMediaType::InitMediaType**](cmediatype-initmediatype.md) method to initialize the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="935bf-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="935bf-117">Requirements</span></span>



| <span data-ttu-id="935bf-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="935bf-118">Requirement</span></span> | <span data-ttu-id="935bf-119">Value</span><span class="sxs-lookup"><span data-stu-id="935bf-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="935bf-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="935bf-120">Header</span></span><br/>  | <dl> <span data-ttu-id="935bf-121"><dt>Mtype.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="935bf-121"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="935bf-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="935bf-122">Library</span></span><br/> | <dl> <span data-ttu-id="935bf-123"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="935bf-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="935bf-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="935bf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="935bf-125">**CMediaType (clase)**</span><span class="sxs-lookup"><span data-stu-id="935bf-125">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




