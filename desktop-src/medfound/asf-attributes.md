---
description: Atributos ASF
ms.assetid: c1570669-6e9c-4614-af4d-2a148f12e36f
title: Atributos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ccf09542c8b96cc262cbe029111d3cb74e5b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696188"
---
# <a name="asf-attributes"></a><span data-ttu-id="63091-103">Atributos ASF</span><span class="sxs-lookup"><span data-stu-id="63091-103">ASF Attributes</span></span>

### <a name="profile-attributes"></a><span data-ttu-id="63091-104">Atributos de perfil</span><span class="sxs-lookup"><span data-stu-id="63091-104">Profile Attributes</span></span>

<span data-ttu-id="63091-105">Los siguientes atributos se aplican a los perfiles ASF.</span><span class="sxs-lookup"><span data-stu-id="63091-105">The following attributes apply to ASF profiles.</span></span>



| <span data-ttu-id="63091-106">Atributo</span><span class="sxs-lookup"><span data-stu-id="63091-106">Attribute</span></span>                                                                      | <span data-ttu-id="63091-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="63091-107">Description</span></span>                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="63091-108">**MF \_ ASFPROFILE \_ MAXPACKETSIZE**</span><span class="sxs-lookup"><span data-stu-id="63091-108">**MF\_ASFPROFILE\_MAXPACKETSIZE**</span></span>](mf-asfprofile-maxpacketsize-attribute.md) | <span data-ttu-id="63091-109">Especifica el tamaño de paquete máximo para un archivo ASF, en bytes.</span><span class="sxs-lookup"><span data-stu-id="63091-109">Specifies the maximum packet size for an ASF file, in bytes.</span></span> |
| [<span data-ttu-id="63091-110">**MF \_ ASFPROFILE \_ MINPACKETSIZE**</span><span class="sxs-lookup"><span data-stu-id="63091-110">**MF\_ASFPROFILE\_MINPACKETSIZE**</span></span>](mf-asfprofile-minpacketsize-attribute.md) | <span data-ttu-id="63091-111">Especifica el tamaño mínimo de paquete para un archivo ASF, en bytes.</span><span class="sxs-lookup"><span data-stu-id="63091-111">Specifies the minimum packet size for an ASF file, in bytes.</span></span> |



 

### <a name="stream-configuration-attributes"></a><span data-ttu-id="63091-112">Atributos de configuración de secuencia</span><span class="sxs-lookup"><span data-stu-id="63091-112">Stream Configuration Attributes</span></span>

<span data-ttu-id="63091-113">Los siguientes atributos se aplican al objeto de configuración de secuencia ASF.</span><span class="sxs-lookup"><span data-stu-id="63091-113">The following attributes apply to the ASF stream configuration object.</span></span>



| <span data-ttu-id="63091-114">Atributo</span><span class="sxs-lookup"><span data-stu-id="63091-114">Attribute</span></span>                                                                              | <span data-ttu-id="63091-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="63091-115">Description</span></span>                                                                   |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="63091-116">**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**</span><span class="sxs-lookup"><span data-stu-id="63091-116">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**</span></span>](mf-asfstreamconfig-leakybucket1-attribute.md) | <span data-ttu-id="63091-117">Establece los parámetros de "cubo de fugas" promedio para codificar un archivo de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="63091-117">Sets the average "leaky bucket" parameters for encoding a Windows Media file.</span></span> |
| [<span data-ttu-id="63091-118">**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**</span><span class="sxs-lookup"><span data-stu-id="63091-118">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**</span></span>](mf-asfstreamconfig-leakybucket2-attribute.md) | <span data-ttu-id="63091-119">Establece los parámetros de límite máximo de "depósito de fugas" para codificar un archivo de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="63091-119">Sets the peak "leaky bucket" parameters for encoding a Windows Media file.</span></span>    |



 

### <a name="media-buffer-attributes"></a><span data-ttu-id="63091-120">Atributos de búfer de medios</span><span class="sxs-lookup"><span data-stu-id="63091-120">Media Buffer Attributes</span></span>

<span data-ttu-id="63091-121">Los siguientes atributos se aplican a los búferes de medios para los paquetes ASF.</span><span class="sxs-lookup"><span data-stu-id="63091-121">The following attributes apply to media buffers for ASF packets.</span></span>



| <span data-ttu-id="63091-122">Atributo</span><span class="sxs-lookup"><span data-stu-id="63091-122">Attribute</span></span>                                                                          | <span data-ttu-id="63091-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="63091-123">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="63091-124">**\_límite de paquetes de MFASFSPLITTER \_**</span><span class="sxs-lookup"><span data-stu-id="63091-124">**MFASFSPLITTER\_PACKET\_BOUNDARY**</span></span>](mfasfsplitter-packet-boundary-attribute.md) | <span data-ttu-id="63091-125">Especifica si un búfer contiene el inicio de un paquete de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="63091-125">Specifies whether a buffer contains the start of an Advanced Systems Format (ASF) packet.</span></span> |



 

### <a name="presentation-descriptor-attributes"></a><span data-ttu-id="63091-126">Atributos de descriptor de presentación</span><span class="sxs-lookup"><span data-stu-id="63091-126">Presentation Descriptor Attributes</span></span>

<span data-ttu-id="63091-127">Para obtener una lista de los atributos que se aplican a los descriptores de presentación ASF, vea [atributos de descriptor de presentación](presentation-descriptor-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="63091-127">For a list of attributes that apply to ASF presentation descriptors, see [Presentation Descriptor Attributes](presentation-descriptor-attributes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="63091-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="63091-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63091-129">**IMFASFProfile**</span><span class="sxs-lookup"><span data-stu-id="63091-129">**IMFASFProfile**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile)
</dt> <dt>

[<span data-ttu-id="63091-130">**IMFASFStreamConfig**</span><span class="sxs-lookup"><span data-stu-id="63091-130">**IMFASFStreamConfig**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig)
</dt> <dt>

[<span data-ttu-id="63091-131">Atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="63091-131">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 



