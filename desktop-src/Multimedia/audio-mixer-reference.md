---
title: Referencia del mezclador de audio
description: Referencia del mezclador de audio
ms.assetid: 9d8751b1-9c0b-4238-a961-27c09a869bb3
keywords:
- audio multimedia, mezcladores de audio
- audio, mezclador de audio
- audio multimedia, referencia de mezclador
- audio, referencia de mezclador
- mezclador de audio, referencia
- mezclador, referencia
- referencia de los mezcladores de audio, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be1d86f305714d72631b56495753417699b1a146
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104271202"
---
# <a name="audio-mixer-reference"></a><span data-ttu-id="1bba7-110">Referencia del mezclador de audio</span><span class="sxs-lookup"><span data-stu-id="1bba7-110">Audio Mixer Reference</span></span>

<span data-ttu-id="1bba7-111">En esta sección se describen las funciones, las estructuras y los mensajes asociados a los mezcladores de audio.</span><span class="sxs-lookup"><span data-stu-id="1bba7-111">This section describes the functions, structures, and messages associated with audio mixers.</span></span> <span data-ttu-id="1bba7-112">Estos elementos se agrupan de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="1bba7-112">These elements are grouped as follows.</span></span>

## <a name="querying-devices"></a><span data-ttu-id="1bba7-113">Consultar dispositivos</span><span class="sxs-lookup"><span data-stu-id="1bba7-113">Querying Devices</span></span>

-   [<span data-ttu-id="1bba7-114">**MIXERCAPS**</span><span class="sxs-lookup"><span data-stu-id="1bba7-114">**MIXERCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-mixercaps)
-   [<span data-ttu-id="1bba7-115">**mixerGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="1bba7-115">**mixerGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetdevcaps)
-   [<span data-ttu-id="1bba7-116">**mixerGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="1bba7-116">**mixerGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs)

## <a name="opening-and-closing"></a><span data-ttu-id="1bba7-117">Abrir y cerrar</span><span class="sxs-lookup"><span data-stu-id="1bba7-117">Opening and Closing</span></span>

-   [<span data-ttu-id="1bba7-118">**mixerClose**</span><span class="sxs-lookup"><span data-stu-id="1bba7-118">**mixerClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose)
-   [<span data-ttu-id="1bba7-119">**mixerOpen**</span><span class="sxs-lookup"><span data-stu-id="1bba7-119">**mixerOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen)

## <a name="retrieving-mixer-identifiers"></a><span data-ttu-id="1bba7-120">Recuperando identificadores de mezclador</span><span class="sxs-lookup"><span data-stu-id="1bba7-120">Retrieving Mixer Identifiers</span></span>

-   [<span data-ttu-id="1bba7-121">**mixerGetID**</span><span class="sxs-lookup"><span data-stu-id="1bba7-121">**mixerGetID**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetid)

## <a name="retrieving-line-controls"></a><span data-ttu-id="1bba7-122">Recuperar controles de línea</span><span class="sxs-lookup"><span data-stu-id="1bba7-122">Retrieving Line Controls</span></span>

-   [<span data-ttu-id="1bba7-123">**MIXERCONTROL**</span><span class="sxs-lookup"><span data-stu-id="1bba7-123">**MIXERCONTROL**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-mixercontrol)
-   [<span data-ttu-id="1bba7-124">**mixerGetLineControls**</span><span class="sxs-lookup"><span data-stu-id="1bba7-124">**mixerGetLineControls**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols)
-   [<span data-ttu-id="1bba7-125">**MIXERLINECONTROLS**</span><span class="sxs-lookup"><span data-stu-id="1bba7-125">**MIXERLINECONTROLS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols)

## <a name="changing-control-attributes"></a><span data-ttu-id="1bba7-126">Cambiar atributos de control</span><span class="sxs-lookup"><span data-stu-id="1bba7-126">Changing Control Attributes</span></span>

-   [<span data-ttu-id="1bba7-127">**MIXERCONTROLDETAILS**</span><span class="sxs-lookup"><span data-stu-id="1bba7-127">**MIXERCONTROLDETAILS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta)
-   <span data-ttu-id="1bba7-128">[**MIXERCONTROLDETAILS \_ booleano**](/previous-versions//dd757295(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1bba7-128">[**MIXERCONTROLDETAILS\_BOOLEAN**](/previous-versions//dd757295(v=vs.85))</span></span>
-   <span data-ttu-id="1bba7-129">[**MIXERCONTROLDETAILS \_ LISTTEXT**](/previous-versions//dd757296(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1bba7-129">[**MIXERCONTROLDETAILS\_LISTTEXT**](/previous-versions//dd757296(v=vs.85))</span></span>
-   <span data-ttu-id="1bba7-130">[**MIXERCONTROLDETAILS \_ firmado**](/previous-versions//dd757297(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1bba7-130">[**MIXERCONTROLDETAILS\_SIGNED**](/previous-versions//dd757297(v=vs.85))</span></span>
-   <span data-ttu-id="1bba7-131">[**MIXERCONTROLDETAILS \_ sin signo**](/previous-versions//dd757298(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1bba7-131">[**MIXERCONTROLDETAILS\_UNSIGNED**](/previous-versions//dd757298(v=vs.85))</span></span>
-   [<span data-ttu-id="1bba7-132">**mixerGetControlDetails**</span><span class="sxs-lookup"><span data-stu-id="1bba7-132">**mixerGetControlDetails**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails)
-   [<span data-ttu-id="1bba7-133">**mixerSetControlDetails**</span><span class="sxs-lookup"><span data-stu-id="1bba7-133">**mixerSetControlDetails**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails)

## <a name="retrieving-line-information"></a><span data-ttu-id="1bba7-134">Recuperar información de línea</span><span class="sxs-lookup"><span data-stu-id="1bba7-134">Retrieving Line Information</span></span>

-   [<span data-ttu-id="1bba7-135">**mixerGetLineInfo**</span><span class="sxs-lookup"><span data-stu-id="1bba7-135">**mixerGetLineInfo**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo)
-   [<span data-ttu-id="1bba7-136">**MIXERLINE**</span><span class="sxs-lookup"><span data-stu-id="1bba7-136">**MIXERLINE**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-mixerline)
-   [<span data-ttu-id="1bba7-137">**cambio de control de MM \_ MIXM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1bba7-137">**MM\_MIXM\_CONTROL\_CHANGE**</span></span>](mm-mixm-control-change.md)
-   [<span data-ttu-id="1bba7-138">**\_cambio de \_ línea mm MIXM \_**</span><span class="sxs-lookup"><span data-stu-id="1bba7-138">**MM\_MIXM\_LINE\_CHANGE**</span></span>](mm-mixm-line-change.md)

## <a name="sending-user-defined-messages"></a><span data-ttu-id="1bba7-139">Envío de mensajes de User-Defined</span><span class="sxs-lookup"><span data-stu-id="1bba7-139">Sending User-Defined Messages</span></span>

-   [<span data-ttu-id="1bba7-140">**mixerMessage**</span><span class="sxs-lookup"><span data-stu-id="1bba7-140">**mixerMessage**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixermessage)

## <a name="related-topics"></a><span data-ttu-id="1bba7-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1bba7-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bba7-142">Referencia del mezclador de audio</span><span class="sxs-lookup"><span data-stu-id="1bba7-142">Audio Mixer Reference</span></span>](audio-mixer-reference.md)
</dt> </dl>

 

 