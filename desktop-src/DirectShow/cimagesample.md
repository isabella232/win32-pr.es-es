---
description: La clase CImageSample implementa un ejemplo multimedia que administra un mapa de bits independiente del dispositivo GDI (DIB).
ms.assetid: 620ea791-458e-441e-8f0c-2184c44c742e
title: Clase CImageSample (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2235d50c952ce1b76e4a70eda0341f0fe3c4167c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679031"
---
# <a name="cimagesample-class"></a><span data-ttu-id="f7ac6-103">Clase CImageSample</span><span class="sxs-lookup"><span data-stu-id="f7ac6-103">CImageSample class</span></span>

![jerarquía de clases cimagesample](images/wutil03.png)

<span data-ttu-id="f7ac6-105">La `CImageSample` clase implementa un ejemplo multimedia que administra un mapa de bits independiente del dispositivo GDI (DIB).</span><span class="sxs-lookup"><span data-stu-id="f7ac6-105">The `CImageSample` class implements a media sample that manages a GDI device-independent bitmap (DIB).</span></span> <span data-ttu-id="f7ac6-106">Esta clase se deriva de la clase [**CMediaSample**](cmediasample.md) .</span><span class="sxs-lookup"><span data-stu-id="f7ac6-106">This class derives from the [**CMediaSample**](cmediasample.md) class.</span></span> <span data-ttu-id="f7ac6-107">Está diseñado para usarse con la clase [**CImageAllocator**](cimageallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="f7ac6-107">It is intended to be used with the [**CImageAllocator**](cimageallocator.md) class.</span></span> <span data-ttu-id="f7ac6-108">La clase **CImageAllocator** proporciona un asignador que crea `CImageSample` objetos.</span><span class="sxs-lookup"><span data-stu-id="f7ac6-108">The **CImageAllocator** class provides an allocator that creates `CImageSample` objects.</span></span>



| <span data-ttu-id="f7ac6-109">Variables de miembro protegidas</span><span class="sxs-lookup"><span data-stu-id="f7ac6-109">Protected Member Variables</span></span>                        | <span data-ttu-id="f7ac6-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f7ac6-110">Description</span></span>                                                       |
|---------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="f7ac6-111">**m \_ DibData**</span><span class="sxs-lookup"><span data-stu-id="f7ac6-111">**m\_DibData**</span></span>](cimagesample-m-dibdata.md)      | <span data-ttu-id="f7ac6-112">Contiene información sobre el DIB que está administrando este objeto.</span><span class="sxs-lookup"><span data-stu-id="f7ac6-112">Contains information about the DIB that this object is managing.</span></span>  |
| [<span data-ttu-id="f7ac6-113">**m \_ bInit**</span><span class="sxs-lookup"><span data-stu-id="f7ac6-113">**m\_bInit**</span></span>](cimagesample-m-binit.md)          | <span data-ttu-id="f7ac6-114">Indica si el objeto se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="f7ac6-114">Indicates whether the object has been initialized.</span></span>                |
| <span data-ttu-id="f7ac6-115">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="f7ac6-115">Public Methods</span></span>                                    | <span data-ttu-id="f7ac6-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="f7ac6-116">Description</span></span>                                                       |
| [<span data-ttu-id="f7ac6-117">**CImageSample**</span><span class="sxs-lookup"><span data-stu-id="f7ac6-117">**CImageSample**</span></span>](cimagesample-cimagesample.md) | <span data-ttu-id="f7ac6-118">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="f7ac6-118">Constructor method.</span></span>                                               |
| [<span data-ttu-id="f7ac6-119">**GetDIBData**</span><span class="sxs-lookup"><span data-stu-id="f7ac6-119">**GetDIBData**</span></span>](cimagesample-getdibdata.md)     | <span data-ttu-id="f7ac6-120">Recupera información sobre el DIB que está administrando este objeto.</span><span class="sxs-lookup"><span data-stu-id="f7ac6-120">Retrieves information about the DIB that this object is managing.</span></span> |
| [<span data-ttu-id="f7ac6-121">**SetDIBData**</span><span class="sxs-lookup"><span data-stu-id="f7ac6-121">**SetDIBData**</span></span>](cimagesample-setdibdata.md)     | <span data-ttu-id="f7ac6-122">Establece información sobre el DIB que está administrando este objeto.</span><span class="sxs-lookup"><span data-stu-id="f7ac6-122">Sets information about the DIB that this object is managing.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="f7ac6-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7ac6-123">Requirements</span></span>



| <span data-ttu-id="f7ac6-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7ac6-124">Requirement</span></span> | <span data-ttu-id="f7ac6-125">Value</span><span class="sxs-lookup"><span data-stu-id="f7ac6-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7ac6-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f7ac6-126">Header</span></span><br/>  | <dl> <span data-ttu-id="f7ac6-127"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f7ac6-127"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f7ac6-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f7ac6-128">Library</span></span><br/> | <dl> <span data-ttu-id="f7ac6-129"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="f7ac6-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




