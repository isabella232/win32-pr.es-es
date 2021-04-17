---
description: Contiene el CLSID de un cargador de topología para la sesión multimedia.
ms.assetid: 672274fb-71fc-49ca-bab6-1fc4de21d17c
title: MF_SESSION_TOPOLOADER atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb5299e058862ad2d26b1fb9debe0028aba4703
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716953"
---
# <a name="mf_session_topoloader-attribute"></a><span data-ttu-id="08afd-103">\_Atributo TOPOLOADER de sesión MF \_</span><span class="sxs-lookup"><span data-stu-id="08afd-103">MF\_SESSION\_TOPOLOADER attribute</span></span>

<span data-ttu-id="08afd-104">Contiene el CLSID de un cargador de topología para la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="08afd-104">Contains the CLSID of a topology loader for the Media Session.</span></span>

## <a name="data-type"></a><span data-ttu-id="08afd-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="08afd-105">Data type</span></span>

<span data-ttu-id="08afd-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="08afd-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="08afd-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="08afd-107">Remarks</span></span>

<span data-ttu-id="08afd-108">Puede usar este atributo para proporcionar un cargador de topología personalizado para la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="08afd-108">You can use this attribute to provide a custom topology loader for the Media Session.</span></span>

<span data-ttu-id="08afd-109">Establezca este atributo mediante el parámetro *pConfiguration* de la función [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) o la función [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .</span><span class="sxs-lookup"><span data-stu-id="08afd-109">Set this attribute using the *pConfiguration* parameter of the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) function or the [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function.</span></span>

<span data-ttu-id="08afd-110">Si se establece este atributo, la sesión multimedia llama a **CoCreateInstance** con el CLSID especificado al crear el cargador de topología.</span><span class="sxs-lookup"><span data-stu-id="08afd-110">If this attribute is set, the Media Session calls **CoCreateInstance** with the specified CLSID when it creates the topology loader.</span></span> <span data-ttu-id="08afd-111">El objeto creado por este CLSID debe exponer la interfaz [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) .</span><span class="sxs-lookup"><span data-stu-id="08afd-111">The object created by this CLSID must expose the [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) interface.</span></span>

<span data-ttu-id="08afd-112">Si no se establece este atributo, la sesión multimedia crea el cargador de topología predeterminado proporcionado en Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="08afd-112">If this attribute is not set, the Media Session creates the default topology loader provided in Media Foundation.</span></span>

<span data-ttu-id="08afd-113">Un cargador de topología debe admitir apartamentos multiproceso.</span><span class="sxs-lookup"><span data-stu-id="08afd-113">A topology loader must support multithreaded apartments.</span></span> <span data-ttu-id="08afd-114">Debe registrar el cargador de topología como ThreadingModel = "both".</span><span class="sxs-lookup"><span data-stu-id="08afd-114">You should register the topology loader as ThreadingModel="Both".</span></span> <span data-ttu-id="08afd-115">Además, si usa el cargador de topología dentro de la ruta de acceso a medios protegidos (PMP), el cargador de topología debe ser un componente de confianza.</span><span class="sxs-lookup"><span data-stu-id="08afd-115">Also, if you are using the topology loader inside the protected media path (PMP), the topology loader must be a trusted component.</span></span> <span data-ttu-id="08afd-116">Para obtener más información, vea [ruta de acceso a medios protegidos](protected-media-path.md).</span><span class="sxs-lookup"><span data-stu-id="08afd-116">For more information, see [Protected Media Path](protected-media-path.md).</span></span>

<span data-ttu-id="08afd-117">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="08afd-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="08afd-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08afd-118">Requirements</span></span>



| <span data-ttu-id="08afd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="08afd-119">Requirement</span></span> | <span data-ttu-id="08afd-120">Value</span><span class="sxs-lookup"><span data-stu-id="08afd-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="08afd-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08afd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="08afd-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="08afd-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="08afd-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08afd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="08afd-124">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="08afd-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="08afd-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="08afd-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="08afd-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="08afd-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08afd-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="08afd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08afd-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="08afd-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="08afd-129">**IMFAttributes:: GetGUID**</span><span class="sxs-lookup"><span data-stu-id="08afd-129">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="08afd-130">**IMFAttributes:: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="08afd-130">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="08afd-131">Atributos de la sesión multimedia</span><span class="sxs-lookup"><span data-stu-id="08afd-131">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> <dt>

[<span data-ttu-id="08afd-132">Cargadores de topología personalizados</span><span class="sxs-lookup"><span data-stu-id="08afd-132">Custom Topology Loaders</span></span>](custom-topology-loaders.md)
</dt> </dl>

 

 




