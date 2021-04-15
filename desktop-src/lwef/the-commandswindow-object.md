---
title: El objeto CommandsWindow
description: El objeto CommandsWindow
ms.assetid: f7f37499-f16b-47fb-85d1-23a68171bf0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 574f803c12779f5ea9e690ca9c7a586d9d5df50e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105714352"
---
# <a name="the-commandswindow-object"></a><span data-ttu-id="8128d-103">El objeto CommandsWindow</span><span class="sxs-lookup"><span data-stu-id="8128d-103">The CommandsWindow Object</span></span>

<span data-ttu-id="8128d-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8128d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="8128d-105">El objeto [**CommandsWindow**](/windows/desktop/lwef/the-commandswindow-object) proporciona acceso a las propiedades de la ventana comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="8128d-105">The [**CommandsWindow**](/windows/desktop/lwef/the-commandswindow-object) object provides access to properties of the Voice Commands Window.</span></span> <span data-ttu-id="8128d-106">La ventana comandos de voz es un recurso compartido diseñado principalmente para permitir a los usuarios ver comandos habilitados para voz.</span><span class="sxs-lookup"><span data-stu-id="8128d-106">The Voice Commands Window is a shared resource primarily designed to enable users to view voice-enabled commands.</span></span> <span data-ttu-id="8128d-107">Si el reconocimiento de voz está deshabilitado, se muestra la ventana comandos de voz, con el texto "entrada de voz deshabilitada" (en el idioma del carácter).</span><span class="sxs-lookup"><span data-stu-id="8128d-107">If speech recognition is disabled, the Voice Commands Window still displays, with the text "Speech input disabled" (in the language of the character).</span></span> <span data-ttu-id="8128d-108">Si no hay instalado ningún motor de voz que coincida con la configuración de idioma del carácter, se muestra "entrada de voz no disponible".</span><span class="sxs-lookup"><span data-stu-id="8128d-108">If no speech engine is installed that matches the character's language setting the window displays, "Speech input not available."</span></span> <span data-ttu-id="8128d-109">Si el cliente de entrada-activo no ha definido los parámetros de voz para sus comandos y ha deshabilitado los comandos de voz globales, la ventana muestra el mensaje "no hay comandos de voz".</span><span class="sxs-lookup"><span data-stu-id="8128d-109">If the input-active client has not defined voice parameters for its commands and has disabled global voice commands, the window displays, "No voice commands."</span></span> <span data-ttu-id="8128d-110">También puede consultar las propiedades de la ventana comandos de voz independientemente de si la entrada de voz está deshabilitada o si se ha instalado un motor de voz compatible.</span><span class="sxs-lookup"><span data-stu-id="8128d-110">You can also query the properties of the Voice Commands Window regardless of whether speech input is disabled or a compatible speech engine is installed.</span></span>

-   [<span data-ttu-id="8128d-111">Propiedades de CommandsWindow</span><span class="sxs-lookup"><span data-stu-id="8128d-111">CommandsWindow Properties</span></span>](commandswindow-properties.md)

 

 