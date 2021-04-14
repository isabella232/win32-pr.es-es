---
title: Marcas de creación de la lista de imágenes (ShlObj. h)
description: Conjunto de marcadores de bits que especifica el tipo de lista de imágenes que se va a crear. Este parámetro puede ser una combinación de los valores siguientes, pero solo puede incluir uno de los valores de \_ color ILC. Lo usan ImageList \_ Create y IImageList2 Initialize.
ms.assetid: DFEB1934-DB7F-4151-97F9-DDB2BCCC782A
topic_type:
- apiref
api_name:
- ILC_MASK
- ILC_COLOR
- ILC_COLORDDB
- ILC_COLOR4
- ILC_COLOR8
- ILC_COLOR16
- ILC_COLOR24
- ILC_COLOR32
- ILC_PALETTE
- ILC_MIRROR
- ILC_PERITEMMIRROR
- ILC_ORIGINALSIZE
- ILC_HIGHQUALITYSCALE
api_location:
- Shlobj.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f27f9a83c119b8e201ba41c002bf7c166ba3e4dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490210"
---
# <a name="image-list-creation-flags"></a><span data-ttu-id="15a2a-105">Marcas de creación de lista de imágenes</span><span class="sxs-lookup"><span data-stu-id="15a2a-105">Image List Creation Flags</span></span>

<span data-ttu-id="15a2a-106">Conjunto de marcadores de bits que especifica el tipo de lista de imágenes que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="15a2a-106">The set of bit flags that specifies the type of image list to create.</span></span> <span data-ttu-id="15a2a-107">Este parámetro puede ser una combinación de los valores siguientes, pero solo puede incluir uno de los valores de \_ color ILC.</span><span class="sxs-lookup"><span data-stu-id="15a2a-107">This parameter can be a combination of the following values, but it can include only one of the ILC\_COLOR values.</span></span> <span data-ttu-id="15a2a-108">Usado por [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) y [**IImageList2:: Initialize**](/windows/desktop/api/Commoncontrols/nf-commoncontrols-iimagelist2-initialize).</span><span class="sxs-lookup"><span data-stu-id="15a2a-108">Used by [**ImageList\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) and [**IImageList2::Initialize**](/windows/desktop/api/Commoncontrols/nf-commoncontrols-iimagelist2-initialize).</span></span>



