---
description: Contiene el CLSID de un administrador de calidad para la sesión multimedia.
ms.assetid: 24b4a5e3-84f1-44d0-a8ac-75c127ec8a8a
title: MF_SESSION_QUALITY_MANAGER atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 736f37a46c3aeb4216243f058ea7fb8a33bdbd1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360930"
---
# <a name="mf_session_quality_manager-attribute"></a><span data-ttu-id="a5a4e-103">\_Atributo de \_ Administrador de calidad de sesión MF \_</span><span class="sxs-lookup"><span data-stu-id="a5a4e-103">MF\_SESSION\_QUALITY\_MANAGER attribute</span></span>

<span data-ttu-id="a5a4e-104">Contiene el CLSID de un administrador de calidad para la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="a5a4e-104">Contains the CLSID of a quality manager for the Media Session.</span></span>

## <a name="data-type"></a><span data-ttu-id="a5a4e-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a5a4e-105">Data type</span></span>

<span data-ttu-id="a5a4e-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="a5a4e-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="a5a4e-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a5a4e-107">Remarks</span></span>

<span data-ttu-id="a5a4e-108">Puede usar este atributo para proporcionar un administrador de calidad personalizado para la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="a5a4e-108">You can use this attribute to provide a custom quality manager for the Media Session.</span></span>

<span data-ttu-id="a5a4e-109">Establezca este atributo mediante el parámetro *pConfiguration* de la función [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) o [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .</span><span class="sxs-lookup"><span data-stu-id="a5a4e-109">Set this attribute by using the *pConfiguration* parameter of the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) or [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function.</span></span>

<span data-ttu-id="a5a4e-110">Si se establece este atributo, la sesión multimedia llama a **CoCreateInstance** con el CLSID especificado para crear el administrador de calidad.</span><span class="sxs-lookup"><span data-stu-id="a5a4e-110">If this attribute is set, the Media Session calls **CoCreateInstance** with the specified CLSID to create the quality manager.</span></span> <span data-ttu-id="a5a4e-111">El objeto creado por este CLSID debe exponer la interfaz [**IMFQualityManager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager) .</span><span class="sxs-lookup"><span data-stu-id="a5a4e-111">The object created by this CLSID must expose the [**IMFQualityManager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager) interface.</span></span>

<span data-ttu-id="a5a4e-112">Si no se establece este atributo, la sesión multimedia crea el administrador de calidad predeterminado proporcionado en Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="a5a4e-112">If this attribute is not set, the Media Session creates the default quality manager provided in Media Foundation.</span></span>

<span data-ttu-id="a5a4e-113">Si desea ejecutar la sesión de medios sin administrador de calidad, establezca este atributo en **GUID \_ null**.</span><span class="sxs-lookup"><span data-stu-id="a5a4e-113">If you want to run the Media Session with no quality manager at all, set this attribute to **GUID\_NULL**.</span></span>

<span data-ttu-id="a5a4e-114">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="a5a4e-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5a4e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5a4e-115">Requirements</span></span>



| <span data-ttu-id="a5a4e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5a4e-116">Requirement</span></span> | <span data-ttu-id="a5a4e-117">Value</span><span class="sxs-lookup"><span data-stu-id="a5a4e-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a5a4e-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5a4e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a5a4e-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a5a4e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a5a4e-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5a4e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a5a4e-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a5a4e-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a5a4e-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a5a4e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5a4e-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5a4e-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5a4e-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="a5a4e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5a4e-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a5a4e-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a5a4e-126">**IMFAttributes:: GetGUID**</span><span class="sxs-lookup"><span data-stu-id="a5a4e-126">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="a5a4e-127">**IMFAttributes:: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="a5a4e-127">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="a5a4e-128">Atributos de la sesión multimedia</span><span class="sxs-lookup"><span data-stu-id="a5a4e-128">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> </dl>

 

 




