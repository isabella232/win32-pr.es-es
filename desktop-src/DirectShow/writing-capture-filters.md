---
description: Escribir filtros de captura
ms.assetid: 7dfd1009-da09-49dc-a200-3d7a9f1c70c1
title: Escribir filtros de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de1a64de2b56dbc0728432307036fc46387f539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687717"
---
# <a name="writing-capture-filters"></a><span data-ttu-id="6ef8f-103">Escribir filtros de captura</span><span class="sxs-lookup"><span data-stu-id="6ef8f-103">Writing Capture Filters</span></span>

<span data-ttu-id="6ef8f-104">No se recomienda escribir un filtro de captura de audio o vídeo para DirectShow.</span><span class="sxs-lookup"><span data-stu-id="6ef8f-104">Writing an audio or video capture filter for DirectShow is not recommended.</span></span> <span data-ttu-id="6ef8f-105">En su lugar, DirectShow proporciona compatibilidad automática para dispositivos de captura de audio y vídeo, mediante filtros de contenedor y el [enumerador de dispositivos de sistema](system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="6ef8f-105">Instead, DirectShow provides automatic support for audio and video capture devices, using wrapper filters and the [System Device Enumerator](system-device-enumerator.md).</span></span> <span data-ttu-id="6ef8f-106">Para obtener más información acerca de la implementación de un controlador de dispositivo, consulte la documentación del kit de controladores de Windows (WDK).</span><span class="sxs-lookup"><span data-stu-id="6ef8f-106">For more information about implementing a device driver, refer to the Windows Driver Kit (WDK) documentation.</span></span>

<span data-ttu-id="6ef8f-107">Esta sección está destinada únicamente a los desarrolladores que necesitan capturar algún tipo de datos personalizados desde un dispositivo de hardware inusual.</span><span class="sxs-lookup"><span data-stu-id="6ef8f-107">This section is intended only for developers who need to capture some kind of custom data from an unusual hardware device.</span></span>

<span data-ttu-id="6ef8f-108">Este artículo contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="6ef8f-108">This article contains the following sections:</span></span>

-   [<span data-ttu-id="6ef8f-109">Requisitos de PIN para los filtros de captura</span><span class="sxs-lookup"><span data-stu-id="6ef8f-109">Pin Requirements for Capture Filters</span></span>](pin-requirements-for-capture-filters.md)
-   [<span data-ttu-id="6ef8f-110">Implementación de un PIN de versión preliminar (opcional)</span><span class="sxs-lookup"><span data-stu-id="6ef8f-110">Implementing a Preview Pin (Optional)</span></span>](implementing-a-preview-pin--optional.md)
-   [<span data-ttu-id="6ef8f-111">Generar datos en un filtro de captura</span><span class="sxs-lookup"><span data-stu-id="6ef8f-111">Producing Data in a Capture Filter</span></span>](producing-data-in-a-capture-filter.md)

## <a name="related-topics"></a><span data-ttu-id="6ef8f-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6ef8f-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ef8f-113">Escribir filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="6ef8f-113">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



