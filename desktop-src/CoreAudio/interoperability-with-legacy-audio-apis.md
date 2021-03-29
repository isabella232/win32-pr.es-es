---
description: Interoperabilidad con las API de audio heredadas
ms.assetid: 34939f6d-a6e4-4f7a-afa3-b1fed52b471f
title: Interoperabilidad con las API de audio heredadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a6b9a80b55695ffcfd3ac54e871f00ea27744d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000719"
---
# <a name="interoperability-with-legacy-audio-apis"></a><span data-ttu-id="c7ff8-103">Interoperabilidad con las API de audio heredadas</span><span class="sxs-lookup"><span data-stu-id="c7ff8-103">Interoperability with Legacy Audio APIs</span></span>

<span data-ttu-id="c7ff8-104">Muchas aplicaciones existentes usan las API de audio heredadas como DirectSound, DirectShow y las funciones multimedia de Windows.</span><span class="sxs-lookup"><span data-stu-id="c7ff8-104">Many existing applications use legacy audio APIs such as DirectSound, DirectShow, and the Windows multimedia functions.</span></span> <span data-ttu-id="c7ff8-105">Con solo modificaciones menores, estas aplicaciones se pueden aumentar para hacer uso de [roles de dispositivo](device-roles.md), [controles de volumen de sesión](session-volume-controls.md)y otras características de las API de audio principales en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c7ff8-105">With only minor modifications, these applications can be augmented to make use of [device roles](device-roles.md), [session volume controls](session-volume-controls.md), and other features of the core audio APIs in Windows Vista.</span></span>

<span data-ttu-id="c7ff8-106">Como se describe en [componentes de audio de modo de usuario](user-mode-audio-components.md), las API de audio principales sirven como base para la creación de las API de audio de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="c7ff8-106">As discussed in [User-Mode Audio Components](user-mode-audio-components.md), the core audio APIs serve as the foundation on which higher-level audio APIs are built.</span></span> <span data-ttu-id="c7ff8-107">En Windows Vista, los dispositivos de audio a los que las aplicaciones acceden a través de las API de audio heredadas como DirectSound y las funciones **waveOutXxx** y **waveInXxx** de Windows Media son, de hecho, [dispositivos de punto de conexión](audio-endpoint-devices.md) de audio implementados por las API de audio principales.</span><span class="sxs-lookup"><span data-stu-id="c7ff8-107">In Windows Vista, the audio devices that applications access through legacy audio APIs such as DirectSound and the Windows media **waveOutXxx** and **waveInXxx** functions are, in fact, [audio endpoint devices](audio-endpoint-devices.md) that are implemented by the core audio APIs.</span></span> <span data-ttu-id="c7ff8-108">Debido a las limitaciones inherentes en las interfaces de las API de audio heredadas, una aplicación puede acceder a algunas de las funcionalidades de los dispositivos de punto de conexión de audio, pero no a ellas, a través de estas interfaces.</span><span class="sxs-lookup"><span data-stu-id="c7ff8-108">Because of inherent limitations in the interfaces of legacy audio APIs, an application can access some but not all of the capabilities of audio endpoint devices through these interfaces.</span></span> <span data-ttu-id="c7ff8-109">En las secciones siguientes se describen técnicas para mejorar las aplicaciones existentes mediante el acceso a funciones adicionales de los dispositivos de punto de conexión de audio directamente a través de las API de audio principales.</span><span class="sxs-lookup"><span data-stu-id="c7ff8-109">The following sections describe techniques for enhancing existing applications by accessing additional capabilities of audio endpoint devices directly through the core audio APIs.</span></span> <span data-ttu-id="c7ff8-110">Estas mejoras normalmente solo requieren pequeños cambios en el código de aplicación existente.</span><span class="sxs-lookup"><span data-stu-id="c7ff8-110">These enhancements typically require only minor changes to the existing application code.</span></span>

<span data-ttu-id="c7ff8-111">En las secciones siguientes se describe cómo incorporar características de las API de audio principales en aplicaciones existentes que usan las API de audio heredadas:</span><span class="sxs-lookup"><span data-stu-id="c7ff8-111">The following sections describe how to incorporate features of the core audio APIs into existing applications that use legacy audio APIs:</span></span>

-   [<span data-ttu-id="c7ff8-112">Roles de dispositivo para aplicaciones DirectSound</span><span class="sxs-lookup"><span data-stu-id="c7ff8-112">Device Roles for DirectSound Applications</span></span>](device-roles-for-directsound-applications.md)
-   [<span data-ttu-id="c7ff8-113">Roles de dispositivo para aplicaciones de DirectShow</span><span class="sxs-lookup"><span data-stu-id="c7ff8-113">Device Roles for DirectShow Applications</span></span>](device-roles-for-directshow-applications.md)
-   [<span data-ttu-id="c7ff8-114">Roles de dispositivo para aplicaciones multimedia heredadas de Windows</span><span class="sxs-lookup"><span data-stu-id="c7ff8-114">Device Roles for Legacy Windows Multimedia Applications</span></span>](device-roles-for-legacy-windows-multimedia-applications.md)
-   [<span data-ttu-id="c7ff8-115">Eventos de audio para aplicaciones de audio heredadas</span><span class="sxs-lookup"><span data-stu-id="c7ff8-115">Audio Events for Legacy Audio Applications</span></span>](audio-events-for-legacy-audio-applications.md)
-   [<span data-ttu-id="c7ff8-116">Sonidos de notificación para aplicaciones de audio heredadas</span><span class="sxs-lookup"><span data-stu-id="c7ff8-116">Notification Sounds for Legacy Audio Applications</span></span>](notification-sounds-for-legacy-audio-applications.md)

## <a name="related-topics"></a><span data-ttu-id="c7ff8-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c7ff8-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7ff8-118">Roles de dispositivo</span><span class="sxs-lookup"><span data-stu-id="c7ff8-118">Device Roles</span></span>](device-roles.md)
</dt> </dl>

 

 



