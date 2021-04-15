---
title: Crear un complemento de la interfaz de usuario para Windows Media Player 10 Mobile
description: Crear un complemento de la interfaz de usuario para Windows Media Player 10 Mobile
ms.assetid: 050418b7-d99c-49ab-8ce6-6511b194ffe6
keywords:
- Windows Media Player Mobile, Complementos
- Windows Media Player Mobile, Complementos de la interfaz de usuario
- Complementos móviles de Windows Media Player
- complementos, interfaz de usuario
- complementos, Windows Media Player Mobile
- Complementos de la interfaz de usuario, Windows Media Player Mobile
- Complementos de la interfaz de usuario, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d649ef1d8ed1b8fb1e1b54dc7eed106f798b1ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695350"
---
# <a name="creating-a-user-interface-plug-in-for-windows-media-player-10-mobile"></a><span data-ttu-id="95c19-110">Crear un complemento de la interfaz de usuario para Windows Media Player 10 Mobile</span><span class="sxs-lookup"><span data-stu-id="95c19-110">Creating a User Interface Plug-in for Windows Media Player 10 Mobile</span></span>

<span data-ttu-id="95c19-111">Windows Media Player 10 Mobile usa el mismo modelo de complemento de interfaz de usuario que el Media Player de Windows de escritorio.</span><span class="sxs-lookup"><span data-stu-id="95c19-111">Windows Media Player 10 Mobile uses the same UI plug-in model as the desktop Windows Media Player.</span></span> <span data-ttu-id="95c19-112">Sin embargo, Windows Media Player 10 Mobile solo puede interactuar con complementos de la interfaz de usuario de fondo. Debido a los modelos de complementos similares, las mismas llamadas de API que se aplican a los complementos de la interfaz de usuario en segundo plano en el escritorio también se aplican a los complementos de la interfaz de usuario en segundo plano en un dispositivo móvil de Windows.</span><span class="sxs-lookup"><span data-stu-id="95c19-112">However, Windows Media Player 10 Mobile can only interact with background UI plug-ins. Because of the similar plug-in models, the same API calls that apply to background UI plug-ins on the desktop also apply to background UI plug-ins on a Windows Mobile device.</span></span>

<span data-ttu-id="95c19-113">En las secciones siguientes se describe cómo crear un complemento de la interfaz de usuario de fondo mediante el código generado por el asistente desde el Asistente para complementos de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="95c19-113">The following sections describe how to create a background UI plug-in by using wizard-generated code from the Windows Media Player Plug-in Wizard.</span></span>



| <span data-ttu-id="95c19-114">Sección</span><span class="sxs-lookup"><span data-stu-id="95c19-114">Section</span></span>                                                                | <span data-ttu-id="95c19-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="95c19-115">Description</span></span>                                                                                                                                            |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="95c19-116">Introducción</span><span class="sxs-lookup"><span data-stu-id="95c19-116">Getting Started</span></span>](getting-started.md)                                 | <span data-ttu-id="95c19-117">Describe lo que necesita instalar y cómo usar el Asistente para complementos de Media Player de Windows para ayudar a automatizar la creación de un complemento de interfaz de usuario en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="95c19-117">Describes what you need to install and how to use the Windows Media Player Plug-in Wizard to help automate the creation of a background UI plug-in.</span></span>    |
| [<span data-ttu-id="95c19-118">Modificar el código generado por el asistente</span><span class="sxs-lookup"><span data-stu-id="95c19-118">Modifying Wizard-generated Code</span></span>](modifying-wizard-generated-code.md) | <span data-ttu-id="95c19-119">Describe lo que necesita modificar a partir del código generado por el asistente creado en la sección anterior para que funcione con Windows Media Player 10 Mobile.</span><span class="sxs-lookup"><span data-stu-id="95c19-119">Describes what you need to modify from the wizard-generated code created in the previous section so that it works with Windows Media Player 10 Mobile.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="95c19-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="95c19-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95c19-121">**Guía de programación de complementos de la interfaz de usuario**</span><span class="sxs-lookup"><span data-stu-id="95c19-121">**User Interface Plug-ins Programming Guide**</span></span>](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 




