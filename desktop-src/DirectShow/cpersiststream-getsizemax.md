---
description: Recupera el tamaño máximo de bytes necesario para la secuencia actual, incluido el número de versión.
ms.assetid: 55ea4568-5ca4-4139-8def-bef20071835d
title: Método CPersistStream. GetSizeMax (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetSizeMax
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4ef9fcd176463aa8b0bc69fabbd74d78d4ca17cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671001"
---
# <a name="cpersiststreamgetsizemax-method"></a><span data-ttu-id="a5c54-103">CPersistStream. GetSizeMax, método</span><span class="sxs-lookup"><span data-stu-id="a5c54-103">CPersistStream.GetSizeMax method</span></span>

<span data-ttu-id="a5c54-104">Recupera el tamaño máximo de bytes necesario para la secuencia actual, incluido el número de versión.</span><span class="sxs-lookup"><span data-stu-id="a5c54-104">Retrieves the maximum byte size needed for the current stream, including the version number.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5c54-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a5c54-105">Syntax</span></span>


```C++
HRESULT GetSizeMax(
   ULARGE_INTEGER *pcbSize
);
```



## <a name="parameters"></a><span data-ttu-id="a5c54-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a5c54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5c54-107">*PCB*</span><span class="sxs-lookup"><span data-stu-id="a5c54-107">*pcbSize*</span></span> 
</dt> <dd>

<span data-ttu-id="a5c54-108">Puntero al tamaño en bytes necesario para guardar este flujo, incluido el número de versión.</span><span class="sxs-lookup"><span data-stu-id="a5c54-108">Pointer to the size in bytes needed to save this stream, including the version number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5c54-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a5c54-109">Return value</span></span>

<span data-ttu-id="a5c54-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a5c54-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5c54-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a5c54-111">Remarks</span></span>

<span data-ttu-id="a5c54-112">Esta función miembro implementa el método **IPersistStream:: GetSizeMax** .</span><span class="sxs-lookup"><span data-stu-id="a5c54-112">This member function implements the **IPersistStream::GetSizeMax** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5c54-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5c54-113">Requirements</span></span>



| <span data-ttu-id="a5c54-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5c54-114">Requirement</span></span> | <span data-ttu-id="a5c54-115">Value</span><span class="sxs-lookup"><span data-stu-id="a5c54-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5c54-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a5c54-116">Header</span></span><br/>  | <dl> <span data-ttu-id="a5c54-117"><dt>PStream. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a5c54-117"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a5c54-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a5c54-118">Library</span></span><br/> | <dl> <span data-ttu-id="a5c54-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a5c54-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5c54-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="a5c54-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5c54-121">**Clase CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="a5c54-121">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




