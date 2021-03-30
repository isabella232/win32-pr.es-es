---
title: D2D1_POINT_2U (D2DBaseTypes. h)
description: Representa un par de coordenadas x e y en un espacio bidimensional. | D2D1_POINT_2U (D2DBaseTypes. h)
ms.assetid: 652c0dd7-c24d-4941-ae23-2be21b53af69
keywords:
- D2D1_POINT_2U
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050cf6372a1b84ed72647c8c5a5d76e352f4960f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280046"
---
# <a name="d2d1_point_2u"></a><span data-ttu-id="5ae80-105">Punto de D2D1 \_ \_ 2U</span><span class="sxs-lookup"><span data-stu-id="5ae80-105">D2D1\_POINT\_2U</span></span>

<span data-ttu-id="5ae80-106">Representa un par de coordenadas x e y en un espacio bidimensional.</span><span class="sxs-lookup"><span data-stu-id="5ae80-106">Represents an x-coordinate and y-coordinate pair in two-dimensional space.</span></span>


```C++
typedef D2D_POINT_2U D2D1_POINT_2U;
```



## <a name="remarks"></a><span data-ttu-id="5ae80-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5ae80-107">Remarks</span></span>

<span data-ttu-id="5ae80-108">Los puntos en Direct2D se representan mediante las estructuras [**D2D1 \_ punto \_ 2F**](d2d1-point-2f.md) o **D2D1 \_ punto \_ 2U** .</span><span class="sxs-lookup"><span data-stu-id="5ae80-108">Points in Direct2D are represented by the [**D2D1\_POINT\_2F**](d2d1-point-2f.md) or **D2D1\_POINT\_2U** structures.</span></span> <span data-ttu-id="5ae80-109">Ambos contienen un par de coordenada x e y en un espacio bidimensional.</span><span class="sxs-lookup"><span data-stu-id="5ae80-109">Both contain an x-coordinate and y-coordinate pair in two-dimensional space.</span></span> <span data-ttu-id="5ae80-110">La **estructura D2D1 \_ Point \_ 2F** almacena las coordenadas como valores **float** y la estructura **D2D1 \_ Point \_ 2U** las almacena como valores **UINT32** .</span><span class="sxs-lookup"><span data-stu-id="5ae80-110">The **D2D1\_POINT\_2F** structure stores the coordinates as **FLOAT** values, and the **D2D1\_POINT\_2U** structure stores them as **UINT32** values.</span></span>

<span data-ttu-id="5ae80-111">**D2D1 \_ El punto \_ 2U** es un nombre nuevo para el tipo ya definido [**D2D \_ punto \_ 2U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2u).</span><span class="sxs-lookup"><span data-stu-id="5ae80-111">**D2D1\_POINT\_2U** is a new name for the already defined type [**D2D\_POINT\_2U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2u).</span></span>

## <a name="requirements"></a><span data-ttu-id="5ae80-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ae80-112">Requirements</span></span>



| <span data-ttu-id="5ae80-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ae80-113">Requirement</span></span> | <span data-ttu-id="5ae80-114">Value</span><span class="sxs-lookup"><span data-stu-id="5ae80-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ae80-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ae80-115">Minimum supported client</span></span><br/> | <span data-ttu-id="5ae80-116">Windows 7, Windows Vista con SP2 y actualización de plataforma para aplicaciones de UWP de aplicaciones de escritorio de Windows Vista \[ \|\]</span><span class="sxs-lookup"><span data-stu-id="5ae80-116">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="5ae80-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ae80-117">Minimum supported server</span></span><br/> | <span data-ttu-id="5ae80-118">Windows Server 2008 R2, Windows Server 2008 con SP2 y la actualización de la plataforma de aplicaciones de escritorio de Windows Server 2008 \[ \| aplicaciones para UWP\]</span><span class="sxs-lookup"><span data-stu-id="5ae80-118">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="5ae80-119">Teléfono mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ae80-119">Minimum supported phone</span></span><br/>  | <span data-ttu-id="5ae80-120">Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]</span><span class="sxs-lookup"><span data-stu-id="5ae80-120">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="5ae80-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5ae80-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ae80-122"><dt>D2DBaseTypes. h (incluye D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ae80-122"><dt>D2DBaseTypes.h (include D2d1.h)</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="5ae80-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ae80-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ae80-124">**Punto de D2D \_ \_ 2U**</span><span class="sxs-lookup"><span data-stu-id="5ae80-124">**D2D\_POINT\_2U**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2u)
</dt> <dt>

[<span data-ttu-id="5ae80-125">**\_Punto D2D \_ 2F**</span><span class="sxs-lookup"><span data-stu-id="5ae80-125">**D2D\_POINT\_2F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2f)
</dt> </dl>

 

 





