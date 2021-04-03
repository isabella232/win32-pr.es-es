---
title: Mostrar interfaces de usuario modales
description: Mostrar interfaces de usuario modales
ms.assetid: 748a8db7-159d-4043-beac-e0516327bcef
keywords:
- Complementos de Windows Media Player, Mostrar cuadros de diálogo y cuadros de mensaje
- complementos, Mostrar cuadros de diálogo y cuadros de mensaje
- Complementos de la interfaz de usuario, Mostrar cuadros de diálogo y de mensajes
- Complementos de la interfaz de usuario, Mostrar cuadros de diálogo y de mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d96387ca46864064c7b6ff7b9cd3dba8187eed0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103780064"
---
# <a name="displaying-modal-user-interfaces"></a><span data-ttu-id="d0047-107">Mostrar interfaces de usuario modales</span><span class="sxs-lookup"><span data-stu-id="d0047-107">Displaying Modal User Interfaces</span></span>

<span data-ttu-id="d0047-108">Los complementos de interfaz de usuario no deben mostrar cuadros de diálogo modales ni cuadros de mensaje en respuesta a llamadas a métodos desde Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="d0047-108">UI plug-ins should not display modal dialog boxes or message boxes in response to method calls from Windows Media Player.</span></span> <span data-ttu-id="d0047-109">Por ejemplo, no muestre un cuadro de mensaje de la implementación de **IWMPPluginUI:: Create**.</span><span class="sxs-lookup"><span data-stu-id="d0047-109">For example, do not display a message box from your implementation of **IWMPPluginUI::Create**.</span></span>

<span data-ttu-id="d0047-110">Si debe mostrar un cuadro de diálogo o un cuadro de mensaje desde una implementación del método de complemento de la interfaz de usuario a la que llama el reproductor, debe seguir estos pasos:</span><span class="sxs-lookup"><span data-stu-id="d0047-110">If you must display a dialog box or message box from a UI plug-in method implementation that is called by the Player, you must follow these steps:</span></span>

1.  <span data-ttu-id="d0047-111">Registra un nuevo mensaje de ventana mediante **RegisterWindowMessage**.</span><span class="sxs-lookup"><span data-stu-id="d0047-111">Register a new window message using **RegisterWindowMessage**.</span></span>
2.  <span data-ttu-id="d0047-112">Envíe el mensaje de ventana que registró a la ventana del complemento de la interfaz de usuario mediante **PostMessage**.</span><span class="sxs-lookup"><span data-stu-id="d0047-112">Send the window message you registered to your UI plug-in window using **PostMessage**.</span></span>
3.  <span data-ttu-id="d0047-113">Mostrar el cuadro de diálogo o el cuadro de mensaje del controlador de mensajes para el nuevo mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="d0047-113">Show the dialog box or message box from the message handler for your new window message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0047-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d0047-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0047-115">**Información general del complemento de la interfaz de usuario**</span><span class="sxs-lookup"><span data-stu-id="d0047-115">**UI Plug-in Overview**</span></span>](ui-plug-in-overview.md)
</dt> </dl>

 

 




