---
title: Point2 (función de tipo) (D2d1helper. h)
description: Crea un punto que almacena sus coordenadas con el tipo de datos especificado.
ms.assetid: 59a631ae-d70e-4ee2-9546-2d19da40aa9b
keywords:
- Point2 (función de tipo Direct2D)
topic_type:
- apiref
api_name:
- Point2 Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f614f49077ed198c5e85d17b9ee3c84a5e300670
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658244"
---
# <a name="point2type-function"></a><span data-ttu-id="5d213-104">Point2 ( <Type> función)</span><span class="sxs-lookup"><span data-stu-id="5d213-104">Point2<Type> Function</span></span>

<span data-ttu-id="5d213-105">Crea un punto que almacena sus coordenadas con el tipo de datos especificado.</span><span class="sxs-lookup"><span data-stu-id="5d213-105">Creates a point that stores its coordinates using the specified data type.</span></span>

``` syntax
template<typename Type>
typename TypeTraits<Type>::Point Point2(
  Type x,
  Type y
);
```

## <a name="template-parameters"></a><span data-ttu-id="5d213-106">Parámetros de plantilla</span><span class="sxs-lookup"><span data-stu-id="5d213-106">Template Parameters</span></span>



| <span data-ttu-id="5d213-107">Parámetro</span><span class="sxs-lookup"><span data-stu-id="5d213-107">Parameter</span></span> | <span data-ttu-id="5d213-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="5d213-108">Description</span></span>                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d213-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="5d213-109">Type</span></span>      | <span data-ttu-id="5d213-110">El tipo de datos utilizado para almacenar la coordenada x y la coordenada y del punto.</span><span class="sxs-lookup"><span data-stu-id="5d213-110">The data type used to store the x-coordinate and y-coordinate of the point.</span></span> <span data-ttu-id="5d213-111">Los valores posibles son FLOAT y UINT32.</span><span class="sxs-lookup"><span data-stu-id="5d213-111">Possible values are FLOAT and UINT32.</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="5d213-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5d213-112">Parameters</span></span>



| <span data-ttu-id="5d213-113">Parámetro</span><span class="sxs-lookup"><span data-stu-id="5d213-113">Parameter</span></span> | <span data-ttu-id="5d213-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="5d213-114">Description</span></span>                    |
|-----------|--------------------------------|
| <span data-ttu-id="5d213-115">x</span><span class="sxs-lookup"><span data-stu-id="5d213-115">x</span></span>         | <span data-ttu-id="5d213-116">La coordenada x del punto.</span><span class="sxs-lookup"><span data-stu-id="5d213-116">The x-coordinate of the point.</span></span> |
| <span data-ttu-id="5d213-117">y</span><span class="sxs-lookup"><span data-stu-id="5d213-117">y</span></span>         | <span data-ttu-id="5d213-118">La coordenada y del punto.</span><span class="sxs-lookup"><span data-stu-id="5d213-118">The y-coordinate of the point.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="5d213-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5d213-119">Return Value</span></span>

<span data-ttu-id="5d213-120">Un punto que contiene la coordenada x y la coordenada y especificadas.</span><span class="sxs-lookup"><span data-stu-id="5d213-120">A point that contains the specified x-coordinate and y-coordinate.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d213-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d213-121">Requirements</span></span>



| <span data-ttu-id="5d213-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d213-122">Requirement</span></span> | <span data-ttu-id="5d213-123">Value</span><span class="sxs-lookup"><span data-stu-id="5d213-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d213-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d213-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5d213-125">Windows 7, Windows Vista con SP2 y actualización de plataforma para aplicaciones de UWP de aplicaciones de escritorio de Windows Vista \[ \|\]</span><span class="sxs-lookup"><span data-stu-id="5d213-125">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="5d213-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d213-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5d213-127">Windows Server 2008 R2, Windows Server 2008 con SP2 y la actualización de la plataforma de aplicaciones de escritorio de Windows Server 2008 \[ \| aplicaciones para UWP\]</span><span class="sxs-lookup"><span data-stu-id="5d213-127">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="5d213-128">Teléfono mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d213-128">Minimum supported phone</span></span><br/>  | <span data-ttu-id="5d213-129">Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]</span><span class="sxs-lookup"><span data-stu-id="5d213-129">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="5d213-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5d213-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d213-131"><dt>D2d1helper. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d213-131"><dt>D2d1helper.h</dt></span></span> </dl>                                                  |
| <span data-ttu-id="5d213-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5d213-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="5d213-133"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d213-133"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="5d213-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5d213-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d213-135"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d213-135"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



 

 





