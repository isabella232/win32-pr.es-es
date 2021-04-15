---
title: Configurar secuencias de texto
description: Configurar secuencias de texto
ms.assetid: d99baac5-69e5-4e0a-9cd6-35b288d8181a
keywords:
- flujos, configurar secuencias de texto
- códecs, configurar secuencias de texto
- secuencias de texto, configurar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460369eaae02f636f8ddda8bcca4f29ecfc2e1e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486814"
---
# <a name="configuring-text-streams"></a><span data-ttu-id="17c7d-106">Configurar secuencias de texto</span><span class="sxs-lookup"><span data-stu-id="17c7d-106">Configuring Text Streams</span></span>

<span data-ttu-id="17c7d-107">Los flujos de texto son esencialmente los mismos que los flujos arbitrarios personalizados.</span><span class="sxs-lookup"><span data-stu-id="17c7d-107">Text streams are essentially the same as custom arbitrary streams.</span></span> <span data-ttu-id="17c7d-108">No hay información de configuración asociada a una secuencia de texto para identificar el tipo de codificación de texto, por lo que el objeto de escritor no puede comprobar los ejemplos.</span><span class="sxs-lookup"><span data-stu-id="17c7d-108">There is no configuration information associated with a text stream to identify the type of text encoding, so the writer object cannot verify samples.</span></span>

<span data-ttu-id="17c7d-109">Para configurar una secuencia de texto, debe asegurarse de que la estructura de [**\_ \_ tipo de medio de WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) contiene un tipo de medio principal de texto WMMEDIATYPE \_ .</span><span class="sxs-lookup"><span data-stu-id="17c7d-109">To configure a text stream, you must ensure that the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure contains a major media type of WMMEDIATYPE\_TEXT.</span></span> <span data-ttu-id="17c7d-110">También debe establecer una velocidad de bits y una ventana de búfer para la secuencia.</span><span class="sxs-lookup"><span data-stu-id="17c7d-110">You must also set a bit rate and buffer window for the stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="17c7d-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="17c7d-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17c7d-112">**Calcular la velocidad de bits y los valores de la ventana de búfer para flujos arbitrarios**</span><span class="sxs-lookup"><span data-stu-id="17c7d-112">**Calculating Bit Rate and Buffer Window Values for Arbitrary Streams**</span></span>](calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="17c7d-113">**Configuración común para todos los flujos**</span><span class="sxs-lookup"><span data-stu-id="17c7d-113">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="17c7d-114">**Configuración de tipos de flujo arbitrarios**</span><span class="sxs-lookup"><span data-stu-id="17c7d-114">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> <dt>

[<span data-ttu-id="17c7d-115">**Secuencias de texto**</span><span class="sxs-lookup"><span data-stu-id="17c7d-115">**Text Streams**</span></span>](text-streams.md)
</dt> </dl>

 

 




