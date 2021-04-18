---
title: IAgentCommandWindow
description: IAgentCommandWindow
ms.assetid: 315b24b4-110e-4373-a1ee-0317531e6008
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 517f43bf482d043b4ca36ff749e3f496ba2988b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704709"
---
# <a name="iagentcommandwindow"></a><span data-ttu-id="e1f9a-103">IAgentCommandWindow</span><span class="sxs-lookup"><span data-stu-id="e1f9a-103">IAgentCommandWindow</span></span>

<span data-ttu-id="e1f9a-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e1f9a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="e1f9a-105">**IAgentCommandWindow** define una interfaz que permite a las aplicaciones establecer y consultar las propiedades de la ventana comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="e1f9a-105">**IAgentCommandWindow** defines an interface that allows applications to set and query the properties of the Voice Commands Window.</span></span> <span data-ttu-id="e1f9a-106">La ventana comandos de voz es un recurso compartido diseñado principalmente para permitir a los usuarios ver comandos habilitados para voz.</span><span class="sxs-lookup"><span data-stu-id="e1f9a-106">The Voice Commands Window is a shared resource primarily designed to enable users to view voice-enabled commands.</span></span> <span data-ttu-id="e1f9a-107">Si el reconocimiento de voz está deshabilitado, se muestra la ventana comandos de voz, con el texto "entrada de voz deshabilitada" (en el idioma del carácter).</span><span class="sxs-lookup"><span data-stu-id="e1f9a-107">If speech recognition is disabled, the Voice Commands Window still displays, with the text "Speech input disabled" (in the language of the character).</span></span> <span data-ttu-id="e1f9a-108">Si no hay instalado ningún motor de voz que coincida con la configuración de idioma del carácter, la ventana muestra "entrada de voz no disponible".</span><span class="sxs-lookup"><span data-stu-id="e1f9a-108">If no speech engine is installed that matches the character's language setting, the window displays, "Speech input not available."</span></span> <span data-ttu-id="e1f9a-109">Si el cliente de entrada-activo no ha definido los parámetros de voz para sus comandos y ha deshabilitado los comandos de voz globales, la ventana muestra el mensaje "no hay comandos de voz".</span><span class="sxs-lookup"><span data-stu-id="e1f9a-109">If the input-active client has not defined voice parameters for its commands and has disabled global voice commands, the window displays, "No voice commands."</span></span> <span data-ttu-id="e1f9a-110">También puede consultar las propiedades de la ventana comandos de voz independientemente de si la entrada de voz está deshabilitada o si se ha instalado un motor de voz compatible.</span><span class="sxs-lookup"><span data-stu-id="e1f9a-110">You can also query the properties of the Voice Commands Window regardless of whether speech input is disabled or a compatible speech engine is installed.</span></span>

<span data-ttu-id="e1f9a-111">**Métodos en orden de Vtable**</span><span class="sxs-lookup"><span data-stu-id="e1f9a-111">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="e1f9a-112">Métodos IAgentCommandWindow</span><span class="sxs-lookup"><span data-stu-id="e1f9a-112">IAgentCommandWindow Methods</span></span>                             | <span data-ttu-id="e1f9a-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1f9a-113">Description</span></span>                                                                                         |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1f9a-114">**SetVisible**</span><span class="sxs-lookup"><span data-stu-id="e1f9a-114">**SetVisible**</span></span>](iagentcommandwindow--setvisible.md)   | <span data-ttu-id="e1f9a-115">Establece el valor de la propiedad [**visible**](visible-property.md) de la ventana comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="e1f9a-115">Sets the value of the [**Visible**](visible-property.md) property of the Voice Commands Window.</span></span>    |
| [<span data-ttu-id="e1f9a-116">**GetVisible**</span><span class="sxs-lookup"><span data-stu-id="e1f9a-116">**GetVisible**</span></span>](iagentcommandwindow--getvisible.md)   | <span data-ttu-id="e1f9a-117">Devuelve el valor de la propiedad [**visible**](visible-property.md) de la ventana comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="e1f9a-117">Returns the value of the [**Visible**](visible-property.md) property of the Voice Commands Window.</span></span> |
| [<span data-ttu-id="e1f9a-118">**GetPosition**</span><span class="sxs-lookup"><span data-stu-id="e1f9a-118">**GetPosition**</span></span>](iagentcommandwindow--getposition.md) | <span data-ttu-id="e1f9a-119">Devuelve la posición de la ventana comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="e1f9a-119">Returns the position of the Voice Commands Window.</span></span>                                                  |
| [<span data-ttu-id="e1f9a-120">**GetSize (**</span><span class="sxs-lookup"><span data-stu-id="e1f9a-120">**GetSize**</span></span>](iagentcommandwindow--getsize.md)         | <span data-ttu-id="e1f9a-121">Devuelve el tamaño de la ventana comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="e1f9a-121">Returns the size of the Voice Commands Window.</span></span>                                                      |



 

 

 




