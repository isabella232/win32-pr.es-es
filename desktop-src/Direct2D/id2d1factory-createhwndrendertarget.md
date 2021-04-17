---
title: Métodos ID2D1Factory CreateHwndRenderTarget (D2d1. h)
description: Crea un ID2D1HwndRenderTarget, un destino de representación que se representa en una ventana.
ms.assetid: 3b55b1b0-a423-40dc-9581-c1fbe8134ca5
keywords:
- Métodos de CreateHwndRenderTarget Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 984de8aea923c5b90d05fb79bc0c9edc319fb4bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660881"
---
# <a name="id2d1factorycreatehwndrendertarget-methods"></a><span data-ttu-id="edce9-104">ID2D1Factory:: CreateHwndRenderTarget (métodos)</span><span class="sxs-lookup"><span data-stu-id="edce9-104">ID2D1Factory::CreateHwndRenderTarget methods</span></span>

<span data-ttu-id="edce9-105">Crea un [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), un destino de representación que se representa en una ventana.</span><span class="sxs-lookup"><span data-stu-id="edce9-105">Creates an [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), a render target that renders to a window.</span></span>

### <a name="overload-list"></a><span data-ttu-id="edce9-106">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="edce9-106">Overload list</span></span>



| <span data-ttu-id="edce9-107">Método</span><span class="sxs-lookup"><span data-stu-id="edce9-107">Method</span></span>                                                                                                                                                                                                                                                                              | <span data-ttu-id="edce9-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="edce9-108">Description</span></span>                                                                                                             |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edce9-109">[**CreateHwndRenderTarget (D2D1 \_ representar \_ \_ propiedades \* de destino, D2D1 \_ hWnd \_ representación \_ \_ propiedades \* de destino, ID2D1HwndRenderTarget \* \* )**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="edce9-109">[**CreateHwndRenderTarget(D2D1\_RENDER\_TARGET\_PROPERTIES\*,D2D1\_HWND\_RENDER\_TARGET\_PROPERTIES\*,ID2D1HwndRenderTarget\*\*)**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))</span></span> | <span data-ttu-id="edce9-110">Crea un [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), un destino de representación que se representa en una ventana.</span><span class="sxs-lookup"><span data-stu-id="edce9-110">Creates an [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), a render target that renders to a window.</span></span><br/> |
| <span data-ttu-id="edce9-111">[**CreateHwndRenderTarget (D2D1 \_ representar \_ \_ propiedades de destino&, D2D1 \_ hWnd \_ presentar propiedades de \_ destino \_&, ID2D1HwndRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget))</span><span class="sxs-lookup"><span data-stu-id="edce9-111">[**CreateHwndRenderTarget(D2D1\_RENDER\_TARGET\_PROPERTIES&,D2D1\_HWND\_RENDER\_TARGET\_PROPERTIES&,ID2D1HwndRenderTarget\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget))</span></span>   | <span data-ttu-id="edce9-112">Crea un [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), un destino de representación que se representa en una ventana.</span><span class="sxs-lookup"><span data-stu-id="edce9-112">Creates an [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), a render target that renders to a window.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="edce9-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="edce9-113">Remarks</span></span>

<span data-ttu-id="edce9-114">Cuando se crea un destino de representación y la aceleración de hardware está disponible, se asignan recursos en la GPU del equipo.</span><span class="sxs-lookup"><span data-stu-id="edce9-114">When you create a render target and hardware acceleration is available, you allocate resources on the computer's GPU.</span></span> <span data-ttu-id="edce9-115">Al crear un destino de representación una vez y conservarlo lo máximo posible, se obtienen ventajas de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="edce9-115">By creating a render target once and retaining it as long as possible, you gain performance benefits.</span></span> <span data-ttu-id="edce9-116">La aplicación debe crear los destinos de representación una vez y mantenerlos en la vida de la aplicación o hasta que se reciba el error de [**\_ \_ destino de recreación de D2DERR**](direct2d-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="edce9-116">Your application should create render targets once and hold onto them for the life of the application or until the [**D2DERR\_RECREATE\_TARGET**](direct2d-error-codes.md) error is received.</span></span> <span data-ttu-id="edce9-117">Cuando reciba este error, deberá volver a crear el destino de representación (y los recursos que haya creado).</span><span class="sxs-lookup"><span data-stu-id="edce9-117">When you receive this error, you need to recreate the render target (and any resources it created).</span></span>

## <a name="examples"></a><span data-ttu-id="edce9-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="edce9-118">Examples</span></span>

<span data-ttu-id="edce9-119">En el ejemplo siguiente se crea un [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="edce9-119">The following example creates an [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)).</span></span>


```C++
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



## <a name="requirements"></a><span data-ttu-id="edce9-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edce9-120">Requirements</span></span>



| <span data-ttu-id="edce9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="edce9-121">Requirement</span></span> | <span data-ttu-id="edce9-122">Value</span><span class="sxs-lookup"><span data-stu-id="edce9-122">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="edce9-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="edce9-123">Header</span></span><br/>  | <dl> <span data-ttu-id="edce9-124"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="edce9-124"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="edce9-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="edce9-125">Library</span></span><br/> | <dl> <span data-ttu-id="edce9-126"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="edce9-126"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="edce9-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="edce9-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="edce9-128"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edce9-128"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edce9-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="edce9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edce9-130">**ID2D1Factory**</span><span class="sxs-lookup"><span data-stu-id="edce9-130">**ID2D1Factory**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>
