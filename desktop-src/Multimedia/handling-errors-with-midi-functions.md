---
title: Control de errores con funciones MIDI
description: Control de errores con funciones MIDI
ms.assetid: 7ea5db5e-34d7-4506-8157-c24adf5bcdda
keywords:
- Interfaz digital de instrumentos musicales (MIDI), errores
- MIDI (interfaz digital de instrumentos musicales), errores
- Servicios MIDI, errores
- Errores de MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9689fe30b9c4f598cfc9bea892ff3d4fe15d3a9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105651376"
---
# <a name="handling-errors-with-midi-functions"></a><span data-ttu-id="695df-107">Control de errores con funciones MIDI</span><span class="sxs-lookup"><span data-stu-id="695df-107">Handling Errors with MIDI Functions</span></span>

<span data-ttu-id="695df-108">Las funciones de audio MIDI devuelven un código de error distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="695df-108">MIDI audio functions return a nonzero error code.</span></span> <span data-ttu-id="695df-109">En el caso de los errores asociados a MIDI, las funciones [**midiInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midiingeterrortext) y [**midiOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgeterrortext) recuperan las descripciones textuales de los códigos de error.</span><span class="sxs-lookup"><span data-stu-id="695df-109">For MIDI-associated errors, the [**midiInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midiingeterrortext) and [**midiOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgeterrortext) functions retrieve textual descriptions for the error codes.</span></span> <span data-ttu-id="695df-110">La aplicación debe seguir examinando el propio valor de error para determinar cómo proceder, pero puede usar las descripciones de error en los cuadros de diálogo para informar a los usuarios de las condiciones de error.</span><span class="sxs-lookup"><span data-stu-id="695df-110">The application must still look at the error value itself to determine how to proceed, but it can use the error descriptions in dialog boxes to inform users of the error conditions.</span></span>

<span data-ttu-id="695df-111">Las únicas funciones MIDI que no devuelven códigos de error son las funciones [**midiInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs) y [**midiOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) .</span><span class="sxs-lookup"><span data-stu-id="695df-111">The only MIDI functions that do not return error codes are the [**midiInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs) and [**midiOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) functions.</span></span> <span data-ttu-id="695df-112">Estas funciones devuelven un valor de cero si no hay ningún dispositivo presente en un sistema o si la función encuentra algún error.</span><span class="sxs-lookup"><span data-stu-id="695df-112">These functions return a value of zero if no devices are present in a system or if any errors are encountered by the function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="695df-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="695df-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="695df-114">Servicios MIDI</span><span class="sxs-lookup"><span data-stu-id="695df-114">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 