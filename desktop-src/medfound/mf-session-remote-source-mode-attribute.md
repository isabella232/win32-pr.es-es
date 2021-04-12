---
description: Especifica que el origen de medios se creará en un proceso remoto.
ms.assetid: 3a2f9ff5-1780-40f3-b36b-3a7cccb47d05
title: MF_SESSION_REMOTE_SOURCE_MODE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a27b26a71e8bea53ab687eaf6126a1803e71ba16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277831"
---
# <a name="mf_session_remote_source_mode-attribute"></a><span data-ttu-id="92d36-103">\_Atributo de \_ \_ modo de origen remoto de sesión MF \_</span><span class="sxs-lookup"><span data-stu-id="92d36-103">MF\_SESSION\_REMOTE\_SOURCE\_MODE attribute</span></span>

<span data-ttu-id="92d36-104">Especifica que el origen de medios se creará en un proceso remoto.</span><span class="sxs-lookup"><span data-stu-id="92d36-104">Specifies that the media source will be created in a remote process.</span></span>

## <a name="data-type"></a><span data-ttu-id="92d36-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="92d36-105">Data type</span></span>

<span data-ttu-id="92d36-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="92d36-106">**UINT32**</span></span>

<span data-ttu-id="92d36-107">Trata como un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="92d36-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="92d36-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="92d36-108">Remarks</span></span>

<span data-ttu-id="92d36-109">Puede establecer este atributo en la sesión de la ruta de acceso a medios protegidos (PMP) mediante el parámetro *pConfiguration* de la función [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .</span><span class="sxs-lookup"><span data-stu-id="92d36-109">You can set this attribute on the protected media path (PMP) session by using the *pConfiguration* parameter of the [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function.</span></span>

<span data-ttu-id="92d36-110">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="92d36-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="92d36-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92d36-111">Requirements</span></span>



| <span data-ttu-id="92d36-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="92d36-112">Requirement</span></span> | <span data-ttu-id="92d36-113">Value</span><span class="sxs-lookup"><span data-stu-id="92d36-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="92d36-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="92d36-114">Minimum supported client</span></span><br/> | <span data-ttu-id="92d36-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="92d36-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="92d36-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="92d36-116">Minimum supported server</span></span><br/> | <span data-ttu-id="92d36-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="92d36-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="92d36-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="92d36-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="92d36-119"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="92d36-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92d36-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="92d36-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92d36-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="92d36-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="92d36-122">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="92d36-122">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="92d36-123">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="92d36-123">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="92d36-124">Atributos de la sesión multimedia</span><span class="sxs-lookup"><span data-stu-id="92d36-124">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> <dt>

[<span data-ttu-id="92d36-125">Sesión de medios de PMP</span><span class="sxs-lookup"><span data-stu-id="92d36-125">PMP Media Session</span></span>](pmp-media-session.md)
</dt> </dl>

 

 




