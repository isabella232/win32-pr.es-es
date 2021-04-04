---
title: Errores de mciSendString
description: Errores de mciSendString
ms.assetid: 286102bd-fcf3-425b-9adc-e0ca2d62e453
keywords:
- Valores devueltos de MCIERR, errores de mciSendString
- referencia multimedia, errores mciSendString
- referencia para multimedia, errores mciSendString
- Media control Interface (MCI), errores mciSendString
- MCI (media control Interface), errores mciSendString
- referencia para MCI, errores mciSendString
- Referencia de MCI, errores mciSendString
- Media control Interface (MCI), errores
- MCI (interfaz de control multimedia), errores
- referencia de MCI, errores
- Referencia de MCI, errores
- errores de mciSendString
- mciSendString función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 063db1986d3bff2416ad17886afb3b6281e20165
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904566"
---
# <a name="mcisendstring-errors"></a><span data-ttu-id="e402d-116">Errores de mciSendString</span><span class="sxs-lookup"><span data-stu-id="e402d-116">mciSendString Errors</span></span>

<span data-ttu-id="e402d-117">La función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) devuelve los siguientes errores, pero no [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)):</span><span class="sxs-lookup"><span data-stu-id="e402d-117">The following errors are returned by the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function but not by [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)):</span></span>



| <span data-ttu-id="e402d-118">Value</span><span class="sxs-lookup"><span data-stu-id="e402d-118">Value</span></span>                             | <span data-ttu-id="e402d-119">Significado</span><span class="sxs-lookup"><span data-stu-id="e402d-119">Meaning</span></span>                                           |
|-----------------------------------|---------------------------------------------------|
| <span data-ttu-id="e402d-120">MCIERR \_ ( \_ constante incorrecta)</span><span class="sxs-lookup"><span data-stu-id="e402d-120">MCIERR\_BAD\_CONSTANT</span></span>             | <span data-ttu-id="e402d-121">El valor especificado para un parámetro es desconocido.</span><span class="sxs-lookup"><span data-stu-id="e402d-121">The value specified for a parameter is unknown.</span></span>   |
| <span data-ttu-id="e402d-122">MCIERR \_ \_ entero incorrecto</span><span class="sxs-lookup"><span data-stu-id="e402d-122">MCIERR\_BAD\_INTEGER</span></span>              | <span data-ttu-id="e402d-123">Falta un entero en el comando o no era válido.</span><span class="sxs-lookup"><span data-stu-id="e402d-123">An integer in the command was invalid or missing.</span></span> |
| <span data-ttu-id="e402d-124">MCIERR \_ marcas duplicadas \_</span><span class="sxs-lookup"><span data-stu-id="e402d-124">MCIERR\_DUPLICATE\_FLAGS</span></span>          | <span data-ttu-id="e402d-125">Una marca o un valor se especificó dos veces.</span><span class="sxs-lookup"><span data-stu-id="e402d-125">A flag or value was specified twice.</span></span>              |
| <span data-ttu-id="e402d-126">MCIERR \_ falta \_ la \_ cadena de comandos</span><span class="sxs-lookup"><span data-stu-id="e402d-126">MCIERR\_MISSING\_COMMAND\_STRING</span></span>  | <span data-ttu-id="e402d-127">No se especificó ningún comando.</span><span class="sxs-lookup"><span data-stu-id="e402d-127">No command was specified.</span></span>                         |
| <span data-ttu-id="e402d-128">MCIERR \_ falta \_ \_ el nombre del dispositivo</span><span class="sxs-lookup"><span data-stu-id="e402d-128">MCIERR\_MISSING\_DEVICE\_NAME</span></span>     | <span data-ttu-id="e402d-129">No se especificó ningún nombre de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e402d-129">No device name was specified.</span></span>                     |
| <span data-ttu-id="e402d-130">MCIERR \_ \_ argumento de cadena ausente \_</span><span class="sxs-lookup"><span data-stu-id="e402d-130">MCIERR\_MISSING\_STRING\_ARGUMENT</span></span> | <span data-ttu-id="e402d-131">Falta un valor de cadena en el comando.</span><span class="sxs-lookup"><span data-stu-id="e402d-131">A string value was missing from the command.</span></span>      |
| <span data-ttu-id="e402d-132">MCIERR \_ nuevo \_ requiere \_ alias</span><span class="sxs-lookup"><span data-stu-id="e402d-132">MCIERR\_NEW\_REQUIRES\_ALIAS</span></span>      | <span data-ttu-id="e402d-133">Se debe usar un alias con el nombre de dispositivo "nuevo".</span><span class="sxs-lookup"><span data-stu-id="e402d-133">An alias must be used with the "new" device name.</span></span> |
| <span data-ttu-id="e402d-134">MCIERR \_ no \_ hay \_ comilla de cierre</span><span class="sxs-lookup"><span data-stu-id="e402d-134">MCIERR\_NO\_CLOSING\_QUOTE</span></span>        | <span data-ttu-id="e402d-135">Falta una comilla de cierre.</span><span class="sxs-lookup"><span data-stu-id="e402d-135">A closing quotation mark is missing.</span></span>              |
| <span data-ttu-id="e402d-136">MCIERR \_ notificar \_ al \_ \_ abrir automáticamente</span><span class="sxs-lookup"><span data-stu-id="e402d-136">MCIERR\_NOTIFY\_ON\_AUTO\_OPEN</span></span>    | <span data-ttu-id="e402d-137">El indicador "notificar" no es válido con apertura automática.</span><span class="sxs-lookup"><span data-stu-id="e402d-137">The "notify" flag is illegal with auto-open.</span></span>      |
| <span data-ttu-id="e402d-138">\_desbordamiento del parámetro MCIERR \_</span><span class="sxs-lookup"><span data-stu-id="e402d-138">MCIERR\_PARAM\_OVERFLOW</span></span>           | <span data-ttu-id="e402d-139">La cadena de salida no era lo suficientemente larga.</span><span class="sxs-lookup"><span data-stu-id="e402d-139">The output string was not long enough.</span></span>            |
| <span data-ttu-id="e402d-140">\_analizador \_ interno de MCIERR</span><span class="sxs-lookup"><span data-stu-id="e402d-140">MCIERR\_PARSER\_INTERNAL</span></span>          | <span data-ttu-id="e402d-141">Se produjo un error interno del analizador.</span><span class="sxs-lookup"><span data-stu-id="e402d-141">An internal parser error occurred.</span></span>                |
| <span data-ttu-id="e402d-142">\_ \_ palabra clave MCIERR desconocida</span><span class="sxs-lookup"><span data-stu-id="e402d-142">MCIERR\_UNRECOGNIZED\_KEYWORD</span></span>     | <span data-ttu-id="e402d-143">Se especificó un parámetro de comando desconocido.</span><span class="sxs-lookup"><span data-stu-id="e402d-143">An unknown command parameter was specified.</span></span>       |



 

 

 