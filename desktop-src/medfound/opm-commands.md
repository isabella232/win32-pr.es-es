---
description: Comandos OPM
ms.assetid: 52165e1b-a178-4483-bf76-4197281f856d
title: Comandos OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aa14026123656b26e978bc179d65c3b61913c62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705895"
---
# <a name="opm-commands"></a><span data-ttu-id="27daf-103">Comandos OPM</span><span class="sxs-lookup"><span data-stu-id="27daf-103">OPM Commands</span></span>

<span data-ttu-id="27daf-104">En esta sección se enumeran los comandos disponibles para el [Administrador de protección de salida](output-protection-manager.md) (OPM).</span><span class="sxs-lookup"><span data-stu-id="27daf-104">This section lists the available commands for [Output Protection Manager](output-protection-manager.md) (OPM).</span></span>

<span data-ttu-id="27daf-105">Para enviar un comando OPM, llame a [**IOPMVideoOutput:: configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure).</span><span class="sxs-lookup"><span data-stu-id="27daf-105">To send an OPM command, call [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure).</span></span> <span data-ttu-id="27daf-106">Para cada comando, se muestra la siguiente información.</span><span class="sxs-lookup"><span data-stu-id="27daf-106">For each command, the following information is listed.</span></span>



|              |                                                                                                                                                             |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27daf-107">GUID de comando</span><span class="sxs-lookup"><span data-stu-id="27daf-107">Command GUID</span></span> | <span data-ttu-id="27daf-108">Identifica el comando.</span><span class="sxs-lookup"><span data-stu-id="27daf-108">Identifies the command.</span></span> <span data-ttu-id="27daf-109">Establezca el miembro **guidSetting** de la estructura de [**\_ \_ parámetros de configuración de OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) igual a este valor.</span><span class="sxs-lookup"><span data-stu-id="27daf-109">Set the **guidSetting** member of the [**OPM\_CONFIGURE\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) structure equal to this value.</span></span> |
| <span data-ttu-id="27daf-110">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="27daf-110">Input data</span></span>   | <span data-ttu-id="27daf-111">Especifica cómo interpretar la matriz **abParameters** en la estructura [**de \_ \_ parámetros de configuración de OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) .</span><span class="sxs-lookup"><span data-stu-id="27daf-111">Specifies how to interpret the **abParameters** array in the [**OPM\_CONFIGURE\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) structure.</span></span>                      |



 

<span data-ttu-id="27daf-112">Se definen los siguientes comandos:</span><span class="sxs-lookup"><span data-stu-id="27daf-112">The following commands are defined:</span></span>



| <span data-ttu-id="27daf-113">Get-Help</span><span class="sxs-lookup"><span data-stu-id="27daf-113">Command</span></span>                                                                                                       | <span data-ttu-id="27daf-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="27daf-114">Description</span></span>                                                                                         |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="27daf-115">**\_configuración \_ de la \_ \_ señalización de CGMSA de OPM y ACP \_**</span><span class="sxs-lookup"><span data-stu-id="27daf-115">**OPM\_SET\_ACP\_AND\_CGMSA\_SIGNALING**</span></span>](opm-set-acp-and-cgmsa-signaling.md)                               | <span data-ttu-id="27daf-116">Especifica información sobre la señal de vídeo, excepto el nivel de protección.</span><span class="sxs-lookup"><span data-stu-id="27daf-116">Specifies information about the video signal, other than the protection level.</span></span>                      |
| [<span data-ttu-id="27daf-117">**OPM \_ set \_ HDCP \_ SRM**</span><span class="sxs-lookup"><span data-stu-id="27daf-117">**OPM\_SET\_HDCP\_SRM**</span></span>](opm-set-hdcp-srm.md)                                                               | <span data-ttu-id="27daf-118">Actualiza el mensaje de renovación de sistema (SRM) para High-Bandwidth Digital Content Protection (HDCP).</span><span class="sxs-lookup"><span data-stu-id="27daf-118">Updates the system renewability message (SRM) for High-Bandwidth Digital Content Protection (HDCP).</span></span> |
| [<span data-ttu-id="27daf-119">**\_nivel de \_ protección de conjunto de OPM \_**</span><span class="sxs-lookup"><span data-stu-id="27daf-119">**OPM\_SET\_PROTECTION\_LEVEL**</span></span>](opm-set-protection-level.md)                                               | <span data-ttu-id="27daf-120">Establece el nivel de protección de un mecanismo de protección de la salida.</span><span class="sxs-lookup"><span data-stu-id="27daf-120">Sets the protection level for an output protection mechanism.</span></span>                                       |
| [<span data-ttu-id="27daf-121">**\_configuración \_ \_ \_ de nivel de protección de OPM según el \_ \_ DVD de CSS \_**</span><span class="sxs-lookup"><span data-stu-id="27daf-121">**OPM\_SET\_PROTECTION\_LEVEL\_ACCORDING\_TO\_CSS\_DVD**</span></span>](opm-set-protection-level-according-to-css-dvd.md) | <span data-ttu-id="27daf-122">Establece el nivel de protección de HDCP para la reproducción de DVD, siguiendo las reglas del sistema de cifrado de contenido (CSS) de DVD.</span><span class="sxs-lookup"><span data-stu-id="27daf-122">Sets the HDCP protection level for DVD playback, following DVD Content Scramble System (CSS) rules.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="27daf-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="27daf-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27daf-124">Referencia de programación de OPM</span><span class="sxs-lookup"><span data-stu-id="27daf-124">OPM Programming Reference</span></span>](opm-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="27daf-125">Administrador de protección de salida</span><span class="sxs-lookup"><span data-stu-id="27daf-125">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 



