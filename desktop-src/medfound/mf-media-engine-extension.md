---
description: Contiene un puntero a la interfaz IMFMediaEngineExtension.
ms.assetid: D2F3F41D-086A-4DEB-99D0-07574BC8F0D7
title: MF_MEDIA_ENGINE_EXTENSION atributo (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4496b40e9b69091b588ad38ad47d943dce5e1966
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104424131"
---
# <a name="mf_media_engine_extension-attribute"></a><span data-ttu-id="6a23f-103">MF \_ \_ atributo de extensión de motor multimedia \_</span><span class="sxs-lookup"><span data-stu-id="6a23f-103">MF\_MEDIA\_ENGINE\_EXTENSION attribute</span></span>

<span data-ttu-id="6a23f-104">Contiene un puntero a la interfaz [**IMFMediaEngineExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension) .</span><span class="sxs-lookup"><span data-stu-id="6a23f-104">Contains a pointer to the [**IMFMediaEngineExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension) interface.</span></span>

## <a name="data-type"></a><span data-ttu-id="6a23f-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="6a23f-105">Data type</span></span>

<span data-ttu-id="6a23f-106">**IMFMediaEngineExtension \* *_ se almacena como _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="6a23f-106">**IMFMediaEngineExtension\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="6a23f-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="6a23f-107">Get/set</span></span>

<span data-ttu-id="6a23f-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="6a23f-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="6a23f-109">Para establecer este atributo, llame a [**IMFAttributes:: setunknown (**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="6a23f-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="6a23f-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a23f-110">Remarks</span></span>

<span data-ttu-id="6a23f-111">Este atributo se usa con el método [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) para inicializar el motor multimedia.</span><span class="sxs-lookup"><span data-stu-id="6a23f-111">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span>

<span data-ttu-id="6a23f-112">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="6a23f-112">This attribute is optional.</span></span> <span data-ttu-id="6a23f-113">Úselo para proporcionar un objeto que implemente la interfaz [**IMFMediaEngineExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension) .</span><span class="sxs-lookup"><span data-stu-id="6a23f-113">Use it to provide an object that implements the [**IMFMediaEngineExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension) interface.</span></span> <span data-ttu-id="6a23f-114">Esta interfaz permite a la aplicación cargar recursos multimedia personalizados.</span><span class="sxs-lookup"><span data-stu-id="6a23f-114">This interface enables the application to load custom media resources.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a23f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a23f-115">Requirements</span></span>



| <span data-ttu-id="6a23f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a23f-116">Requirement</span></span> | <span data-ttu-id="6a23f-117">Value</span><span class="sxs-lookup"><span data-stu-id="6a23f-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a23f-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a23f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6a23f-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="6a23f-119">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="6a23f-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a23f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6a23f-121">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="6a23f-121">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="6a23f-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6a23f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a23f-123"><dt>Mfmediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a23f-123"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a23f-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a23f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a23f-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6a23f-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




