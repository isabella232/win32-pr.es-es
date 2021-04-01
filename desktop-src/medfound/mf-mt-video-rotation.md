---
description: Especifica el giro de un fotograma de vídeo en el sentido contrario a las agujas del reloj.
ms.assetid: 7C0911A6-6D7C-4510-891F-A6F56CE1EC2B
title: MF_MT_VIDEO_ROTATION atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f46a67c9861b8094e909e5c6fd7bc82e46166dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913554"
---
# <a name="mf_mt_video_rotation-attribute"></a><span data-ttu-id="b6a03-103">\_Atributo de \_ rotación de vídeo MF MT \_</span><span class="sxs-lookup"><span data-stu-id="b6a03-103">MF\_MT\_VIDEO\_ROTATION attribute</span></span>

<span data-ttu-id="b6a03-104">Especifica el giro de un fotograma de vídeo en el sentido contrario a las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="b6a03-104">Specifies the rotation of a video frame in the counter-clockwise direction.</span></span>

## <a name="data-type"></a><span data-ttu-id="b6a03-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b6a03-105">Data type</span></span>

<span data-ttu-id="b6a03-106">**MFVideoRotationFormat** almacenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="b6a03-106">**MFVideoRotationFormat** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="b6a03-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b6a03-107">Remarks</span></span>

<span data-ttu-id="b6a03-108">El vídeo de un dispositivo de mano, como un teléfono móvil, a menudo gira en 90, 180 o 270 grados.</span><span class="sxs-lookup"><span data-stu-id="b6a03-108">Video from a handheld device, such as a mobile phone, is often rotated by 90, 180, or 270 degrees.</span></span> <span data-ttu-id="b6a03-109">Si la cámara almacena la orientación como metadatos en el archivo de vídeo, la imagen se puede ajustar en el momento de la reproducción.</span><span class="sxs-lookup"><span data-stu-id="b6a03-109">If the camera stores the orientation as metadata in the video file, the image can be adjusted at the time of playback.</span></span>

<span data-ttu-id="b6a03-110">Si este atributo se establece en **MFVideoRotationFormat \_ 90**, significa que el contenido se ha girado 90 grados en el sentido contrario a las agujas del reloj.</span><span class="sxs-lookup"><span data-stu-id="b6a03-110">If this attribute set to **MFVideoRotationFormat\_90**, it means that the content has been rotated 90 degrees in the counter-clockwise direction.</span></span> <span data-ttu-id="b6a03-111">Si el contenido se gira 90 grados en sentido de las agujas del reloj, el valor del atributo sería **MFVideoRotationFormat \_ 270**.</span><span class="sxs-lookup"><span data-stu-id="b6a03-111">If the content was rotated 90 degrees in the clockwise direction, the attribute value would be **MFVideoRotationFormat\_270**.</span></span>

<span data-ttu-id="b6a03-112">Los valores admitidos para este atributo se enumeran en [**MFVideoRotationFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideorotationformat).</span><span class="sxs-lookup"><span data-stu-id="b6a03-112">The supported values for this attribute are enumerated in [**MFVideoRotationFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideorotationformat).</span></span>

<span data-ttu-id="b6a03-113">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b6a03-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6a03-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6a03-114">Requirements</span></span>



| <span data-ttu-id="b6a03-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6a03-115">Requirement</span></span> | <span data-ttu-id="b6a03-116">Value</span><span class="sxs-lookup"><span data-stu-id="b6a03-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b6a03-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6a03-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b6a03-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="b6a03-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="b6a03-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6a03-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b6a03-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="b6a03-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="b6a03-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b6a03-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6a03-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6a03-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6a03-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6a03-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6a03-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b6a03-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b6a03-125">Tipos de medios</span><span class="sxs-lookup"><span data-stu-id="b6a03-125">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 




