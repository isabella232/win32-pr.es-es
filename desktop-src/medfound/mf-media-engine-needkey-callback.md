---
description: Atributo que se pasa en el IMFMediaEngineNeedKeyNotify al motor multimedia al crearlo.
ms.assetid: B9625B3C-00AC-4F46-BD76-5C77822F5829
title: MF_MEDIA_ENGINE_NEEDKEY_CALLBACK atributo)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3de502bbe1d7f83dfd8ee7478e20786244f654e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105697964"
---
# <a name="mf_media_engine_needkey_callback-attribute"></a><span data-ttu-id="fd943-103">\_Atributo de \_ devolución de \_ llamada NEEDKEY del motor multimedia MF \_</span><span class="sxs-lookup"><span data-stu-id="fd943-103">MF\_MEDIA\_ENGINE\_NEEDKEY\_CALLBACK attribute</span></span>

<span data-ttu-id="fd943-104">Atributo que se pasa en el [**IMFMediaEngineNeedKeyNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) al motor multimedia al crearlo.</span><span class="sxs-lookup"><span data-stu-id="fd943-104">Attribute which is passed in the [**IMFMediaEngineNeedKeyNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) to the media engine on creation.</span></span>

## <a name="data-type"></a><span data-ttu-id="fd943-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="fd943-105">Data type</span></span>

<span data-ttu-id="fd943-106">**IMFMediaEngineNeedKeyNotify \* *_ se almacena como _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="fd943-106">**IMFMediaEngineNeedKeyNotify\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="fd943-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="fd943-107">Get/set</span></span>

<span data-ttu-id="fd943-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="fd943-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="fd943-109">Para establecer este atributo, llame a [**IMFAttributes:: setunknown (**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="fd943-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="fd943-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd943-110">Remarks</span></span>

<span data-ttu-id="fd943-111">El valor de este atributo es un puntero a la interfaz [**IMFMediaEngineNeedKeyNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) , implementada por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fd943-111">The value of this attribute is a pointer to the [**IMFMediaEngineNeedKeyNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) interface, implemented by the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd943-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd943-112">Requirements</span></span>



| <span data-ttu-id="fd943-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd943-113">Requirement</span></span> | <span data-ttu-id="fd943-114">Value</span><span class="sxs-lookup"><span data-stu-id="fd943-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd943-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd943-115">Minimum supported client</span></span><br/> | <span data-ttu-id="fd943-116">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="fd943-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fd943-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd943-117">Minimum supported server</span></span><br/> | <span data-ttu-id="fd943-118">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="fd943-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="fd943-119">IDL</span><span class="sxs-lookup"><span data-stu-id="fd943-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fd943-120"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fd943-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd943-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd943-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd943-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fd943-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




