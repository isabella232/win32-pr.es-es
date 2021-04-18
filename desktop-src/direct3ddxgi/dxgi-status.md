---
description: Códigos de estado que pueden ser devueltos por las funciones de DXGI.
ms.assetid: dd7480b4-8218-4716-ab9f-74a9955b8aa7
title: DXGI_STATUS (DXGI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39c402880ccdcbda009402d56127e70a61543d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707843"
---
# <a name="dxgi_status"></a><span data-ttu-id="5476f-103">Estado de DXGI \_</span><span class="sxs-lookup"><span data-stu-id="5476f-103">DXGI\_STATUS</span></span>

<span data-ttu-id="5476f-104">Códigos de estado que pueden ser devueltos por las funciones de DXGI.</span><span class="sxs-lookup"><span data-stu-id="5476f-104">Status codes that can be returned by DXGI functions.</span></span>



| <span data-ttu-id="5476f-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="5476f-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                      | <span data-ttu-id="5476f-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="5476f-106">Description</span></span>                                                                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_STATUS_OCCLUDED"></span><span id="dxgi_status_occluded"></span><dl> <span data-ttu-id="5476f-107"><dt>**DXGI \_ ESTADO \_ ocluidos**</dt> <dt>0x087A0001</dt></span><span class="sxs-lookup"><span data-stu-id="5476f-107"><dt>**DXGI\_STATUS\_OCCLUDED**</dt> <dt>0x087A0001</dt></span></span> </dl>                                                 | <span data-ttu-id="5476f-108">El contenido de la ventana no está visible.</span><span class="sxs-lookup"><span data-stu-id="5476f-108">The window content is not visible.</span></span> <span data-ttu-id="5476f-109">Al recibir este estado, una aplicación puede detener la representación y usar DXGI \_ present \_ test para determinar cuándo reanudar la representación.</span><span class="sxs-lookup"><span data-stu-id="5476f-109">When receiving this status, an application can stop rendering and use DXGI\_PRESENT\_TEST to determine when to resume rendering.</span></span> <span data-ttu-id="5476f-110">No recibirá \_ \_ el estado de DXGI ocluidos si usa una cadena de intercambio de Flip Model.</span><span class="sxs-lookup"><span data-stu-id="5476f-110">You will not receive DXGI\_STATUS\_OCCLUDED if you're using a flip model swap chain.</span></span><br/>                                                                                                                           |
| <span id="DXGI_STATUS_MODE_CHANGED"></span><span id="dxgi_status_mode_changed"></span><dl> <span data-ttu-id="5476f-111"><dt>**DXGI \_ Modo de estado \_ \_ cambiado**</dt> <dt>0x087A0007</dt></span><span class="sxs-lookup"><span data-stu-id="5476f-111"><dt>**DXGI\_STATUS\_MODE\_CHANGED**</dt> <dt>0x087A0007</dt></span></span> </dl>                                    | <span data-ttu-id="5476f-112">El modo de presentación del escritorio ha cambiado, puede que haya una conversión o ajuste de color.</span><span class="sxs-lookup"><span data-stu-id="5476f-112">The desktop display mode has been changed, there might be color conversion/stretching.</span></span> <span data-ttu-id="5476f-113">La aplicación debe llamar a [**IDXGISwapChain:: ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) para que coincida con el nuevo modo de presentación.</span><span class="sxs-lookup"><span data-stu-id="5476f-113">The application should call [**IDXGISwapChain::ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) to match the new display mode.</span></span><br/>                                                                       |
| <span id="DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="dxgi_status_mode_change_in_progress"></span><dl> <span data-ttu-id="5476f-114"><dt>**DXGI \_ \_ \_ Cambio en el modo de estado \_ en \_ curso**</dt> <dt>0x087A0008</dt></span><span class="sxs-lookup"><span data-stu-id="5476f-114"><dt>**DXGI\_STATUS\_MODE\_CHANGE\_IN\_PROGRESS**</dt> <dt>0x087A0008</dt></span></span> </dl> | <span data-ttu-id="5476f-115">[**IDXGISwapChain:: ResizeTarget**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizetarget) y [**IDXGISwapChain:: SetFullscreenState**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) devolverán \_ \_ \_ \_ el cambio de modo de estado de DXGI en curso si se está \_ produciendo una transición de modo de pantalla completa o de ventana cuando se llama a una API.</span><span class="sxs-lookup"><span data-stu-id="5476f-115">[**IDXGISwapChain::ResizeTarget**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizetarget) and [**IDXGISwapChain::SetFullscreenState**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) will return DXGI\_STATUS\_MODE\_CHANGE\_IN\_PROGRESS if a fullscreen/windowed mode transition is occurring when either API is called.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5476f-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5476f-116">Remarks</span></span>

<span data-ttu-id="5476f-117">El valor **HRESULT** para cada valor de **\_ Estado de DXGI** se determina a partir de esta macro que se define en DXGItype. h:</span><span class="sxs-lookup"><span data-stu-id="5476f-117">The **HRESULT** value for each **DXGI\_STATUS** value is determined from this macro that is defined in DXGItype.h:</span></span>


```
#define _FACDXGI    0x87a
#define MAKE_DXGI_STATUS(code)  MAKE_HRESULT(0, _FACDXGI, code)
```



<span data-ttu-id="5476f-118">Por ejemplo, **el \_ estado \_ de DXGI ocluidos** se define como **0x087A0001**:</span><span class="sxs-lookup"><span data-stu-id="5476f-118">For example, **DXGI\_STATUS\_OCCLUDED** is defined as **0x087A0001**:</span></span>


```
#define DXGI_STATUS_OCCLUDED                    MAKE_DXGI_STATUS(1)
```



## <a name="requirements"></a><span data-ttu-id="5476f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5476f-119">Requirements</span></span>



| <span data-ttu-id="5476f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5476f-120">Requirement</span></span> | <span data-ttu-id="5476f-121">Value</span><span class="sxs-lookup"><span data-stu-id="5476f-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5476f-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5476f-122">Header</span></span><br/> | <dl> <span data-ttu-id="5476f-123"><dt>DXGI. h</dt></span><span class="sxs-lookup"><span data-stu-id="5476f-123"><dt>DXGI.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5476f-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="5476f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5476f-125">Constantes de DXGI</span><span class="sxs-lookup"><span data-stu-id="5476f-125">DXGI Constants</span></span>](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




