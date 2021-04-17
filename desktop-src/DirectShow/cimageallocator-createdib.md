---
description: El método CreateDIB crea un mapa de bits independiente del dispositivo GDI (DIB). El DIB se asigna en un bloque mempory compartido, que elimina una operación de copia cuando el filtro propietario blits la imagen.
ms.assetid: 8a9ab1cf-4104-48e9-ba6c-28d0f1a1d226
title: Método CImageAllocator. CreateDIB (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CreateDIB
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 316b7aeadfa442a8df4e80075380464758f3c6bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680515"
---
# <a name="cimageallocatorcreatedib-method"></a><span data-ttu-id="4a29b-104">CImageAllocator. CreateDIB, método</span><span class="sxs-lookup"><span data-stu-id="4a29b-104">CImageAllocator.CreateDIB method</span></span>

<span data-ttu-id="4a29b-105">El `CreateDIB` método crea un mapa de bits independiente del dispositivo GDI (DIB).</span><span class="sxs-lookup"><span data-stu-id="4a29b-105">The `CreateDIB` method creates a GDI device-independent bitmap (DIB).</span></span> <span data-ttu-id="4a29b-106">El DIB se asigna en un bloque mempory compartido, que elimina una operación de copia cuando el filtro propietario blits la imagen.</span><span class="sxs-lookup"><span data-stu-id="4a29b-106">The DIB is allocated in a shared mempory block, which eliminates a copy operation when the owning filter blits the image.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a29b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4a29b-107">Syntax</span></span>


```C++
HRESULT CreateDIB(
        LONG    InSize,
  [ref] DIBDATA &DibData
);
```



## <a name="parameters"></a><span data-ttu-id="4a29b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4a29b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a29b-109">*Insize*</span><span class="sxs-lookup"><span data-stu-id="4a29b-109">*InSize*</span></span> 
</dt> <dd>

<span data-ttu-id="4a29b-110">Tamaño del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="4a29b-110">Size of the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="4a29b-111">*DibData* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="4a29b-111">*DibData* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="4a29b-112">Referencia a una estructura [**DIBDATA**](dibdata.md) .</span><span class="sxs-lookup"><span data-stu-id="4a29b-112">Reference to a [**DIBDATA**](dibdata.md) structure.</span></span> <span data-ttu-id="4a29b-113">El método rellena esta estructura con información sobre el DIB.</span><span class="sxs-lookup"><span data-stu-id="4a29b-113">The method fills in this structure with information about the DIB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a29b-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4a29b-114">Return value</span></span>

<span data-ttu-id="4a29b-115">Devuelve \_ si es correcto, o un código de error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="4a29b-115">Returns S\_OK if successful, or an error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a29b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a29b-116">Requirements</span></span>



| <span data-ttu-id="4a29b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a29b-117">Requirement</span></span> | <span data-ttu-id="4a29b-118">Value</span><span class="sxs-lookup"><span data-stu-id="4a29b-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a29b-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4a29b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="4a29b-120"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a29b-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4a29b-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4a29b-121">Library</span></span><br/> | <dl> <span data-ttu-id="4a29b-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="4a29b-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a29b-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a29b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a29b-124">**Clase CImageAllocator**</span><span class="sxs-lookup"><span data-stu-id="4a29b-124">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> <dt>

[<span data-ttu-id="4a29b-125">**CImageAllocator:: Alloc**</span><span class="sxs-lookup"><span data-stu-id="4a29b-125">**CImageAllocator::Alloc**</span></span>](cimageallocator-alloc.md)
</dt> </dl>

 

 




