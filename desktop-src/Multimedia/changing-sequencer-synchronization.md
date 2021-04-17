---
title: Cambiar la sincronización del secuenciador
description: Cambiar la sincronización del secuenciador
ms.assetid: 5c3acb47-e6cc-4957-a306-7039ec110827
keywords:
- MCI_SET mensaje de comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bffdc1606624f63fa05a9cc03c68fe64781620f
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2021
ms.locfileid: "105653113"
---
# <a name="changing-sequencer-synchronization"></a><span data-ttu-id="8137d-104">Cambiar la sincronización del secuenciador</span><span class="sxs-lookup"><span data-stu-id="8137d-104">Changing Sequencer Synchronization</span></span>

> [!NOTE]
> <span data-ttu-id="8137d-105">Comunicación sin polarización: Microsoft admite un entorno diverso y de inclusión.</span><span class="sxs-lookup"><span data-stu-id="8137d-105">Bias-free Communication Microsoft supports a diverse and inclusionary environment.</span></span>  <span data-ttu-id="8137d-106">Dentro de este documento, hay referencias a la palabra ' Slave '.</span><span class="sxs-lookup"><span data-stu-id="8137d-106">Within this document, there are references to the word 'slave.'</span></span> <span data-ttu-id="8137d-107">La guía de estilo de Microsoft [para Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) lo reconoce como una palabra de exclusión.</span><span class="sxs-lookup"><span data-stu-id="8137d-107">Microsoft's [Style Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) recognizes this as an exclusionary word.</span></span>  <span data-ttu-id="8137d-108">Este texto se utiliza como es el que se utiliza actualmente en el software.</span><span class="sxs-lookup"><span data-stu-id="8137d-108">This wording is used as it is currently the wording used within the software.</span></span> <span data-ttu-id="8137d-109">Para mantener la coherencia, este documento contiene esta palabra.</span><span class="sxs-lookup"><span data-stu-id="8137d-109">For consistency, this document contains this word.</span></span> <span data-ttu-id="8137d-110">Cuando se quita esta palabra del software, se corregirá este documento para que esté alineado.</span><span class="sxs-lookup"><span data-stu-id="8137d-110">When this word is removed from the software, we will correct this document to be in alignment.</span></span>

<span data-ttu-id="8137d-111">Para cambiar el modo de sincronización de un dispositivo Sequencer, use el mensaje del comando [**\_ set MCI**](mci-set.md) con las marcas de MCI \_ Seq \_ set \_ Master y MCI \_ Seq \_ set \_ Slave.</span><span class="sxs-lookup"><span data-stu-id="8137d-111">To change the synchronization mode of a sequencer device, use the [**MCI\_SET**](mci-set.md) command message with the MCI\_SEQ\_SET\_MASTER and MCI\_SEQ\_SET\_SLAVE flags.</span></span> <span data-ttu-id="8137d-112">Dos miembros de la estructura de [**parms de MCI \_ Seq \_ set \_**](mci-seq-set-parms.md) , **dwMaster** y **dwSlave**, se usan para especificar los modos de sincronización maestro y subordinado.</span><span class="sxs-lookup"><span data-stu-id="8137d-112">Two members in the [**MCI\_SEQ\_SET\_PARMS**](mci-seq-set-parms.md) structure, **dwMaster** and **dwSlave**, are used to specify the master and subordinate synchronization modes.</span></span>

<span data-ttu-id="8137d-113">El modo de sincronización maestra controla la información de sincronización enviada por Sequencer a un puerto de salida.</span><span class="sxs-lookup"><span data-stu-id="8137d-113">The master synchronization mode controls synchronization information sent by the sequencer to an output port.</span></span> <span data-ttu-id="8137d-114">A continuación se muestran las constantes del miembro **dwMaster** y sus modos de sincronización maestra correspondientes.</span><span class="sxs-lookup"><span data-stu-id="8137d-114">Following are the constants for the **dwMaster** member and their corresponding master synchronization modes.</span></span>



| <span data-ttu-id="8137d-115">Constante</span><span class="sxs-lookup"><span data-stu-id="8137d-115">Constant</span></span>        | <span data-ttu-id="8137d-116">Modo de sincronización</span><span class="sxs-lookup"><span data-stu-id="8137d-116">Synchronization mode</span></span>                                                                             |
|-----------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8137d-117">MCI \_ Seq \_ MIDI</span><span class="sxs-lookup"><span data-stu-id="8137d-117">MCI\_SEQ\_MIDI</span></span>  | <span data-ttu-id="8137d-118">Sincronización MIDI.</span><span class="sxs-lookup"><span data-stu-id="8137d-118">MIDI Synchronization.</span></span> <span data-ttu-id="8137d-119">Enviar información de temporización al puerto de salida mediante mensajes de reloj de temporización de MIDI.</span><span class="sxs-lookup"><span data-stu-id="8137d-119">Send timing information to output port using MIDI timing clock messages.</span></span>   |
| <span data-ttu-id="8137d-120">MCI \_ Seq \_ SMPTE</span><span class="sxs-lookup"><span data-stu-id="8137d-120">MCI\_SEQ\_SMPTE</span></span> | <span data-ttu-id="8137d-121">Sincronización SMPTE.</span><span class="sxs-lookup"><span data-stu-id="8137d-121">SMPTE Synchronization.</span></span> <span data-ttu-id="8137d-122">Enviar información de temporización al puerto de salida mediante mensajes MIDI Quarter-frame.</span><span class="sxs-lookup"><span data-stu-id="8137d-122">Send timing information to output port using MIDI quarter-frame messages.</span></span> |
| <span data-ttu-id="8137d-123">MCI \_ Seq \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="8137d-123">MCI\_SEQ\_NONE</span></span>  | <span data-ttu-id="8137d-124">Sin sincronización.</span><span class="sxs-lookup"><span data-stu-id="8137d-124">No Synchronization.</span></span> <span data-ttu-id="8137d-125">No enviar información de control de tiempo.</span><span class="sxs-lookup"><span data-stu-id="8137d-125">Send no timing information.</span></span>                                                  |



 

