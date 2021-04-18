---
title: D2D1_POINT_2F (D2DBaseTypes. h)
description: Representa un par de coordenadas x e y en un espacio bidimensional. | D2D1_POINT_2F (D2DBaseTypes. h)
ms.assetid: b317ae75-d738-4e1a-bcd1-adf3e95b197e
keywords:
- D2D1_POINT_2F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f93bf4a0d1a1b3f988f1c6d168388e9910080dcb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105678709"
---
# <a name="d2d1_point_2f"></a><span data-ttu-id="6f721-105">\_Punto D2D1 \_ 2F</span><span class="sxs-lookup"><span data-stu-id="6f721-105">D2D1\_POINT\_2F</span></span>

<span data-ttu-id="6f721-106">Representa un par de coordenadas x e y en un espacio bidimensional.</span><span class="sxs-lookup"><span data-stu-id="6f721-106">Represents an x-coordinate and y-coordinate pair in two-dimensional space.</span></span>


```C++
typedef D2D_POINT_2F D2D1_POINT_2F;
```



## <a name="remarks"></a><span data-ttu-id="6f721-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f721-107">Remarks</span></span>

<span data-ttu-id="6f721-108">Los puntos en Direct2D se representan mediante las estructuras **D2D1 \_ punto \_ 2F** o [**D2D1 \_ punto \_ 2U**](d2d1-point-2u.md) .</span><span class="sxs-lookup"><span data-stu-id="6f721-108">Points in Direct2D are represented by the **D2D1\_POINT\_2F** or [**D2D1\_POINT\_2U**](d2d1-point-2u.md) structures.</span></span> <span data-ttu-id="6f721-109">Ambos contienen un par de coordenada x e y en un espacio bidimensional.</span><span class="sxs-lookup"><span data-stu-id="6f721-109">Both contain an x-coordinate and y-coordinate pair in two-dimensional space.</span></span> <span data-ttu-id="6f721-110">La **estructura D2D1 \_ Point \_ 2F** almacena las coordenadas como valores **float** y la estructura **D2D1 \_ Point \_ 2U** las almacena como valores **UINT32** .</span><span class="sxs-lookup"><span data-stu-id="6f721-110">The **D2D1\_POINT\_2F** structure stores the coordinates as **FLOAT** values, and the **D2D1\_POINT\_2U** structure stores them as **UINT32** values.</span></span>

<span data-ttu-id="6f721-111">**D2D1 \_ El punto \_ 2F** es un nombre nuevo para el tipo ya definido [**D2D \_ punto \_ 2F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2f).</span><span class="sxs-lookup"><span data-stu-id="6f721-111">**D2D1\_POINT\_2F** is a new name for the already defined type [**D2D\_POINT\_2F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2f).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f721-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f721-112">Requirements</span></span>



| <span data-ttu-id="6f721-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f721-113">Requirement</span></span> | <span data-ttu-id="6f721-114">Value</span><span class="sxs-lookup"><span data-stu-id="6f721-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f721-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f721-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6f721-116">Windows 7, Windows Vista con SP2 y actualización de plataforma para aplicaciones de UWP de aplicaciones de escritorio de Windows Vista \[ \|\]</span><span class="sxs-lookup"><span data-stu-id="6f721-116">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="6f721-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f721-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6f721-118">Windows Server 2008 R2, Windows Server 2008 con SP2 y la actualización de la plataforma de aplicaciones de escritorio de Windows Server 2008 \[ \| aplicaciones para UWP\]</span><span class="sxs-lookup"><span data-stu-id="6f721-118">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="6f721-119">Teléfono mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f721-119">Minimum supported phone</span></span><br/>  | <span data-ttu-id="6f721-120">Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]</span><span class="sxs-lookup"><span data-stu-id="6f721-120">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="6f721-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6f721-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f721-122"><dt>D2DBaseTypes. h (incluye D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6f721-122"><dt>D2DBaseTypes.h (include D2d1.h)</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="6f721-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f721-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f721-124">**Punto de D2D1 \_ \_ 2U**</span><span class="sxs-lookup"><span data-stu-id="6f721-124">**D2D1\_POINT\_2U**</span></span>](/windows/desktop/Direct2D/d2d1-point-2u)
</dt> <dt>

[<span data-ttu-id="6f721-125">**\_Punto D2D \_ 2F**</span><span class="sxs-lookup"><span data-stu-id="6f721-125">**D2D\_POINT\_2F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2f)
</dt> </dl>

 

