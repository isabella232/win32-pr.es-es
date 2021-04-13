---
title: Ventana Opciones de carácter avanzadas (ventana comandos de voz)
description: La ventana Opciones de carácter avanzadas
ms.assetid: c2f784e9-d1c5-4fa3-b3f7-5061c9b7e6d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f481871d3861da99b54829e5c6e1b34c9137060a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104359592"
---
# <a name="advanced-character-options-window-voice-commands-window"></a><span data-ttu-id="b83df-103">Ventana Opciones de carácter avanzadas (ventana comandos de voz)</span><span class="sxs-lookup"><span data-stu-id="b83df-103">Advanced Character Options Window (Voice Commands Window)</span></span>

<span data-ttu-id="b83df-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b83df-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="b83df-105">La ventana Opciones de carácter avanzadas proporciona opciones para que los usuarios ajusten su interacción con todos los caracteres.</span><span class="sxs-lookup"><span data-stu-id="b83df-105">The Advanced Character Options window provides options for users to adjust their interaction with all characters.</span></span> <span data-ttu-id="b83df-106">Por ejemplo, los usuarios pueden deshabilitar la entrada de voz o cambiar los parámetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="b83df-106">For example, users can disable speech input or change input parameters.</span></span> <span data-ttu-id="b83df-107">Los usuarios también pueden cambiar la configuración de salida del globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="b83df-107">Users can also change the output settings for the word balloon.</span></span> <span data-ttu-id="b83df-108">Estas opciones invalidan cualquier conjunto de una aplicación cliente o se establecen como parte de la definición de caracteres.</span><span class="sxs-lookup"><span data-stu-id="b83df-108">These settings override any set by a client application or set as part of the character definition.</span></span> <span data-ttu-id="b83df-109">La aplicación no puede cambiar o deshabilitar estas opciones porque se aplican a las preferencias de usuario generales para el funcionamiento de todos los caracteres.</span><span class="sxs-lookup"><span data-stu-id="b83df-109">Your application cannot change or disable these options, because they apply to the general user preferences for operation of all characters.</span></span> <span data-ttu-id="b83df-110">Sin embargo, el servidor notificará a la aplicación ([**DefaultCharacterChange**](defaultcharacterchange-event.md)) cuando el usuario cambie y aplique una opción.</span><span class="sxs-lookup"><span data-stu-id="b83df-110">However, the server will notify your application ([**DefaultCharacterChange**](defaultcharacterchange-event.md)) when the user changes and applies an option.</span></span> <span data-ttu-id="b83df-111">También puede mostrar o cerrar la ventana con la propiedad [**visible**](visible-property.md) de la ventana y acceder a su ubicación a través de sus propiedades [**superior**](top-property.md) e [**izquierda**](left-property.md) .</span><span class="sxs-lookup"><span data-stu-id="b83df-111">You can also display or close the window using the window's [**Visible**](visible-property.md) property and access its location through its [**Top**](top-property.md) and [**Left**](left-property.md) properties.</span></span>

<span data-ttu-id="b83df-112">Además de admitir la animación de un carácter, Microsoft Agent admite la salida de audio para el carácter.</span><span class="sxs-lookup"><span data-stu-id="b83df-112">In addition to supporting the animation of a character, Microsoft Agent supports audio output for the character.</span></span> <span data-ttu-id="b83df-113">Esto incluye la salida hablada y los efectos sonoros.</span><span class="sxs-lookup"><span data-stu-id="b83df-113">This includes spoken output and sound effects.</span></span> <span data-ttu-id="b83df-114">En el caso de la salida de voz, el servidor automáticamente sincroniza las imágenes de la boca definidas del carácter con la salida.</span><span class="sxs-lookup"><span data-stu-id="b83df-114">For spoken output, the server automatically lip-syncs the character's defined mouth images to the output.</span></span> <span data-ttu-id="b83df-115">Puede seleccionar síntesis de texto a voz (TTS), audio grabado o solo texto de globo de palabras.</span><span class="sxs-lookup"><span data-stu-id="b83df-115">You can choose text-to-speech (TTS) synthesis, recorded audio, or only word balloon text output.</span></span>

 

 




