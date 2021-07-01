---
description: Comandos de OPM
ms.assetid: 52165e1b-a178-4483-bf76-4197281f856d
title: Comandos de OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b00240925c28322b911ab55a0e4f026f051d6ec
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119150"
---
# <a name="opm-commands"></a><span data-ttu-id="5076e-103">Comandos de OPM</span><span class="sxs-lookup"><span data-stu-id="5076e-103">OPM Commands</span></span>

<span data-ttu-id="5076e-104">En esta sección se enumeran los comandos disponibles para [Output Protection Manager](output-protection-manager.md) (OPM).</span><span class="sxs-lookup"><span data-stu-id="5076e-104">This section lists the available commands for [Output Protection Manager](output-protection-manager.md) (OPM).</span></span>

<span data-ttu-id="5076e-105">Para enviar un comando de OPM, llame a [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure).</span><span class="sxs-lookup"><span data-stu-id="5076e-105">To send an OPM command, call [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure).</span></span> <span data-ttu-id="5076e-106">Para cada comando, se muestra la siguiente información.</span><span class="sxs-lookup"><span data-stu-id="5076e-106">For each command, the following information is listed.</span></span>



| <span data-ttu-id="5076e-107">Valor</span><span class="sxs-lookup"><span data-stu-id="5076e-107">Value</span></span>             | <span data-ttu-id="5076e-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="5076e-108">Description</span></span>                                                                                                                                                            |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5076e-109">GUID de comando</span><span class="sxs-lookup"><span data-stu-id="5076e-109">Command GUID</span></span> | <span data-ttu-id="5076e-110">Identifica el comando .</span><span class="sxs-lookup"><span data-stu-id="5076e-110">Identifies the command.</span></span> <span data-ttu-id="5076e-111">Establezca el **miembro guidSetting** de la estructura [**\_ OPM CONFIGURE \_ PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) igual a este valor.</span><span class="sxs-lookup"><span data-stu-id="5076e-111">Set the **guidSetting** member of the [**OPM\_CONFIGURE\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) structure equal to this value.</span></span> |
| <span data-ttu-id="5076e-112">Datos de entrada</span><span class="sxs-lookup"><span data-stu-id="5076e-112">Input data</span></span>   | <span data-ttu-id="5076e-113">Especifica cómo interpretar la matriz **abParameters** en la [**estructura OPM \_ CONFIGURE \_ PARAMETERS.**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters)</span><span class="sxs-lookup"><span data-stu-id="5076e-113">Specifies how to interpret the **abParameters** array in the [**OPM\_CONFIGURE\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) structure.</span></span>                      |



 

<span data-ttu-id="5076e-114">Se definen los siguientes comandos:</span><span class="sxs-lookup"><span data-stu-id="5076e-114">The following commands are defined:</span></span>



| <span data-ttu-id="5076e-115">Comando</span><span class="sxs-lookup"><span data-stu-id="5076e-115">Command</span></span>                                                                                                       | <span data-ttu-id="5076e-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="5076e-116">Description</span></span>                                                                                         |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5076e-117">**SEÑALIZACIÓN DE \_ OPM SET \_ ACP Y \_ \_ CGMSA \_**</span><span class="sxs-lookup"><span data-stu-id="5076e-117">**OPM\_SET\_ACP\_AND\_CGMSA\_SIGNALING**</span></span>](opm-set-acp-and-cgmsa-signaling.md)                               | <span data-ttu-id="5076e-118">Especifica información sobre la señal de vídeo, aparte del nivel de protección.</span><span class="sxs-lookup"><span data-stu-id="5076e-118">Specifies information about the video signal, other than the protection level.</span></span>                      |
| [<span data-ttu-id="5076e-119">**OPM \_ SET \_ HDCP \_ SRM**</span><span class="sxs-lookup"><span data-stu-id="5076e-119">**OPM\_SET\_HDCP\_SRM**</span></span>](opm-set-hdcp-srm.md)                                                               | <span data-ttu-id="5076e-120">Actualiza el mensaje de renovación del sistema (SRM) para High-Bandwidth Digital Content Protection (HDCP).</span><span class="sxs-lookup"><span data-stu-id="5076e-120">Updates the system renewability message (SRM) for High-Bandwidth Digital Content Protection (HDCP).</span></span> |
| [<span data-ttu-id="5076e-121">**OPM \_ SET \_ PROTECTION \_ LEVEL**</span><span class="sxs-lookup"><span data-stu-id="5076e-121">**OPM\_SET\_PROTECTION\_LEVEL**</span></span>](opm-set-protection-level.md)                                               | <span data-ttu-id="5076e-122">Establece el nivel de protección para un mecanismo de protección de salida.</span><span class="sxs-lookup"><span data-stu-id="5076e-122">Sets the protection level for an output protection mechanism.</span></span>                                       |
| [<span data-ttu-id="5076e-123">**OPM \_ SET \_ PROTECTION \_ LEVEL \_ ACCORDING \_ TO \_ CSS \_ DVD**</span><span class="sxs-lookup"><span data-stu-id="5076e-123">**OPM\_SET\_PROTECTION\_LEVEL\_ACCORDING\_TO\_CSS\_DVD**</span></span>](opm-set-protection-level-according-to-css-dvd.md) | <span data-ttu-id="5076e-124">Establece el nivel de protección de HDCP para la reproducción de DVD, siguiendo las reglas del sistema de codificación de contenido de DVD (CSS).</span><span class="sxs-lookup"><span data-stu-id="5076e-124">Sets the HDCP protection level for DVD playback, following DVD Content Scramble System (CSS) rules.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="5076e-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5076e-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5076e-126">Referencia de programación de OPM</span><span class="sxs-lookup"><span data-stu-id="5076e-126">OPM Programming Reference</span></span>](opm-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="5076e-127">Administrador de protección de salida</span><span class="sxs-lookup"><span data-stu-id="5076e-127">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 



