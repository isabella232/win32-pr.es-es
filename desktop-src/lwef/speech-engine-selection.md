---
title: Selección del motor de voz
description: Selección del motor de voz
ms.assetid: f5afedc6-093f-4247-a5c8-277d6b2d646c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a548f0201ba37c8acb867091cc690a913277ff06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903391"
---
# <a name="speech-engine-selection"></a><span data-ttu-id="c7edc-103">Selección del motor de voz</span><span class="sxs-lookup"><span data-stu-id="c7edc-103">Speech Engine Selection</span></span>

<span data-ttu-id="c7edc-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c7edc-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="c7edc-105">El valor de identificador de idioma de un carácter determina su idioma de entrada de voz predeterminado; El agente de Microsoft solicita a SAPI un motor instalado que coincida con ese idioma.</span><span class="sxs-lookup"><span data-stu-id="c7edc-105">A character's language ID setting determines its default speech input language; Microsoft Agent requests SAPI for an installed engine that matches that language.</span></span> <span data-ttu-id="c7edc-106">Si una aplicación cliente no especifica una preferencia de idioma, Microsoft Agent intentará encontrar un motor de reconocimiento de voz que coincida con el ID. de idioma predeterminado del usuario (con el identificador de idioma principal y, después, el identificador de idioma secundario).</span><span class="sxs-lookup"><span data-stu-id="c7edc-106">If a client application does not specify a language preference, Microsoft Agent will attempt to find a speech recognition engine that matches the user default language ID (using the major language ID, then the minor language ID).</span></span> <span data-ttu-id="c7edc-107">Si no hay ningún motor disponible que coincida con este idioma, la voz se deshabilitará para ese carácter.</span><span class="sxs-lookup"><span data-stu-id="c7edc-107">If no engine is available matching this language, speech is disabled for that character.</span></span>

<span data-ttu-id="c7edc-108">También puede solicitar un motor de reconocimiento de voz específico especificando su identificador de modo (mediante la propiedad [**SRModeID**](srmodeid-property.md) de caracteres).</span><span class="sxs-lookup"><span data-stu-id="c7edc-108">You can also request a specific speech recognition engine by specifying its mode ID (using the character [**SRModeID**](srmodeid-property.md) property).</span></span> <span data-ttu-id="c7edc-109">Sin embargo, si el identificador de idioma para ese ID. de modo no coincide con la configuración de idioma del cliente, se producirá un error en la llamada (se producirá un error en el control).</span><span class="sxs-lookup"><span data-stu-id="c7edc-109">However, if the language ID for that mode ID does not match the client's language setting, the call will fail (raise an error in the control).</span></span> <span data-ttu-id="c7edc-110">Después, el motor de reconocimiento de voz seguirá siendo el último que el cliente estableció correctamente el motor, o bien, si no es así, el motor que coincide con el identificador de idioma actual del sistema.</span><span class="sxs-lookup"><span data-stu-id="c7edc-110">The speech recognition engine will then remain the last successfully set engine by the client, or if none, the engine that matches the current system language ID.</span></span> <span data-ttu-id="c7edc-111">Si todavía no hay ninguna coincidencia, la entrada de voz no está disponible para ese cliente.</span><span class="sxs-lookup"><span data-stu-id="c7edc-111">If there is still no match, speech input is not available for that client.</span></span>

<span data-ttu-id="c7edc-112">El agente de Microsoft carga automáticamente un motor de reconocimiento de voz cuando la entrada de voz la inicia un usuario al presionar la tecla de método de escucha o el cliente de entrada-activo llama al método [**Listen**](listen-method.md) .</span><span class="sxs-lookup"><span data-stu-id="c7edc-112">Microsoft Agent automatically loads a speech recognition engine when speech input is initiated by a user pressing the Listening hotkey or the input-active client calls the [**Listen**](listen-method.md) method.</span></span> <span data-ttu-id="c7edc-113">Sin embargo, también se puede cargar un motor cuando se establece o se consulta su identificador de modo, se establece o se consultan las propiedades de la ventana comandos de voz, se consulta [**SRStatus**](srstatus-property.md)o cuando la voz está habilitada y el usuario muestra la página de entrada de voz de las opciones de caracteres avanzadas.</span><span class="sxs-lookup"><span data-stu-id="c7edc-113">However, an engine may also be loaded when setting or querying its mode ID, setting or querying the properties of the Voice Commands Window, querying [**SRStatus**](srstatus-property.md), or when speech is enabled and the user displays the Speech Input page of the Advanced Character Options.</span></span> <span data-ttu-id="c7edc-114">Sin embargo, el agente de Microsoft solo mantiene cargados los motores de voz que usan los clientes.</span><span class="sxs-lookup"><span data-stu-id="c7edc-114">However, Microsoft Agent only keeps loaded the speech engines that clients are using.</span></span>

 

 




