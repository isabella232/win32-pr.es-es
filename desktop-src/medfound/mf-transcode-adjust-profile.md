---
description: Marcas de perfil que definen la configuración de la secuencia para la topología de transcodificación. Las marcas se definen en la \_ enumeración MF Transcode \_ ADJUST \_ Profile \_ Flags.
ms.assetid: 6782e080-284b-458d-8bc0-6e131a529e7b
title: MF_TRANSCODE_ADJUST_PROFILE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd492cfc7981ca1a36a1cb54a440bec4783fe1b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687056"
---
# <a name="mf_transcode_adjust_profile-attribute"></a><span data-ttu-id="1e30a-104">Atributo de Perfil de ajuste de \_ TRANSCODIFICACIÓN MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="1e30a-104">MF\_TRANSCODE\_ADJUST\_PROFILE attribute</span></span>

<span data-ttu-id="1e30a-105">Marcas de perfil que definen la configuración de la secuencia para la topología de transcodificación.</span><span class="sxs-lookup"><span data-stu-id="1e30a-105">Profile flags that define the stream settings for the transcode topology.</span></span> <span data-ttu-id="1e30a-106">Las marcas se definen en la enumeración [**MF \_ Transcode \_ ADJUST \_ Profile \_ Flags**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_adjust_profile_flags) .</span><span class="sxs-lookup"><span data-stu-id="1e30a-106">The flags are defined in the [**MF\_TRANSCODE\_ADJUST\_PROFILE\_FLAGS**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_adjust_profile_flags) enumeration.</span></span>

## <a name="data-type"></a><span data-ttu-id="1e30a-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="1e30a-107">Data type</span></span>

<span data-ttu-id="1e30a-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1e30a-108">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="1e30a-109">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="1e30a-109">Get/set</span></span>

<span data-ttu-id="1e30a-110">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="1e30a-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="1e30a-111">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="1e30a-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="1e30a-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1e30a-112">Remarks</span></span>

<span data-ttu-id="1e30a-113">Una aplicación puede establecer este atributo en el nivel de contenedor en el perfil de transcodificación.</span><span class="sxs-lookup"><span data-stu-id="1e30a-113">An application can set this attribute at the container level on the transcode profile.</span></span> <span data-ttu-id="1e30a-114">Si se establece este atributo, la función [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) cambia los atributos de la secuencia durante la compilación de la topología, en función de la marca especificada.</span><span class="sxs-lookup"><span data-stu-id="1e30a-114">If this attribute is set, the [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) function changes the stream attributes during topology building, depending on the specified flag.</span></span> <span data-ttu-id="1e30a-115">Por ejemplo, si la aplicación especifica la marca **MF \_ Transcode \_ ADJUST \_ Profile \_ predeterminada** , se utiliza la configuración de la secuencia especificada por la aplicación para crear el perfil.</span><span class="sxs-lookup"><span data-stu-id="1e30a-115">For example, if the application specifies the **MF\_TRANSCODE\_ADJUST\_PROFILE\_DEFAULT** flag, the application-specified stream settings are used to create the profile.</span></span>

<span data-ttu-id="1e30a-116">En el flujo de vídeo, la velocidad de fotogramas se actualiza en función del origen de los medios.</span><span class="sxs-lookup"><span data-stu-id="1e30a-116">For the video stream, the frame rate is updated based on the media source.</span></span> <span data-ttu-id="1e30a-117">Si la aplicación no especifica el modo entrelazado, el perfil se actualiza para utilizar fotogramas progresivos de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="1e30a-117">If the application does not specify the interlaced mode, the profile is updated to use progressive frames by default.</span></span>

<span data-ttu-id="1e30a-118">Si la aplicación especifica la marca **MF \_ Transcode \_ ADJUST \_ Profile \_ use \_ source \_ attributes** , los atributos de secuencia que faltan se copian desde el origen de medios de entrada a la configuración de la secuencia en el perfil de transcodificación.</span><span class="sxs-lookup"><span data-stu-id="1e30a-118">If the application specifies the **MF\_TRANSCODE\_ADJUST\_PROFILE\_USE\_SOURCE\_ATTRIBUTES** flag, then missing stream attributes are copied from the input media source to the stream settings in the transcode profile.</span></span>

<span data-ttu-id="1e30a-119">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="1e30a-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e30a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e30a-120">Requirements</span></span>



| <span data-ttu-id="1e30a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e30a-121">Requirement</span></span> | <span data-ttu-id="1e30a-122">Value</span><span class="sxs-lookup"><span data-stu-id="1e30a-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1e30a-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e30a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1e30a-124">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="1e30a-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1e30a-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e30a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1e30a-126">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="1e30a-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="1e30a-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1e30a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e30a-128"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e30a-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e30a-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e30a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e30a-130">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1e30a-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1e30a-131">API de transcodificación</span><span class="sxs-lookup"><span data-stu-id="1e30a-131">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="1e30a-132">**IMFTranscodeProfile::SetContainerAttributes**</span><span class="sxs-lookup"><span data-stu-id="1e30a-132">**IMFTranscodeProfile::SetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




