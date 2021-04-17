---
title: Métodos ID2D1Factory CreateWicBitmapRenderTarget
description: Crea un destino de representación que se representa en un mapa de bits de Microsoft Windows Imaging Component (WIC).
ms.assetid: 93141743-c11d-40b4-83c5-07c9066836c7
keywords:
- Métodos de CreateWicBitmapRenderTarget Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 4025028582c254e7a5724a575ef0d7f1c7d91570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660327"
---
# <a name="id2d1factorycreatewicbitmaprendertarget-methods"></a><span data-ttu-id="f663d-104">ID2D1Factory:: CreateWicBitmapRenderTarget (métodos)</span><span class="sxs-lookup"><span data-stu-id="f663d-104">ID2D1Factory::CreateWicBitmapRenderTarget methods</span></span>

<span data-ttu-id="f663d-105">Crea un destino de representación que se representa en un mapa de bits de Microsoft Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="f663d-105">Creates a render target that renders to a Microsoft Windows Imaging Component (WIC) bitmap.</span></span>

### <a name="overload-list"></a><span data-ttu-id="f663d-106">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="f663d-106">Overload list</span></span>



| <span data-ttu-id="f663d-107">Método</span><span class="sxs-lookup"><span data-stu-id="f663d-107">Method</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="f663d-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="f663d-108">Description</span></span>                                                                                            |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f663d-109">[**CreateWicBitmapRenderTarget (IWICBitmap \* , D2D1 \_ representar \_ \_ propiedades \* de destino, ID2D1RenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties_id2d1rendertarget))</span><span class="sxs-lookup"><span data-stu-id="f663d-109">[**CreateWicBitmapRenderTarget(IWICBitmap\*,D2D1\_RENDER\_TARGET\_PROPERTIES\*,ID2D1RenderTarget\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties_id2d1rendertarget))</span></span> | <span data-ttu-id="f663d-110">Crea un destino de representación que se representa en un mapa de bits de Microsoft Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="f663d-110">Creates a render target that renders to a Microsoft Windows Imaging Component (WIC) bitmap.</span></span><br/> |
| <span data-ttu-id="f663d-111">[**CreateWicBitmapRenderTarget (IWICBitmap \* , D2D1 \_ \_ \_ propiedades de destino de representación&, ID2D1RenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties__id2d1rendertarget))</span><span class="sxs-lookup"><span data-stu-id="f663d-111">[**CreateWicBitmapRenderTarget(IWICBitmap\*,D2D1\_RENDER\_TARGET\_PROPERTIES&,ID2D1RenderTarget\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties__id2d1rendertarget))</span></span>  | <span data-ttu-id="f663d-112">Crea un destino de representación que se representa en un mapa de bits de Microsoft Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="f663d-112">Creates a render target that renders to a Microsoft Windows Imaging Component (WIC) bitmap.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f663d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f663d-113">Remarks</span></span>

<span data-ttu-id="f663d-114">La aplicación debe crear los destinos de representación una vez y mantenerlos en la vida de la aplicación o hasta que se reciba el error de [**\_ \_ destino de recreación de D2DERR**](direct2d-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="f663d-114">Your application should create render targets once and hold onto them for the life of the application or until the [**D2DERR\_RECREATE\_TARGET**](direct2d-error-codes.md) error is received.</span></span> <span data-ttu-id="f663d-115">Cuando reciba este error, deberá volver a crear el destino de representación (y los recursos que haya creado).</span><span class="sxs-lookup"><span data-stu-id="f663d-115">When you receive this error, you need to recreate the render target (and any resources it created).</span></span>

<span data-ttu-id="f663d-116">**Nota:**   Este método no se admite en Windows Phone y se producirá un error cuando se lo llame en un dispositivo con el código de error 0x8899000b (no hay ningún dispositivo de representación de hardware disponible para esta operación).</span><span class="sxs-lookup"><span data-stu-id="f663d-116">**Note**   This method isn't supported on Windows Phone and will fail when called on a device with error code 0x8899000b ( There is no hardware rendering device available for this operation ).</span></span> <span data-ttu-id="f663d-117">Dado que el emulador de Windows Phone admite la representación de ALABEo, este método producirá un error cuando se llame en el emulador con un código de error diferente, 0x88982f80 (wincodec \_ Err \_ unsupportedpixelformat).</span><span class="sxs-lookup"><span data-stu-id="f663d-117">Because the Windows Phone Emulator supports WARP rendering, this method will fail when called on the emulator with a different error code, 0x88982f80 (wincodec\_err\_unsupportedpixelformat).</span></span>

## <a name="requirements"></a><span data-ttu-id="f663d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f663d-118">Requirements</span></span>



| <span data-ttu-id="f663d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f663d-119">Requirement</span></span> | <span data-ttu-id="f663d-120">Value</span><span class="sxs-lookup"><span data-stu-id="f663d-120">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f663d-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f663d-121">Library</span></span><br/> | <dl> <span data-ttu-id="f663d-122"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f663d-122"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="f663d-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f663d-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="f663d-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f663d-124"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f663d-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="f663d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f663d-126">**ID2D1Factory**</span><span class="sxs-lookup"><span data-stu-id="f663d-126">**ID2D1Factory**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>

 

