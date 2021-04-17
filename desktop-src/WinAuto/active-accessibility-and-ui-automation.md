---
title: Active Accessibility y automatización de la interfaz de usuario
description: Microsoft Active Accessibility está diseñado para su uso con Windows XP y sistemas operativos anteriores.
ms.assetid: 8eb36d2c-0c2f-4311-8690-52ce070c9f33
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2483f4f6679926ef2f87c380d4ac0febcc88652
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704787"
---
# <a name="active-accessibility-and-ui-automation"></a><span data-ttu-id="fc907-103">Active Accessibility y automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="fc907-103">Active Accessibility and UI Automation</span></span>

<span data-ttu-id="fc907-104">Microsoft Active Accessibility está diseñado para su uso con Windows XP y sistemas operativos anteriores.</span><span class="sxs-lookup"><span data-stu-id="fc907-104">Microsoft Active Accessibility is designed for use with Windows XP and earlier operating systems.</span></span> <span data-ttu-id="fc907-105">Los desarrolladores de controles personalizados y aplicaciones cliente de tecnología accesible para Windows XP y Windows Vista deben considerar el uso de la automatización de la [interfaz de usuario](entry-uiauto-win32.md) de Microsoft en su lugar.</span><span class="sxs-lookup"><span data-stu-id="fc907-105">Developers of custom controls and accessible technology client applications for Windows XP and Windows Vista should consider using Microsoft [UI Automation](entry-uiauto-win32.md) instead.</span></span>

<span data-ttu-id="fc907-106">La automatización de la interfaz de usuario de Microsoft es un sistema con todas las características que proporciona información más precisa sobre la interfaz de usuario y proporciona al usuario más capacidad para interactuar con los controles.</span><span class="sxs-lookup"><span data-stu-id="fc907-106">Microsoft UI Automation is a full-featured system that provides more precise information about the user interface and gives the user more ability to interact with controls.</span></span> <span data-ttu-id="fc907-107">En concreto, proporciona compatibilidad mejorada con el texto.</span><span class="sxs-lookup"><span data-stu-id="fc907-107">In particular, it provides greatly enhanced support for text.</span></span>

<span data-ttu-id="fc907-108">Un conjunto de objetos proxy proporciona compatibilidad con la automatización de la interfaz de usuario para los controles estándar de Microsoft Win32 y Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="fc907-108">A set of proxy objects provides UI Automation support for standard Microsoft Win32 and Windows Forms controls.</span></span> <span data-ttu-id="fc907-109">La compatibilidad más enriquecida está disponible para los controles que se escriben específicamente con automatización de la interfaz de usuario, incluidos los elementos de Windows Presentation Foundation nativa (WPF), que no admiten directamente Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="fc907-109">Richer support is available for controls specifically written with UI Automation in mind, including native Windows Presentation Foundation (WPF) elements, which do not directly support Microsoft Active Accessibility.</span></span> <span data-ttu-id="fc907-110">Los controles personalizados que admiten la automatización de la interfaz de usuario se pueden escribir en código administrado o no administrado.</span><span class="sxs-lookup"><span data-stu-id="fc907-110">Custom controls that support UI Automation can be written in either managed or unmanaged code.</span></span>

<span data-ttu-id="fc907-111">Los clientes de Microsoft Active Accessibility tienen acceso limitado, a través de una capa de puente, a elementos de interfaz de usuario que solo admiten la automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="fc907-111">Microsoft Active Accessibility clients have limited access, through a bridging layer, to UI elements that support only UI Automation.</span></span> <span data-ttu-id="fc907-112">Para obtener más información, vea el [Apéndice G: Active Accessibility Bridge to UI Automation](appendix-g--active-accessibility-bridge-to-ui-automation.md).</span><span class="sxs-lookup"><span data-stu-id="fc907-112">For more information, see [Appendix G: Active Accessibility Bridge to UI Automation](appendix-g--active-accessibility-bridge-to-ui-automation.md).</span></span>

<span data-ttu-id="fc907-113">Para obtener más información sobre las similitudes y diferencias entre Microsoft Active Accessibility y la automatización de la interfaz de usuario, consulte [comparación de microsoft Active Accessibility y UI Automation](microsoft-active-accessibility-and-ui-automation-compared.md).</span><span class="sxs-lookup"><span data-stu-id="fc907-113">For more information about the similarities and differences between Microsoft Active Accessibility and UI Automation, see [Microsoft Active Accessibility and UI Automation Compared](microsoft-active-accessibility-and-ui-automation-compared.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc907-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fc907-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="fc907-115">**Vista**</span><span class="sxs-lookup"><span data-stu-id="fc907-115">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fc907-116">Introducción</span><span class="sxs-lookup"><span data-stu-id="fc907-116">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="fc907-117">Automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="fc907-117">UI Automation</span></span>](entry-uiauto-win32.md)
</dt> </dl>

 

 




