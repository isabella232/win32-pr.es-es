---
title: Plantillas de conformidad de dispositivos
description: Plantillas de conformidad de dispositivos
ms.assetid: 5172ab39-819a-4d74-8e6e-b275b43f664c
keywords:
- SDK de Windows Media Format, plantillas de conformidad de dispositivos
- códecs, plantillas de conformidad de dispositivos
- plantillas de conformidad de dispositivos, acerca de
- plantillas, plantillas de conformidad de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eccb88b372f9e0eb463d88db83d70102408a7a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357685"
---
# <a name="device-conformance-templates"></a><span data-ttu-id="5f3a8-107">Plantillas de conformidad de dispositivos</span><span class="sxs-lookup"><span data-stu-id="5f3a8-107">Device Conformance Templates</span></span>

<span data-ttu-id="5f3a8-108">Los códecs de Windows Media 9 Series admiten plantillas de conformidad de dispositivos, que son intervalos definidos de valores de configuración de secuencia y algoritmos de códecs.</span><span class="sxs-lookup"><span data-stu-id="5f3a8-108">The Windows Media 9 Series codecs support device conformance templates, which are defined ranges of stream configuration settings and codec algorithms.</span></span> <span data-ttu-id="5f3a8-109">Cada plantilla define los intervalos de valores adecuados para determinados dispositivos.</span><span class="sxs-lookup"><span data-stu-id="5f3a8-109">Each template defines the ranges of values appropriate for certain devices.</span></span>

<span data-ttu-id="5f3a8-110">En el pasado, los fabricantes de hardware que hacían que los dispositivos capaces de reproducir archivos ASF estaban trabajando con sus propios estándares.</span><span class="sxs-lookup"><span data-stu-id="5f3a8-110">In the past, the hardware manufacturers that made devices capable of playing ASF files were all working to their own standards.</span></span> <span data-ttu-id="5f3a8-111">Como resultado, la gama de funcionalidades es muy dispares en dispositivos similares que continúan hoy en día.</span><span class="sxs-lookup"><span data-stu-id="5f3a8-111">This resulted in the widely disparate range of capabilities on similar devices that continues today.</span></span>

<span data-ttu-id="5f3a8-112">Con las plantillas de conformidad de dispositivos, los códecs de Windows Media establecen una base común para dispositivos similares.</span><span class="sxs-lookup"><span data-stu-id="5f3a8-112">With device conformance templates, the Windows Media codecs establish common ground for similar devices.</span></span> <span data-ttu-id="5f3a8-113">Los fabricantes de hardware pueden indicar las plantillas a las que se ajustan los dispositivos, lo que permite a los creadores de contenido destinar con mayor seguridad sus archivos a los dispositivos de lectura.</span><span class="sxs-lookup"><span data-stu-id="5f3a8-113">Hardware manufacturers can state which templates their devices conform to, enabling content creators to more confidently target their files to reading devices.</span></span> <span data-ttu-id="5f3a8-114">También es más fácil que las aplicaciones de reproducción determinen si un archivo no es apropiado para el dispositivo antes de intentar reproducirlo.</span><span class="sxs-lookup"><span data-stu-id="5f3a8-114">It is also easier for player applications to determine whether a file is inappropriate for the device before attempting to play it.</span></span>

<span data-ttu-id="5f3a8-115">Una plantilla de conformidad de dispositivos se identifica mediante una cadena, que se almacena como un atributo de metadatos asociado con la secuencia a la que se aplica la plantilla.</span><span class="sxs-lookup"><span data-stu-id="5f3a8-115">A device conformance template is identified by a string, which is stored as a metadata attribute associated with the stream to which the template applies.</span></span> <span data-ttu-id="5f3a8-116">Para obtener una lista de las plantillas y sus cadenas y parámetros, vea parámetros de la [plantilla de conformidad de dispositivos](device-conformance-template-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="5f3a8-116">For a list of the templates and their strings and parameters, see [Device Conformance Template Parameters](device-conformance-template-parameters.md).</span></span>

<span data-ttu-id="5f3a8-117">Las plantillas de conformidad de dispositivos se admiten para todos los códecs de la serie Windows Media 9 y posteriores, excepto el códec de pantalla de Windows Media Video 9 y el códec Windows Media Audio 9 Lossless.</span><span class="sxs-lookup"><span data-stu-id="5f3a8-117">Device conformance templates are supported for all of the Windows Media 9 Series and later codecs except the Windows Media Video 9 Screen codec and the Windows Media Audio 9 Lossless codec.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5f3a8-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5f3a8-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f3a8-119">**Características del códec**</span><span class="sxs-lookup"><span data-stu-id="5f3a8-119">**Codec Features**</span></span>](codec-features.md)
</dt> <dt>

[<span data-ttu-id="5f3a8-120">**Trabajar con plantillas de cumplimiento de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="5f3a8-120">**Working with Device Conformance Templates**</span></span>](working-with-device-conformance-templates.md)
</dt> </dl>

 

 




