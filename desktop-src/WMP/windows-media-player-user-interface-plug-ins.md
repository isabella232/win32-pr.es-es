---
title: Complementos de la interfaz de usuario de Windows Media Player
description: Complementos de la interfaz de usuario de Windows Media Player
ms.assetid: 71f53abe-310f-429a-bb23-5291bebdc432
keywords:
- Media Player de Windows, Complementos
- Media Player de Windows, Complementos de la interfaz de usuario
- Complementos de Windows Media Player, interfaz de usuario
- complementos, interfaz de usuario
- Complementos de la interfaz de usuario, acerca de
- Complementos de la interfaz de usuario, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24050f24ef4412d3de9efd5faac6c2af90451dc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704621"
---
# <a name="windows-media-player-user-interface-plug-ins"></a><span data-ttu-id="4289a-109">Complementos de la interfaz de usuario de Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="4289a-109">Windows Media Player User Interface Plug-ins</span></span>

<span data-ttu-id="4289a-110">Microsoft Windows Media Player proporciona una arquitectura que permite al usuario instalar y activar programas de complementos que agregan la funcionalidad de la interfaz de usuario (IU) al modo completo del reproductor.</span><span class="sxs-lookup"><span data-stu-id="4289a-110">Microsoft Windows Media Player provides an architecture that enables the user to install and activate plug-in programs that add user interface (UI) functionality to the full mode of the player.</span></span> <span data-ttu-id="4289a-111">Un complemento de IU típico podría permitir que un usuario compre el CD que contiene la pista que se está reproduciendo o tener acceso a información adicional sobre el artista.</span><span class="sxs-lookup"><span data-stu-id="4289a-111">A typical UI plug-in might allow a user to buy the CD that contains the currently playing track or to access additional information about the artist.</span></span> <span data-ttu-id="4289a-112">Esta sección del kit de desarrollo de software (SDK) de Windows Media Player proporciona la información de programación que necesita para crear su propio complemento de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4289a-112">This section of the Windows Media Player Software Development Kit (SDK) provides you with the programming information you need to create your own UI plug-in.</span></span>

<span data-ttu-id="4289a-113">La documentación del complemento de la interfaz de usuario se divide en tres secciones:</span><span class="sxs-lookup"><span data-stu-id="4289a-113">The UI plug-in documentation is divided into three sections:</span></span>



| <span data-ttu-id="4289a-114">Sección</span><span class="sxs-lookup"><span data-stu-id="4289a-114">Section</span></span>                                                                                            | <span data-ttu-id="4289a-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="4289a-115">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4289a-116">Acerca de los complementos de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="4289a-116">About User Interface Plug-ins</span></span>](about-user-interface-plug-ins.md)                                 | <span data-ttu-id="4289a-117">Proporciona información general sobre la arquitectura utilizada para los complementos de la interfaz de usuario. Lea esta sección para obtener información sobre los conceptos generales implicados en esta tecnología.</span><span class="sxs-lookup"><span data-stu-id="4289a-117">Provides an overview of the architecture used for UI plug-ins. Read this section to learn the general concepts involved with this technology.</span></span> |
| [<span data-ttu-id="4289a-118">Guía de programación de complementos de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="4289a-118">User Interface Plug-ins Programming Guide</span></span>](user-interface-plug-ins-programming-guide.md)         | <span data-ttu-id="4289a-119">Explica lo que debe hacer para crear un complemento de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4289a-119">Explains what you need to do to create a UI plug-in.</span></span> <span data-ttu-id="4289a-120">Esta sección contiene código de ejemplo y procedimientos paso a paso.</span><span class="sxs-lookup"><span data-stu-id="4289a-120">This section contains example code and step-by-step procedures.</span></span>                          |
| [<span data-ttu-id="4289a-121">Referencia de programación de complementos de interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="4289a-121">User Interface Plug-ins Programming Reference</span></span>](user-interface-plug-ins-programming-reference.md) | <span data-ttu-id="4289a-122">Proporciona una referencia detallada para la interfaz COM y los métodos admitidos por el SDK de Windows Media Player para los complementos de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4289a-122">Provides a detailed reference for the COM interface and methods supported by the Windows Media Player SDK for UI plug-ins.</span></span>                    |



 

> [!Note]  
> <span data-ttu-id="4289a-123">Windows Media Player 10 Mobile proporciona el mismo modelo de complemento que el Media Player de Windows de escritorio.</span><span class="sxs-lookup"><span data-stu-id="4289a-123">Windows Media Player 10 Mobile provides the same plug-in model as the desktop Windows Media Player.</span></span> <span data-ttu-id="4289a-124">Este modelo de complemento permite usar complementos de fondo para supervisar eventos, mostrar el estado de las propiedades, etc.</span><span class="sxs-lookup"><span data-stu-id="4289a-124">This plug-in model enables you to use background plug-ins for monitoring events, displaying the status of properties, and so on.</span></span> <span data-ttu-id="4289a-125">En la guía de programación de esta sección se describe cómo crear un complemento de interfaz de usuario de fondo para Windows Media Player 10 Mobile mediante el Asistente para complementos de Windows Media Player de escritorio.</span><span class="sxs-lookup"><span data-stu-id="4289a-125">The programming guide in this section describes how to create a background UI plug-in for Windows Media Player 10 Mobile by using the desktop Windows Media Player Plug-in Wizard.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4289a-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4289a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4289a-127">**Complementos de Media Player de Windows**</span><span class="sxs-lookup"><span data-stu-id="4289a-127">**Windows Media Player Plug-ins**</span></span>](windows-media-player-plug-ins.md)
</dt> </dl>

 

 




