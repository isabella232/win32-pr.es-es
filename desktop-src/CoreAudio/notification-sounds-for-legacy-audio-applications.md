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
# <a name="notification-sounds-for-legacy-audio-applications"></a>Sonidos de notificación para aplicaciones de audio heredadas

En Windows Vista, el sistema operativo asigna todos los sonidos de notificación del sistema a una sesión de audio entre procesos que se reproduce a través del dispositivo de punto de conexión de representación que está asignado actualmente al [rol de dispositivo](device-roles.md)eConsole. El programa de control de volumen del sistema, Sndvol, muestra un control deslizante de volumen dedicado a los sonidos de notificación del sistema.

Algunas aplicaciones juegan sonidos de notificación. En lugar de solicitar al usuario que administre los sonidos de la notificación de una aplicación a través de un control deslizante de volumen independiente en Sndvol, la aplicación puede asignar sus sonidos de notificación a la misma sesión que los sonidos de notificación del sistema. El control deslizante de volumen Sndvol que controla los sonidos de notificación del sistema controla los sonidos de notificación de la aplicación.

Para habilitar este comportamiento, Windows Vista define una \_ marca de sistema SND para la función de [**PlaySound**](/previous-versions//dd743680(v=vs.85)) heredada. (Esta marca no se admite en versiones anteriores de Windows, incluidas Windows Server 2003, Windows XP y Windows 2000). Si el autor de la llamada establece esta marca, la función **PlaySound** asigna el sonido que se reproduce a la sesión entre procesos que el sistema operativo utiliza para sus sonidos de notificación. Si el autor de la llamada no establece la marca, **PlaySound** asigna el sonido que se reproduce a la sesión predeterminada: la sesión específica del proceso que se identifica mediante el GUID NULL del valor GUID de la sesión \_ . SND \_ System se define en el archivo de encabezado mmsystem. h. Para obtener más información sobre **PlaySound**, vea la documentación de Windows SDK.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interoperabilidad con las API de audio heredadas](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
