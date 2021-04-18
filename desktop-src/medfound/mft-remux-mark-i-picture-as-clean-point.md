---
description: Especifica si el Remux de vídeo H. 264 debe marcar las imágenes como punto limpio para mejorar la capacidad de búsqueda. Esto tiene la posibilidad de que se produzcan daños en las búsquedas en archivos MP4 finales no conformes.
ms.assetid: BB521E13-40A4-4643-B071-76B8CBC62074
title: MFT_REMUX_MARK_I_PICTURE_AS_CLEAN_POINT atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26c9fe8398507f6d7af5d0e4bf45a36a4454f220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706126"
---
# <a name="mft_remux_mark_i_picture_as_clean_point-attribute"></a><span data-ttu-id="c8402-104">\_REMUX \_ de MFT marca \_ I \_ imagen \_ como \_ atributo de \_ punto limpio</span><span class="sxs-lookup"><span data-stu-id="c8402-104">MFT\_REMUX\_MARK\_I\_PICTURE\_AS\_CLEAN\_POINT attribute</span></span>

<span data-ttu-id="c8402-105">Especifica si el Remux de vídeo H. 264 debe marcar las imágenes como punto limpio para mejorar la capacidad de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="c8402-105">Specifies whether the H.264 video remux MFT should mark I pictures as clean point for better seek-ability.</span></span> <span data-ttu-id="c8402-106">Esto tiene la posibilidad de que se produzcan daños en las búsquedas en archivos MP4 finales no conformes.</span><span class="sxs-lookup"><span data-stu-id="c8402-106">This has the potential for corruptions on seeks in non-conforming final MP4 files.</span></span>

## <a name="data-type"></a><span data-ttu-id="c8402-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c8402-107">Data type</span></span>

<span data-ttu-id="c8402-108">**Bool** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="c8402-108">**Bool** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="c8402-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c8402-109">Remarks</span></span>

<span data-ttu-id="c8402-110">La imagen del punto de limpieza debe comprimir las imágenes de IDR por definición.</span><span class="sxs-lookup"><span data-stu-id="c8402-110">Clean point picture should be compressed IDR pictures by definition.</span></span>

<span data-ttu-id="c8402-111">Esto no se recomienda para la grabación o la remuxing de archivos MP4, a menos que un ejercicio de este tipo sea generar algunos archivos seudopersonalizados intermedios para la edición de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c8402-111">This is not recommended for recording or remuxing MP4 files, unless such an exercise is to produce some intermediate pseudo MP4 files for video editing.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8402-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8402-112">Requirements</span></span>



| <span data-ttu-id="c8402-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8402-113">Requirement</span></span> | <span data-ttu-id="c8402-114">Value</span><span class="sxs-lookup"><span data-stu-id="c8402-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8402-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8402-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c8402-116">Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="c8402-116">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="c8402-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8402-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c8402-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="c8402-118">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                             |
| <span data-ttu-id="c8402-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8402-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8402-120"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8402-120"><dt>Mftransform.h</dt></span></span> </dl>   |
| <span data-ttu-id="c8402-121">IDL</span><span class="sxs-lookup"><span data-stu-id="c8402-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c8402-122"><dt>Mftransform. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c8402-122"><dt>Mftransform.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8402-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8402-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8402-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c8402-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