| <span data-ttu-id="15a2a-109">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="15a2a-109">Constant/value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="15a2a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="15a2a-110">Description</span></span>                                                                                                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILC_MASK"></span><span id="ilc_mask"></span><dl> <span data-ttu-id="15a2a-111"><dt>**ILC \_ MÁSCARA**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="15a2a-111"><dt>**ILC\_MASK**</dt> <dt>0x00000001</dt></span></span> </dl>                                     | <span data-ttu-id="15a2a-112">Use una máscara.</span><span class="sxs-lookup"><span data-stu-id="15a2a-112">Use a mask.</span></span> <span data-ttu-id="15a2a-113">La lista de imágenes contiene dos mapas de bits, uno de los cuales es un mapa de bits monocromo que se usa como máscara.</span><span class="sxs-lookup"><span data-stu-id="15a2a-113">The image list contains two bitmaps, one of which is a monochrome bitmap used as a mask.</span></span> <span data-ttu-id="15a2a-114">Si no se incluye este valor, la lista de imágenes solo contiene un mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="15a2a-114">If this value is not included, the image list contains only one bitmap.</span></span><br/>      |
| <span id="ILC_COLOR"></span><span id="ilc_color"></span><dl> <span data-ttu-id="15a2a-115"><dt>**ILC \_ COLOR**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="15a2a-115"><dt>**ILC\_COLOR**</dt> <dt>0x00000000</dt></span></span> </dl>                                  | <span data-ttu-id="15a2a-116">Use el comportamiento predeterminado si no se especifica ninguna de las otras marcas de ILC \_ COLORx.</span><span class="sxs-lookup"><span data-stu-id="15a2a-116">Use the default behavior if none of the other ILC\_COLORx flags is specified.</span></span> <span data-ttu-id="15a2a-117">Normalmente, el valor predeterminado es ILC \_ COLOR4, pero para los controladores de pantalla anteriores, el valor predeterminado es ILC \_ COLORDDB.</span><span class="sxs-lookup"><span data-stu-id="15a2a-117">Typically, the default is ILC\_COLOR4, but for older display drivers, the default is ILC\_COLORDDB.</span></span><br/> |
| <span id="ILC_COLORDDB"></span><span id="ilc_colorddb"></span><dl> <span data-ttu-id="15a2a-118"><dt>**ILC \_ COLORDDB**</dt> <dt>0x000000FE</dt></span><span class="sxs-lookup"><span data-stu-id="15a2a-118"><dt>**ILC\_COLORDDB**</dt> <dt>0x000000FE</dt></span></span> </dl>                         | <span data-ttu-id="15a2a-119">Use un mapa de bits dependiente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="15a2a-119">Use a device-dependent bitmap.</span></span><br/>                                                                                                                                                    |
| <span id="ILC_COLOR4"></span><span id="ilc_color4"></span><dl> <span data-ttu-id="15a2a-120"><dt>**ILC \_ COLOR4**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="15a2a-120"><dt>**ILC\_COLOR4**</dt> <dt>0x00000004</dt></span></span> </dl>                               | <span data-ttu-id="15a2a-121">Use una sección de mapa de bits independiente del dispositivo (DIB) de 4 bits (16 colores) como mapa de bits para la lista de imágenes.</span><span class="sxs-lookup"><span data-stu-id="15a2a-121">Use a 4-bit (16-color) device-independent bitmap (DIB) section as the bitmap for the image list.</span></span><br/>                                                                                  |
| <span id="ILC_COLOR8"></span><span id="ilc_color8"></span><dl> <span data-ttu-id="15a2a-122"><dt>**ILC \_ COLOR8**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="15a2a-122"><dt>**ILC\_COLOR8**</dt> <dt>0x00000008</dt></span></span> </dl>                               | <span data-ttu-id="15a2a-123">Use una sección DIB de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="15a2a-123">Use an 8-bit DIB section.</span></span> <span data-ttu-id="15a2a-124">Los colores usados para la tabla de colores son los mismos que los colores de la paleta de semitonos.</span><span class="sxs-lookup"><span data-stu-id="15a2a-124">The colors used for the color table are the same colors as the halftone palette.</span></span><br/>                                                                        |
| <span id="ILC_COLOR16"></span><span id="ilc_color16"></span><dl> <span data-ttu-id="15a2a-125"><dt>**ILC \_ COLOR16**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="15a2a-125"><dt>**ILC\_COLOR16**</dt> <dt>0x00000010</dt></span></span> </dl>                            | <span data-ttu-id="15a2a-126">Use una sección DIB de 16 bits (32/64k-color).</span><span class="sxs-lookup"><span data-stu-id="15a2a-126">Use a 16-bit (32/64k-color) DIB section.</span></span><br/>                                                                                                                                          |
| <span id="ILC_COLOR24"></span><span id="ilc_color24"></span><dl> <span data-ttu-id="15a2a-127"><dt>**ILC \_ COLOR24**</dt> <dt>0x00000018</dt></span><span class="sxs-lookup"><span data-stu-id="15a2a-127"><dt>**ILC\_COLOR24**</dt> <dt>0x00000018</dt></span></span> </dl>                            | <span data-ttu-id="15a2a-128">Use una sección DIB de 24 bits.</span><span class="sxs-lookup"><span data-stu-id="15a2a-128">Use a 24-bit DIB section.</span></span><br/>                                                                                                                                                         |
| <span id="ILC_COLOR32"></span><span id="ilc_color32"></span><dl> <span data-ttu-id="15a2a-129"><dt>**ILC \_ COLOR32**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="15a2a-129"><dt>**ILC\_COLOR32**</dt> <dt>0x00000020</dt></span></span> </dl>                            | <span data-ttu-id="15a2a-130">Use una sección DIB de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="15a2a-130">Use a 32-bit DIB section.</span></span><br/>                                                                                                                                                         |
| <span id="ILC_PALETTE"></span><span id="ilc_palette"></span><dl> <span data-ttu-id="15a2a-131"><dt>**ILC \_ PALETA**</dt> <dt>0x00000800</dt></span><span class="sxs-lookup"><span data-stu-id="15a2a-131"><dt>**ILC\_PALETTE**</dt> <dt>0x00000800</dt></span></span> </dl>                            | <span data-ttu-id="15a2a-132">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="15a2a-132">Not implemented.</span></span><br/>                                                                                                                                                                  |
| <span id="ILC_MIRROR"></span><span id="ilc_mirror"></span><dl> <span data-ttu-id="15a2a-133"><dt>**ILC \_**</dt> <dt></dt> Recreativo de reflejo</span><span class="sxs-lookup"><span data-stu-id="15a2a-133"><dt>**ILC\_MIRROR**</dt> <dt>0x00002000</dt></span></span> </dl>                               | <span data-ttu-id="15a2a-134">Reflejar los iconos contenidos, si el proceso está reflejado</span><span class="sxs-lookup"><span data-stu-id="15a2a-134">Mirror the icons contained, if the process is mirrored</span></span><br/>                                                                                                                            |
| <span id="ILC_PERITEMMIRROR"></span><span id="ilc_peritemmirror"></span><dl> <span data-ttu-id="15a2a-135"><dt>**ILC \_ PERITEMMIRROR**</dt> <dt>0x00008000</dt></span><span class="sxs-lookup"><span data-stu-id="15a2a-135"><dt>**ILC\_PERITEMMIRROR**</dt> <dt>0x00008000</dt></span></span> </dl>          | <span data-ttu-id="15a2a-136">Hace que el código de creación de reflejo refleje cada elemento al insertar un conjunto de imágenes, en lugar de toda la franja.</span><span class="sxs-lookup"><span data-stu-id="15a2a-136">Causes the mirroring code to mirror each item when inserting a set of images, versus the whole strip.</span></span><br/>                                                                             |
| <span id="ILC_ORIGINALSIZE"></span><span id="ilc_originalsize"></span><dl> <span data-ttu-id="15a2a-137"><dt>**ILC \_ ORIGINALSIZE**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="15a2a-137"><dt>**ILC\_ORIGINALSIZE**</dt> <dt>0x00010000</dt></span></span> </dl>             | <span data-ttu-id="15a2a-138">**Windows Vista y versiones posteriores.**</span><span class="sxs-lookup"><span data-stu-id="15a2a-138">**Windows Vista and later.**</span></span> <span data-ttu-id="15a2a-139">ImageList debe aceptar menor que las imágenes establecidas y aplicar el tamaño original en función de la imagen agregada.</span><span class="sxs-lookup"><span data-stu-id="15a2a-139">Imagelist should accept smaller than set images and apply original size based on image added.</span></span><br/>                                                        |
| <span id="ILC_HIGHQUALITYSCALE"></span><span id="ilc_highqualityscale"></span><dl> <span data-ttu-id="15a2a-140"><dt>**ILC \_ HIGHQUALITYSCALE**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="15a2a-140"><dt>**ILC\_HIGHQUALITYSCALE**</dt> <dt>0x00020000</dt></span></span> </dl> | <span data-ttu-id="15a2a-141">**Windows Vista y versiones posteriores.**</span><span class="sxs-lookup"><span data-stu-id="15a2a-141">**Windows Vista and later.**</span></span> <span data-ttu-id="15a2a-142">Reservado.</span><span class="sxs-lookup"><span data-stu-id="15a2a-142">Reserved.</span></span><br/>                                                                                                                                            |



## <a name="requirements"></a><span data-ttu-id="15a2a-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15a2a-143">Requirements</span></span>



| <span data-ttu-id="15a2a-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="15a2a-144">Requirement</span></span> | <span data-ttu-id="15a2a-145">Value</span><span class="sxs-lookup"><span data-stu-id="15a2a-145">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="15a2a-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15a2a-146">Minimum supported client</span></span><br/> | <span data-ttu-id="15a2a-147">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="15a2a-147">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="15a2a-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15a2a-148">Minimum supported server</span></span><br/> | <span data-ttu-id="15a2a-149">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="15a2a-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="15a2a-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="15a2a-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="15a2a-151"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="15a2a-151"><dt>Shlobj.h</dt></span></span> </dl> |



 

 





