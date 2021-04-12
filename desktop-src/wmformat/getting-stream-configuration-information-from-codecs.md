---
title: Obtención de información de configuración de la secuencia de códecs
description: Obtención de información de configuración de la secuencia de códecs
ms.assetid: 76c734a1-6fe4-4958-8773-a65f5ced80c6
keywords:
- flujos, configuraciones de códecs
- códecs, obtener configuraciones de secuencia de
- secuencias, formatos de códecs
- códecs, formatos
- streams, interfaz IWMCodecInfo
- IWMCodecInfo, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8657e03af97f9e4f1cae953d541c0e4369da193
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/21/2020
ms.locfileid: "104420435"
---
# <a name="getting-stream-configuration-information-from-codecs"></a><span data-ttu-id="2df20-109">Obtención de información de configuración de la secuencia de códecs</span><span class="sxs-lookup"><span data-stu-id="2df20-109">Getting Stream Configuration Information from Codecs</span></span>

<span data-ttu-id="2df20-110">En el caso de las secuencias de audio y vídeo que usan los códecs de Windows Media Audio y vídeo, debe obtener los valores de las estructuras de configuración de la secuencia del códec que desee usar.</span><span class="sxs-lookup"><span data-stu-id="2df20-110">For audio and video streams that use the Windows Media Audio and Video codecs, you should get the values for the stream configuration structures from the codec you want to use.</span></span> <span data-ttu-id="2df20-111">Aunque es posible establecer estos valores personalmente, el uso de los códecs garantiza que los valores sean precisos.</span><span class="sxs-lookup"><span data-stu-id="2df20-111">While it is possible to set these values yourself, using the codecs ensures that the values are accurate.</span></span> <span data-ttu-id="2df20-112">No debe modificar los valores de estas estructuras a menos que la documentación recomiende específicamente un cambio determinado.</span><span class="sxs-lookup"><span data-stu-id="2df20-112">You should not alter the values in these structures unless the documentation specifically recommends a particular change.</span></span>

<span data-ttu-id="2df20-113">La información de los códecs tiene formato de códec.</span><span class="sxs-lookup"><span data-stu-id="2df20-113">Information from the codecs comes in the form of codec formats.</span></span> <span data-ttu-id="2df20-114">Cada formato de códec es un formato de flujo único compatible con el códec.</span><span class="sxs-lookup"><span data-stu-id="2df20-114">Each codec format is a single stream format supported by the codec.</span></span> <span data-ttu-id="2df20-115">Para obtener más información sobre los formatos de secuencias, vea [formatos](formats.md).</span><span class="sxs-lookup"><span data-stu-id="2df20-115">For more information about stream formats, see [Formats](formats.md).</span></span>

<span data-ttu-id="2df20-116">Puede solicitar información de los códecs de Windows Media con las interfaces [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo), [**IWMCodecInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2)y [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) del objeto de administrador de perfiles.</span><span class="sxs-lookup"><span data-stu-id="2df20-116">You can request information from the Windows Media codecs using the [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo), [**IWMCodecInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2), and [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) interfaces of the profile manager object.</span></span> <span data-ttu-id="2df20-117">Para obtener la interfaz [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) de un objeto de administrador de perfiles, llame a la función [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="2df20-117">To get the [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface of a profile manager object, call the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span> <span data-ttu-id="2df20-118">Llame a **QueryInterface** en **IWMProfileManager** para obtener **IWMCodecInfo3**.</span><span class="sxs-lookup"><span data-stu-id="2df20-118">Call **QueryInterface** on **IWMProfileManager** to get **IWMCodecInfo3**.</span></span>

<span data-ttu-id="2df20-119">En las secciones siguientes se describe cómo obtener la información que necesita.</span><span class="sxs-lookup"><span data-stu-id="2df20-119">The following sections describe how to get the information you need.</span></span>



| <span data-ttu-id="2df20-120">Sección</span><span class="sxs-lookup"><span data-stu-id="2df20-120">Section</span></span>                                                                                                | <span data-ttu-id="2df20-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="2df20-121">Description</span></span>                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2df20-122">Para enumerar todos los códecs de Windows Media instalados</span><span class="sxs-lookup"><span data-stu-id="2df20-122">To Enumerate All Installed Windows Media Codecs</span></span>](to-enumerate-all-installed-windows-media-codecs.md) | <span data-ttu-id="2df20-123">Describe cómo usar los métodos de las interfaces **IWMCodecInfo** y **IWMCodecInfo2** para recuperar el nombre y el índice de códec de cada códec de Windows Media instalado.</span><span class="sxs-lookup"><span data-stu-id="2df20-123">Describes how to use the methods of the **IWMCodecInfo** and **IWMCodecInfo2** interfaces to retrieve the name and codec index of each Windows Media codec installed.</span></span> |
| [<span data-ttu-id="2df20-124">Para enumerar formatos de códecs</span><span class="sxs-lookup"><span data-stu-id="2df20-124">To Enumerate Codec Formats</span></span>](to-enumerate-codec-formats.md)                                           | <span data-ttu-id="2df20-125">Describe cómo obtener objetos de configuración de secuencia a partir de códecs para su uso en los perfiles.</span><span class="sxs-lookup"><span data-stu-id="2df20-125">Describes how to get stream configuration objects from codecs for use in your profiles.</span></span>                                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="2df20-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2df20-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2df20-127">**Configuración de secuencias**</span><span class="sxs-lookup"><span data-stu-id="2df20-127">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> </dl>

 

 




