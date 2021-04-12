---
description: Especifica si el lector de origen habilita la aceleración de vídeo DirectX (DXVA) en el descodificador de vídeo.
ms.assetid: ec539038-3fd3-41b7-a0e6-e75e3f2828a7
title: MF_SOURCE_READER_DISABLE_DXVA atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9362f067d1d6ceae426e9ee6530e08b95837595f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361346"
---
# <a name="mf_source_reader_disable_dxva-attribute"></a><span data-ttu-id="337b2-103">\_Lector de origen MF \_ \_ deshabilitar el \_ atributo DXVA</span><span class="sxs-lookup"><span data-stu-id="337b2-103">MF\_SOURCE\_READER\_DISABLE\_DXVA attribute</span></span>

<span data-ttu-id="337b2-104">Especifica si el [lector de origen](source-reader.md) habilita la aceleración de vídeo DirectX (DXVA) en el descodificador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="337b2-104">Specifies whether the [Source Reader](source-reader.md) enables DirectX Video Acceleration (DXVA) on the video decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="337b2-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="337b2-105">Data type</span></span>

<span data-ttu-id="337b2-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="337b2-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="337b2-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="337b2-107">Get/set</span></span>

<span data-ttu-id="337b2-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="337b2-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="337b2-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="337b2-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="337b2-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="337b2-110">Remarks</span></span>

<span data-ttu-id="337b2-111">Este atributo se aplica si se cumplen las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="337b2-111">This attribute applies if the following conditions are true:</span></span>

-   <span data-ttu-id="337b2-112">El lector de origen descodifica una secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="337b2-112">The source reader decodes a video stream.</span></span>
-   <span data-ttu-id="337b2-113">El descodificador de vídeo admite la descodificación de DXVA.</span><span class="sxs-lookup"><span data-stu-id="337b2-113">The video decoder supports DXVA decoding.</span></span>
-   <span data-ttu-id="337b2-114">La aplicación usa el atributo de [Administrador de D3D de \_ lector de origen \_ \_ \_ MF](mf-source-reader-d3d-manager.md) para establecer la [Administrador de dispositivos de Direct3D](direct3d-device-manager.md) en el lector de origen.</span><span class="sxs-lookup"><span data-stu-id="337b2-114">The application uses the [MF\_SOURCE\_READER\_D3D\_MANAGER](mf-source-reader-d3d-manager.md) attribute to set the [Direct3D Device Manager](direct3d-device-manager.md) on the source reader.</span></span>

<span data-ttu-id="337b2-115">Este atributo permite a la aplicación deshabilitar DXVA mientras se está descodificando en superficies de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="337b2-115">This attribute enables the application to disable DXVA while still decoding to Direct3D surfaces.</span></span>

<span data-ttu-id="337b2-116">De forma predeterminada, el lector de origen usa la [Administrador de dispositivos de Direct3D](direct3d-device-manager.md) para dos propósitos:</span><span class="sxs-lookup"><span data-stu-id="337b2-116">By default, the source reader uses the [Direct3D Device Manager](direct3d-device-manager.md) for two purposes:</span></span>

-   <span data-ttu-id="337b2-117">Para habilitar la descodificación de DXVA en el descodificador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="337b2-117">To enable DXVA decoding in the video decoder.</span></span>
-   <span data-ttu-id="337b2-118">Para asignar las superficies de Direct3D para los ejemplos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="337b2-118">To allocate Direct3D surfaces for the video samples.</span></span>

<span data-ttu-id="337b2-119">Si el valor del atributo del \_ lector de código fuente MF \_ \_ deshabilitar el \_ atributo DXVA es **true**, el lector de origen deshabilita la descodificación de DXVA, aunque todavía usa [Direct3D administrador de dispositivos](direct3d-device-manager.md) para asignar las superficies de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="337b2-119">If the value of the MF\_SOURCE\_READER\_DISABLE\_DXVA attribute is **TRUE**, the source reader does disables DXVA decoding, although it still uses the [Direct3D Device Manager](direct3d-device-manager.md) to allocate Direct3D surfaces.</span></span>

<span data-ttu-id="337b2-120">Si no se establece el atributo de [ \_ \_ \_ \_ Administrador D3D del lector de origen MF](mf-source-reader-d3d-manager.md) , \_ se omite el atributo del lector de origen MF \_ \_ deshabilitar el \_ atributo DXVA.</span><span class="sxs-lookup"><span data-stu-id="337b2-120">If the [MF\_SOURCE\_READER\_D3D\_MANAGER](mf-source-reader-d3d-manager.md) attribute is not set, the MF\_SOURCE\_READER\_DISABLE\_DXVA attribute is ignored.</span></span>

<span data-ttu-id="337b2-121">El valor predeterminado de este atributo es **false**, lo que significa que la descodificación de DXVA está habilitada cuando está disponible.</span><span class="sxs-lookup"><span data-stu-id="337b2-121">The default value of this attribute is **FALSE**, meaning that DXVA decoding is enabled when available.</span></span>

## <a name="requirements"></a><span data-ttu-id="337b2-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="337b2-122">Requirements</span></span>



| <span data-ttu-id="337b2-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="337b2-123">Requirement</span></span> | <span data-ttu-id="337b2-124">Value</span><span class="sxs-lookup"><span data-stu-id="337b2-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="337b2-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="337b2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="337b2-126">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="337b2-126">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="337b2-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="337b2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="337b2-128">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="337b2-128">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="337b2-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="337b2-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="337b2-130"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="337b2-130"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="337b2-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="337b2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="337b2-132">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="337b2-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="337b2-133">Lector de origen</span><span class="sxs-lookup"><span data-stu-id="337b2-133">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="337b2-134">Atributos del lector de código fuente</span><span class="sxs-lookup"><span data-stu-id="337b2-134">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




