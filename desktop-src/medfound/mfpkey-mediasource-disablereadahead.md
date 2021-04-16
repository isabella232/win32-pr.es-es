---
description: Habilita o deshabilita la lectura previa en un origen de multimedia.
ms.assetid: b2b8711f-ba63-4fba-bb88-8d254135eb21
title: Propiedad MFPKEY_MediaSource_DisableReadAhead (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d06fe354431a24e15152268ba0ea6352e535c5e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649832"
---
# <a name="mfpkey_mediasource_disablereadahead-property"></a><span data-ttu-id="5c974-103">\_Propiedad MFPKEY MediaSource \_ DisableReadAhead</span><span class="sxs-lookup"><span data-stu-id="5c974-103">MFPKEY\_MediaSource\_DisableReadAhead property</span></span>

<span data-ttu-id="5c974-104">Habilita o deshabilita la lectura previa en un origen de multimedia.</span><span class="sxs-lookup"><span data-stu-id="5c974-104">Enables or disables read-ahead in a media source.</span></span>



<span data-ttu-id="5c974-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="5c974-105">Data type</span></span>

<span data-ttu-id="5c974-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="5c974-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="5c974-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="5c974-107">PROPVARIANT member</span></span>

<span data-ttu-id="5c974-108">**VARIANTE \_ bool**</span><span class="sxs-lookup"><span data-stu-id="5c974-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="5c974-109">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="5c974-109">VT\_BOOL</span></span>

<span data-ttu-id="5c974-110">**boolVal**</span><span class="sxs-lookup"><span data-stu-id="5c974-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="5c974-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5c974-111">Remarks</span></span>

<span data-ttu-id="5c974-112">Las aplicaciones pueden utilizar esta propiedad para configurar algunos orígenes de medios.</span><span class="sxs-lookup"><span data-stu-id="5c974-112">Applications can use this property to configure some media sources.</span></span> <span data-ttu-id="5c974-113">Para establecer la propiedad, pase un puntero **IPropertyStore** a la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="5c974-113">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="5c974-114">Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="5c974-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="5c974-115">Si el valor es **Variant \_ true**, el origen del medio no se leerá con anterioridad en el flujo de bytes.</span><span class="sxs-lookup"><span data-stu-id="5c974-115">If the value is **VARIANT\_TRUE**, the media source will not read ahead in the byte stream.</span></span> <span data-ttu-id="5c974-116">Esta configuración puede optimizar el rendimiento si tiene previsto leer una cantidad limitada de datos del origen de medios, por ejemplo, para obtener una imagen en miniatura de un archivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5c974-116">This setting can optimize performance if you plan to read a limited amount of data from the media source—for example, to get a thumbnail image from a video file.</span></span>

<span data-ttu-id="5c974-117">Para la reproducción de audio/vídeo típica, esta propiedad debe establecerse en **variante \_ falsa**.</span><span class="sxs-lookup"><span data-stu-id="5c974-117">For typical audio/video playback, this property should be set to **VARIANT\_FALSE**.</span></span> <span data-ttu-id="5c974-118">El valor predeterminado es **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="5c974-118">The default value is **VARIANT\_FALSE**.</span></span>

<span data-ttu-id="5c974-119">No todos los orígenes multimedia admiten esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="5c974-119">Not every media source supports this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c974-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c974-120">Requirements</span></span>



| <span data-ttu-id="5c974-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c974-121">Requirement</span></span> | <span data-ttu-id="5c974-122">Value</span><span class="sxs-lookup"><span data-stu-id="5c974-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5c974-123">Remoto</span><span class="sxs-lookup"><span data-stu-id="5c974-123">Client</span></span><br/> | <span data-ttu-id="5c974-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5c974-124">Windows 7</span></span><br/>                                                               |
| <span data-ttu-id="5c974-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5c974-125">Header</span></span><br/> | <dl> <span data-ttu-id="5c974-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c974-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c974-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c974-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c974-128">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5c974-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




