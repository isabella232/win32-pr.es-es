---
title: D2D1_SIZE_F (D2DBaseTypes. h)
description: Almacena un par ordenado de flotantes, normalmente el ancho y el alto de un rectángulo.
ms.assetid: c2fd41fb-72b3-418b-ad87-65549b04657d
keywords:
- D2D1_SIZE_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a031e1e6a1e9ad7d6975f3dea63427655aa92f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489760"
---
# <a name="d2d1_size_f"></a><span data-ttu-id="bfb29-104">Tamaño de D2D1 \_ \_ F</span><span class="sxs-lookup"><span data-stu-id="bfb29-104">D2D1\_SIZE\_F</span></span>

<span data-ttu-id="bfb29-105">Almacena un par ordenado de flotantes, normalmente el ancho y el alto de un rectángulo.</span><span class="sxs-lookup"><span data-stu-id="bfb29-105">Stores an ordered pair of floats, typically the width and height of a rectangle.</span></span>


```C++
typedef D2D_SIZE_F D2D1_SIZE_F;
```



## <a name="remarks"></a><span data-ttu-id="bfb29-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bfb29-106">Remarks</span></span>

<span data-ttu-id="bfb29-107">Al igual que los puntos, los tamaños son otro concepto de gráficos importante.</span><span class="sxs-lookup"><span data-stu-id="bfb29-107">Like points, sizes are another important graphics concept.</span></span> <span data-ttu-id="bfb29-108">En Direct2D, los tamaños se representan mediante las estructuras **D2D1 \_ size \_ F** o [**D2D1 \_ size \_ U**](d2d1-size-u.md) .</span><span class="sxs-lookup"><span data-stu-id="bfb29-108">In Direct2D, sizes are represented by the **D2D1\_SIZE\_F** or [**D2D1\_SIZE\_U**](d2d1-size-u.md) structures.</span></span> <span data-ttu-id="bfb29-109">Ambos contienen un par ordenado de números, normalmente el ancho y el alto de un rectángulo.</span><span class="sxs-lookup"><span data-stu-id="bfb29-109">Both contain an ordered pair of numbers, typically the width and height of a rectangle.</span></span> <span data-ttu-id="bfb29-110">La **estructura \_ \_ F de tamaño D2D1** contiene un par ordenado de valores **float** y la **estructura \_ \_ U de tamaño de D2D1** contiene un par ordenado de valores **UINT32** .</span><span class="sxs-lookup"><span data-stu-id="bfb29-110">The **D2D1\_SIZE\_F** structure contains an ordered pair of **FLOAT** values, and the **D2D1\_SIZE\_U** structure contains an ordered pair of **UINT32** values.</span></span>

<span data-ttu-id="bfb29-111">**D2D1 \_ EL tamaño \_ f** es un nombre nuevo para un tipo ya definido **D2D \_ tamaño \_ F**.</span><span class="sxs-lookup"><span data-stu-id="bfb29-111">**D2D1\_SIZE\_F** is a new name for an already defined type **D2D\_SIZE\_F**.</span></span> <span data-ttu-id="bfb29-112">Para obtener una lista de los campos proporcionados por **D2D1 \_ size \_ f**, consulte **D2D \_ size \_ f**.</span><span class="sxs-lookup"><span data-stu-id="bfb29-112">For a list of the fields provided by **D2D1\_SIZE\_F**, see **D2D\_SIZE\_F**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfb29-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfb29-113">Requirements</span></span>



| <span data-ttu-id="bfb29-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfb29-114">Requirement</span></span> | <span data-ttu-id="bfb29-115">Value</span><span class="sxs-lookup"><span data-stu-id="bfb29-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfb29-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bfb29-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bfb29-117">Windows 7, Windows Vista con SP2 y actualización de plataforma para aplicaciones de UWP de aplicaciones de escritorio de Windows Vista \[ \|\]</span><span class="sxs-lookup"><span data-stu-id="bfb29-117">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="bfb29-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bfb29-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bfb29-119">Windows Server 2008 R2, Windows Server 2008 con SP2 y la actualización de la plataforma de aplicaciones de escritorio de Windows Server 2008 \[ \| aplicaciones para UWP\]</span><span class="sxs-lookup"><span data-stu-id="bfb29-119">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="bfb29-120">Teléfono mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bfb29-120">Minimum supported phone</span></span><br/>  | <span data-ttu-id="bfb29-121">Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]</span><span class="sxs-lookup"><span data-stu-id="bfb29-121">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="bfb29-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bfb29-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfb29-123"><dt>D2DBaseTypes. h (incluye D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bfb29-123"><dt>D2DBaseTypes.h (include D2d1.h)</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="bfb29-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="bfb29-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfb29-125">**Tamaño de D2D \_ \_ F**</span><span class="sxs-lookup"><span data-stu-id="bfb29-125">**D2D\_SIZE\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_f)
</dt> <dt>

[<span data-ttu-id="bfb29-126">**Tamaño de D2D1 \_ \_ U**</span><span class="sxs-lookup"><span data-stu-id="bfb29-126">**D2D1\_SIZE\_U**</span></span>](d2d1-size-u.md)
</dt> <dt>

[<span data-ttu-id="bfb29-127">**\_Punto D2D1 \_ 2F**</span><span class="sxs-lookup"><span data-stu-id="bfb29-127">**D2D1\_POINT\_2F**</span></span>](d2d1-point-2f.md)
</dt> </dl>

 

