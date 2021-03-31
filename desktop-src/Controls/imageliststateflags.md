---
title: IMAGELISTSTATEFLAGS (commctrl. h)
description: Las marcas siguientes se pasan al método draw IImageList en el miembro fState de IMAGELISTDRAWPARAMS.
ms.assetid: a22b4acf-c290-44b2-9216-b006d0326236
topic_type:
- apiref
api_name:
- ILS_NORMAL
- ILS_GLOW
- ILS_SHADOW
- ILS_SATURATE
- ILS_ALPHA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fea580294f54b6e2fc5c3e5b6aee1119811c22e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079207"
---
# <a name="imageliststateflags"></a><span data-ttu-id="e0329-103">IMAGELISTSTATEFLAGS</span><span class="sxs-lookup"><span data-stu-id="e0329-103">IMAGELISTSTATEFLAGS</span></span>

<span data-ttu-id="e0329-104">Las marcas siguientes se pasan al método [**IImageList::D RAW**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-draw) en el miembro **fState** de [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams).</span><span class="sxs-lookup"><span data-stu-id="e0329-104">The following flags are passed to the [**IImageList::Draw**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-draw) method in the **fState** member of [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams).</span></span>



| <span data-ttu-id="e0329-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="e0329-105">Constant/value</span></span>                                                                                                                                                                                                             | <span data-ttu-id="e0329-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="e0329-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILS_NORMAL"></span><span id="ils_normal"></span><dl> <span data-ttu-id="e0329-107"><dt>**ILS \_ NORMAL**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="e0329-107"><dt>**ILS\_NORMAL**</dt> <dt>0x00000000</dt></span></span> </dl>       | <span data-ttu-id="e0329-108">El estado de la imagen no se ha modificado.</span><span class="sxs-lookup"><span data-stu-id="e0329-108">The image state is not modified.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                   |
| <span id="ILS_GLOW"></span><span id="ils_glow"></span><dl> <span data-ttu-id="e0329-109"><dt>**ILS \_ RESPLANDOR**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="e0329-109"><dt>**ILS\_GLOW**</dt> <dt>0x00000001</dt></span></span> </dl>             | <span data-ttu-id="e0329-110">No se admite.</span><span class="sxs-lookup"><span data-stu-id="e0329-110">Not supported.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="ILS_SHADOW"></span><span id="ils_shadow"></span><dl> <span data-ttu-id="e0329-111"><dt>**ILS \_ SOMBRA**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="e0329-111"><dt>**ILS\_SHADOW**</dt> <dt>0x00000002</dt></span></span> </dl>       | <span data-ttu-id="e0329-112">No se admite.</span><span class="sxs-lookup"><span data-stu-id="e0329-112">Not supported.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="ILS_SATURATE"></span><span id="ils_saturate"></span><dl> <span data-ttu-id="e0329-113"><dt>**ILS \_ SATURAr**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="e0329-113"><dt>**ILS\_SATURATE**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="e0329-114">Reduce la saturación de color del icono a escala de grises.</span><span class="sxs-lookup"><span data-stu-id="e0329-114">Reduces the color saturation of the icon to grayscale.</span></span> <span data-ttu-id="e0329-115">Esto solo afecta a las imágenes de 32 bpp.</span><span class="sxs-lookup"><span data-stu-id="e0329-115">This only affects 32bpp images.</span></span> <br/>                                                                                                                                                                                                                                                                                            |
| <span id="ILS_ALPHA"></span><span id="ils_alpha"></span><dl> <span data-ttu-id="e0329-116"><dt>**ILS \_ ALFA**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="e0329-116"><dt>**ILS\_ALPHA**</dt> <dt>0x00000008</dt></span></span> </dl>          | <span data-ttu-id="e0329-117">Alfa combina el icono.</span><span class="sxs-lookup"><span data-stu-id="e0329-117">Alpha blends the icon.</span></span> <span data-ttu-id="e0329-118">La combinación alfa controla el nivel de transparencia de un icono, según el valor de su canal alfa.</span><span class="sxs-lookup"><span data-stu-id="e0329-118">Alpha blending controls the transparency level of an icon, according to the value of its alpha channel.</span></span> <span data-ttu-id="e0329-119">El valor del canal alfa se indica mediante el miembro de **marco** en el método [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) .</span><span class="sxs-lookup"><span data-stu-id="e0329-119">The value of the alpha channel is indicated by the **frame** member in the [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) method.</span></span> <span data-ttu-id="e0329-120">El canal alfa puede estar comprendido entre 0 y 255, donde 0 es completamente transparente y 255 es totalmente opaco.</span><span class="sxs-lookup"><span data-stu-id="e0329-120">The alpha channel can be from 0 to 255, with 0 being completely transparent, and 255 being completely opaque.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="e0329-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0329-121">Requirements</span></span>



| <span data-ttu-id="e0329-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0329-122">Requirement</span></span> | <span data-ttu-id="e0329-123">Value</span><span class="sxs-lookup"><span data-stu-id="e0329-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e0329-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0329-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e0329-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e0329-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e0329-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0329-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e0329-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e0329-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e0329-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e0329-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0329-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0329-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

