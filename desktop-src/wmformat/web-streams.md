---
title: Secuencias Web
description: Secuencias Web
ms.assetid: 78a2c703-a3f8-4afc-85d3-1c0a8f5a52b5
keywords:
- SDK de Windows Media Format, secuencias Web
- Advanced Systems Format (ASF), streams Web
- ASF (formato de sistemas avanzados), secuencias Web
- Windows Media Format SDK, secuencias
- Advanced Systems Format (ASF), streams
- ASF (formato de sistemas avanzados), secuencias
- Secuencias Web, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710eb9903662d9707d575a09b55ec8e99a224c38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075651"
---
# <a name="web-streams"></a><span data-ttu-id="7258a-110">Secuencias Web</span><span class="sxs-lookup"><span data-stu-id="7258a-110">Web Streams</span></span>

<span data-ttu-id="7258a-111">Una secuencia web es como una secuencia de archivos en que contiene archivos de datos.</span><span class="sxs-lookup"><span data-stu-id="7258a-111">A Web stream is like a file stream in that it contains data files.</span></span> <span data-ttu-id="7258a-112">En una secuencia Web, estos archivos suelen ser páginas HTML y gráficos asociados en formato GIF o JPEG.</span><span class="sxs-lookup"><span data-stu-id="7258a-112">In a Web stream, these files are typically HTML pages and associated graphics in GIF or JPEG format.</span></span>

<span data-ttu-id="7258a-113">Las secuencias Web pueden ser especialmente útiles para los archivos ASF que se usan como presentaciones.</span><span class="sxs-lookup"><span data-stu-id="7258a-113">Web streams can be particularly useful for ASF files that are used as presentations.</span></span> <span data-ttu-id="7258a-114">Antes de la compatibilidad de las secuencias Web, las presentaciones tendrían direcciones URL en secuencias de scripts dentro de un archivo para que una página web se cargara en un tiempo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="7258a-114">Prior to the support of Web streams, presentations would have URLs in script streams within a file so that a Web page would load at a predetermined time.</span></span> <span data-ttu-id="7258a-115">La dificultad era que la congestión de la red podría provocar retrasos y crear una experiencia de visualización deficiente.</span><span class="sxs-lookup"><span data-stu-id="7258a-115">The difficulty was that network congestion could cause delays and create a poor viewing experience.</span></span>

<span data-ttu-id="7258a-116">Con las secuencias Web, las partes constituyentes de las páginas web pueden incluirse en el archivo ASF como una secuencia.</span><span class="sxs-lookup"><span data-stu-id="7258a-116">With Web streams, the constituent parts of Web pages can be included in the ASF file as a stream.</span></span> <span data-ttu-id="7258a-117">A medida que se reciben los archivos, se pueden almacenar en caché para que, cuando el comando para mostrar (o representar) una dirección URL se entregue, se pueda acceder al instante mediante un explorador.</span><span class="sxs-lookup"><span data-stu-id="7258a-117">As the files are received, they can be cached so that, when the command to display (or render) a URL is delivered, they can be instantly accessed by a browser.</span></span> <span data-ttu-id="7258a-118">Esto permite una reproducción fluida y coherente.</span><span class="sxs-lookup"><span data-stu-id="7258a-118">This enables smooth, consistent playback.</span></span> <span data-ttu-id="7258a-119">El comando Render se entrega en la propia secuencia Web, no como un comando de script en una secuencia independiente.</span><span class="sxs-lookup"><span data-stu-id="7258a-119">The render command is delivered in the Web stream itself, not as a script command in a separate stream.</span></span>

<span data-ttu-id="7258a-120">Se recomienda que las secuencias web creadas con el SDK de Windows Media Format 9 series o posterior se les proporcione el número de versión 1.</span><span class="sxs-lookup"><span data-stu-id="7258a-120">It is recommended that Web streams created by using the Windows Media Format 9 Series SDK, or later be given the version number 1.</span></span> <span data-ttu-id="7258a-121">Este valor se especifica en la estructura de [**\_ \_ formato de Webstream WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) en el miembro **wVersion** .</span><span class="sxs-lookup"><span data-stu-id="7258a-121">This value is specified in the [**WMT\_WEBSTREAM\_FORMAT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) structure in the **wVersion** member.</span></span> <span data-ttu-id="7258a-122">El propio SDK no hace nada para aplicar esta versión.</span><span class="sxs-lookup"><span data-stu-id="7258a-122">The SDK itself does nothing to enforce this version.</span></span>

> [!Note]  
> <span data-ttu-id="7258a-123">Al conectarse a secuencias de difusión en directo que tienen secuencias Web, es posible que el usuario reciba un comando de representación antes de que el archivo especificado se encuentra realmente en la caché local.</span><span class="sxs-lookup"><span data-stu-id="7258a-123">When connecting to live broadcast streams that have Web streams, it is possible that the user may receive a render command before the specified file is actually in the local cache.</span></span> <span data-ttu-id="7258a-124">A menos que la aplicación controle esta condición, el explorador mostrará el error "página no encontrada".</span><span class="sxs-lookup"><span data-stu-id="7258a-124">Unless your application handles this condition, the browser will display a "Page not found" error.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="7258a-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7258a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7258a-126">**Flujos arbitrarios**</span><span class="sxs-lookup"><span data-stu-id="7258a-126">**Arbitrary Streams**</span></span>](arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="7258a-127">**Configuración de secuencias Web**</span><span class="sxs-lookup"><span data-stu-id="7258a-127">**Configuring Web Streams**</span></span>](configuring-web-streams.md)
</dt> </dl>

 

 




