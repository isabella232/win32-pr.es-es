---
title: D2D1_SIZE_U (D2DBaseTypes. h)
description: Almacena un par de enteros ordenados, normalmente el ancho y el alto de un rectángulo.
ms.assetid: e28da5ee-7d68-4ec5-b477-c6ead0c725e6
keywords:
- D2D1_SIZE_U
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c78b5c317a98169957402dd125c054b8f6e0bc69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150056"
---
# <a name="d2d1_size_u"></a><span data-ttu-id="f860f-104">Tamaño de D2D1 \_ \_ U</span><span class="sxs-lookup"><span data-stu-id="f860f-104">D2D1\_SIZE\_U</span></span>

<span data-ttu-id="f860f-105">Almacena un par de enteros ordenados, normalmente el ancho y el alto de un rectángulo.</span><span class="sxs-lookup"><span data-stu-id="f860f-105">Stores an ordered pair of integers, typically the width and height of a rectangle.</span></span>


```C++
typedef D2D_SIZE_U D2D1_SIZE_U;
```



## <a name="remarks"></a><span data-ttu-id="f860f-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f860f-106">Remarks</span></span>

<span data-ttu-id="f860f-107">Al igual que los puntos, los tamaños son otro concepto de gráficos importante.</span><span class="sxs-lookup"><span data-stu-id="f860f-107">Like points, sizes are another important graphics concept.</span></span> <span data-ttu-id="f860f-108">En Direct2D, los tamaños se representan mediante las estructuras **D2D1 \_ size \_ u** o [**D2D1 \_ size \_ F**](d2d1-size-f.md) .</span><span class="sxs-lookup"><span data-stu-id="f860f-108">In Direct2D, sizes are represented by the **D2D1\_SIZE\_U** or [**D2D1\_SIZE\_F**](d2d1-size-f.md) structures.</span></span> <span data-ttu-id="f860f-109">Ambos contienen un par ordenado de números.</span><span class="sxs-lookup"><span data-stu-id="f860f-109">They both contain an ordered pair of numbers.</span></span> <span data-ttu-id="f860f-110">La **estructura \_ \_ U de tamaño de D2D1** contiene un par ordenado de valores **UINT32** y la estructura **\_ \_ F de tamaño D2D1** contiene un par ordenado de valores **float** .</span><span class="sxs-lookup"><span data-stu-id="f860f-110">The **D2D1\_SIZE\_U** structure contains an ordered pair of **UINT32** values, and the **D2D1\_SIZE\_F** structure contains an ordered pair of **FLOAT** values.</span></span>

<span data-ttu-id="f860f-111">La **estructura \_ \_ U de tamaño de D2D1** proporciona una manera cómoda de almacenar un par ordenado de números, como el ancho y el alto de un rectángulo.</span><span class="sxs-lookup"><span data-stu-id="f860f-111">The **D2D1\_SIZE\_U** structure provides a convenient way for you to store an ordered pair of numbers, such as the width and height of a rectangle.</span></span>

<span data-ttu-id="f860f-112">**D2D1 \_ EL tamaño \_ u** es un nombre nuevo para un tipo ya definido **D2D \_ tamaño \_ u**.</span><span class="sxs-lookup"><span data-stu-id="f860f-112">**D2D1\_SIZE\_U** is a new name for an already defined type **D2D\_SIZE\_U**.</span></span> <span data-ttu-id="f860f-113">Puede usar la función **D2D1:: SizeU** para crear una estructura **\_ \_ U de tamaño de D2D1** .</span><span class="sxs-lookup"><span data-stu-id="f860f-113">You can use the **D2D1::SizeU** function to create a **D2D1\_SIZE\_U** structure.</span></span> <span data-ttu-id="f860f-114">Un uso común de esta estructura es especificar el tamaño en píxeles de una estructura de [**propiedades de destino de representación de D2D1 \_ hWnd \_ \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) .</span><span class="sxs-lookup"><span data-stu-id="f860f-114">A common use for this structure is to specify the pixel size of a [**D2D1\_HWND\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) structure.</span></span> <span data-ttu-id="f860f-115">A continuación se proporciona un ejemplo del uso de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="f860f-115">The following provides an example of using this structure.</span></span>


```C++
    if (!m_pRenderTarget)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        D2D1_SIZE_U size = D2D1::SizeU(
            rc.right - rc.left,
            rc.bottom - rc.top
            );

        // Create a Direct2D render target.
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties(),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );
```



## <a name="requirements"></a><span data-ttu-id="f860f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f860f-116">Requirements</span></span>



| <span data-ttu-id="f860f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f860f-117">Requirement</span></span> | <span data-ttu-id="f860f-118">Value</span><span class="sxs-lookup"><span data-stu-id="f860f-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f860f-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f860f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f860f-120">Windows 7, Windows Vista con SP2 y actualización de plataforma para aplicaciones de UWP de aplicaciones de escritorio de Windows Vista \[ \|\]</span><span class="sxs-lookup"><span data-stu-id="f860f-120">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="f860f-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f860f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f860f-122">Windows Server 2008 R2, Windows Server 2008 con SP2 y la actualización de la plataforma de aplicaciones de escritorio de Windows Server 2008 \[ \| aplicaciones para UWP\]</span><span class="sxs-lookup"><span data-stu-id="f860f-122">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="f860f-123">Teléfono mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f860f-123">Minimum supported phone</span></span><br/>  | <span data-ttu-id="f860f-124">Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]</span><span class="sxs-lookup"><span data-stu-id="f860f-124">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="f860f-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f860f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f860f-126"><dt>D2DBaseTypes. h (incluye D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f860f-126"><dt>D2DBaseTypes.h (include D2d1.h)</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="f860f-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="f860f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f860f-128">**Tamaño de D2D \_ \_ U**</span><span class="sxs-lookup"><span data-stu-id="f860f-128">**D2D\_SIZE\_U**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_u)
</dt> <dt>

[<span data-ttu-id="f860f-129">**Tamaño de D2D1 \_ \_ F**</span><span class="sxs-lookup"><span data-stu-id="f860f-129">**D2D1\_SIZE\_F**</span></span>](d2d1-size-f.md)
</dt> <dt>

[<span data-ttu-id="f860f-130">**D2D1::HwndRenderTargetProperties**</span><span class="sxs-lookup"><span data-stu-id="f860f-130">**D2D1::HwndRenderTargetProperties**</span></span>](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties)
</dt> </dl>

 

