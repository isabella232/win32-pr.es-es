---
description: El método ReallocFormatBuffer reasigna el bloque de formato a un nuevo tamaño.
ms.assetid: 49bec677-09cc-4e1a-994a-13e873e61713
title: Método CMediaType. ReallocFormatBuffer (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.ReallocFormatBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22e861c61f01a7594d720833e2b3a4b923a1e183
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670559"
---
# <a name="cmediatypereallocformatbuffer-method"></a><span data-ttu-id="6cf7e-103">CMediaType. ReallocFormatBuffer, método</span><span class="sxs-lookup"><span data-stu-id="6cf7e-103">CMediaType.ReallocFormatBuffer method</span></span>

<span data-ttu-id="6cf7e-104">El `ReallocFormatBuffer` método reasigna el bloque de formato a un nuevo tamaño.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-104">The `ReallocFormatBuffer` method reallocates the format block to a new size.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cf7e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6cf7e-105">Syntax</span></span>


```C++
BYTE* ReallocFormatBuffer(
   ULONG length
);
```



## <a name="parameters"></a><span data-ttu-id="6cf7e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6cf7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cf7e-107">*length*</span><span class="sxs-lookup"><span data-stu-id="6cf7e-107">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="6cf7e-108">Nuevo tamaño necesario para el bloque de formato, en bytes.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-108">New size required for the format block, in bytes.</span></span> <span data-ttu-id="6cf7e-109">Debe ser mayor que cero.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-109">Must be greater than zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cf7e-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6cf7e-110">Return value</span></span>

<span data-ttu-id="6cf7e-111">Devuelve un puntero al nuevo bloque si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-111">Returns a pointer to the new block if successful.</span></span> <span data-ttu-id="6cf7e-112">De lo contrario, devuelve un puntero al bloque de formato antiguo o **null**.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-112">Otherwise, returns either a pointer to the old format block, or **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cf7e-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6cf7e-113">Remarks</span></span>

<span data-ttu-id="6cf7e-114">Este método asigna un nuevo bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-114">This method allocates a new format block.</span></span> <span data-ttu-id="6cf7e-115">Copia tanto como sea posible el bloque de formato existente en el nuevo bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-115">It copies as much of the existing format block as possible into the new format block.</span></span> <span data-ttu-id="6cf7e-116">Si el nuevo bloque es más pequeño que el bloque existente, el bloque de formato existente se trunca.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-116">If the new block is smaller than the existing block, the existing format block is truncated.</span></span> <span data-ttu-id="6cf7e-117">Si el nuevo bloque es mayor, el contenido del espacio adicional no está definido.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-117">If the new block is larger, the contents of the additional space are undefined.</span></span> <span data-ttu-id="6cf7e-118">No se establecen explícitamente en cero.</span><span class="sxs-lookup"><span data-stu-id="6cf7e-118">They are not explicitly set to zero.</span></span>

<span data-ttu-id="6cf7e-119">El método actualiza los miembros **cbFormat** y **pbFormat** de la estructura de **\_ \_ tipo de medio am** .</span><span class="sxs-lookup"><span data-stu-id="6cf7e-119">The method updates the **cbFormat** and **pbFormat** members of the **AM\_MEDIA\_TYPE** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cf7e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6cf7e-120">Requirements</span></span>



| <span data-ttu-id="6cf7e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cf7e-121">Requirement</span></span> | <span data-ttu-id="6cf7e-122">Value</span><span class="sxs-lookup"><span data-stu-id="6cf7e-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cf7e-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6cf7e-123">Header</span></span><br/>  | <dl> <span data-ttu-id="6cf7e-124"><dt>Mtype. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6cf7e-124"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="6cf7e-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6cf7e-125">Library</span></span><br/> | <dl> <span data-ttu-id="6cf7e-126"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="6cf7e-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cf7e-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="6cf7e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cf7e-128">**Clase CMediaType**</span><span class="sxs-lookup"><span data-stu-id="6cf7e-128">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




