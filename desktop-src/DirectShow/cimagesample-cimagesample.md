---
description: Método de constructor.
ms.assetid: d7550c38-d728-41b2-80a6-20728abf6012
title: Constructor CImageSample. CImageSample (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.CImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 805be59cfc899b6461fa8c761eebb5821118640f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670490"
---
# <a name="cimagesamplecimagesample-constructor"></a><span data-ttu-id="47369-103">Constructor CImageSample. CImageSample</span><span class="sxs-lookup"><span data-stu-id="47369-103">CImageSample.CImageSample constructor</span></span>

<span data-ttu-id="47369-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="47369-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="47369-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="47369-105">Syntax</span></span>


```C++
CImageSample(
   CBaseAllocator *pAllocator,
   TCHAR          *pName,
   HRESULT        *phr,
   LPBYTE         pBuffer,
   LONG           length
);
```



## <a name="parameters"></a><span data-ttu-id="47369-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47369-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47369-107">*pAllocator*</span><span class="sxs-lookup"><span data-stu-id="47369-107">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="47369-108">Puntero al asignador que creó este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="47369-108">Pointer to the allocator that created this sample.</span></span>

</dd> <dt>

<span data-ttu-id="47369-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="47369-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="47369-110">ignorado.</span><span class="sxs-lookup"><span data-stu-id="47369-110">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="47369-111">*phr*</span><span class="sxs-lookup"><span data-stu-id="47369-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="47369-112">ignorado.</span><span class="sxs-lookup"><span data-stu-id="47369-112">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="47369-113">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="47369-113">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="47369-114">Puntero a un búfer de memoria asignado por el autor de la llamada, de *longitud* de tamaño.</span><span class="sxs-lookup"><span data-stu-id="47369-114">Pointer to a memory buffer allocated by the caller, of size *length*.</span></span> <span data-ttu-id="47369-115">El búfer debe contener un mapa de bits independiente del dispositivo GDI (DIB).</span><span class="sxs-lookup"><span data-stu-id="47369-115">The buffer should contain a GDI device-independent bitmap (DIB).</span></span>

</dd> <dt>

<span data-ttu-id="47369-116">*length*</span><span class="sxs-lookup"><span data-stu-id="47369-116">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="47369-117">Longitud del búfer.</span><span class="sxs-lookup"><span data-stu-id="47369-117">Length of the buffer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="47369-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="47369-118">Remarks</span></span>

<span data-ttu-id="47369-119">La clase [**CImageAllocator**](cimageallocator.md) crea un archivo DIB mediante un objeto de asignación de archivos respaldado por el archivo de paginación del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="47369-119">The [**CImageAllocator**](cimageallocator.md) class creates a DIB using a file-mapping object that is backed by the operating-system paging file.</span></span> <span data-ttu-id="47369-120">El identificador del objeto de asignación de archivos se almacena en el miembro **hMapping** de la estructura **m \_ DibData** .</span><span class="sxs-lookup"><span data-stu-id="47369-120">The handle to the file-mapping object is stored in the **hMapping** member of the **m\_DibData** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="47369-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47369-121">Requirements</span></span>



| <span data-ttu-id="47369-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="47369-122">Requirement</span></span> | <span data-ttu-id="47369-123">Value</span><span class="sxs-lookup"><span data-stu-id="47369-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47369-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="47369-124">Header</span></span><br/>  | <dl> <span data-ttu-id="47369-125"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="47369-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="47369-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="47369-126">Library</span></span><br/> | <dl> <span data-ttu-id="47369-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="47369-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47369-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="47369-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47369-129">**Clase CImageSample**</span><span class="sxs-lookup"><span data-stu-id="47369-129">**CImageSample Class**</span></span>](cimagesample.md)
</dt> </dl>

 

 