<span data-ttu-id="8137d-126">El modo de sincronización subordinado controla dónde el secuenciador obtiene la información de tiempo para reproducir un archivo MIDI.</span><span class="sxs-lookup"><span data-stu-id="8137d-126">The subordinate synchronization mode controls where the sequencer gets its timing information to play a MIDI file.</span></span> <span data-ttu-id="8137d-127">A continuación se enumeran las constantes para el miembro **dwSlave** y sus modos de sincronización subordinados correspondientes.</span><span class="sxs-lookup"><span data-stu-id="8137d-127">Following are the constants for the **dwSlave** member and their corresponding subordinate synchronization modes.</span></span>



| <span data-ttu-id="8137d-128">Constante</span><span class="sxs-lookup"><span data-stu-id="8137d-128">Constant</span></span>        | <span data-ttu-id="8137d-129">Modo de sincronización</span><span class="sxs-lookup"><span data-stu-id="8137d-129">Synchronization mode</span></span>                                                                                                                               |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8137d-130">\_archivo de SEQ de MCI \_</span><span class="sxs-lookup"><span data-stu-id="8137d-130">MCI\_SEQ\_FILE</span></span>  | <span data-ttu-id="8137d-131">Sincronización de archivos.</span><span class="sxs-lookup"><span data-stu-id="8137d-131">File Synchronization.</span></span> <span data-ttu-id="8137d-132">Obtiene la información de tiempo del archivo MIDI.</span><span class="sxs-lookup"><span data-stu-id="8137d-132">Get timing information from MIDI file.</span></span>                                                                                       |
| <span data-ttu-id="8137d-133">MCI \_ Seq \_ MIDI</span><span class="sxs-lookup"><span data-stu-id="8137d-133">MCI\_SEQ\_MIDI</span></span>  | <span data-ttu-id="8137d-134">Sincronización MIDI.</span><span class="sxs-lookup"><span data-stu-id="8137d-134">MIDI Synchronization.</span></span> <span data-ttu-id="8137d-135">Obtiene la información de tiempo del puerto de entrada mediante mensajes de reloj de temporización de MIDI.</span><span class="sxs-lookup"><span data-stu-id="8137d-135">Get timing information from input port using MIDI timing clock messages.</span></span>                                                     |
| <span data-ttu-id="8137d-136">MCI \_ Seq \_ SMPTE</span><span class="sxs-lookup"><span data-stu-id="8137d-136">MCI\_SEQ\_SMPTE</span></span> | <span data-ttu-id="8137d-137">Sincronización SMPTE.</span><span class="sxs-lookup"><span data-stu-id="8137d-137">SMPTE Synchronization.</span></span> <span data-ttu-id="8137d-138">Obtenga información de control de tiempo desde el puerto de entrada mediante mensajes MIDI Quarter-frame.</span><span class="sxs-lookup"><span data-stu-id="8137d-138">Get timing information from input port using MIDI quarter-frame messages.</span></span>                                                   |
| <span data-ttu-id="8137d-139">MCI \_ Seq \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="8137d-139">MCI\_SEQ\_NONE</span></span>  | <span data-ttu-id="8137d-140">Sin sincronización.</span><span class="sxs-lookup"><span data-stu-id="8137d-140">No Synchronization.</span></span> <span data-ttu-id="8137d-141">Obtiene la información de tiempo de los comandos MCI únicamente y omite la información de tiempo (por ejemplo, los cambios de Temp.) que se encuentran en el archivo MIDI.</span><span class="sxs-lookup"><span data-stu-id="8137d-141">Get timing information from MCI commands only and ignore timing information (such as tempo changes) that are in the MIDI file.</span></span> |



 

> [!Note]  
> <span data-ttu-id="8137d-142">Actualmente, para la sincronización maestra, el secuenciador MIDI de MCI solo admite el modo sin sincronización (MCI \_ Seq \_ None).</span><span class="sxs-lookup"><span data-stu-id="8137d-142">Currently, for master synchronization, the MCI MIDI sequencer supports only the No Synchronization mode (MCI\_SEQ\_NONE).</span></span> <span data-ttu-id="8137d-143">Para la sincronización subordinada, solo admite el modo de sincronización de archivos ( \_ archivo de sec. SEQ \_ ) y el modo sin sincronización (MCI \_ Seq \_ ninguno).</span><span class="sxs-lookup"><span data-stu-id="8137d-143">For subordinate synchronization, it supports only the File Synchronization mode (MCI\_SEQ\_FILE) and the No Synchronization mode (MCI\_SEQ\_NONE).</span></span>

 

 

 




