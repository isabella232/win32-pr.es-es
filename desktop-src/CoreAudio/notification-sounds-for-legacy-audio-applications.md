---
description: Sonidos de notificación para aplicaciones de audio heredadas
ms.assetid: c5ad67d9-56fb-4bf0-aea4-5b49b0e5bf95
title: Sonidos de notificación para aplicaciones de audio heredadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4ce813fb2d38a9995f929c62936879f502392415d040e88ddb50f3b4699734a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077529"
---
# <a name="notification-sounds-for-legacy-audio-applications"></a>Sonidos de notificación para aplicaciones de audio heredadas

En Windows Vista, el sistema operativo asigna todos sus sonidos de notificación del sistema a una sesión de audio entre [](device-roles.md)procesos que se reproduce a través del dispositivo del punto de conexión de representación que está asignado actualmente al rol de dispositivo eConsole . El programa de control de volumen del sistema, Sndvol, muestra un control deslizante de volumen dedicado a los sonidos de notificación del sistema.

Algunas aplicaciones reproducen sonidos de notificación. En lugar de requerir al usuario que administre los sonidos de notificación de una aplicación a través de un control deslizante de volumen independiente en Sndvol, la aplicación puede asignar sus sonidos de notificación a la misma sesión que los sonidos de notificación del sistema. El control deslizante del volumen Sndvol que controla los sonidos de notificación del sistema controla los sonidos de notificación de la aplicación.

Para habilitar este comportamiento, Windows Vista define una marca \_ SND SYSTEM para la función [**PlaySound**](/previous-versions//dd743680(v=vs.85)) heredada. (Esta marca no se admite en versiones anteriores de Windows, incluidos Windows Server 2003, Windows XP y Windows 2000). Si el autor de la llamada establece esta marca, la función **PlaySound** asigna el sonido que reproduce a la sesión entre procesos que el sistema operativo usa para sus sonidos de notificación. Si el autor de la llamada no establece la marca, **PlaySound** asigna el sonido que reproduce a la sesión predeterminada, la sesión específica del proceso identificada por el VALOR GUID de la sesión \_ NULL. SND \_ SYSTEM se define en el archivo de encabezado Mmsystem.h. Para más información sobre **PlaySound,** consulte la documentación Windows SDK.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interoperabilidad con las API de audio heredadas](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
