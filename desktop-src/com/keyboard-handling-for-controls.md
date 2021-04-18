---
title: Control de teclado para controles
description: Un control responde a los aceleradores de teclado para que el usuario final pueda iniciar acciones realizadas por el control.
ms.assetid: 59aca5cb-f109-49ee-897d-43610501f7f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbe03058fdb0192a0f8f7b13032612288045775b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357727"
---
# <a name="keyboard-handling-for-controls"></a><span data-ttu-id="8cc57-103">Control de teclado para controles</span><span class="sxs-lookup"><span data-stu-id="8cc57-103">Keyboard Handling for Controls</span></span>

<span data-ttu-id="8cc57-104">Un control responde a los aceleradores de teclado para que el usuario final pueda iniciar acciones realizadas por el control.</span><span class="sxs-lookup"><span data-stu-id="8cc57-104">A control responds to keyboard accelerators so the end-user can initiate actions performed by the control.</span></span> <span data-ttu-id="8cc57-105">El contenedor administra la actividad del teclado de todos sus controles incrustados.</span><span class="sxs-lookup"><span data-stu-id="8cc57-105">The container manages keyboard activity for all its embedded controls.</span></span> <span data-ttu-id="8cc57-106">Con los documentos compuestos, los aceleradores de teclado solo se aplican al objeto activo.</span><span class="sxs-lookup"><span data-stu-id="8cc57-106">With compound documents, keyboard accelerators apply only to the currently active object.</span></span> <span data-ttu-id="8cc57-107">Con los controles, se ha agregado un mecanismo para que un control pueda responder a sus teclas de método de teclado aunque no esté actualmente en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="8cc57-107">With controls, a mechanism has been added so that a control can respond to its keyboard mnemonics even if it is not currently UI-active.</span></span>

<span data-ttu-id="8cc57-108">Los métodos [**IOleControl:: GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) y [**IOleControl:: mnemónicos**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) y el método [**IOleControlSite:: OnControlInfoChanged**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-oncontrolinfochanged) controlan las teclas de tecla del control.</span><span class="sxs-lookup"><span data-stu-id="8cc57-108">The [**IOleControl::GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) and [**IOleControl::OnMnemonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) methods and the [**IOleControlSite::OnControlInfoChanged**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-oncontrolinfochanged) method handle a control's keyboard mnemonics.</span></span> <span data-ttu-id="8cc57-109">Una estructura [**CONTROLINFO**](/windows/win32/api/ocidl/ns-ocidl-controlinfo) describe los aceleradores de la tecla de acceso de un control y las marcas que se devuelven con él a través del método **GetControlInfo** describen el comportamiento de los controles con las teclas entrar y ESC.</span><span class="sxs-lookup"><span data-stu-id="8cc57-109">A [**CONTROLINFO**](/windows/win32/api/ocidl/ns-ocidl-controlinfo) structure describes a control's mnemonic accelerators, and the flags passed back with it through the **GetControlInfo** method describe the controls behavior with the Enter and Esc keys.</span></span> <span data-ttu-id="8cc57-110">Cuando un control cambia sus teclas de método, llama a **OnControlInfoChanged** para que el contenedor pueda volver a cargar la estructura si es necesario.</span><span class="sxs-lookup"><span data-stu-id="8cc57-110">When a control changes its mnemonics, it calls **OnControlInfoChanged** so the container can reload the structure if necessary.</span></span>

<span data-ttu-id="8cc57-111">Cuando un control está activo en la interfaz de usuario, también es el control con el foco.</span><span class="sxs-lookup"><span data-stu-id="8cc57-111">When a control is UI active, it is also the control with the focus.</span></span> <span data-ttu-id="8cc57-112">A medida que los controles se activan y desactivan entre los Estados activo en contexto y activo de la interfaz de usuario, el control llama a [**IOleControlSite:: onfocus**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-onfocus) para indicar al contenedor de dichos cambios.</span><span class="sxs-lookup"><span data-stu-id="8cc57-112">As controls are activated and deactivated between the in-place active and the UI active states, the control calls [**IOleControlSite::OnFocus**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-onfocus) to tell the container of such changes.</span></span>

<span data-ttu-id="8cc57-113">Además, cuando un control está activo en la interfaz de usuario, tendrá la primera oportunidad de procesar cualquier pulsación de tecla.</span><span class="sxs-lookup"><span data-stu-id="8cc57-113">In addition, when a control is UI active, it will have first chance to process any keystrokes.</span></span> <span data-ttu-id="8cc57-114">Para dar a un contenedor la oportunidad de procesar la pulsación de tecla antes del control, el control llama a [**IOleControlSite:: TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator).</span><span class="sxs-lookup"><span data-stu-id="8cc57-114">To give a container the opportunity to process the keystroke before the control, the control calls [**IOleControlSite::TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator).</span></span> <span data-ttu-id="8cc57-115">Si el contenedor no controla la pulsación de tecla, el control lo procesa.</span><span class="sxs-lookup"><span data-stu-id="8cc57-115">If the container does not handle the keystroke, the control then processes it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8cc57-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8cc57-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cc57-117">Controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="8cc57-117">ActiveX Controls</span></span>](activex-controls.md)
</dt> </dl>

 

 




