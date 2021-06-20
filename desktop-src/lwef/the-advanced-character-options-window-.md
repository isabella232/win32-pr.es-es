---
title: Ventana Opciones avanzadas de caracteres (ventana Comandos de voz)
description: Obtenga información sobre la ventana Opciones avanzadas de caracteres, que proporciona opciones para que los usuarios ajusten su interacción con todos los caracteres.
ms.assetid: c2f784e9-d1c5-4fa3-b3f7-5061c9b7e6d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd49ff2f3c948594756f8d02bd4417e4f4f684fc
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404368"
---
# <a name="advanced-character-options-window-voice-commands-window"></a><span data-ttu-id="4af92-103">Ventana Opciones avanzadas de caracteres (ventana Comandos de voz)</span><span class="sxs-lookup"><span data-stu-id="4af92-103">Advanced Character Options Window (Voice Commands Window)</span></span>

<span data-ttu-id="4af92-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4af92-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="4af92-105">La ventana Opciones avanzadas de caracteres proporciona opciones para que los usuarios ajusten su interacción con todos los caracteres.</span><span class="sxs-lookup"><span data-stu-id="4af92-105">The Advanced Character Options window provides options for users to adjust their interaction with all characters.</span></span> <span data-ttu-id="4af92-106">Por ejemplo, los usuarios pueden deshabilitar la entrada de voz o cambiar los parámetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="4af92-106">For example, users can disable speech input or change input parameters.</span></span> <span data-ttu-id="4af92-107">Los usuarios también pueden cambiar la configuración de salida del globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="4af92-107">Users can also change the output settings for the word balloon.</span></span> <span data-ttu-id="4af92-108">Esta configuración invalida cualquier conjunto de una aplicación cliente o un conjunto como parte de la definición de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4af92-108">These settings override any set by a client application or set as part of the character definition.</span></span> <span data-ttu-id="4af92-109">La aplicación no puede cambiar ni deshabilitar estas opciones, ya que se aplican a las preferencias generales del usuario para el funcionamiento de todos los caracteres.</span><span class="sxs-lookup"><span data-stu-id="4af92-109">Your application cannot change or disable these options, because they apply to the general user preferences for operation of all characters.</span></span> <span data-ttu-id="4af92-110">Sin embargo, el servidor notificará a la aplicación ([**DefaultCharacterChange**](defaultcharacterchange-event.md)) cuando el usuario cambie y aplique una opción.</span><span class="sxs-lookup"><span data-stu-id="4af92-110">However, the server will notify your application ([**DefaultCharacterChange**](defaultcharacterchange-event.md)) when the user changes and applies an option.</span></span> <span data-ttu-id="4af92-111">También puede mostrar o cerrar la ventana mediante la propiedad [**Visible**](visible-property.md) de la ventana y acceder a su ubicación a través de sus [**propiedades Superior**](top-property.md) [**e**](left-property.md) Izquierda.</span><span class="sxs-lookup"><span data-stu-id="4af92-111">You can also display or close the window using the window's [**Visible**](visible-property.md) property and access its location through its [**Top**](top-property.md) and [**Left**](left-property.md) properties.</span></span>

<span data-ttu-id="4af92-112">Además de admitir la animación de un carácter, Microsoft Agent admite la salida de audio del carácter.</span><span class="sxs-lookup"><span data-stu-id="4af92-112">In addition to supporting the animation of a character, Microsoft Agent supports audio output for the character.</span></span> <span data-ttu-id="4af92-113">Esto incluye la salida hablada y los efectos de sonido.</span><span class="sxs-lookup"><span data-stu-id="4af92-113">This includes spoken output and sound effects.</span></span> <span data-ttu-id="4af92-114">En el caso de la salida hablada, el servidor sincroniza automáticamente las imágenes de la cadena definidas por el carácter con la salida.</span><span class="sxs-lookup"><span data-stu-id="4af92-114">For spoken output, the server automatically lip-syncs the character's defined mouth images to the output.</span></span> <span data-ttu-id="4af92-115">Puede elegir la síntesis de texto a voz (TTS), el audio grabado o solo la salida de texto de globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="4af92-115">You can choose text-to-speech (TTS) synthesis, recorded audio, or only word balloon text output.</span></span>

 

 




