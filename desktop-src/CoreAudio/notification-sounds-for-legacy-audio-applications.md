---
description: Sonidos de notificación para aplicaciones de audio heredadas
ms.assetid: c5ad67d9-56fb-4bf0-aea4-5b49b0e5bf95
title: Sonidos de notificación para aplicaciones de audio heredadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e9ee2ef1155694e32a21779c55d290da6b3799c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539004"
---
# <a name="notification-sounds-for-legacy-audio-applications"></a><span data-ttu-id="fb7cd-103">Sonidos de notificación para aplicaciones de audio heredadas</span><span class="sxs-lookup"><span data-stu-id="fb7cd-103">Notification Sounds for Legacy Audio Applications</span></span>

<span data-ttu-id="fb7cd-104">En Windows Vista, el sistema operativo asigna todos los sonidos de notificación del sistema a una sesión de audio entre procesos que se reproduce a través del dispositivo de punto de conexión de representación que está asignado actualmente al [rol de dispositivo](device-roles.md)eConsole.</span><span class="sxs-lookup"><span data-stu-id="fb7cd-104">In Windows Vista, the operating system assigns all of its system notification sounds to a cross-process audio session that plays through the rendering endpoint device that is currently assigned to the eConsole [device role](device-roles.md).</span></span> <span data-ttu-id="fb7cd-105">El programa de control de volumen del sistema, Sndvol, muestra un control deslizante de volumen dedicado a los sonidos de notificación del sistema.</span><span class="sxs-lookup"><span data-stu-id="fb7cd-105">The system volume-control program, Sndvol, displays a volume slider that is dedicated to system notification sounds.</span></span>

<span data-ttu-id="fb7cd-106">Algunas aplicaciones juegan sonidos de notificación.</span><span class="sxs-lookup"><span data-stu-id="fb7cd-106">Some applications play notification sounds.</span></span> <span data-ttu-id="fb7cd-107">En lugar de solicitar al usuario que administre los sonidos de la notificación de una aplicación a través de un control deslizante de volumen independiente en Sndvol, la aplicación puede asignar sus sonidos de notificación a la misma sesión que los sonidos de notificación del sistema.</span><span class="sxs-lookup"><span data-stu-id="fb7cd-107">Instead of requiring the user to manage an application's notification sounds through a separate volume slider in Sndvol, the application can assign its notification sounds to the same session as the system notification sounds.</span></span> <span data-ttu-id="fb7cd-108">El control deslizante de volumen Sndvol que controla los sonidos de notificación del sistema controla los sonidos de notificación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fb7cd-108">The Sndvol volume slider that controls the system notification sounds then controls the notification sounds from the application.</span></span>

<span data-ttu-id="fb7cd-109">Para habilitar este comportamiento, Windows Vista define una \_ marca de sistema SND para la función de [**PlaySound**](/previous-versions//dd743680(v=vs.85)) heredada.</span><span class="sxs-lookup"><span data-stu-id="fb7cd-109">To enable this behavior, Windows Vista defines a SND\_SYSTEM flag for the legacy [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function.</span></span> <span data-ttu-id="fb7cd-110">(Esta marca no se admite en versiones anteriores de Windows, incluidas Windows Server 2003, Windows XP y Windows 2000). Si el autor de la llamada establece esta marca, la función **PlaySound** asigna el sonido que se reproduce a la sesión entre procesos que el sistema operativo utiliza para sus sonidos de notificación.</span><span class="sxs-lookup"><span data-stu-id="fb7cd-110">(This flag is not supported in earlier versions of Windows, including Windows Server 2003, Windows XP, and Windows 2000.) If the caller sets this flag, then the **PlaySound** function assigns the sound that it plays to the cross-process session that the operating system uses for its notification sounds.</span></span> <span data-ttu-id="fb7cd-111">Si el autor de la llamada no establece la marca, **PlaySound** asigna el sonido que se reproduce a la sesión predeterminada: la sesión específica del proceso que se identifica mediante el GUID NULL del valor GUID de la sesión \_ .</span><span class="sxs-lookup"><span data-stu-id="fb7cd-111">If the caller does not set the flag, then **PlaySound** assigns the sound that it plays to the default session—the process-specific session that is identified by the session GUID value GUID\_NULL.</span></span> <span data-ttu-id="fb7cd-112">SND \_ System se define en el archivo de encabezado mmsystem. h.</span><span class="sxs-lookup"><span data-stu-id="fb7cd-112">SND\_SYSTEM is defined in the header file Mmsystem.h.</span></span> <span data-ttu-id="fb7cd-113">Para obtener más información sobre **PlaySound**, vea la documentación de Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="fb7cd-113">For more information about **PlaySound**, see the Windows SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb7cd-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fb7cd-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb7cd-115">Interoperabilidad con las API de audio heredadas</span><span class="sxs-lookup"><span data-stu-id="fb7cd-115">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
