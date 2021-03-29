---
title: Errores del secuenciador
description: Errores del secuenciador
ms.assetid: 07f2d6c5-8c23-4f3e-8b8a-4f659eda57f7
keywords:
- Valores devueltos de MCIERR, errores del secuenciador
- referencia multimedia, errores del secuenciador
- referencia de los elementos multimedia, errores del secuenciador
- Media control Interface (MCI), errores del secuenciador
- MCI (interfaz de control de medios), errores del secuenciador
- referencia de MCI, errores del secuenciador
- Referencia de MCI, errores del secuenciador
- Media control Interface (MCI), errores
- MCI (interfaz de control multimedia), errores
- referencia de MCI, errores
- Referencia de MCI, errores
- errores del secuenciador
- Errores del secuenciador de MCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dd7d55d3b49be3d641f7396148d98766b224a58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775978"
---
# <a name="sequencer-errors"></a><span data-ttu-id="16b8f-116">Errores del secuenciador</span><span class="sxs-lookup"><span data-stu-id="16b8f-116">Sequencer Errors</span></span>

<span data-ttu-id="16b8f-117">Se definen los siguientes valores devueltos adicionales para los secuenciadores MCI:</span><span class="sxs-lookup"><span data-stu-id="16b8f-117">The following additional return values are defined for MCI sequencers:</span></span>



| <span data-ttu-id="16b8f-118">Value</span><span class="sxs-lookup"><span data-stu-id="16b8f-118">Value</span></span>                          | <span data-ttu-id="16b8f-119">Significado</span><span class="sxs-lookup"><span data-stu-id="16b8f-119">Meaning</span></span>                                                                                                                                                  |
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16b8f-120">MCIERR \_ Seq \_ div \_ incompatible</span><span class="sxs-lookup"><span data-stu-id="16b8f-120">MCIERR\_SEQ\_DIV\_INCOMPATIBLE</span></span> | <span data-ttu-id="16b8f-121">Los formatos de hora del "puntero de canción" y SMPTE son singulares.</span><span class="sxs-lookup"><span data-stu-id="16b8f-121">The time formats of the "song pointer" and SMPTE are singular.</span></span> <span data-ttu-id="16b8f-122">No se pueden usar juntos.</span><span class="sxs-lookup"><span data-stu-id="16b8f-122">You can't use them together.</span></span>                                                              |
| <span data-ttu-id="16b8f-123">MCIERR \_ Seq \_ NOMIDIPRESENT</span><span class="sxs-lookup"><span data-stu-id="16b8f-123">MCIERR\_SEQ\_NOMIDIPRESENT</span></span>     | <span data-ttu-id="16b8f-124">Este sistema no tiene dispositivos MIDI instalados.</span><span class="sxs-lookup"><span data-stu-id="16b8f-124">This system has no installed MIDI devices.</span></span> <span data-ttu-id="16b8f-125">Use la opción controladores del panel de control para instalar un controlador MIDI.</span><span class="sxs-lookup"><span data-stu-id="16b8f-125">Use the Drivers option from the Control Panel to install a MIDI driver.</span></span>                                       |
| <span data-ttu-id="16b8f-126">MCIERR \_ Seq \_ Puerto \_ inuse</span><span class="sxs-lookup"><span data-stu-id="16b8f-126">MCIERR\_SEQ\_PORT\_INUSE</span></span>       | <span data-ttu-id="16b8f-127">El puerto MIDI especificado ya está en uso.</span><span class="sxs-lookup"><span data-stu-id="16b8f-127">The specified MIDI port is already in use.</span></span> <span data-ttu-id="16b8f-128">Espere hasta que sea gratuito; a continuación, vuelva a intentarlo.</span><span class="sxs-lookup"><span data-stu-id="16b8f-128">Wait until it is free; then, try again.</span></span>                                                                       |
| <span data-ttu-id="16b8f-129">MCIERR \_ Seq \_ Puerto \_ MAPNODEVICE</span><span class="sxs-lookup"><span data-stu-id="16b8f-129">MCIERR\_SEQ\_PORT\_MAPNODEVICE</span></span> | <span data-ttu-id="16b8f-130">La configuración actual del asignador de MIDI hace referencia a un dispositivo MIDI que no está instalado en el sistema.</span><span class="sxs-lookup"><span data-stu-id="16b8f-130">The current MIDI Mapper setup refers to a MIDI device that is not installed on the system.</span></span> <span data-ttu-id="16b8f-131">Use el asignador MIDI del panel de control para editar la configuración.</span><span class="sxs-lookup"><span data-stu-id="16b8f-131">Use the MIDI Mapper from the Control Panel to edit the setup.</span></span> |
| <span data-ttu-id="16b8f-132">MCIERR \_ Seq \_ Puerto \_ MISCERROR</span><span class="sxs-lookup"><span data-stu-id="16b8f-132">MCIERR\_SEQ\_PORT\_MISCERROR</span></span>   | <span data-ttu-id="16b8f-133">Se produjo un error con el puerto especificado.</span><span class="sxs-lookup"><span data-stu-id="16b8f-133">An error occurred with specified port.</span></span>                                                                                                                   |
| <span data-ttu-id="16b8f-134">Puerto de MCIERR \_ Seq \_ \_ inexistente</span><span class="sxs-lookup"><span data-stu-id="16b8f-134">MCIERR\_SEQ\_PORT\_NONEXISTENT</span></span> | <span data-ttu-id="16b8f-135">El dispositivo MIDI especificado no está instalado en el sistema.</span><span class="sxs-lookup"><span data-stu-id="16b8f-135">The specified MIDI device is not installed on the system.</span></span> <span data-ttu-id="16b8f-136">Use la opción controladores del panel de control para instalar un dispositivo MIDI.</span><span class="sxs-lookup"><span data-stu-id="16b8f-136">Use the Drivers option from the Control Panel to install a MIDI device.</span></span>                        |
| <span data-ttu-id="16b8f-137">MCIERR \_ Seq \_ PORTUNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="16b8f-137">MCIERR\_SEQ\_PORTUNSPECIFIED</span></span>   | <span data-ttu-id="16b8f-138">El sistema no tiene especificado un puerto MIDI actual.</span><span class="sxs-lookup"><span data-stu-id="16b8f-138">The system does not have a current MIDI port specified.</span></span>                                                                                                  |
| <span data-ttu-id="16b8f-139">temporizador de MCIERR \_ Seq \_</span><span class="sxs-lookup"><span data-stu-id="16b8f-139">MCIERR\_SEQ\_TIMER</span></span>             | <span data-ttu-id="16b8f-140">Todos los temporizadores multimedia están siendo utilizados por otras aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="16b8f-140">All multimedia timers are being used by other applications.</span></span> <span data-ttu-id="16b8f-141">Salga de una de estas aplicaciones; a continuación, vuelva a intentarlo.</span><span class="sxs-lookup"><span data-stu-id="16b8f-141">Quit one of these applications; then, try again.</span></span>                                             |



 

 

 




