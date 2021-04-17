---
description: Proporciona una interfaz de devolución de llamada para que la aplicación reciba un objeto de habilitador de contenido de la sesión de la ruta de acceso a medios protegidos (PMP).
ms.assetid: 66482541-63d4-439b-862f-7507605af5d8
title: MF_SESSION_CONTENT_PROTECTION_MANAGER atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c90321ae3c10fd7fa2ec39a4fb478e256291b049
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716491"
---
# <a name="mf_session_content_protection_manager-attribute"></a><span data-ttu-id="accb9-103">\_Atributo de \_ Administrador de protección de contenido de sesión MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="accb9-103">MF\_SESSION\_CONTENT\_PROTECTION\_MANAGER attribute</span></span>

<span data-ttu-id="accb9-104">Proporciona una interfaz de devolución de llamada para que la aplicación reciba un objeto de habilitador de contenido de la sesión de la ruta de acceso a medios protegidos (PMP).</span><span class="sxs-lookup"><span data-stu-id="accb9-104">Provides a callback interface for the application to receive a content enabler object from the protected media path (PMP) session.</span></span>

## <a name="data-type"></a><span data-ttu-id="accb9-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="accb9-105">Data type</span></span>

<span data-ttu-id="accb9-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="accb9-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="accb9-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="accb9-107">Remarks</span></span>

<span data-ttu-id="accb9-108">El valor de este atributo es un puntero a la interfaz [_ *IMFContentProtectionManager* \*](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="accb9-108">The value of this attribute is a pointer to the application's [_ *IMFContentProtectionManager*\*](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) interface.</span></span>

<span data-ttu-id="accb9-109">Establezca este atributo en la sesión de PMP mediante el parámetro *pConfiguration* de la función [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .</span><span class="sxs-lookup"><span data-stu-id="accb9-109">Set this attribute on the PMP session by using the *pConfiguration* parameter of the [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function.</span></span>

<span data-ttu-id="accb9-110">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="accb9-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="accb9-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="accb9-111">Requirements</span></span>



| <span data-ttu-id="accb9-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="accb9-112">Requirement</span></span> | <span data-ttu-id="accb9-113">Value</span><span class="sxs-lookup"><span data-stu-id="accb9-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="accb9-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="accb9-114">Minimum supported client</span></span><br/> | <span data-ttu-id="accb9-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="accb9-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="accb9-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="accb9-116">Minimum supported server</span></span><br/> | <span data-ttu-id="accb9-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="accb9-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="accb9-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="accb9-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="accb9-119"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="accb9-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="accb9-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="accb9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="accb9-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="accb9-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="accb9-122">**IMFAttributes::GetUnknown**</span><span class="sxs-lookup"><span data-stu-id="accb9-122">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="accb9-123">**IMFAttributes:: Setunknown (**</span><span class="sxs-lookup"><span data-stu-id="accb9-123">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="accb9-124">Atributos de la sesión multimedia</span><span class="sxs-lookup"><span data-stu-id="accb9-124">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> <dt>

[<span data-ttu-id="accb9-125">Cómo reproducir archivos multimedia protegidos</span><span class="sxs-lookup"><span data-stu-id="accb9-125">How to Play Protected Media Files</span></span>](how-to-play-protected-media-files.md)
</dt> </dl>

 

 




