---
description: Especifica una ventana para que el motor multimedia aplique protecciones de administrador de protección de la información (OPM).
ms.assetid: E5271D72-FE16-4D28-9BBA-1440C7CE0921
title: MF_MEDIA_ENGINE_OPM_HWND atributo (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d60dd38f4f9eaca3e4eefbf84142c1509463f9b9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104003343"
---
# <a name="mf_media_engine_opm_hwnd-attribute"></a><span data-ttu-id="3b423-103">\_ \_ \_ \_ Atributo HWND de el motor de multimedia MF</span><span class="sxs-lookup"><span data-stu-id="3b423-103">MF\_MEDIA\_ENGINE\_OPM\_HWND attribute</span></span>

<span data-ttu-id="3b423-104">Especifica una ventana para que el motor multimedia aplique protecciones de [Administrador de protección](output-protection-manager.md) de la información (OPM).</span><span class="sxs-lookup"><span data-stu-id="3b423-104">Specifies a window for the Media Engine to apply [Output Protection Manager](output-protection-manager.md) (OPM) protections.</span></span>

## <a name="data-type"></a><span data-ttu-id="3b423-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="3b423-105">Data type</span></span>

<span data-ttu-id="3b423-106">**HWnd** almacenado como **UINT64**</span><span class="sxs-lookup"><span data-stu-id="3b423-106">**HWND** stored as **UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="3b423-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b423-107">Remarks</span></span>

<span data-ttu-id="3b423-108">Este atributo se usa con el método [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) para inicializar el motor multimedia.</span><span class="sxs-lookup"><span data-stu-id="3b423-108">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span>

<span data-ttu-id="3b423-109">Para habilitar la protección de OPM para la reproducción de vídeo, la aplicación debe realizar una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="3b423-109">To enable OPM protections for video playback, the application must do one of the following:</span></span>

-   <span data-ttu-id="3b423-110">Establezca el [atributo \_ \_ hWnd de \_ reproducción \_ del motor multimedia MF](mf-media-engine-playback-hwnd.md) al crear el motor multimedia.</span><span class="sxs-lookup"><span data-stu-id="3b423-110">Set the [MF\_MEDIA\_ENGINE\_PLAYBACK\_HWND](mf-media-engine-playback-hwnd.md) attribute when creating the Media Engine.</span></span>
-   <span data-ttu-id="3b423-111">Establezca el atributo del HWND del motor de multimedia de MF \_ \_ \_ \_ al crear el motor multimedia.</span><span class="sxs-lookup"><span data-stu-id="3b423-111">Set the MF\_MEDIA\_ENGINE\_OPM\_HWND attribute when creating the Media Engine.</span></span>
-   <span data-ttu-id="3b423-112">Llame a [**IMFMediaEngineProtectedContent:: SetOPMWindow**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setopmwindow) en cualquier momento después de crear el motor multimedia, pero antes de que se muestre el contenido protegido.</span><span class="sxs-lookup"><span data-stu-id="3b423-112">Call [**IMFMediaEngineProtectedContent::SetOPMWindow**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setopmwindow) at any point after creating the Media Engine, but before protected content is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b423-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b423-113">Requirements</span></span>



| <span data-ttu-id="3b423-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b423-114">Requirement</span></span> | <span data-ttu-id="3b423-115">Value</span><span class="sxs-lookup"><span data-stu-id="3b423-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b423-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b423-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3b423-117">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="3b423-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="3b423-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b423-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3b423-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="3b423-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="3b423-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3b423-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b423-121"><dt>Mfmediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b423-121"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b423-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b423-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b423-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3b423-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3b423-124">Atributos del motor multimedia</span><span class="sxs-lookup"><span data-stu-id="3b423-124">Media Engine Attributes</span></span>](media-engine-attributes.md)
</dt> </dl>

 

 




