---
description: Las aplicaciones no se pueden representar en estéreo a menos que el sistema operativo indique que habilita el comportamiento de pantalla 3D estéreo. Las aplicaciones determinan si se representa en 3D estereo estéreo de forma diferente en función de si están en ventanas o en pantalla completa.
ms.assetid: FB8AC57E-38DD-47B5-8666-1F4B73488F8B
title: Representación en estéreo y notificación sobre el estado estéreo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f17f324a884c5784c98a8f5c21ef9c9dac7b048fc72ae7ed0ea1a75e61e2551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987015"
---
# <a name="rendering-in-stereo-and-notifying-about-stereo-status"></a>Representación en estéreo y notificación sobre el estado estéreo

Las aplicaciones no se pueden representar en estéreo a menos que el sistema operativo indique que habilita el comportamiento de pantalla 3D estéreo. Las aplicaciones determinan si se representa en 3D estereo estéreo de forma diferente en función de si están en ventanas o en pantalla completa.

Una aplicación en ventanas llama al método [**IDXGIFactory2::IsWindowedStereoEnabled**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-iswindowedstereoenabled) para determinar si se representa en estéreo. Una aplicación de pantalla completa llama al método [**IDXGIOutput1::GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) y, a continuación, determina si alguno de los modos de presentación devueltos admite la representación en estéreo. El **método GetDisplayModeList1** no enumera los modos estéreo a menos que especifique la marca [**DXGI \_ ENUM MODES \_ \_ STEREO**](dxgi-enum-modes.md) en *el parámetro Flags.* Una aplicación de pantalla completa o con ventanas que admite estéreo primero toma la determinación de representar en estéreo en función de una llamada al método **IDXGIFactory2::IsWindowedStereoEnabled** o **IDXGIOutput1::GetDisplayModeList1** respectivamente y, a continuación, se registra para recibir notificaciones de cambios de estado estéreo. Dado que la aplicación no puede basarse en la notificación para indicar el estado actual del comportamiento de presentación 3D estereofónico, cuando recibe un mensaje de ventana o evento de notificación, debe llamar de nuevo a **IDXGIFactory2::IsWindowedStereoEnabled** o **IDXGIOutput1::GetDisplayModeList1 para** determinar el estado actual del comportamiento de presentación 3D estereo inofensivo del sistema operativo.

Si desea representar en estéreo, debe registrarse para recibir notificaciones estéreo para saber cuándo el usuario desactiva o activa el comportamiento estéreo. Una aplicación puede registrarse para recibir notificaciones sobre los cambios de estado 3D estéreo a través de un mensaje a una ventana o a través de la señalización de eventos. Para registrarse para recibir mensajes de notificación en una ventana sobre los cambios de estado estéreo, una aplicación llama al método [**IDXGIFactory2::RegisterStereoStatusWindow.**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatuswindow) Para registrarse para recibir la notificación de los cambios de estado estéreo a través de la señalización de eventos, una aplicación llama al método [**IDXGIFactory2::RegisterStereoStatusEvent.**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatusevent) Ambos métodos devuelven un puntero a un valor de clave que la aplicación puede usar para anular el registro de la notificación. Para anular el registro de la notificación, la aplicación pasa este valor de clave al [**método IDXGIFactory2::UnregisterStereoStatus.**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterstereostatus)

El estado estéreo puede contener los siguientes elementos:

-   Configuración del usuario.

    Windows los usuarios pueden habilitar o deshabilitar la pantalla estéreo con la opción habilitar 3D estéreo en la Panel de control vista de cambios Configuración.

-   La funcionalidad y configuración del equipo, que incluye el adaptador de gráficos, el controlador de gráficos y la configuración del monitor.

El ejemplo 3D estéreo 3D simple de [Direct3D 11.1](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20stereoscopic%203D%20sample) muestra cómo agregar un efecto 3D estéreo y cómo responder a los cambios estéreo del sistema.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mejoras de DXGI 1.2](dxgi-1-2-improvements.md)
</dt> </dl>

 

 
