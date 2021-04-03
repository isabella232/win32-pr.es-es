---
title: Consultas de línea y control de audio
description: Consultas de línea y control de audio
ms.assetid: f0954fc7-9961-410a-a638-a7025fb2616a
keywords:
- audio multimedia, controles de mezclador
- audio, controles de mezclador
- Mezcladores de audio, líneas de audio
- líneas de audio
- Mezcladores de audio, controles
- mezcladores, controles
- mezcladores, líneas de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec581f2ddb54b06de8fa1a1b1356d9b80422ad5c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789964"
---
# <a name="audio-line-and-control-queries"></a><span data-ttu-id="3e85a-110">Consultas de línea y control de audio</span><span class="sxs-lookup"><span data-stu-id="3e85a-110">Audio Line and Control Queries</span></span>

<span data-ttu-id="3e85a-111">Los servicios de mezclador proporcionan funciones para determinar la información sobre las líneas de audio, los controles de línea de audio y los detalles de control.</span><span class="sxs-lookup"><span data-stu-id="3e85a-111">The mixer services provide functions for determining information about audio lines, audio-line controls, and control details.</span></span> <span data-ttu-id="3e85a-112">Los servicios también proporcionan funciones para establecer los detalles del control.</span><span class="sxs-lookup"><span data-stu-id="3e85a-112">The services also provide functions for setting control details.</span></span>

<span data-ttu-id="3e85a-113">Puede usar la función [**mixerGetLineInfo**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo) para recuperar información sobre una línea de audio especificada.</span><span class="sxs-lookup"><span data-stu-id="3e85a-113">You can use the [**mixerGetLineInfo**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo) function to retrieve information about a specified audio line.</span></span> <span data-ttu-id="3e85a-114">Esta función rellena la estructura [**MIXERLINE**](/windows/win32/api/mmeapi/ns-mmeapi-mixerline) para una línea de audio de origen, una línea de audio de destino o un identificador de línea especificados.</span><span class="sxs-lookup"><span data-stu-id="3e85a-114">This function fills the [**MIXERLINE**](/windows/win32/api/mmeapi/ns-mmeapi-mixerline) structure for a specified source audio line, destination audio line, or line identifier.</span></span> <span data-ttu-id="3e85a-115">La estructura incluye el número de línea de destino, el número de canales en la línea de audio, así como un nombre corto y largo para la línea de audio.</span><span class="sxs-lookup"><span data-stu-id="3e85a-115">The structure includes the destination line number, the number of channels in the audio line, as well as a short and a long name for the audio line.</span></span>

<span data-ttu-id="3e85a-116">La función [**mixerGetLineControls**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols) recupera información general acerca de uno o más controles asociados a una línea de audio.</span><span class="sxs-lookup"><span data-stu-id="3e85a-116">The [**mixerGetLineControls**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols) function retrieves general information about one or more controls associated with an audio line.</span></span> <span data-ttu-id="3e85a-117">Esta función rellena la estructura [**MIXERLINECONTROLS**](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols) con información sobre el control o los controles especificados.</span><span class="sxs-lookup"><span data-stu-id="3e85a-117">This function fills the [**MIXERLINECONTROLS**](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols) structure with information about the specified control or controls.</span></span> <span data-ttu-id="3e85a-118">Puede usar **mixerGetLineControls** para recuperar las propiedades de control de una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="3e85a-118">You can use **mixerGetLineControls** to retrieve control properties for one of the following:</span></span>

-   <span data-ttu-id="3e85a-119">Todos los controles de una línea de código fuente especificada</span><span class="sxs-lookup"><span data-stu-id="3e85a-119">All controls for a specified source line</span></span>
-   <span data-ttu-id="3e85a-120">Control especificado para una línea de código fuente especificada</span><span class="sxs-lookup"><span data-stu-id="3e85a-120">A specified control for a specified source line</span></span>
-   <span data-ttu-id="3e85a-121">El primer control de una clase específica para una línea de código fuente especificada</span><span class="sxs-lookup"><span data-stu-id="3e85a-121">The first control of a specific class for a specified source line</span></span>

<span data-ttu-id="3e85a-122">La función [**mixerGetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails) recupera las propiedades de un único control asociado a una línea de audio.</span><span class="sxs-lookup"><span data-stu-id="3e85a-122">The [**mixerGetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails) function retrieves properties of a single control associated with an audio line.</span></span> <span data-ttu-id="3e85a-123">Esta función rellena la estructura [**MIXERCONTROLDETAILS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta) con los valores actuales de un control.</span><span class="sxs-lookup"><span data-stu-id="3e85a-123">This function fills the [**MIXERCONTROLDETAILS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta) structure with the current values for a control.</span></span>

<span data-ttu-id="3e85a-124">La función [**mixerSetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails) usa el contenido de la estructura **MIXERCONTROLDETAILS** para establecer las propiedades del control especificado.</span><span class="sxs-lookup"><span data-stu-id="3e85a-124">The [**mixerSetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails) function uses the contents of the **MIXERCONTROLDETAILS** structure to set the properties of the specified control.</span></span> <span data-ttu-id="3e85a-125">Debe asegurarse de que todos los miembros de esta estructura se rellenan antes de llamar a **mixerSetControlDetails**.</span><span class="sxs-lookup"><span data-stu-id="3e85a-125">You must ensure that all members of this structure are filled before you call **mixerSetControlDetails**.</span></span>

 

 