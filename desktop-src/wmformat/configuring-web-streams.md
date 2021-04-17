---
title: Configuración de secuencias Web
description: Configuración de secuencias Web
ms.assetid: 1eeb6243-5095-4dba-994c-2083beda7b78
keywords:
- flujos, configurar secuencias Web
- códecs, configurar secuencias Web
- Flujos web, configurar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27c91c36788b858b2378ebf46b553f076c5ec490
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357589"
---
# <a name="configuring-web-streams"></a><span data-ttu-id="2be31-106">Configuración de secuencias Web</span><span class="sxs-lookup"><span data-stu-id="2be31-106">Configuring Web Streams</span></span>

<span data-ttu-id="2be31-107">Las secuencias web son un tipo especializado de flujo de transferencia de archivos que se usa para proporcionar los archivos asociados a un sitio web en un único flujo.</span><span class="sxs-lookup"><span data-stu-id="2be31-107">Web streams are a specialized type of file transfer stream used to deliver the files associated with a Web site in a single stream.</span></span> <span data-ttu-id="2be31-108">La configuración de la secuencia Web se resume en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="2be31-108">Web stream configuration is summarized in the following table.</span></span>



| <span data-ttu-id="2be31-109">Configuración</span><span class="sxs-lookup"><span data-stu-id="2be31-109">Setting</span></span>                                            | <span data-ttu-id="2be31-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="2be31-110">Description</span></span>                                                                       |
|----------------------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="2be31-111">**Tipo de medio de WM \_ \_ . majortype**</span><span class="sxs-lookup"><span data-stu-id="2be31-111">**WM\_MEDIA\_TYPE.majortype**</span></span>                      | <span data-ttu-id="2be31-112">Establézcalo en WMMEDIATYPE \_ FileTransfer.</span><span class="sxs-lookup"><span data-stu-id="2be31-112">Set to WMMEDIATYPE\_FileTransfer.</span></span>                                                 |
| <span data-ttu-id="2be31-113">**Tipo de medio de WM \_ \_ . SubType**</span><span class="sxs-lookup"><span data-stu-id="2be31-113">**WM\_MEDIA\_TYPE.subtype**</span></span>                        | <span data-ttu-id="2be31-114">Establezca en WMMEDIASUBTYPE \_ Webstream.</span><span class="sxs-lookup"><span data-stu-id="2be31-114">Set to WMMEDIASUBTYPE\_WebStream.</span></span>                                                 |
| <span data-ttu-id="2be31-115">**Tipo de medio de WM \_ \_ . bFixedSizeSamples**</span><span class="sxs-lookup"><span data-stu-id="2be31-115">**WM\_MEDIA\_TYPE.bFixedSizeSamples**</span></span>              | <span data-ttu-id="2be31-116">Establézcalo en false.</span><span class="sxs-lookup"><span data-stu-id="2be31-116">Set to False.</span></span>                                                                     |
| <span data-ttu-id="2be31-117">**Tipo de medio de WM \_ \_ . bTemporalCompression**</span><span class="sxs-lookup"><span data-stu-id="2be31-117">**WM\_MEDIA\_TYPE.bTemporalCompression**</span></span>           | <span data-ttu-id="2be31-118">Se establece en True.</span><span class="sxs-lookup"><span data-stu-id="2be31-118">Set to True.</span></span>                                                                      |
| <span data-ttu-id="2be31-119">**Tipo de medio de WM \_ \_ . lSampleSize**</span><span class="sxs-lookup"><span data-stu-id="2be31-119">**WM\_MEDIA\_TYPE.lSampleSize**</span></span>                    | <span data-ttu-id="2be31-120">Establecer en 0.</span><span class="sxs-lookup"><span data-stu-id="2be31-120">Set to 0.</span></span>                                                                         |
| <span data-ttu-id="2be31-121">**Tipo de medio de WM \_ \_ . FormatType**</span><span class="sxs-lookup"><span data-stu-id="2be31-121">**WM\_MEDIA\_TYPE.formattype**</span></span>                     | <span data-ttu-id="2be31-122">Establezca en WMFORMAT \_ Webstream.</span><span class="sxs-lookup"><span data-stu-id="2be31-122">Set to WMFORMAT\_WebStream.</span></span>                                                       |
| <span data-ttu-id="2be31-123">**Tipo de medio de WM \_ \_ . pUnk**</span><span class="sxs-lookup"><span data-stu-id="2be31-123">**WM\_MEDIA\_TYPE.pUnk**</span></span>                           | <span data-ttu-id="2be31-124">Se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="2be31-124">Set to **NULL**.</span></span>                                                                  |
| <span data-ttu-id="2be31-125">**Tipo de medio de WM \_ \_ . cbFormat**</span><span class="sxs-lookup"><span data-stu-id="2be31-125">**WM\_MEDIA\_TYPE.cbFormat**</span></span>                       | <span data-ttu-id="2be31-126">Establézcalo en `sizeof(WMT_WEBSTREAM_FORMAT)`.</span><span class="sxs-lookup"><span data-stu-id="2be31-126">Set to `sizeof(WMT_WEBSTREAM_FORMAT)`.</span></span>                                            |
| <span data-ttu-id="2be31-127">**Tipo de medio de WM \_ \_ . pbFormat**</span><span class="sxs-lookup"><span data-stu-id="2be31-127">**WM\_MEDIA\_TYPE.pbFormat**</span></span>                       | <span data-ttu-id="2be31-128">Se establece en la dirección de una estructura **de \_ \_ formato de Webstream WMT** configurada correctamente.</span><span class="sxs-lookup"><span data-stu-id="2be31-128">Set to the address of a properly configured **WMT\_WEBSTREAM\_FORMAT** structure.</span></span> |
| <span data-ttu-id="2be31-129">**\_Formato WEBstream de WMT \_ . cbSampleHeaderFixedData**</span><span class="sxs-lookup"><span data-stu-id="2be31-129">**WMT\_WEBSTREAM\_FORMAT.cbSampleHeaderFixedData**</span></span> | <span data-ttu-id="2be31-130">Establézcalo en `sizeof(WMT_WEBSTREAM_SAMPLE_HEADER)`.</span><span class="sxs-lookup"><span data-stu-id="2be31-130">Set to `sizeof(WMT_WEBSTREAM_SAMPLE_HEADER)`.</span></span>                                     |
| <span data-ttu-id="2be31-131">**\_Formato WEBstream de WMT \_ . wVersion**</span><span class="sxs-lookup"><span data-stu-id="2be31-131">**WMT\_WEBSTREAM\_FORMAT.wVersion**</span></span>                | <span data-ttu-id="2be31-132">establézcalo en 1.</span><span class="sxs-lookup"><span data-stu-id="2be31-132">Set to 1.</span></span>                                                                         |
| <span data-ttu-id="2be31-133">**\_Formato WEBstream de WMT \_ . wreserved**</span><span class="sxs-lookup"><span data-stu-id="2be31-133">**WMT\_WEBSTREAM\_FORMAT.wreserved**</span></span>               | <span data-ttu-id="2be31-134">Establecer en 0.</span><span class="sxs-lookup"><span data-stu-id="2be31-134">Set to 0.</span></span>                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="2be31-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2be31-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2be31-136">**Configuración común para todos los flujos**</span><span class="sxs-lookup"><span data-stu-id="2be31-136">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="2be31-137">**Configuración de tipos de flujo arbitrarios**</span><span class="sxs-lookup"><span data-stu-id="2be31-137">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> <dt>

[<span data-ttu-id="2be31-138">**Secuencias Web**</span><span class="sxs-lookup"><span data-stu-id="2be31-138">**Web Streams**</span></span>](web-streams.md)
</dt> </dl>

 

 




