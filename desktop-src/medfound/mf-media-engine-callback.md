---
description: Contiene un puntero a la interfaz de devolución de llamada para el motor multimedia.
ms.assetid: 5FAEF29A-B978-410A-8F5B-EB6F7E35EE6D
title: MF_MEDIA_ENGINE_CALLBACK atributo (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1173e22f9d87f4a77f9ed4a1d1b405fc040bd32b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105707541"
---
# <a name="mf_media_engine_callback-attribute"></a><span data-ttu-id="31f25-103">MF \_ \_ atributo de devolución de llamada del motor multimedia \_</span><span class="sxs-lookup"><span data-stu-id="31f25-103">MF\_MEDIA\_ENGINE\_CALLBACK attribute</span></span>

<span data-ttu-id="31f25-104">Contiene un puntero a la interfaz de devolución de llamada para el motor multimedia.</span><span class="sxs-lookup"><span data-stu-id="31f25-104">Contains a pointer to the callback interface for the Media Engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="31f25-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="31f25-105">Data type</span></span>

<span data-ttu-id="31f25-106">**IMFMediaEngineNotify \* *_ se almacena como _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="31f25-106">**IMFMediaEngineNotify\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="31f25-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="31f25-107">Get/set</span></span>

<span data-ttu-id="31f25-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="31f25-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="31f25-109">Para establecer este atributo, llame a [**IMFAttributes:: setunknown (**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="31f25-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="31f25-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="31f25-110">Remarks</span></span>

<span data-ttu-id="31f25-111">El valor de este atributo es un puntero a la interfaz [**IMFMediaEngineNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginenotify) , implementada por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="31f25-111">The value of this attribute is a pointer to the [**IMFMediaEngineNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginenotify) interface, implemented by the application.</span></span>

<span data-ttu-id="31f25-112">Este atributo se usa con el método [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) para inicializar el motor multimedia.</span><span class="sxs-lookup"><span data-stu-id="31f25-112">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span> <span data-ttu-id="31f25-113">El atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="31f25-113">The attribute is required.</span></span>

## <a name="requirements"></a><span data-ttu-id="31f25-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31f25-114">Requirements</span></span>



| <span data-ttu-id="31f25-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="31f25-115">Requirement</span></span> | <span data-ttu-id="31f25-116">Value</span><span class="sxs-lookup"><span data-stu-id="31f25-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="31f25-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31f25-117">Minimum supported client</span></span><br/> | <span data-ttu-id="31f25-118">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="31f25-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="31f25-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31f25-119">Minimum supported server</span></span><br/> | <span data-ttu-id="31f25-120">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="31f25-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="31f25-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="31f25-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="31f25-122"><dt>Mfmediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="31f25-122"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31f25-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="31f25-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31f25-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="31f25-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="31f25-125">**IMFMediaEngineClassFactory:: CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="31f25-125">**IMFMediaEngineClassFactory::CreateInstance**</span></span>](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> <dt>

[<span data-ttu-id="31f25-126">**IMFMediaEngineNotify**</span><span class="sxs-lookup"><span data-stu-id="31f25-126">**IMFMediaEngineNotify**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginenotify)
</dt> </dl>

 

 




