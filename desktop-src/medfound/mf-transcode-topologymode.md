---
description: Especifica para una topología de transcodificación si el cargador de topología va a cargar transformaciones basadas en hardware.
ms.assetid: 33db8621-114a-4531-908f-f30034441973
title: MF_TRANSCODE_TOPOLOGYMODE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f700397914faf7fee35e7f82027d8f8771e8b099
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908251"
---
# <a name="mf_transcode_topologymode-attribute"></a><span data-ttu-id="e6dcf-103">\_Atributo TOPOLOGYMODE de TRANSCODE MF \_</span><span class="sxs-lookup"><span data-stu-id="e6dcf-103">MF\_TRANSCODE\_TOPOLOGYMODE attribute</span></span>

<span data-ttu-id="e6dcf-104">Especifica para una topología de transcodificación si el cargador de topología va a cargar transformaciones basadas en hardware.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-104">Specifies for a transcode topology whether the topology loader will load hardware-based transforms.</span></span>

<span data-ttu-id="e6dcf-105">El modo de topología especifica si se pueden usar transformaciones de hardware (como códecs de hardware) en la topología de transcodificación.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-105">The topology mode specifies whether hardware transforms (such as hardware codecs) may be used in the transcode topology.</span></span> <span data-ttu-id="e6dcf-106">La aplicación puede almacenar este atributo en un perfil de transcodificación llamando a [**IMFTranscodeProfile:: SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes).</span><span class="sxs-lookup"><span data-stu-id="e6dcf-106">The application can store this attribute in a transcode profile by calling [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes).</span></span>

## <a name="data-type"></a><span data-ttu-id="e6dcf-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e6dcf-107">Data type</span></span>

<span data-ttu-id="e6dcf-108">**[**MF \_ Transcodificar las \_ \_ marcas TOPOLOGYMODE**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_topologymode_flags)** almacenadas como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="e6dcf-108">**[**MF\_TRANSCODE\_TOPOLOGYMODE\_FLAGS**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_topologymode_flags)** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="e6dcf-109">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="e6dcf-109">Get/set</span></span>

<span data-ttu-id="e6dcf-110">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="e6dcf-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="e6dcf-111">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="e6dcf-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="e6dcf-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e6dcf-112">Remarks</span></span>

<span data-ttu-id="e6dcf-113">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-113">This attribute is optional.</span></span> <span data-ttu-id="e6dcf-114">Debe tener uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-114">It must have one of the following values.</span></span>



| <span data-ttu-id="e6dcf-115">Value</span><span class="sxs-lookup"><span data-stu-id="e6dcf-115">Value</span></span>                                              | <span data-ttu-id="e6dcf-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6dcf-116">Description</span></span>                                                                                                                                                                                                                                                                       |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6dcf-117">**se \_ permite el \_ hardware TOPOLOGYMODE de TRANScodificación MF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e6dcf-117">**MF\_TRANSCODE\_TOPOLOGYMODE\_HARDWARE\_ALLOWED**</span></span> | <span data-ttu-id="e6dcf-118">El cargador de topología cargará los MFTs basados en hardware, como los descodificadores de hardware, si están disponibles.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-118">The Topology Loader will load hardware-based MFTs, such as hardware decoders, when available.</span></span><br/> <span data-ttu-id="e6dcf-119">El cargador de topología recurre automáticamente a la descodificación de software si no se encuentra ningún descodificador de hardware o si un descodificador de hardware no puede conectarse por algún motivo.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-119">The Topology Loader automatically falls back to software decoding if no hardware decoder is found, or if a hardware decoder fails to connect for some reason.</span></span><br/> |
| <span data-ttu-id="e6dcf-120">**MF \_ Transcode \_ TOPOLOGYMODE \_ \_ solo software**</span><span class="sxs-lookup"><span data-stu-id="e6dcf-120">**MF\_TRANSCODE\_TOPOLOGYMODE\_SOFTWARE\_ONLY**</span></span>    | <span data-ttu-id="e6dcf-121">El cargador de topología solo cargará software MFTs, incluidos los descodificadores de software.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-121">The Topology Loader will load only software MFTs, including software decoders.</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="e6dcf-122">El valor predeterminado es **MF \_ Transcode \_ TOPOLOGYMODE \_ \_ solo software**.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-122">The default value is **MF\_TRANSCODE\_TOPOLOGYMODE\_SOFTWARE\_ONLY**.</span></span>

<span data-ttu-id="e6dcf-123">Si el cargador de topología inserta un MFT de hardware en la topología, establece el atributo de [ \_ atributo de \_ \_ dirección URL \_ de hardware de enumeración MFT](mft-enum-hardware-url-attribute.md) en el nodo de la topología.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-123">If the Topology Loader inserts a hardware MFT into the topology, it sets the [MFT\_ENUM\_HARDWARE\_URL\_Attribute](mft-enum-hardware-url-attribute.md) attribute on the topology node.</span></span> <span data-ttu-id="e6dcf-124">Para comprobar si existe un MFT de hardware, enumere los nodos de la topología resuelta y compruebe si este atributo está presente.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-124">To check whether a hardware MFT is present, enumerate the nodes in the resolved topology and check whether this attribute is present.</span></span>

<span data-ttu-id="e6dcf-125">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-125">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6dcf-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6dcf-126">Requirements</span></span>



| <span data-ttu-id="e6dcf-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6dcf-127">Requirement</span></span> | <span data-ttu-id="e6dcf-128">Value</span><span class="sxs-lookup"><span data-stu-id="e6dcf-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e6dcf-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6dcf-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e6dcf-130">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="e6dcf-130">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e6dcf-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e6dcf-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e6dcf-132">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e6dcf-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e6dcf-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e6dcf-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6dcf-134"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6dcf-134"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6dcf-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6dcf-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6dcf-136">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e6dcf-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e6dcf-137">API de transcodificación</span><span class="sxs-lookup"><span data-stu-id="e6dcf-137">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="e6dcf-138">**IMFTranscodeProfile::GetContainerAttributes**</span><span class="sxs-lookup"><span data-stu-id="e6dcf-138">**IMFTranscodeProfile::GetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
</dt> <dt>

[<span data-ttu-id="e6dcf-139">**IMFTranscodeProfile::SetContainerAttributes**</span><span class="sxs-lookup"><span data-stu-id="e6dcf-139">**IMFTranscodeProfile::SetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




