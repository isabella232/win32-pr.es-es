---
title: Opciones del complemento de la interfaz de usuario
description: Opciones del complemento de la interfaz de usuario
ms.assetid: 3c188506-865c-4e0c-965d-1429eafd01ef
keywords:
- Complementos de Media Player de Windows, opciones
- complementos, opciones
- Complementos de la interfaz de usuario, opciones
- Complementos de la interfaz de usuario, opciones
- Complementos de área de configuración
- Complementos de fondo
- Complementos de ventana independientes
- Complementos de área de metadatos
- Complementos de área de presentación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281dd0679e6a975b1c867624f2f652f2b3e6b9ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704599"
---
# <a name="ui-plug-in-options"></a><span data-ttu-id="c4f30-112">Opciones del complemento de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="c4f30-112">UI Plug-in Options</span></span>

<span data-ttu-id="c4f30-113">Cualquiera de los cinco tipos de complementos de la interfaz de usuario puede tener una página de propiedades en la que el usuario puede modificar la configuración del complemento.</span><span class="sxs-lookup"><span data-stu-id="c4f30-113">Any of the five UI plug-in types can have a property page where the user can modify plug-in settings.</span></span> <span data-ttu-id="c4f30-114">Esta página de propiedades se puede establecer para que se muestre automáticamente cuando se carga un complemento por primera vez.</span><span class="sxs-lookup"><span data-stu-id="c4f30-114">This property page can be set to display automatically when a plug-in is loaded for the first time.</span></span> <span data-ttu-id="c4f30-115">También se puede obtener acceso a él desde la pestaña complementos del cuadro de diálogo Opciones.</span><span class="sxs-lookup"><span data-stu-id="c4f30-115">It can also be accessed from the Plug-ins tab of the Options dialog box.</span></span>

<span data-ttu-id="c4f30-116">Se puede configurar un complemento de la interfaz de usuario para que se cargue automáticamente después de la instalación cuando se inicie Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="c4f30-116">A UI plug-in can be set to load automatically after installation when Windows Media Player is started.</span></span> <span data-ttu-id="c4f30-117">Si no se inicia automáticamente, el usuario puede cargarla seleccionándola en la lista de **Complementos** del menú **herramientas** .</span><span class="sxs-lookup"><span data-stu-id="c4f30-117">If it is not started automatically, the user can load it by selecting it from the **Plug-ins** list on the **Tools** menu.</span></span>

<span data-ttu-id="c4f30-118">Un complemento de área de presentación puede tener varios valores predeterminados, que son vistas diferentes que el complemento puede poner a disposición del usuario.</span><span class="sxs-lookup"><span data-stu-id="c4f30-118">A display area plug-in can have multiple presets, which are different views that the plug-in can make available to the user.</span></span> <span data-ttu-id="c4f30-119">El usuario puede cambiar el valor preestablecido seleccionando una entrada diferente de la lista **visualizaciones y vistas** en el menú **Ver** o mediante los botones de flecha proporcionados en la parte inferior del panel **reproducción en curso** justo encima del mensaje de estado y los controles de transporte.</span><span class="sxs-lookup"><span data-stu-id="c4f30-119">The user can change the preset by selecting a different entry from the **Visualizations and Views** list on the **View** menu, or by using the arrow buttons provided at the bottom of the **Now Playing** pane just above the status message and transport controls.</span></span>

<span data-ttu-id="c4f30-120">Los complementos de la interfaz de usuario de ventana independiente y de fondo se pueden programar para que acepten un elemento multimedia o una lista de reproducción que el usuario le envíe.</span><span class="sxs-lookup"><span data-stu-id="c4f30-120">Background and separate window UI plug-ins can be programmed to accept a media item or playlist that the user sends to it.</span></span> <span data-ttu-id="c4f30-121">Si un complemento es compatible con esta característica, su nombre aparecerá en la lista **Enviar a** disponible en el menú contextual del control de lista de reproducción o de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="c4f30-121">If a plug-in supports this feature, its name will appear on the **Send to** list available from the shortcut menu of the playlist control or the library.</span></span>

<span data-ttu-id="c4f30-122">Un complemento de interfaz de usuario se puede programar para interceptar los métodos abreviados de teclado cuando tiene el foco de teclado.</span><span class="sxs-lookup"><span data-stu-id="c4f30-122">A UI plug-in can be programmed to intercept keyboard shortcuts when it has the keyboard focus.</span></span> <span data-ttu-id="c4f30-123">El foco de teclado es necesario para evitar conflictos cuando se cargan varios complementos de la interfaz de usuario que interceptan el mismo método abreviado de teclado.</span><span class="sxs-lookup"><span data-stu-id="c4f30-123">Keyboard focus is required to prevent conflicts when multiple UI plug-ins that intercept the same keyboard shortcut are loaded.</span></span> <span data-ttu-id="c4f30-124">Aunque esto evita conflictos, también puede provocar confusión en los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="c4f30-124">Although this prevents conflicts, it can also cause confusion to end users.</span></span> <span data-ttu-id="c4f30-125">Por esta razón, no se recomienda el uso de métodos abreviados de teclado con complementos de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="c4f30-125">For this reason, the use of keyboard shortcuts with UI plug-ins is not recommended.</span></span> <span data-ttu-id="c4f30-126">Sin embargo, cuando se utilizan, no deben interceptar los métodos abreviados de teclado que se usan en Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="c4f30-126">When they are used, however, they should not intercept any keyboard shortcuts that are used by Windows Media Player.</span></span> <span data-ttu-id="c4f30-127">Para obtener una lista completa de los métodos abreviados de teclado utilizados por el reproductor, consulte la ayuda de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="c4f30-127">For a complete list of keyboard shortcuts used by the Player, see Windows Media Player Help.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4f30-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c4f30-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4f30-129">**Información general del complemento de la interfaz de usuario**</span><span class="sxs-lookup"><span data-stu-id="c4f30-129">**UI Plug-in Overview**</span></span>](ui-plug-in-overview.md)
</dt> </dl>

 

 




