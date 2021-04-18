---
title: Métodos de CreateImageSourceFromWic de ID2D1DeviceContext2 (D2d1 \_ 3. h)
description: Crea un objeto de origen de imagen a partir de un origen de mapa de bits de WIC y rellena toda la memoria de píxeles dentro del origen de la imagen. La imagen se carga y se almacena al usar una cantidad mínima de memoria.
ms.assetid: af02630d-a9ca-f5b4-6f2a-31a73ef603e5
keywords:
- Métodos de CreateImageSourceFromWic Direct2D
topic_type:
- apiref
api_location:
- d2d1_3.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 20773912886840a185e1b9fc71576f89e9a40fde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681113"
---
# <a name="id2d1devicecontext2createimagesourcefromwic-methods"></a><span data-ttu-id="15f6a-105">ID2D1DeviceContext2:: CreateImageSourceFromWic (métodos)</span><span class="sxs-lookup"><span data-stu-id="15f6a-105">ID2D1DeviceContext2::CreateImageSourceFromWic methods</span></span>

<span data-ttu-id="15f6a-106">Crea un objeto de origen de imagen a partir de un origen de mapa de bits de WIC y rellena toda la memoria de píxeles dentro del origen de la imagen.</span><span class="sxs-lookup"><span data-stu-id="15f6a-106">Creates an image source object from a WIC bitmap source, while populating all pixel memory within the image source.</span></span> <span data-ttu-id="15f6a-107">La imagen se carga y se almacena al usar una cantidad mínima de memoria.</span><span class="sxs-lookup"><span data-stu-id="15f6a-107">The image is loaded and stored while using a minimal amount of memory.</span></span>

### <a name="overload-list"></a><span data-ttu-id="15f6a-108">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="15f6a-108">Overload list</span></span>



| <span data-ttu-id="15f6a-109">Método</span><span class="sxs-lookup"><span data-stu-id="15f6a-109">Method</span></span>                                                                                                                                                                                       | <span data-ttu-id="15f6a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="15f6a-110">Description</span></span>                                                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15f6a-111">[**CreateImageSourceFromWic (IWICBitmapSource \* , opciones de carga de origen de la \_ imagen \_ de D2D1 \_ \_ , ID2D1ImageSourceFromWic \* \* )**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_d2d1_image_source_loading_options_id2d1imagesourcefromwic))</span><span class="sxs-lookup"><span data-stu-id="15f6a-111">[**CreateImageSourceFromWic (IWICBitmapSource\*, D2D1\_IMAGE\_SOURCE\_LOADING\_OPTIONS, ID2D1ImageSourceFromWic\*\*)**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_d2d1_image_source_loading_options_id2d1imagesourcefromwic))</span></span>                   | <span data-ttu-id="15f6a-112">Versión del método que le permite especificar el origen de mapa de bits de WIC, el objeto de origen de la imagen de salida y las opciones de carga con el modo alfa predeterminado.</span><span class="sxs-lookup"><span data-stu-id="15f6a-112">Version of the method that allows you to specify the WIC bitmap source, the output image source object, and loading options with default alpha mode.</span></span><br/>   |
| <span data-ttu-id="15f6a-113">[**CreateImageSourceFromWic (IWICBitmapSource \* , D2D1 \_ Image \_ source \_ Load \_ Options, D2D1 \_ alpha \_ Mode, ID2D1ImageSourceFromWic \* \* )**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_d2d1_image_source_loading_options_d2d1_alpha_mode_id2d1imagesourcefromwic))</span><span class="sxs-lookup"><span data-stu-id="15f6a-113">[**CreateImageSourceFromWic (IWICBitmapSource\*, D2D1\_IMAGE\_SOURCE\_LOADING\_OPTIONS, D2D1\_ALPHA\_MODE, ID2D1ImageSourceFromWic\*\*)**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_d2d1_image_source_loading_options_d2d1_alpha_mode_id2d1imagesourcefromwic))</span></span> | <span data-ttu-id="15f6a-114">Versión del método que le permite especificar el origen de mapa de bits de WIC, el objeto de origen de la imagen de salida y las opciones de carga, y el modo alfa.</span><span class="sxs-lookup"><span data-stu-id="15f6a-114">Version of the method that allows you to specify the WIC bitmap source, the output image source object, and loading options, and alpha mode.</span></span><br/>           |
| <span data-ttu-id="15f6a-115">[**CreateImageSourceFromWic (IWICBitmapSource \* , ID2D1ImageSourceFromWic \* \* )**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_id2d1imagesourcefromwic))</span><span class="sxs-lookup"><span data-stu-id="15f6a-115">[**CreateImageSourceFromWic (IWICBitmapSource\*, ID2D1ImageSourceFromWic\*\*)**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-createimagesourcefromwic(iwicbitmapsource_id2d1imagesourcefromwic))</span></span>                                                          | <span data-ttu-id="15f6a-116">Versión del método que le permite especificar el origen de mapa de bits de WIC y el objeto de origen de la imagen de salida con la carga predeterminada opitons y el modo alfa.</span><span class="sxs-lookup"><span data-stu-id="15f6a-116">Version of the method that allows you to specify the WIC bitmap source and the output image source object with default loading opitons and alpha mode.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="15f6a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15f6a-117">Requirements</span></span>



| <span data-ttu-id="15f6a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="15f6a-118">Requirement</span></span> | <span data-ttu-id="15f6a-119">Value</span><span class="sxs-lookup"><span data-stu-id="15f6a-119">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="15f6a-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="15f6a-120">Header</span></span><br/> | <dl> <span data-ttu-id="15f6a-121"><dt>D2d1 \_ 3. h</dt></span><span class="sxs-lookup"><span data-stu-id="15f6a-121"><dt>D2d1\_3.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15f6a-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="15f6a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15f6a-123">**ID2D1DeviceContext2**</span><span class="sxs-lookup"><span data-stu-id="15f6a-123">**ID2D1DeviceContext2**</span></span>](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1devicecontext2)
</dt> </dl>

<span data-ttu-id="15f6a-124">�</span><span class="sxs-lookup"><span data-stu-id="15f6a-124">�</span></span>

<span data-ttu-id="15f6a-125">�</span><span class="sxs-lookup"><span data-stu-id="15f6a-125">�</span></span>
