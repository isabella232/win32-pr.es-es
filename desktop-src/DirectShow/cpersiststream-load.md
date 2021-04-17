---
description: Carga los datos del filtro desde una secuencia determinada.
ms.assetid: c2bfd379-2916-4698-bc41-653161723706
title: Método CPersistStream. Load (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.Load
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 83b16c3fe7bf905d1ade6b7f38cf27c61b44e4d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670998"
---
# <a name="cpersiststreamload-method"></a><span data-ttu-id="31da9-103">CPersistStream. Load (método)</span><span class="sxs-lookup"><span data-stu-id="31da9-103">CPersistStream.Load method</span></span>

<span data-ttu-id="31da9-104">Carga los datos del filtro desde una secuencia determinada.</span><span class="sxs-lookup"><span data-stu-id="31da9-104">Loads the filter's data from a given stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="31da9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="31da9-105">Syntax</span></span>


```C++
HRESULT Load(
   LPSTREAM pStm
);
```



## <a name="parameters"></a><span data-ttu-id="31da9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="31da9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31da9-107">*pStm*</span><span class="sxs-lookup"><span data-stu-id="31da9-107">*pStm*</span></span> 
</dt> <dd>

<span data-ttu-id="31da9-108">Puntero a la secuencia de la que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="31da9-108">Pointer to the stream from which to be loaded.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31da9-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="31da9-109">Return value</span></span>

<span data-ttu-id="31da9-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="31da9-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="31da9-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="31da9-111">Remarks</span></span>

<span data-ttu-id="31da9-112">Esta función miembro implementa el método **IPersistStream:: Load** .</span><span class="sxs-lookup"><span data-stu-id="31da9-112">This member function implements the **IPersistStream::Load** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="31da9-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31da9-113">Requirements</span></span>



| <span data-ttu-id="31da9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="31da9-114">Requirement</span></span> | <span data-ttu-id="31da9-115">Value</span><span class="sxs-lookup"><span data-stu-id="31da9-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31da9-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="31da9-116">Header</span></span><br/>  | <dl> <span data-ttu-id="31da9-117"><dt>PStream. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="31da9-117"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="31da9-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="31da9-118">Library</span></span><br/> | <dl> <span data-ttu-id="31da9-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="31da9-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31da9-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="31da9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31da9-121">**Clase CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="31da9-121">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




