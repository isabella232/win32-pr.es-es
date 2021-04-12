---
description: Las aplicaciones no se pueden representar en estéreo a menos que el sistema operativo indique que habilita el comportamiento de presentación de Stereoscopic 3D. Las aplicaciones determinan si se va a representar en Stereoscopic 3D de manera diferente, en función de si están en ventanas o en pantalla completa.
ms.assetid: FB8AC57E-38DD-47B5-8666-1F4B73488F8B
title: Representación en estéreo y notificación sobre el estado de estéreo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 379c6335e0bd060cf0065fe92bf2ec6c086289c3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104151938"
---
# <a name="rendering-in-stereo-and-notifying-about-stereo-status"></a>Representación en estéreo y notificación sobre el estado de estéreo

Las aplicaciones no se pueden representar en estéreo a menos que el sistema operativo indique que habilita el comportamiento de presentación de Stereoscopic 3D. Las aplicaciones determinan si se va a representar en Stereoscopic 3D de manera diferente, en función de si están en ventanas o en pantalla completa.

Una aplicación en ventana llama al método [**IDXGIFactory2:: IsWindowedStereoEnabled**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-iswindowedstereoenabled) para determinar si se va a representar en estéreo. Una aplicación de pantalla completa llama al método [**IDXGIOutput1:: GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) y, a continuación, determina si alguno de los modos de presentación devueltos admite la representación en estéreo. El método **GetDisplayModeList1** no enumera los modos estéreo a menos que especifique la [**marca \_ \_ \_ estéreo de modos de enumeración de DXGI**](dxgi-enum-modes.md) en el parámetro *Flags* . Una aplicación de ventana o de pantalla completa que admite el estéreo primero realiza la determinación de representar en estéreo en función de una llamada al método **IDXGIFactory2:: IsWindowedStereoEnabled** o **IDXGIOutput1:: GetDisplayModeList1** , respectivamente, y, a continuación, se registra para recibir notificaciones de los cambios de estado de estéreo. Dado que la aplicación no puede confiar en la notificación para indicar el estado actual del comportamiento de presentación de Stereoscopic 3D, cuando recibe un evento de notificación o un mensaje de ventana, debe llamar de nuevo a **IDXGIFactory2:: IsWindowedStereoEnabled** o **IDXGIOutput1:: GetDisplayModeList1** para determinar el estado actual del comportamiento de visualización 3D de Stereoscopic del sistema operativo.

Si desea representar en estéreo, debe registrarse para que las notificaciones estéreo sepan cuándo el usuario apaga o está en un comportamiento estéreo. Una aplicación puede registrarse para recibir notificaciones sobre los cambios de estado de Stereoscopic 3D a través de un mensaje a una ventana o a través de la señalización de eventos. Para registrarse para recibir mensajes de notificación en una ventana sobre los cambios de estado de estéreo, una aplicación llama al método [**IDXGIFactory2:: RegisterStereoStatusWindow**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatuswindow) . Para registrarse para recibir notificaciones de los cambios de estado de estéreo a través de la señalización de eventos, una aplicación llama al método [**IDXGIFactory2:: RegisterStereoStatusEvent**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatusevent) . Ambos métodos devuelven un puntero a un valor de clave que la aplicación puede usar para anular el registro de la notificación. Para anular el registro de la notificación, la aplicación pasa este valor de clave al método [**IDXGIFactory2:: UnregisterStereoStatus**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterstereostatus) .

El estado de estéreo puede contener los elementos siguientes:

-   La configuración del usuario.

    Los usuarios de Windows pueden habilitar o deshabilitar la visualización de estéreo con la opción Habilitar Stereoscopic 3D en la configuración de pantalla de cambios del panel de control.

-   La capacidad y la configuración del equipo, que incluye el adaptador de gráficos, el controlador de gráficos y el monitor de configuración.

En el [ejemplo Direct3D 11,1 simple estéreo 3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20stereoscopic%203D%20sample) se muestra cómo agregar un efecto Stereoscopic 3D y cómo responder a los cambios de estéreo del sistema.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mejoras en DXGI 1,2](dxgi-1-2-improvements.md)
</dt> </dl>

 

 
